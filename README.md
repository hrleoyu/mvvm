# mvvm
**MVVM**是**Model-View-ViewModel**的简写，是一个软件架构设计模式。而在MVVM框架中，View(视图)和Model(数据)是不可以直接通讯的，在他们之间存在着ViewModel这个中间介充当着观察者的角色。当用户操作View，ViewModel感知到变化然后传递给Model发生相应的改变，反之亦然。这一来一回就是我们所说的双向绑定。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200401013431920.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NjUxMjY5MA==,size_16,color_FFFFFF,t_70#pic_center)
**Object.defineProperty()**
这个 api 是实现双向绑定的核心，最主要的作用是重写数据的 get 、 set 方法。

通过`observer`函数进行数据的监听，通过`compile`函数遍历dom对象进行编译。