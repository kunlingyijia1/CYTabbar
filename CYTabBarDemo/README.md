# CYTabBar - 底部控制器
[![Platform](http://img.shields.io/badge/platform-ios-blue.svg?style=flat
             )](https://developer.apple.com/iphone/index.action)
[![Language](http://img.shields.io/badge/language-ObjC-brightgreen.svg?style=flat)](https://developer.apple.com/Objective-C)</br>
![](http://upload-images.jianshu.io/upload_images/2028853-71816e3e435ea4b3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)</br>
![](http://upload-images.jianshu.io/upload_images/2028853-3ad54ef949ad7cbe.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/320)

## 一.  功能简介 - Introduction

- [x] 中间按钮可凸出 （bulge设为YES 否则不突出）
- [x] 中按钮可设置控制器 或 普通按钮 (Controller传入nil为普通按钮)
- [x] 二级页面不显示tababr 
- [x] 小红点提醒 (当前控制器.tabBarItem.badgeValue = @"remind";)
- [x] 数字提醒用户(当前控制器.tabBarItem.badgeValue = @"100";)
- [x] 改变数字提醒背景颜色(当前控制器.tabBarItem.badgeColor = [UIColor xxxColor];)
- [x] 切换控制器 (当前tabBarController.selectedIndex = x(索引为添加控制器时的顺序);)

## 二.  安装 - Installation

- 暂不支持CocoaPods
- 手动导入：将项目中的“CYTabBar”文件夹拖入项目中
- 在AppDelegate中导入头文件 "CYTabBarController.h" 

-  你可以这样来设置你的tabbar
```
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    self.window = [[UIWindow alloc]initWithFrame:[[UIScreen mainScreen]bounds]];
    CYTabBarController * tabbar = [[CYTabBarController alloc]init];
    [tabbar addChildController:[ViewController new] title:@"xx" imageName:@"xx" selectedImageName:@"xx"];
    [tabbar addChildController:[ViewController2 new] title:@"xx" imageName:@"xx" selectedImageName:@"xx"];
    [tabbar addCenterController:nil bulge:YES title:@"xx" imageName:@xx" selectedImageName:@"xx"];
    self.window.rootViewController = tabbar;
    [self.window makeKeyAndVisible];
    return YES;
}
```


## 三.  要求 - Requirements

- ARC环境. - Requires ARC


## 四.  更新历史 - Update History

- 2017.03.12  修复tabbar销毁的时候观察者移除问题
- 2017.03.31  修复子控制器未添加时tabbar懒加载带来的问题
- 2017.04.05  修复更新提醒角标UI更新不及时问题
- 2017.04.10  修复设置导航栏为不透明后，坐标偏移问题(Bug 由 QQ用户龙卷风发现)
- 2017.04.18  更新Hiddentabbar的控制器方法，并将tabbar中间按钮点击方法委托出去(issue by star5cbh )

## 五.  更多 - More

- 如果你发现任何Bug 或者 新需求请issue我.

- 大家一起讨论一起学习进步.
 
- QQ : 707214577 点击<a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=707214577&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:707214577:52" alt="点击这里给我发消息" title="点击这里给我发消息"/>来给我发消息。</a>
  