shopex Prism sdk (IOS version)
===============================================

用途
-----------------------------------------------
实现shopex Prism 的IOS版SDK供第三方使用

功能
-----------------------------------------------
- 提供http API调用（GET/POST方式）
------------------------------
要求
-----------------------------------------------
IOS 5.0

配置
------------
根据需要将所需类型的静态库引入到工程中

用法
-------
	//测试账号
	static NSString const *host = @"http://dilbmtcv.apihub.cn/api";
	static NSString const *appkey = @"buwb2lii";
	static NSString const *secret = @"ucr72ygfutspqeuu6s36";


Get方式

	PrismClient *client = [[PrismClient 	alloc]initWithHost:host appKey:appkey appSecret:secret];
	client.delegate = self;
    [client doGetMetod:@"/platform/notify/status" appParams:@{@"data":@"你好!"}];

POST方式

	PrismClient *client = [[PrismClient alloc]initWithHost:host appKey:appkey appSecret:secret];
	client.delegate = self;
    [client doPOSTMetod:@"/platform/notify/write" appParams:@{@"data":@"你好"}];


---------------
