# nsobj

isequal
如果两个对象相同怎返回true，表明者两个对象有相同的hash值，着在当需要在集合对象中添加子对象时通常先要确认isequal，然后安hash表保证对象唯一性，详见photonimal。

 @protocol NSObject 协议
 - (BOOL)isEqual:(id)object;  首先判断两个对象是否类型一致， 再判断具体内容是否一致
 - (NSUInteger)hash;  返回一个整数，可以用来作为哈希表结构中的表地址
 - (Class)superclass; 返回超类对象
 - (Class)class; 返回类对象
 - (id)self;  返回当前对象
 - (NSZone *)zone; 垃圾自动回收
 - (id)performSelector:(SEL)aSelector; 将指定的消息配送到接收器，应用aSelector指定的消息
 - (id)performSelector:(SEL)aSelector withObject:(id)object;将一个对象的消息配送到接收器，应用aSelector指定的消息
 - (id)performSelector:(SEL)aSelector withObject:(id)object1 withObject:(id)object2;  将2个对象消息配送到接收器，应用aSelector指定的消息
 - (BOOL)isProxy;  判断是否接收器是否从NSObject协议继承
 - (BOOL)isKindOfClass:(Class)aClass; 判断是否是这个类或者这个类的子类的实例
 - (BOOL)isMemberOfClass:(Class)aClass; 判断是否是这个类的实例
 - (BOOL)conformsToProtocol:(Protocol *)aProtocol; 判断是否符合指定协议
 - (BOOL)respondsToSelector:(SEL)aSelector;   判断是否实现了某方法
 - (id)retain; 增加对象的计数器
 - (oneway void)release;  减少对象的计数器
 - (id)autorelease; 自动减少对象的计数器，但是以推迟的方式来实现
 - (NSUInteger)retainCount;  返回一个对象当前的计数器
 - (NSString *)description;  允许一个对象返回一个字符串来描述它的内容；这个常用于调试debugging (“print  object”命令 )
 - (NSString *)debugDescription; 返回一个字符串，描述在调试器中的接收器演示的内容
 @end
