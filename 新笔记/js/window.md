### window 对象表示一个包含 DOM 文档的窗口

### window 作为全局变量，代表了脚本正在运行的窗口，暴露给 Javascript 代码。

### 一个窗口可能会有多个标签,如果一样东西无法恰当地作用于标签，那么它就会作用于窗口。

- window.open

  - 它能够新建一个独立窗口,具有自己独立的 js 环境
  - 多数浏览器会阻止非法弹窗以保护用户,各浏览器的阻止规则有所不同
  - 参数
    - `url` 新建窗口的 url
    - `name` 新窗口名称,如果有相同名字的窗口则会在改窗口打开给定 url
    - `params` 配置(字符串),用逗号分割,参数间不能有空格
      - left/top
      - width/height
      - menubar（yes/no）—— 显示或隐藏新窗口的浏览器菜单。
      - toolbar（yes/no）—— 显示或隐藏新窗口的浏览器导航栏（后退，前进，重新加载等）。
      - location（yes/no）—— 显示或隐藏新窗口的 URL 字段。Firefox 和 IE 浏览器不允许默认隐藏它。
      - status（yes/no）—— 显示或隐藏状态栏。同样，大多数浏览器都强制显示它。
      - resizable（yes/no）—— 允许禁用新窗口大小调整。不建议使用。
      - scrollbars（yes/no）—— 允许禁用新窗口的滚动条。不建议使用。
  - 窗口访问
    窗口直接的连接是双向的,主窗口和弹窗之间是相互引用
    - 调用 open 方法会返回新窗口的引用,如果是同源的地址,就可以用它来措置新窗口(试了一下,如果使用同一个 name 多次打开新的 url 好像引用会失效)
    - 弹窗也可以使用`window.opener`来访问`opener`窗口(打开它的那个窗口)
  - 窗口关闭
    - win.close()
    - win.closed 可以查看该窗口是否已关闭
  - 窗口的引用还可以控制滚动,位置,大小,聚/失焦

- [window.navigator](https://developer.mozilla.org/zh-CN/docs/Web/API/Window/navigator)
  [菜鸟](https://www.runoob.com/jsref/obj-navigator.html)

  - 会返回一个 Navigator 对象的引用,可以用于请求运行当前代码的应用程序相关信息
  - 可以用于判断当前使用的是什么浏览器

- [window.screen](https://www.runoob.com/jsref/obj-screen.html)
  - 返回当前客户端屏幕信息

### window 下有很多事件,可以利用 addEventListen 对这些事件进行监听,从而实现功能

[传送门](https://developer.mozilla.org/zh-CN/docs/Web/API/Window#history_events)

- 普通

  - `error`
  - `languagechange`
  - `oriendtationchange` 方向改变
  - `devicemotion` 指示设备接收的物理加速度的数量和旋转的速率
  - `deviceorientation`当从磁力计方位传感器获得有关设备当前相对于地球坐标系的方位的新数据时触发
  - `resize`
  - `storage` storage 改变

- 动画事件

  - `animationcancel` 动画意外中止时触发
  - `animationend` 动画正常完成时触发
  - `animationiteration` 动画迭代完成时触发
  - `animationstart` 动画启动时触发

- 剪切板事件

  - `clipboardchange` 系统剪贴板内容更改时触发
  - `copy` 复制
  - `cut` 剪切
  - `paste` 粘贴

- 网络连接事件

  - `offline` 断网
  - `online` 联网

- 聚焦事件

  - `blur` 失焦
  - `focus` 聚焦

- 手柄事件

  - `gamepadconnected` 浏览器检测到手柄已连接或手柄的按钮/轴首次被使用时触发
  - `gamepaddisconnected` 浏览器检测到手柄已断开连接时触发

- 历史事件

  - `hashchange` 地址栏哈希值改变时触发
  - `pagehide` 页面隐藏
  - `pageshow` 页面显示
  - `popstate` 活动历史记录条目更改时触发

- 加载事件

  - `beforeunload` 浏览器窗口关闭或者刷新时会触发
  - `DOMContentLoaded` 初始的 HTML 文档被完全加载和解析完成之后触发
  - `load` 整个页面及所有依赖资源如样式表和图片都已完成加载时触发
  - `unload` 文档或一个子资源正在被卸载时触发

- 消息事件

  - `message` 当窗口接收到另一个窗口的消息时触发
  - `messageerror` 当窗口接收到另一个窗口的消息出错时触发

- 打印事件

  - `afterprint` 关联的文档已开始打印或打印预览已关闭之后触发
  - `beforeprint` 关联文档即将被打印或预览以供打印时触发

- promise rejecttion 事件

  - `rejectionhandled` Promise 被 rejected 且有 rejection 处理器时会在全局触发
  - `unhandledrejection` 当 Promise 被 reject 且没有 reject 处理器的时候触发

- 过渡事件

  - `transitioncancel` CSS 转换被取消时触发
  - `transitionend` CSS 转换完成时触发
  - `transitionrun` 第一次创建 CSS 转换时触发
  - `transitionstart` CSS 转换实际启动时触发

- [WebVr 事件](https://developer.mozilla.org/zh-CN/docs/Web/API/Window#webvr_events)
