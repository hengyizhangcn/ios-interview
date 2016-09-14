# ios-interview
ios 面试知识点

#基础知识点
1.import和class的区别<br>
2.数据库增加/修改表属性，DDL, DML, DQL, DCL分别是什么<br>
3.viewdidload和loadview区别, controller的生命周期是怎样的，调用顺序呢<br>
Implement loadView to create a view hierarchy programmatically, without using a nib, no super to call<br>
Implement viewDidLoad to do additional setup after loading the view, typically from a nib. Has to call super<br>
（controller的view默认为uiview，如果想修改类型，可以在loadview里面完成）<br>
controller生命周期：alloc->init->loadview->viewdidload->viewwillappear->viewdidappear->viewwilldisapper->viewdiddisappear->dealloc<br>
如果有内存警告，可能调用的顺序是:viewdiddisappear->内存警告->viewdidunload->对象被释放<br>
4.post和get的区别<br>
5.swift和oc优缺点<br>
6.swift中!和?是做什么的<br>
7.http请求方式有哪些<br>
8.工作中用到的工具或插件有哪些<br>
VVDocument, Backlight(Xcode8中已内置该功能，可废弃), KSImageNamed(Xcode8中已内置该功能，可废弃)<br>
git, zsh, brew, fastlane, cocopods, dyci, iterms<br>
JSONView, OneTab<br>
souretree, cornerstone, sublime, Xmind, Reveal, Charles, MarkMan, Jenkins, iTools<br>
9.类别和子类的区别<br>
10.循环引用怎么产生的<br>
11.xib和storyboard的区别<br>
12.kvo有哪些，kvc呢<br>
13.代理和通知的区别，<br>
14.UIAlertViewController为什么舍弃了代理模式，而UITableView还保留<br>
15.sdwebimage工作原理，为什么不直接使用afnetworking<br>
16.oc中extension和swift区别<br>
17.c中的内存类型有哪些<br>
18.NSCopying协议<br>
19.storyboard和纯代码的区别<br>
20.mvc是怎么通信的<br>
21.autolayout和frame的区别, autolayout什么实现的<br>
22.以空间复杂度换时间复杂度会产生什么影响<br>
23.NSIteger和int的区别<br>
24.本地保存数据机制有哪些<br>
25.swift和ios10了解多少<br>
26.常去的网站有哪些<br>
27.cell中子视图添加到self和self.contentview的区别<br>
28.__block和__weak的区别<br>
29.使用的第三方组件有哪些<br>
30.GCD队列分类<br>
31.内存管理是怎样的<br>
32.设计模式有哪些<br>
33.APNS原理是怎样的<br>
34.网络请求常见的错误代号是什么<br>
35.XML解析方式<br>
36.多线程有哪些，比较它们的不同<br>
37.以+ scheduledTimerWithTimeInterval...的方式触发的timer，在滑动页面上的列表时，timer会暂定回调，为什么？如何解决？<br>
38.retain和strong的区别<br>
39.autorelease什么时候释放<br>
40.GCD并发控制<br>
41.MRC和ARC的区别<br>
42.dealloc不调用的原因有哪些<br>
43.视图一闪而过，可能原因是什么<br>
<br>
#进阶知识点
1.KVO怎么手动调用<br>
2.UITableView的卡顿处理<br>
3.方法调用顺序是什么<br>
4.NSDictionary使用了哪些数据结构和算法<br>
5.类方法，实例方法与Runtime特性的联系<br>
6.block调用时，变量的生命周期有哪几种，分别是什么样的<br>
7.CALayer的多个Sub Layer的数据结构以及重绘顺序<br>
8.如何制作静态库或动态库<br>
9.如何降低应用的大小<br>
10.cocoa touch<br>
11.coredata<br>
12.runtime<br>
13.并行开发<br>
14.rest application<br>
15.encrypt/decrypt<br>
16.http cline/server<br>
17.graphic<br>
18.语音压缩<br>
19.内存分析调优<br>

#高阶
1.插件化开发<br>
2.面向协议开发<br>
3.代码调试和调优<br>
4.事件响应机制<br>
5.响应式编程<br>
6.函数式编程<br>
7.OOA/OOD<br>
8.OpenGL ES、ffmpeg<br>
9.NFC<br>

#热点技术
1.MVVM<br>
2.React Native<br>
3.Hybrid App<br>
4.JsPath<br>
5.逆向反编译技术<br>

