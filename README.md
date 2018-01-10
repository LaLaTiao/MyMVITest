# MyMVITest
### MVI模式Demo
> https://github.com/pcdack/MyMVITest

>https://mp.weixin.qq.com/s?__biz=MzIxNzU1Nzk3OQ==&mid=2247486456&idx=1&sn=fab25b3b85c8ad178d6c4b0d498206d5&chksm=97f6b54ca0813c5a0b2758836105b569c5ae86379c9019907240c283bb4014de8ab727817579&scene=0#rd
>基于这个,不过这个是Kotlin版本的,写一个java版本的玩玩

emmm....咋感觉和MVP差不多啊.
整体流程就是View发送intent,Present通过rxBinding接收到发送的intent,然后调用属于Model层的data类,data类去调用Repository,将网络请求返回的数据封装在state内,最后返回给Present.
Present通过subscribeViewState将返回的封装好的数据返回给与之关联的View层的activity,最终activity对数据进行处理.