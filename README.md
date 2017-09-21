
iOS 11
=======

这里总结了大家iOS 11，iPhone X 适配问题
-------------------------------------

#点击右上角的 star、watch 按钮，可以收藏本仓库，看到本仓库的更新！
     

iOS 11适配
---------

[简书App适配iOS 11](http://www.jianshu.com/p/26fc39135c34)  
 
[掘金客户端适配iOS11简单记录](https://juejin.im/entry/59bb92ab6fb9a00a681ac051)
 
[iOS 11 安全区域适配总结](http://www.jianshu.com/p/efbc8619d56b)
 
[iOS开发-适配iOS 11](http://www.jianshu.com/p/a356b2ed4ceb)
 
[完美适配 iOS11 导航栏](http://www.cocoachina.com/ios/20170919/20597.html)

[腾讯WeTest 你可能需要为你的APP适配iOS11](http://wetest.qq.com/lab/view/326.html)

[iOS 11 适配看这篇还不够？](http://www.jishux.com/plus/view-606748-1.html)

iPhone X 适配
------------

[饿了么 UED iPhone X设计适配指南 & iOS 11新特性](https://zhuanlan.zhihu.com/p/29327102)

[iPhone X 适配](http://www.jianshu.com/p/9796cd3f180e)

[iPhone X 的 UI界面适配官方指南](https://juejin.im/entry/59b938f86fb9a00a5c3c32df)

[iOS11 &amp; iPhone X 适配指南](http://www.10tiao.com/html/216/201709/2652552758/2.html)

[iOS iPhone X 适配启动图片](http://www.cnblogs.com/someonelikeyou/p/7515025.html)

[三分钟弄懂iPhone X 设计尺寸和适配](http://www.zcool.com.cn/article/ZNTU1MTUy.html)

[ iPhone X 适配指南 (官方翻译版)](http://m.blog.csdn.net/happyshaotang2/article/details/77991536)


新增加iPhone X 上TabBar拉伸的,压缩的问题
------------------------------------
[TabBar被拉伸的解决方法](https://stackoverflow.com/questions/46214740/ios-11-iphone-x-simulator-uitabbar-icons-and-titles-being-rendered-on-top-coveri)

[ios 11 UITabBar UITabBarItem positioning issue](https://stackoverflow.com/questions/44822558/ios-11-uitabbar-uitabbaritem-positioning-issue)

    #define IS_IPHONEX (([[UIScreen mainScreen] bounds].size.height-812)?NO:YES)
    self.tabBarController = [[UITabBarController alloc] init];
    self.window.rootViewController = [[UIViewController alloc] init];
    if(IS_IPHONEX)
        self.window.rootViewController.view.frame = CGRectMake(self.window.rootViewController.view.frame.origin.x, self.window.rootViewController.view.frame.origin.y, self.window.rootViewController.view.frame.size.width, self.window.rootViewController.view.frame.size.height + 32);
    [self.window.rootViewController.view addSubview:self.tabBarController.view];
    self.tabBarController.tabBar.barTintColor = [UIColor colorWithWhite:0.98 alpha:1.0];
    self.window.rootViewController.view.backgroundColor = [UIColor colorWithWhite:0.98 alpha:1.0];
    



iOS 11获取设备名称
-----------------

    if ([platform isEqualToString:@"iPhone10,1"]) return @"iPhone 8";
    if ([platform isEqualToString:@"iPhone10,4"]) return @"iPhone 8";
    if ([platform isEqualToString:@"iPhone10,2"]) return @"iPhone 8 Plus";
    if ([platform isEqualToString:@"iPhone10,5"]) return @"iPhone 8 Plus";
    if ([platform isEqualToString:@"iPhone10,3"]) return @"iPhone X";
    if ([platform isEqualToString:@"iPhone10,6"]) return @"iPhone X";

