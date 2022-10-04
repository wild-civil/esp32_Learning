# ESP32初识

ESP32是由[乐鑫公司（Espressif）](https://www.espressif.com/zh-hans)研发，结合Wi-Fi和蓝牙的32位系统级芯片(SoC)。常见的esp32芯片内部有两个处理器：==<u>32位双核心主处理器</u>==和==<u>8位低功耗处理器</u>==，主处理器采用Xtensa架构。低功耗处理器可在主处理器进入睡眠状态时，维持在运行状态，定在有"状况"发生时，唤醒主处理器。

![doublecpu](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/esp32doublecpu.png)

- PRO_CPU: 负责处理和操控Wi-Fi、蓝牙和其他通信协议(I^2^C, SPI, ...等);
- APP_CPU: 执行主程序(用户自己写的代码);

[ESP32-DevKitC](https://www.espressif.com.cn/zh-hans/products/devkits/esp32-devkitc)是一款由乐鑫公司（Espressif）基于 ESP32 模组的小型开发板，支持 Wi-Fi 和蓝牙功能。



<div align='center'>
  <img src='https://raw.githubusercontent.com/wild-civil/typora_img/main/images/esp32-devkitC-v4-pinout.png' width=450px>
  <p align='center' style='font-size:15px;font-family:kaiti;color:red'>esp32管脚布局</p>
</div>



## 使用Arduino的原因——简单易上手

​	我第一次有意识的接触到乐鑫的产品是在大二那会儿，买了一个esp-01s的小模块，也是那时开始接触Arduino生态，发现arduino真的很简单，拿起来就能用，非常适合适合培养新手的开发兴趣。但也正因为它太简单，完全不需要考虑硬件底层的环境配置，只需要了解常用的接口函数即可快速开发一个项目，这很不利于我们提升自己的技能。而esp32官方的SDK(esp-idf)不是很适合新手，而且教程较少，因此我建议，仍然有必要去学习stm32，了解寄存器，存储器等。

~~另外，各大招聘平台很少招只会arduino开发的，大多数都是需要你会其他单片机的。简单来说，arduino只考验c语言和你的编程逻辑，至于其他什么的会不会，问题都不大，这大大降低了各位的创作门槛，圆各位一个创客梦，这也是本教学的任务。~~



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
