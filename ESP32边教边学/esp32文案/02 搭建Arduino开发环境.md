# 一、Why Arduino？

常见的ESP32开发方式有三种：

- ESP-IDF

- Arduino IDE

- Micro Python

  

​	在乐鑫官网搜索ESP32设计开发资料时，会看到乐鑫公司针对ESP32的软件开发包是ESP-IDF，IDF是IoT Development Framework 的简称，即 物联网开发框架。ESP-IDF包含C/C++语言编辑器，所需的库函数，链接器等等......但ESP-IDF开发并不适合新手，使用它开发会直接劝退一大部分新人，而Arduino IDE自从1.6.4版本后，便将ESP32加入到了开发板管理工具，使得不属于Arduino家族的开发板也能通过Arduino语言和开发工具来编辑，编译和上传......

![compiler](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/arduinoesp32.png)



​	我第一次有意识的接触到乐鑫的产品是在大二那会儿，买了一个esp-01s的小模块，也是那时开始接触Arduino生态，发现arduino真的很简单，拿起来就能用，非常适合适合培养新手的开发兴趣。但也正因为它太简单，完全不需要考虑硬件底层的环境配置，只需要了解常用的接口函数即可快速开发一个项目，这很不利于我们提升自己的技能。而esp32官方的SDK(esp-idf)不是很适合新手，而且教程较少，因此我建议，仍然有必要去学习stm32，了解寄存器，存储器等。

~~另外，各大招聘平台很少招只会arduino开发的，大多数都是需要你会其他单片机的。简单来说，arduino只考验c语言和你的编程逻辑，至于其他什么的会不会，问题都不大，这大大降低了各位的创作门槛，圆各位一个创客梦，这也是本教学的任务。~~



