常用的CSS命名规则
头部：header		内容：content    容器container		尾：footer	导航：nav
侧栏：sidebar		栏目：column		页面外围控制整体框架布局：wrapper
左中右：left center right	登录条：loginbar		标志：logo
广告：banner		页面主体：main	  热点：hot		新闻：news
下载：download	子导航：subnav		菜单：menu		子菜单：submenu
搜索：search		友情链接：link	版权：copyright	滚动：scroll
标签页：tab		文章列表：list	提示信息：msg	小技巧：tips
栏目标题：title	加入：joinus		指南：guide	服务：service
注册：register		状态：status		投票：vote		合作伙伴：partner

1）页面结构
容器：container		页头：header		内容：content
页面主体：main		页尾：footer		导航：nav
侧栏：sidebar			栏目：column		左中右：left center right
页面外围控制整体布局宽度：wrapper

2）导航
导航：nav		    主导航：mainnav		子导航：subnav
顶部导航：topnav		侧导航：sidebar		左导航：leftsidebar
右导航：rightsidebar	菜单：menu			子菜单：submenu
标题：title			摘要：summary

3）功能
标志：logo　　广告：banner　　登陆：login　　登录条：loginbar
注册：regsiter　　搜索：search　　标题：title　　加入：joinus 　
状态：status　　按钮：btn		滚动：scroll　　标签页：tab　　
文章列表：list　　提示信息：msg		当前的: current　　小技巧：tips　　
图标: icon　　注释：note		指南：guild　	服务：service　　
热点：hot　　新闻：news			下载：download　　投票：vote　　
合作伙伴：partner		友情链接：link　　版权：copyright

*注：class定义的命名一般用“-”或者“_”连接，如：top-nav，header_left等
id定义的命名一般采用驼峰法命名（跟JS命名保持一致），如newsList，newsTitle等等
按样式取名规范举例
.red { color: red; }			/*按文字颜色名定义颜色为红色的样式*/
.w1000{width:1000px}		/*宽度首字母缩写加上宽度数值定义宽度为1000px的样式*/
.h500{height:500px}		/*高度首字母缩写加上高度数值定义高度为500px的样式*/
.fl{float:left}				/*浮动首字母缩写+浮动方位首字母缩写定义左浮动样式 */
.fr{float:right}				/*浮动首字母缩写+浮动方位首字母缩写定义右浮动样式 */
.clear{clear:both}			/*定义清除浮动样式 */
.font12px { font-size: 12px; }/*文字样式名+文字大小来定义字体为12px的样式*/

常用的css文件名
基本共用base.css	public		主要的master.css			主题：themes.css
布局，版面layout.css		专栏：columns.css			模块：module.css