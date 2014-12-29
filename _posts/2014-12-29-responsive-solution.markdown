响应式设计方案
=======
1. 分辨率划分
2. Javascript方案
3. 通用UI组件
4. CSS编写规范
5. grunt自动化编译

分辨率划分
-----------------
![](http://d.pcs.baidu.com/thumbnail/7ef2ce4d5adc9a98d9ecbb54ee49b17e?fid=774302184-250528-189015127821770&time=1419829200&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-kWmIb%2FuVPwks9HLto44sDOq%2FqMg%3D&expires=2h&prisign=unkown&chkv=0&chkbd=0&chkpc=&size=c850_u580&quality=100 "")
+ <=1280
 + 页面宽度：1000px
 + 包含的主要分辨率：1024x768、1280x800、1280x1024
+ <=1440
 + 页面宽度：1200px
 + 包含的主要分辨率：1360x768、1366x768、1440x900
+ <=1680
 + 页面宽度：1500px
 + 包含的主要分辨率：1600x900、1680x1050
+ <=1920
 + 页面宽度：1700px
 + 包含的主要分辨率：1920*1080
+ >1920
 + 页面宽度：2000px
 + 包含的主要分辨率：2048x1152、2560x1600

Javascript方案
-----------------
<pre>
 <code>
   dev.responsive.screenConfig = {
        "global-media-1280" : "1280",
        "global-media-1440" : "1440",
        "global-media-1680" : "1680",
        "global-media-1920" : "1920",
        "global-media-2560" : "2560"
    };
 </code>
</pre>
 
![](http://d.pcs.baidu.com/thumbnail/3bb643bb649c40593b6b26178e8422b7?fid=774302184-250528-421403417141004&time=1419829200&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-7FN%2F2RDaAesRheIThvJM5kxaE0I%3D&expires=2h&prisign=unkown&chkv=0&chkbd=0&chkpc=&size=c850_u580&quality=100 "")

通用UI组件
-----------------
> 根据屏幕高度分为：<=900、<=1080、<=1600、>1600
> 默认pageSize设为25
> 定义一个pageconfig如下：

<pre>
 <code>
    var PAGECONFIG = {
          "900" : 10,
         "1080" : 15,
         "1600" : 20
    };
 </code>
</pre>
业务相关可以在使用pager的页面重新指定pageSize，反之根据配置设置的pageSize。

CSS编写规范
-----------------
### 定义通用样式 ######
* navbar.less:导航
* sidebar.less:左侧菜单
* table.less:表格的通用样式
* graph.less:图表通用样式
* form.less指定表单通用样式
* pager. less:分页样式
* footer.less:页脚样式
* responsive.less:定义各个区间下页面宽度及内容区宽度等通用样式
![](http://d.pcs.baidu.com/thumbnail/d49e2cf98d2762377fed23f730ff10e4?fid=774302184-250528-289959640975567&time=1419829200&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-v15JhwtthAjWkGkiOmcqFhLtJ8k%3D&expires=2h&prisign=unkown&chkv=0&chkbd=0&chkpc=&size=c850_u580&quality=100 "")

grunt自动化编译
-----------------
![](http://d.pcs.baidu.com/thumbnail/7d5e32cb7b36a8bc44440c351712bab1?fid=774302184-250528-1028679028203381&time=1419829200&rt=sh&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-RdMMHahBf25aMLBDMrGSNVeX02I%3D&expires=2h&prisign=unkown&chkv=0&chkbd=0&chkpc=&size=c850_u580&quality=100 "")
