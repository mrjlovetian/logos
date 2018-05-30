
# Logos语法
###fishhook
//结构体
struct rebinding bd;
bd.name //函数名称 字符串
bd.replacement //新函数的地址
bd.replaced //原始函数的地址的指针!
rebind_symbols(数组,数组长度);


#### 1.MachO是被谁加载的   DYLD 动态加载
#### 2.ASLR技术 MachO文件加载的时候是随机地址!
#### 3.PIC 位置代码独立
	: 如果MachO内部需要调用 系统的库函数时
	: 先在 _DATA段中建立一个指针,指向外部函数
	: DYLD 会动态的进行绑定!将MachO中的DATA段中的指针,指向外部函数!

-- 防护的作用!! OC HOOK防护的

Logos:

 
//Class1         Class2
//Method1     Method2

Method_ExchangeIMP(method1,method2);

Method2{
	self;//Class1 ? Class2  self 是根据方法的调用来的!谁调用的我,self就是谁!!
}

Method1{

}

[Objc1  method1];




