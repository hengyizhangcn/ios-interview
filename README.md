# ios-interview
ios 面试知识点<br>
欢迎提出错误点


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
一个用于发送数据，一个用于获取数据<br>
5.http请求方式有哪些<br>
增删改查put, delete, post, get<br>
options, head, trace, connect, 实际中用post/get来间接实现其它的功能<br>
6.swift和oc优缺点<br>
7.swift中!和?是做什么的<br>
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
代理模式，如tableview，等</br>
工厂模式，<br>
单例模式<br>
装饰器模式，不改变原来代码的情况下，给对象增加新的行为和职责，如类别和代理<br>
观察者设计模式，如notification, kvo<br>
策略模式，<br>
33.APNS原理是怎样的<br>
34.网络请求常见的错误代号是什么<br>
1xx 信息提示<br>
-100 继续<br>
-101 切换协议<br>
2xx 成功<br>
-200 客户端请求已成功<br>
-201 已创建<br>
-202 已接受<br>
-203 非权威信息<br>
-204 无内容<br>
-205 重置内容<br>
-206 部分内容<br>
-207 多状态<br>
3xx 重定向<br>
-301 已永久移动<br>
-302 对象已移动<br>
-304 未修改<br>
-307 临时重定向<br>
4xx 客户端错误，如请求了不存在的页面，没有进行有效的身份验证<br>
-400 错误的请求<br>
-401 访问被拒绝<br>
-403 禁止访问<br>
-404 未找到<br>
-406 客户端浏览器不接受所请求页面的MIME类型<br>
-412 前提条件失败<br>
-413 请求实体太长<br>
-414 请求URI太长<br>
-415 不支持的媒体类型<br>
-417 执行失败<br>
5xx 服务器错误<br>
-500 内部服务器错误<br>
-504 网关超时<br>
-505 http版本不受支持<br>
35.XML解析方式<br>
NSXMLParse<br>
36.多线程有哪些，比较它们的不同<br>
37.以+ scheduledTimerWithTimeInterval...的方式触发的timer，在滑动页面上的列表时，timer会暂定回调，为什么？如何解决？<br>
38.retain和strong的区别<br>
39.autorelease什么时候释放<br>
40.GCD并发控制<br>
dispatch_semaphore_create<br>
dispatch_semaphore_signal<br>
dispatch_semaphore_wait<br>
41.MRC和ARC的区别<br>
42.dealloc不调用的原因有哪些<br>
43.视图一闪而过，可能原因是什么<br>
<br>
<br>
#进阶知识点
1.KVO怎么手动调用<br>
2.UITableView的卡顿处理<br>
3.方法调用流程是什么<br>
objc_msgSend(receiver, selector, arg1, ...)<br>
动态方法解析+resolveInstanceMethod或+resolveClassMethod<br>
备用接收者forwardingTargetForSelector<br>
消息转发forwardInvocation<br>
methodSignatureForSelector<br>

4.NSDictionary使用了哪些数据结构和算法<br>
5.类方法，实例方法与Runtime特性的联系<br>
6.block调用时，变量的生命周期有哪几种，分别是什么样的<br>
7.CALayer的多个Sub Layer的数据结构以及重绘顺序<br>
8.如何制作静态库或动态库<br>
9.如何降低应用的大小<br>
10.cocoa touch<br>
11.coredata<br>
12.runtime<br>
项目中用到runtime的地方有哪些？获取类的属性名，属性类型等，保存对象，替换方法的实现<br>
1)类与对象<br>
class_getName<br>
class_getSuperclass<br>
class_isMetaClass是否是元类<br>
class_getInstanceSize获取实例大小<br>
class_getInstanceVariable获取类中指定名称实例成员变量的信息<br>
class_getClassVariable获取类成员变量信息<br>
class_addIvar添加成员变量<br>
class_copyIvarList获取整个成员变量列表<br>
class_addProperty添加属性<br>
class_replaceProperty替换类属性<br>
class_addMethod添加方法<br>
class_getInstanceMethod获取实例方法<br>
class_getClassMethod获取类方法<br>
class_copyMethodList获取所有方法的数组<br>
class_replaceMethod替代方法实现<br>
class_getMethodImplementation返回具体的方法实现<br>
class_getMethodImplementation_stret返回具体的方法实现<br>
class_respondsToSelector类实例是否响应指定的selector<br>
class_addProtocol<br>
class_conformsToProtocol<br>
class_copyProtocolList<br>
class_getVersion获取版本号<br>
class_setVersion设置版本号<br>
objc_getFutureClass<br>
objc_setFutureClass<br>
动态创建类<br>
objc_allocateClassPair创建一个新类和元类<br>
objc_disposeClassPair销毁一个类及其相关联的类<br>
objc_registerClassPair在应用中注册由objc_allocateClassPair创建的类<br>
动态创建对象<br>
class_createInstance创建类实例<br>
objc_constructInstance指定位置创建类实例<br>
objc_destructInstance销毁类实例<br>
实例操作函数<br>
object_copy拷贝对象<br>
object_dispose释放指定对象占用的内存<br>
object_setInstanceVariable修改类实例的实例变量的值<br>
object_getInstanceVariable获取对象实例变量的值<br>
object_getIndexedIvars获取指向给定对象分配的任何额外字节的指针<br>
object_getIvar返回对象中实例变量的值<br>
object_setIvar设置对象中实例变量的值<br>
object_getClassName返回对象的类名<br>
object_getClass返回对象的类<br>
object_setClass设置对象的类<br>
获取类定义<br>
objc_getClassList获取已注册类定义的列表<br>
objc_copyClassList创建并返回一个指向所有已注册类的指针列表<br>
objc_lookUpClass返回指定类的定义<br>
objc_getClass<br>
objc_getRequiredClass<br>
objc_getMetaClass<br>
参考：http://www.codeceo.com/article/objective-c-runtime-class.html<br>
2)成员变量与属性<br>
objc_property_t，指向objc_property结构体指针<br>
objc_property_attribute_t，定义属性特性的结构体<br>
objc_setAssociatedObject设置关联对象<br>
objc_getAssociatedObject获取关联对象<br>
objc_removeAssociatedObjects移除关联对象<br>
ivar_getName获取成员变量名<br>
ivar_getTypeEncoding获取成员变量类型编码<br>
ivar_getOffset获取成员变量偏移量<br>
property_getName获取属性名<br>
property_getAttributes获取属性特性描述字符串<br>
property_copyAttributeValue获取属性的特性列表<br>
参考：http://www.cocoachina.com/ios/20141105/10134.html<br>
3)方法与消息<br>
objc_selector<br>
objc_method<br>
method_invoke调用指定方法的实现<br>
method_invoke_stret调用返回一个数据结构的方法的实现<br>
method_getName获取方法名<br>
method_getImplementation返回方法的实现<br>
method_getTypeEncoding获取描述方法参数和返回值类型的字符串<br>
method_copyReturnType获取方法的返回值类型的字符串<br>
method_copyArgumentType获取方法的指定位置参数的类型字符串<br>
method_getReturnType通过引用返回方法的返回值类型字符串<br>
method_getNumberOfArguments返回方法的参数个数<br>
method_getArgumentType通过引用返回方法指定位置参数类型字符串<br>
objc_method_description返回指定方法的方法描述结构体<br>
method_setImplementation设置方法的实现<br>
method_exchangeImplmentations交换两个方法的实现<br>
消息发送<br>
objc_msgSend(receiver, selector, arg1, ...)<br>
动态方法解析+resolveInstanceMethod或+resolveClassMethod<br>
备用接收者forwardingTargetForSelector<br>
消息转发forwardInvocation<br>
methodSignatureForSelector<br>
参考：http://www.cocoachina.com/ios/20141106/10150.html<br>
4)method swizzling方法混写<br>
运行时特点：选择器、方法和实现<br>
swizzling应该在+load中执行<br>
swizzling应该在dispatch_once中执行<br>
注意事项：<br>
a.总是调用方法的原始实现<br>
b.避免命名冲突<br>
c.明白怎么回事<br>
d.小心操作<br>
参考：http://blog.jobbole.com/79580/<br>
http://www.cocoachina.com/ios/20140225/7880.html<br>
5)协议与分类<br>
objc_category<br>
<br>
objc_getProtocol返回指定协议<br>
objc_copyProtocolList获取运行时，所知道的所有协议的数组<br>
objc_allocateProtocol创建新的协议实例<br>
objc_registerProtocol注册新的协议<br>
protocol_addMethodDescription为协议添加方法<br>
protocol_addProtocol添加到一个已注册的协议到协议中<br>
protocol_addProperty为协议添加属性<br>
protocol_getName返回协议名<br>
protocol_isEqual检测两个协议是否相等<br>
protocol_copyMethodDescriptionList获取协议中指定条件的方法描述数组<br>
protocol_getMethodDescription获取协议中指定方法的方法描述<br>
protocol_copyPropertyList获取协议中的属性列表<br>
protocol_getProperty获取协议的指定属性<br>
protocol_copyProtocolList获取协议采用的协议<br>
protocol_conformsToProtocol查看协议是否采用了另一个协议<br>
注：协议一旦注册不可再修改<br>
参考：http://www.cocoachina.com/ios/20141110/10174.html<br>
6)补充<br>
库相关<br>
objc_copyImageNames获取所有加载的objective-c框架和动态库的名称<br>
class_getImageName获取指定类所在的动态库<br>
objc_copyClassNameForImage获取指定库或框架中所有类的类名<br>
块操作<br>
imp_implementationWithBlock创建一个指针函数的指针，该函数调用时会调用特定的block<br>
imp_getBlock返回与IMP相关的block<br>
imp_removeBlock解除block与imp的关联关系，并释放block的拷贝<br>
弱引用<br>
objc_loadWeak加载弱引用指针引用的对象<br>
objc_storeWeak存储__weak变量的新值<br>
宏定义<br>
<br>
参考：http://www.cocoachina.com/ios/20141111/10186.html<br>
<br>
13.并行开发<br>
14.rest application<br>
15.encrypt/decrypt<br>
16.http cline/server<br>
17.graphic<br>
18.语音压缩<br>
19.内存分析调优<br>
20.GCD<br>
dispatch_once<br>
dispatch_async<br>
dispatch_sync<br>
dispatch_get_main_queue<br>
dispatch_get_global_queue<br>
dispatch_get_current_queue，如果targetqueue是current_queue,同步阻塞会导致死锁
dispatch_after<br>
dispatch_semaphore_create<br>
dispatch_semaphore_signal<br>
dispatch_semaphore_wait<br>
dispatch_group_create<br>
dispatch_group_async<br>
dispatch_group_sync<br>
dispatch_group_notify<br>
dispatch_group_wait<br>
dispatch_group_enter<br>
dispatch_group_leave<br>
dispatch_source_create<br>
dispatch_source_cancel<br>
dispatch_source_release<br>
dispatch_source_set_timer<br>
dispatch_resume<br>
dispatch_release<br>
dispatch_retain<br>

dispatch_queue_set_specific标记队列



#高阶
1.插件化开发<br>
2.面向协议编程(POP)<br>
protocol oriented programming
3.代码调试和调优<br>
4.事件响应机制<br>
5.响应式编程<br>
6.函数式编程(functional programming)<br>
面向值的编程(VOP)<br>
value-oriented pragramming
7.OOA/OOD<br>
8.OpenGL ES、ffmpeg<br>
9.NFC<br>
10.依赖注入<br>

#热点技术
1.MVVM<br>
2.React Native<br>
3.Hybrid App<br>
4.JsPath<br>
5.逆向反编译技术<br>
6.Rest Application<br>

