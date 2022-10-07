# 一、Why Arduino？

常见的ESP32开发方式有三种：

- ESP-IDF

- Arduino IDE

- Micro Python

  

​	在乐鑫官网搜索[ESP32设计开发资料](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32/get-started/index.html#id8)时，会看到乐鑫公司针对ESP32的软件开发包是ESP-IDF，IDF是IoT Development Framework 的简称，即 物联网开发框架。ESP-IDF包含C/C++语言编辑器，所需的库函数，链接器等等......但ESP-IDF开发并不适合新手，使用它开发会直接劝退一大部分新人。而Arduino IDE自从1.6.4版本后，便将ESP32加入到了开发板管理工具，使得不属于Arduino家族的开发板也能通过Arduino语言和开发工具来编辑，编译和上传......

![compiler](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/arduinoesp32.png)

​	对于初学者来说，一个简单的入门方法是使用 Arduino IDE。

​	Arduino有简洁的编译器界面，一键编译和下载代码，丰富的函数库，及免费开源的环境，支持很多的种类的单片机。虽然这不一定是使用 ESP32 的最佳环境，但它的优势在于基本不需要考虑硬件底层的环境配置，只需要了解常用的接口函数即可快速开发一个项目，并且网上有大把的教程。

​	我第一次有意识的接触到乐鑫的产品是在大二那会儿，买了一个esp-01s的小模块，也是那时开始接触Arduino生态，发现arduino真的很简单，拿起来就能用，非常适合适合培养新手的开发兴趣。

使用arduino开发简单的项目，只考验c语言和你的编程逻辑，至于其他什么的会不会，问题都不大，这大大降低了各位的创作门槛，可以圆各位一个创客梦，这也是本视频的任务。



~~后话：但也正因为它太简单，这很不利于我们提升自己的其他技能。而esp32官方的SDK(esp-idf)不是很适合新手，而且教程较少；因此我建议，另外，各大招聘平台很少招只会arduino开发的，大多数都是需要你会其他单片机的。仍然有必要去学习stm32，了解寄存器，存储器等。~~



# 二、下载并安装Arduino IDE

Arduino IDE下载链接：https://www.arduino.cc/en/software

![image-20221007105611289](https://raw.githubusercontent.com/wild-civil/typora_img/main/images/image-20221007105611289.png)

基本一路Next，安装成功后会提示你安装一些驱动，选择信任并安装即可。(PS：可以自行修改安装路径),



常用函数参考：https://www.arduino.cc/reference/en/



# 三、设置ESP32的开发环境

### 1、常规操作：

参考Github开源实例https://github.com/espressif/arduino-esp32

①在Arduino IDE 首选项中添加 esp32开发版管理器地址：

```html
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json
```

②然后打开 **”工具“ -> ”开发板“ -> “开发板管理器”**，在搜索栏中输入esp32，选择适当的版本点击安装即可

（此方法适合网络良好的同学）



### 2、提供package安装

①将我提供的package解压在`C:\Users\[你的用户名]\AppData\Local\Arduino15\staging\packages`中

②打开 **”工具“ -> ”开发板“ -> “开发板管理器”**，在搜索栏中输入esp32，选择与我提供的安装包相同的版本安装



### 3、傻瓜式一键操作

双击我提供的安装包安装即可（安装包版本为1.0.6，问题不大）

地址：https://wwm.lanzoum.com/iuin20d2tyti 密码:1uh9



