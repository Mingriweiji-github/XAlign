###XAlign:用于代码对齐的Xcode插件
XAlign 是一个 Xcode 的实用插件，用于对齐规范代码。除了插件作者 qfish 提供的 3 种对齐格式，还可以自定义任意你想要的格式。

示例

qfish 分享的 3 张示例图（ Gif ），如下：

**1.按首个 = 对齐**

 ![](http://ww3.sinaimg.cn/large/7cc829d3gw1eb5sxhxi2xg20jy0eokfw.gif)


**2.宏定义组对齐**

![](http://ww4.sinaimg.cn/large/7cc829d3gw1eb5sxk9pjtg20jy0d8e3r.gif) 

**3. 按属性群组对齐**

![](http://ww3.sinaimg.cn/large/7cc829d3gw1eb5sxp4vcgg20iq0cmaq5.gif)

###安装方法
####自动安装（打开终端，复制下面代码到终端）
>curl -fsSL http://qfi.sh/XAlign/build/install.sh | sh

####手动安装
- 下载
- 解压后，复制 *XAlign.xcplugin* 到下面的目录中
>~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/

- 友情提示: cmd+shift+g 快速查找；如果没有 Plug-ins 目录，你得创建一个

- 重启Xcode即可

###使用说明
- 直接打开Xcode
>Xcode -> Edit -> XAlign 

- 或者快捷键
>shfit + cmd + x

###卸载
>打开command-line，输入下面代码

> curl github.so/XAlign/build/uninstall.sh | sh


###或者直接删除下面的目录，代码如下：

>~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/XAlign.xcplugin



>翻译说明地址
**@github地址**：https://github.com/Mingriweiji-github/XAlign

我是中文分割线

---

XAlign
======

An amazing Xcode plugin to align regular code. It can align anything by using custom alignment patterns.

## What's XAlign

Here are some example alignment patterns. Of course you can make your own. The pattern file is here:  `XAlign/patterns.plist`, and the patterns are based on regular expression.

**Tips**: 

   * _You may not like the alignment style below, **try it yourself** or **tell me at the  [[Issues]](https://github.com/qfish/XAlign/issues?state=open)**._ :)
   * There is no need to align all codes at a time when they are complicated, try to align by group which the codes are more similar in.
   * 对齐不需要一次全部对齐，可以分组多对几次，那些等号差的太远的就别让它参与对齐了。
   * 默认对齐的风格不是你喜欢的，可以自定义，或者提个 [Issues](https://github.com/qfish/XAlign/issues?state=open)。

### Align by equals sign
![Equal](http://qfi.sh/XAlign/images/equal.gif)

### Align by define group
![Define](http://qfi.sh/XAlign/images/define.gif)

### Align by property group
![Property](http://qfi.sh/XAlign/images/property.gif)

### Todo:

- [x] Much easier to customize alignment patterns.

## Install & Update

### Via source

1. Clone this repo

2. Then build the `XAlign` target in the Xcode project and the plug-in will automatically be installed in `~/Library/Application Support/Developer/Shared/Xcode/Plug-ins`

3. Restart Xcode.

### Via command-line

```shell
curl -fsSL http://qfi.sh/XAlign/build/install.sh | sh
```

### Manually

1. Download this package [XAlign.tar.gz](http://qfi.sh/XAlign/build/XAlign.tar.gz)
2. Unpack it, copy or move the `XAlign.xcplugin` to the following path:
    ```
    ~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/
    ```
    Tips: To quickly go to Finder type `Shift + Cmd + G`. If there is no `Plug-ins` directory, you should make one.

3. Restart Xcode.

## Uninstall
```shell
curl -fsSL http://qfi.sh/XAlign/build/uninstall.sh | sh
```

or Delete the following directory:

```
~/Library/Application Support/Developer/Shared/Xcode/Plug-ins/XAlign.xcplugin
```

## Usage
### In Xcode
```
Xcode -> Edit -> XAlign 
```

### Auto Align Shortcut (default)
```
Shift + Cmd + X
```
You can choose the shortcut in the Settings panel, `Xcode -> Edit -> XAlign -> Setting`.

## Trouble-Shooting
  
  * [wiki](https://github.com/qfish/XAlign/wiki)
  
### New version Xcode ? Try this in your terminal : 
  
  1. Get current Xcode UUID  
  
  ```shell
  XCODEUUID=`defaults read /Applications/Xcode.app/Contents/Info DVTPlugInCompatibilityUUID`
  ```
  2. Write it into the Plug-ins's plist  
  
  ```shell
  for f in ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins/*; do defaults write "$f/Contents/Info" DVTPlugInCompatibilityUUIDs -array-add $XCODEUUID; done
  ```
  3. Restart your Xcode, and select <kbd>Load Bundles</kbd> on the alert
   
## Want to help
  
  * [Star this repository](https://github.com/qfish/XAlign/)
  * [Bugs Report & Advice](https://github.com/qfish/XAlign/issues)
  * [Fork & Pull Request](https://github.com/qfish/XAlign/pulls)

## Special thanks to

* [![Geek-Zoo](http://geek-zoo.com/img/images/logo_2.png)](http://www.geek-zoo.com)

  They provide awesome design and development works continues to help the open-source community even better.


* [BeeFramework](https://github.com/gavinkwoe/BeeFramework) 

  BeeFramework is a new generation of development framework which makes faster and easier app development, Build your app by geek's way.

