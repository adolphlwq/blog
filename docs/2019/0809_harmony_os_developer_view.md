# 鸿蒙OS揭面纱，开发者怎么看
千呼万唤使出来，2019.8.9下午，华为消费者业务CEO余承东正式官方宣布鸿蒙操作系统(HarmonyOS)。小编将从研发工程师的视角、结合官方报道，说说我对鸿蒙OS的理解。

## 四大技术特性
![](https://raw.githubusercontent.com/adolphlwq/osshub/master/oss/blog/2019/08/harmony_os_1.webp)

### 分布式架构
>鸿蒙OS的**分布式OS架构**和**分布式软总线技术**通过`公共通信平台`、`分布式数据管理`、`分布式能力调度`和`虚拟外设`四大能力，将相应分布式应用的底层技术实现难度对应用开发者屏蔽。

鸿蒙的一个理念是`把复杂留给自己，把简单留给开发者`。因此，鸿蒙OS把复杂的分布式架构向用户、开发者屏蔽，可能会通过SDK/API的方式提供给开发者，使开发者能够聚焦自身业务逻辑，像开发同一终端一样开发跨终端分布式应用。

### 流畅运行
>为了满足万物互联的全场景智慧时代对OS提出的新要求，鸿蒙OS将硬件能力与终端解耦，通过`分布式软总线`连接不同终端，让应用轻松调用其他终端的硬件外设能力，为消费者带来跨终端无缝协同体验。

流畅运行的性能是通过软硬件解耦实现的，其中技术核心是**分布式软总线**，这种技术有点像云计算，但云计算的主要计算资源是服务器，而鸿蒙OS的分布式软总线技术**还能够调用其它硬件设备**，这给笔者留下了巨大的想象空间！

### 安全
![](https://github.com/adolphlwq/osshub/raw/master/oss/blog/2019/08/harmony_os_2.webp)

>鸿蒙OS采用全新的微内核设计，拥有更强的安全特性和低时延等特点。

这里有很多专业术语，我们一一来看：
1. TEE(可信执行环境)：这是一种安全协议，它在硬件（包括芯片）、OS、软件单个层面提出了规范来保证安全可信。
![](https://github.com/adolphlwq/osshub/raw/master/oss/blog/2019/08/tee.jpeg)
2. 微内核：它是一种设计理念，将系统核心功能模块化运行在用户空间，只有需要的功能才运行在内核空间。设计上更简单，分布式系统中具备优势。但也要在服务间通信，这需要上下文切换，影响时延和性能。
![](https://github.com/adolphlwq/osshub/raw/master/oss/blog/2019/08/OS_structure.png)

从上面的名词解释可以知道，鸿蒙OS采用微内核有其使用场景上的考虑，它在分布式上具备优势，同时在性能上还需要优化。


### 生态
>鸿蒙OS配备面向多终端开发的统一IDE（集成开发工具），可支撑开发者实现一次开发、多端部署，最终实现跨终端生态共享

从上面可以知道，鸿蒙OS会为开发者提供IDE（有点像苹果，苹果向开发者提供了Xcode IDE），IDE帮开发者省去很多复杂的设置，让开发者可以快速开发出程序，在多终端部署，实现一次开发、多终端部署。

## 总结
操作系统不仅在于技术上的好坏，还涉及生态的建设，否则系统再好却没人用，也没有多大意义。华为做系统和生态有自身独特的优势：
- 核心技术：独立设计芯片的能力，5G芯片标准和专利。
- 庞大的用户群：不解释，出货量全球前三。

这样的优势使得OS的推广和生态建设更容易些，不想微软的Windows Phone，因为没有用户在推广上非常艰难，最终失败。

不过，华为对于鸿蒙OS的介绍还是很简洁，对于`分布式`这个特点，看完官方介绍后发现和笔者理解的分布式技术似乎有区别，不过随着后续开源应该会明确。

5G技术的发展，我们很快会进入IoT时代，那时的终端将会更加丰富,已知的有智能手表、智能音箱、AR/VR眼镜、汽车，未来还有更多的智能终端出现。这对操作系统提出了新的需求，因此，开发出面向未来、符合未来需求的操作系统是一种战略，就像移动互联网时代的Android，谁掌握了IoT时代的操作系统，谁就拥用行业和生态的话语权。工业界已经在尝试自己的方案，比如Google的[Flutter框架](https://flutter.dev/)和[FuchsiaOS](https://fuchsia.dev/)。从这个角度看，鸿蒙OS，未来可期。

## 参考
- [可信执行环境（TEE）技术介绍](https://blog.csdn.net/trustbo/article/details/78234373)
- [微内核](https://zh.wikipedia.org/wiki/%E5%BE%AE%E5%85%A7%E6%A0%B8)