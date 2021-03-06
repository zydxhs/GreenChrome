# GreenChrome

超好用的Chrome浏览器增强软件


## 重要
- **已经停止开源**
- **已经停止服务** :loudspeaker:

## 简介
* GreenChrome具有双击关闭标签页，右键关闭标签页，保留最后标签页，悬停快速标签切换，悬停激活标签页，追加Chrome运行参数，启动、关闭时运行程序，老板键，空白新标签页面，移除开发者模式警告，鼠标手势，支持特殊页面使用，支持任意形状，支持自定义功能，灵敏度可调节，轨迹颜色粗细均可设置，便携化绿色版，内置hosts，完美支持32位，64位，按键转换，破解flash锁区等功能。
* 具体功能可打开GreenChrome.ini进行配置。
* 如有问题，可以加QQ群186383225，186385220反馈。

## 安装
**由于软件的特殊实现方式，各种安全软件很可能会进行拦截。如果你担心安全问题，请不要使用。如果使用，请主动把dll加入白名单，否则容易出现各种问题。**
本软件并非第三方独立浏览器，把winmm.dll放到chrome.exe同一个目录下，启动Chrome即可自动生效。

根据Chrome是多少位，自行选择32位(x86)或64位(x64)目录下的dll，选择错误则不能成功加载，不会有任何反应。如果操作正确也无法加载还可以尝试把winmm.dll重命名为version.dll或userenv.dll。改完所有名称都还不能用，请再次确认32位64位是否选择正确（在Chrome的关于界面中会有显示）。所有方法都尝试过还不行，那么这里有一个最终解决方案：https://blog.shuax.com/archives/setdll.html

本软件默认为便携版设计，所以默认会保存数据到当前目录。已有数据的安装版用户如果只是想使用其它增强功能，则需要打开配置文件，删除数据重定向（在追加参数里面）以及关闭便携化选项（设置为0）。

升级则很简单，直接使用新版dll覆盖老版dll即可，注意不要覆盖GreenChrome.ini，否则将会还原默认设置，如果ini内容有改动会在更新日志中说明。

如果你实在不会用，就直接用配套更新器：https://csharp.love/chrome-update-tool.html ，可以自动更新Chrome以及GreenChrome。

## 版本
判断GreenChrome是否加载成功：

关于页面会出现GreenChrome的字样，并且写明版本号

## 更新日志
* 6.6.6：修复一个内存越界问题；其它小修改。
* 6.6.5：修复打开GreenChrome设置时崩溃。
* 6.6.4：修复追加参数插入位置不正确。
* 6.6.3：修复使用chromedriver的兼容性问题。
* 6.6.2：修复模拟按键底层bug，修复左右键交换产生bug。
* 6.6.1：开启便携化时，Chrome密码管理可以直接显示密码。（避免某些用户无法进行查看密码）（另外涉及到密码问题我多说两句：1、我不致力于虚假的安全* 感， 2、ChromePass软件了解一下）
* 6.6.0：更改GreenChrome设置页面地址。（注意修改ini手势中的设置网址为：https://tools.shuax.com/greenchrome/）
* 6.5.8：优化 防止关闭最后的标签时关闭整个浏览器。
* 6.5.7：优化对新版Chrome的兼容性，默认使用winmm.dll。（注意winhttp.dll已经无法使用）

## 下载
2019年3月19日更新（增加数字签名） 

由于报毒过多，永久停止更新，停止接收反馈，自行判断是否使用。 

下载地址：https://shuax.com/gc

## 常见问题【必看】
* 如果当前目录不可写，那么即使当前目录下有GreenChrome.ini配置文件也不会生效，而是会自动使用%appdata%下的同名文件。具体GreenChrome.ini位置可以在web设置界面中点击定位。
* 如果配置文件GreenChrome.ini有改动需要同步修改（几乎不会修改，有修改会通知），推荐使用beyond compare对比软件进行同步。
* 软件工作的原理是在chrome界面外覆盖了一层，比如双击关闭，是在外层捕获到双击消息后转换为发送中键消息，从而实现关闭标签。所以涉及到网页内部的功能就无法处理了，比如拖拽打开网页，真的实现不了，还是装个扩展吧。能够实现的功能基本都已经实现了，所以需求新功能基本不能得到。
* 另外很多功能都是通过发送快捷键来实现，特别是鼠标手势的控制。所以如果当前快捷键不生效时，鼠标手势也会失灵。比如当前网页正在播放视频，播放器处理了一些快捷键等等。
* 没说有的功能那就是没有，比如装了以后能不能上google，能不能用npapi，能不能关闭DirectWrite。
* 怎么XX功能不起作用，有问题？有些安全软件可能会进行拦截而无提示，请自行排查。另外作者精力有限，不可能各种系统各种环境都测试一遍，只保证大多数人能用就好。
* 为什么打开后任务栏两个图标？可以尝试取消已经锁定的图标，并且清理 %appdata%\Microsoft\Internet Explorer\Quick Launch\User Pinned\TaskBar\ 下面的捷方式后重新锁定。注意一定要在打开Chrome后在运行时进行锁定，因为程序会自动把快捷方式设置为只读，避免产生双图标。
* 如何设置为默认浏览器？一般情况下直接点击Chrome设置里面的设置默认浏览器即可，如果不行可能是之前有老数据，可以尝试使用管理员运行chrome以后再次设置，如果还不行可能是某些安全软件锁定了默认浏览器，请检查。
* 为什么在关于界面我的Chrome变成了金色图标？这是因为启用了“移除开发者模式警告”，这个功能会把当前浏览器模拟为金丝雀版本，并不影响任何功能，请放心使用。
* 怎么Chrome老是提示更新？你可以添加启动参数：--disable-background-networking
* 在设置页面更新报错？软件自带一个脚本版的简易更新功能，如果出错建议使用完整版更新器，会更加稳定。
* chrome设置打不开？由于位置原因，有时候移除开发者模式警告会导致这个问题，关闭后即可打开设置，然后再次打开移除开发者模式警告设置依然正常。
* 软件发布时只会测试 https://tools.shuax.com/chrome/ 中的Chrome版本兼容，不能保证Chrome升级后依然可用。其它比如chromium内核的浏览器一概不会测试兼容，有任何bug都很正常，能不能用全看运气。
* 如果你的Chrome不打算更新，那么GreenChrome也不要更新，因为GreenChrome都是根据当前最新Chrome进行兼容的。如果你时常更新Chrome，请务必常来更新GreenChrome。
* 任何非最新版GreenChrome的bug不予理会。另外有些时候有一些bug不一定是GreenChrome引起的，可以暂时把GreenChrome关掉，使用排除法测试。
* 本软件绝无流氓行为，报毒我也管不了，相信我就用，不信我不要安装。

## 免责申明
**本软件是免费软件，不收一分钱，只是分享给朋友们使用，不负责售后服务。使用/更新前务必备份用户数据，软件造成任何数据丢失，本人概不负责。**
