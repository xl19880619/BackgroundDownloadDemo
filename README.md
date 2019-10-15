# BackgroundDownloadDemo

面试题
https://github.com/ChenYilong/iOSInterviewQuestions/issues

[iOS原生级别后台下载详解]
https://juejin.im/post/5c4ed0b0e51d4511dc730799
https://github.com/Danie1s/Tiercel

[iOS使用NSURLSession进行下载（包括后台下载，断点下载）]

https://www.jianshu.com/p/1211cf99dfc3

[iOS后台下载功能（收集）]
https://www.jianshu.com/p/15d97c6a4f7f

12（后台下载）
正常做法：

使用 `backgroundSessionConfigurationWithIdentifier` 
初始化的configure初始化一个后台下载使用的session。

实现
```
	NSURLSessionDelegate
	NSURLSessionTaskDelegate
	NSURLSessionDownloadDelegat
```
中的
`didCompleteWithError、didFinishDownloadingToURL、URLSessionDidFinishEventsForBackgroundURLSession`和其他业务需求的protocol。

实现`UIApplicationDelegate handleEventsForBackgroundURLSession`方法。

邪门歪道：