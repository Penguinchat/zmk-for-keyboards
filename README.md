# zmk for keyboards
这是一个存放有多个分体式键盘zmk固件源码以及已编译固件的仓库  
corne sofle（RGB，choc） lily58 heiix（目前只有这几个，以后或许会有其他键盘放入）  
本仓库固件所测试用pcb均来自[PandaKB外设](https://pandakb.taobao.com/shop/view_shop.htm?spm=a21n57.1.0.0.5d79523cNmnkU0&appUid=RAzN8HWMnqHhQPoqPWJj8vvpxQEUo4LsYqKaxNw4JRKQfkmLoFX)
## 仓库中的固件可能有以下功能
### key（基础按键功能）
zmk潜在的combo，tap dance等按键功能如需要请参照[zmk文档](https://zmk.dev/docs/keymaps)添加代码进行适配
### rgb（zmk光效比较少，四种）
参考[zmk文档](https://zmk.dev/docs/config/underglow)  
若需修改灯效，可通过zmk studio添加灯效切换按键  
或直接于键盘固件代码config文件中  
`CONFIG_ZMK_RGB_UNDERGLOW_EFF_START`
|value|       光效        |
|-|-|
|  0  |       纯色        |
|-|-|
|  1  |       呼吸        |
|-|-|
|  2  |       光谱        |
|-|-|
|  3  |       旋流        |
### zmk studio（zmk studio是zmk推出的在线改键软件，包括app及web，其中web支持usb改键，app同时支持usb改键以及蓝牙改键）
usb改键[zmk studio_web在线改键](https://zmk.studio/)  
app改键[zmk studio_app](https://github.com/zmkfirmware/zmk-studio/releases/tag/v0.2.4)  

usb改键只需连接分体键盘左手即可进行改键，蓝牙改键只需键盘处于连接状态打开app进行匹配就可进行改键  
（注：zmk studio的启用暂处于起步阶段，功能支持有限，相比于已较为完善的via以及vial改键，仍有发展空间，zmk studio目前支持功能请参考[zmk文档](https://zmk.dev/docs/features/studio)  
### 键盘休眠
没什么好说的，请参考[zmk文档](https://zmk.dev/docs/config/power#low-power-states)
电池上报√ rgb休眠√ 休眠时间设置√ 
### oled
默认的oled显示的内容用了github上开源的zmk module[nice_oled](https://github.com/mctechnology17/zmk-nice-oled?tab=readme-ov-file)
这个module是动画的，还是很好玩的，同时感谢作者的开源@mctechnology17
![image](https://github.com/mctechnology17/zmk-nice-oled/blob/main/assets/preview2.JPG?raw=true)
### nice view
nice view作为一款基本可以说为zmk而生的屏幕，其显示内容也十分丰富  
本仓库默认使用的nice view module为[Hammerbeam Slideshow](https://github.com/GPeye/hammerbeam-slideshow) @GPeye  
![image](https://github.com/GPeye/hammerbeam-slideshow/blob/main/assets/hammerbeam.png)  
![image](https://github.com/GPeye/hammerbeam-slideshow/blob/main/assets/20240913_193934.png)  
这是一个非常好玩的module，他为nice view提供相当多的图片，并且能够进行10秒一次的切换，切换时间可以进行修改。  
以下为github上开源的nice view的zmk module  
[nice_view_elemental](https://github.com/kevinpastor/nice-view-elemental)l @kevinpastor  
![image](https://github.com/kevinpastor/nice-view-elemental/blob/main/assets/banner.png)  
[nice_view_gem](https://github.com/M165437/nice-view-gem) @M165437  
![image](https://github.com/m165437/nice-view-gem/blob/main/.github/assets/preview.jpg?raw=true)  
这个和默认的oled显示内容是一样的，为动画，但其实oled那个module是从这个module移植来的，反正就是好玩就行了  
[nice_view_cats](https://github.com/s6t/zmk-shield-nice-view-cats) @s6t  
![image](https://github.com/s6t/zmk-shield-nice-view-cats/blob/main/images/image1.png)  
谁不想要在键盘上养两只猫猫呢  
[nice_view_battery](https://github.com/infely/nice-view-battery) @infely    
![image](https://github.com/infely/nice-view-battery/blob/main/.github/assets/preview.jpg?raw=true)  
这个module显示的内容十分简约，有一种简单的美  
而如何进行nice view显示内容的切换？以下为简单教程
如在build.yaml文件中  
`shield: corne_left nice_view_adapter nice_view_custom` 
`shield: corne_right nice_view_adapter nice_view_custom`  
只需通过修改nice_view_custom为其他module相应的内容就可以进行切换
|       module       |       修改内容        |
|-|-|
|Hammerbeam Slideshow|   nice_view_custom   |
|-|-|
|nice_view_elemental |  nice_view_elemental |
|-|-|
|    nice_view_gem   |    nice_view_gem     |
|-|-|
|   nice_view_cats   |    nice_view_cats    |
|-|-|
| nice_view_battery  |   nice_view_battery  |
## 可能会有的其他功能
zmk在最近加入了point device（指点设备），就是一些类似于鼠标键，轨迹球，触摸板，指点杆等设备的支持，未来可能会有，是一个futural todo :)  
其次是dongle的支持，目前最新的有彩屏的st7789屏幕做2.4g接收器，这也是一个 futural todo :)  
最后，感谢zmk的开源，以及各种module的开源的作者的无私奉献  
如果这个仓库对你有帮助，:)  


