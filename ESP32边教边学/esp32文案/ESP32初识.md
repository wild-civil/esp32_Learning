# 一、ESP32初识

## ESP32是什么？

ESP32是由[乐鑫公司（Espressif）](https://www.espressif.com/zh-hans)研发，结合Wi-Fi和蓝牙的32位系统级芯片(SoC)[^1]。常见的esp32芯片内部有两个处理器：==<u>32位双核心主处理器</u>==和==<u>8位低功耗处理器</u>==，主处理器采用Xtensa架构。低功耗处理器可在主处理器进入睡眠状态时，维持在运行状态，可以在有"状况"发生时，唤醒主处理器。

![doublecpu](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/esp32doublecpu.png)

- PRO_CPU: 负责处理和操控Wi-Fi、蓝牙和其他接口(I^2^C, SPI, ...等);
- APP_CPU: 执行主程序(用户自己写的代码).

---

## ESP32芯片

esp32芯片有不同的型号，并且持续更新中：


- ESP32-D0WDQ6: 最常见的型号，双核心...

- ESP32-PICO-D4: 内置4M闪存...
- ESP32-S3: 单核心LX7处理器，支持Wi-Fi 4 和 蓝牙5.0、AI加速运算...
- ESP32-C3: 单核心RISC-V处理器，支持Wi-Fi 4 和 蓝牙5.0...

- $\cdots$

---

## ESP32模组

乐鑫公司也有推出整合ESP32和闪存的模组，例如常见的ESP-WROOM-32模组，并被广泛应用于各种开发板中，

![](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/espwromm32.png)

WROOM模组加上 <u>直流电源降压芯片</u> 和 <u>UART转USB芯片</u>，就能组成一个基本的ESP32开发板： 

![](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/uartusb.png)



## ESP32开发板

[ESP32-DevKitC](https://www.espressif.com.cn/zh-hans/products/devkits/esp32-devkitc)是一款由乐鑫公司（Espressif）基于 <u>ESP-WROOM-32 模组</u>的小型开发板，支持 Wi-Fi 和蓝牙功能，其 外观 以及 引脚分布 如下图：

![](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/esp32devkitc.png)

<div align='center'>
  <img src='https://raw.githubusercontent.com/wild-civil/typora_img/main/images/esp32-devkitC-v4-pinout.png' width=560px>
  <p align='center' style='font-size:16px;font-family:kaiti;color:red'>esp32管脚布局</p>
</div>



ESP32 的其他特性包括：

- 多达 18 个 12 位模数转换器
- 两个 8 位数模转换器
- 10 个电容式触摸开关传感器
- 四个 SPI 通道
- 两个 I^2^C 接口
- 两个 I^2^S 接口（用于数字音频）
- 三个用于通信的 UART
- 多达 8 个通道的 IR 遥控器
- 多达 16 个 LED PWM（脉冲宽度调制）通道
- 集成霍尔效应传感器
- 超低功耗模拟前置放大器
- 一个内部低压差稳压器

- ……



​      


# 二、Why Arduino？

​	在乐鑫官网搜索ESP32设计开发资料时，会看到乐鑫公司针对ESP32的软件开发包是ESP-IDF，IDF是IoT Development Framework 的简称，即 物联网开发框架。ESP-IDF包含C/C++语言编辑器，所需的库函数，链接器等等......但ESP-IDF开发并不适合新手，使用它开发会直接劝退一大部分新人，而Arduino IDE自从1.6.4版本后，便将ESP32加入到了开发板管理工具，使得不属于Arduino家族的开发板也能通过Arduino语言和开发工具来编辑，编译和上传......

![](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/arduinoesp32.png)



​	我第一次有意识的接触到乐鑫的产品是在大二那会儿，买了一个esp-01s的小模块，也是那时开始接触Arduino生态，发现arduino真的很简单，拿起来就能用，非常适合适合培养新手的开发兴趣。但也正因为它太简单，完全不需要考虑硬件底层的环境配置，只需要了解常用的接口函数即可快速开发一个项目，这很不利于我们提升自己的技能。而esp32官方的SDK(esp-idf)不是很适合新手，而且教程较少，因此我建议，仍然有必要去学习stm32，了解寄存器，存储器等。

~~另外，各大招聘平台很少招只会arduino开发的，大多数都是需要你会其他单片机的。简单来说，arduino只考验c语言和你的编程逻辑，至于其他什么的会不会，问题都不大，这大大降低了各位的创作门槛，圆各位一个创客梦，这也是本教学的任务。~~



大家手上的ESP32开发板应该都大同小异，之后编写的程序也应该是相通的。







# 课余兴趣作业：

[^1]:了解MCU、MPU、SoC是什么，有什么区别

