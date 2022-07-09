# HTML5学习

## 总结当日所学回顾

并采用小米医生进行演示

### 图片标签学习

在HTML5的规范中插入图片有以下方法：

> <img src="文件具体路径">

> 其中img为image缩写，src是source（来源）的缩写。

> 实例代码如下

```html
<img src="images/banner.png" alt="">
```

> 如在上一级文件夹中则需要使用../来进行访问，../../为上二级文件夹，以此类推。并注意后缀名一定要写，而alt则是为了图片无法正确加载时使用的“代替品”备用文本并显示于浏览器。

> img标签的width,height属性分别对应宽度和高度，且单位为像素（无需编写单位），当图片拥有width或height属性其一时，会按照原始比例缩放图片，也可以自己设置，一般来说当有需要时只写一个，除非图片本身比例不一，代码如下:

```html
<img src="../images/4.jpg" alt="" height="" width="">
```

### 2

> 网页上所支持的图片格式

| .bmp        | Windows画图软件默认保存格式，位图                  |
| ----------- | -------------------------------------------------- |
| .gif        | 支持动画，如表情包                                 |
| .jpeg(.jpg) | 有损压缩图片，常用于照片                           |
| .png        | 便携式网络图像，用于logo，背景图形等，支持矢量图形 |
| .svg        | 矢量图形                                           |
| .webp       | 最新的压缩算法很优秀的图片格式                     |

#### 相对路径

图片的相对路径，如描述网页出发，如何找到图片。如前方路口右转，直走30米左转就到了。其中默认为当前文件位置的文件夹，回退层级使用‘../’写法。

```html
<img src="../images/4.jpg" alt="" height="" width="">
```

#### 绝对路径

描述图片精确地位置，使用网址进行定位，不随着网页的位置改变而改变，绝对路径不需要改变。

#### 超级链接

是超级链接将网页和网页连结道一起的方法，是互联网成网的原因，其中使用<a>标签进行制作。

```html
<a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_jzxz.png" alt="">
```

忽略网址，a字母是anchor（锚）的首字母，href为hypertext reference（超文本引用），同时href属性也支持相对路径和绝对路径同上，可以包裹div，p，图片img等，而target="blank"属性则为在新窗口中打开网页，比较常用。当网址后紧跟#类名，则可以直接跳转为class类名地址，#top则为最顶端。如果是下载链接如exe，zip，rar后缀，将自动转为下载链接代码如下：

```html
<a href=1.zip">下载</a>

```

##### 邮箱链接,电话链接

* 前有mailto:前缀的链接是邮箱链接，系统将会自动打开Email相关软件：  

```html
<a href="mailto:qa@qq.com">给我发邮件</a>
<a href="tel:12306">给我打电话</a>
```

### 插入音频，视频

以往使用Flash插入，现即将淘汰（bug，内存占用），被HTMl5取代，在浏览器插入则需要使用<audio>标签，常用音频格式为mp3和ogg格式，代码如下：

```
<audio controls src="../music/hangpaibgm(ogg).ogg" loop></audio>
```

其中controls添加控件，中间段为路径同上，如添加auttopplay属性音频会自动播放，loop则表示循环播放

***

以下为所学参考，没什么东西，上面没写完

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>小牧医生 - 责任，品质，关爱</title>
    <meta name="Description" content="小牧医生是专业的医院，理念就是责任，品质，关爱">
    <meta name="Keywords" content="美容，减脂，内科，外科">
</head>
<body>
    <!-- 页面头部 -->
    <header>
        <!-- 网页的LOGO -->
        <div class="logo">
            <h1>小米医生</h1>   
        </div>
        
        <!-- 网页的功能区 -->
        <div class="tool">
            <a href="tel:086-66622233"><img src="images/tel.png" alt="电话：088-88888888"></a>
            <span class="telnumber">086-66622233</span>
            <!-- 留空（测试：target="blank"跳转且新建） -->
            <a href="https://translate.google.cn/" target="blank" ><img src="images/chinese_icon.png" alt=""><img src="images/english_icon.png" alt="">
            </a>
        </div>
        <!-- 网页的导航条 -->
        <nav class="main-nav">
            <ul>
                <li>首页</li>
                <li>医院概况</li>
                <li>医院动态</li>
                <li>专业学科</li>
                <li>服务指南</li>
                <li>医院文化</li>
                <li>互动交流</li>
            </ul>
        </nav>
    </header>   
    
    <!-- 网页的banner -->
    <section class="banner">
        <!-- 小圆点 -->
        <img src="images/banner.png" alt="">
        <h2>责任，科学，严谨</h2>
        <ol>
            <li></li>
            <li></li>
            <li></li>
            <li></li>
        </ol>
    </section>

    <!-- 网页的主要内容 -->
    <section class="content">
        <!-- 常用链接 -->
        <div class="use_links">
            <ul>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_jzxz.png" alt="">
                        <span>就医须知</span>
                    </a>
                </li>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_jylc.png" alt="">
                        <span>就医流程</span>
                    </a>
                </li>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_zjjs.png" alt="">
                        <span>专家介绍</span>
                    </a>
                </li>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_ksjs.png" alt="">
                        <span>科室介绍</span>
                    </a>
                </li>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_ybjy.png" alt="">
                        <span>医保就医</span>
                    </a>
                </li>
                <li>
                    <a href="http://www.yy8080120.com/54964/54981/54984/index.htm" target="blank">
                        <img src="images/icon_jktj.png" alt="">
                        <span>健康体验</span>
                    </a>
                </li>
            </ul>
        </div>
        <!-- 医院动态和医院公告区域 -->
        <div class="news-and-notice">
            <!-- 医院动态 -->
            <div class="news">
                <h3>医院动态</h3>
                <div class="news-content">
                    <!-- 图片新闻 -->
                    <a href="">
                        <img src="images/news_pic.png" alt="">
                        <div>
                            '全国首届健康预防与商业医疗保险论坛'在北京医院举办
                        </div>
                    </a>
                    <div class="hot-news">
                        <!-- 新闻的大图片 -->
                    </div>
                    <!-- 新闻列表 -->


                    <ul>
                        <li><a href="">年度医疗机构用血自查评分表和科室基本信息表</a></li>
                        <li><a href="">关于上报北京市医疗机构临床用血信息的通知</a></li>
                        <li><a href="">北京医院输血科通过验收并获批开展“临床基…</a></li>
                        <li><a href="">国家药品监督管理局关于修订都梁软胶囊非处…</a></li>
                        <li><a href="">关于将多拉司琼注射剂等药品纳入本市基本医…</a></li>
                        <li><a href="">关于调整完善本市基本医疗保险门诊特殊疾病…</a></li>
                        <li><a href="">广东省药学会：关于印发《超药品说明书用药…</a></li>
                        <li><a href="">人力资源社会保障部关于将36种药品纳入国家…</a></li>
                    </ul>
                </div>
            </div>
            <!-- 医院公告 -->
            <div class="notice">
                <h3>医院公告</h3>
                <ol>
                    <li>
                        <dl><a href="">《养生堂》</dl></a>
                        <dd><a href="">公郭立新主任 特殊时期糖尿病人的新冠…</dd></a>
                    </li>
                    <li>
                        <dl><a href="">《《养生堂》</dl>
                        <dd><a href="">《王少为主任 新型冠状病毒防控指引十八…</dd></a>
                    </li>
                    <li>
                        <dl><a href="">《《我要当医生》</dl></a>
                        <dd><a href="">《谭玲副主任 李同舟 姚晨蕊药师</dd></a>
                    </li>
                    <li>
                        <dl><a href="">《《全民健康学院》</dl></a>
                        <dd><a href="">《王建业院长 “医”路有你 健康同行</dd></a>
                    </li>
                    <li>
                        <dl><a href="">《《健康北京》</dl></a>
                        <dd><a href="">《王建业院长 莫把衰老当病治</dd></a>
                    </li>  
                </ol>
            </div>
        </div>
        
        <!-- 广告图片 -->
        <div class="ad-images">
            <a href="">
                <img src="images/xuanchuan.png" alt="">
            </a>
        </div>

        <!-- 科室介绍 -->
        <div class="dep-info">
            <h3>科室介绍</h3>
            <div class="dep-content">
                <div>
                    <h4>内科</h4>
                    <ul>
                        <li><a href="">呼吸内科</a></li>
                        <li><a href="">消化内科</a></li>
                        <li><a href="">神经内科</a></li>
                        <li><a href="">心血管内科</a></li>
                        <li><a href="">肾内科</a></li>
                        <li><a href="">血液内科</a></li>
                        <li><a href="">放疗科</a><li>
                        <li><a href="">放疗科</a></li>
                        <li><a href="">肿瘤康复科</a></li>
                        <li><a href="">免疫科</a></li>
                        <li><a href="">內分泌科</a></li>
                        <li><a href="">肿瘤综合科</a></li>
                    </ul>
                </div>
                <div>
                    <h4>肿瘤科</h4>
                    <ul>
                        <li><a href="">肿瘤内科</a></li>
                        <li><a href="">肿瘤外科</a></li>
                        <li><a href="">肿瘤妇科</a></li>
                        <li><a href="">骨肿瘤科</a></li>
                        <li><a href="">放疗科</a></li>
                        <li><a href="">肿瘤康复科</a></li>
                        <li><a href="">放疗科</a></li>
                        <li><a href="">放疗科</a></li>
                        <li><a href="">放疗科</a></li>
                        <li><a href="">肿瘤康复科</a></li>
                        <li><a href="">肿瘤综合科</a></li>
                    </ul>
                </div>
                <div>
                    <h4>外科</h4>
                    <ul>
                        <li><a href="">普通外科</a></li>
                        <li><a href="">神经外科</a></li>
                        <li><a href="">心胸外科</a></li>
                        <li><a href="">泌尿外科</a></li>
                        <li><a href="">肝胆外科</a></li>
                        <li><a href="">肛肠外科</a></li>
                        <li><a href="">心血管外科</a></li>
                        <li><a href="">烧伤科</a></li>
                        <li><a href="">骨外科</a></li>
                        <li><a href="">乳腺外科</a></li>
                    </ul>             </div>
                <div>
                    <h4>儿科</h4>
                    <ul>
                        <li><a href="">儿科综合</a></li>
                        <li><a href="">小儿内科</a></li>
                        <li><a href="">小儿外科</a></li>
                        <li><a href="">新生儿科</a></li>
                        <li><a href="">儿童营养科</a></li>
                        <li><a href="">消化内科</a></li>
                    </ul>
                </div>
            </div>
        </div>

           <!-- 专家介绍 -->  
        <div class="exp-info">
            <h3>专家介绍</h3>
            <a href="">查看更多</a>
            <ul>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images/lilin.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：李琳</p>
                        <p>科室：肿瘤内科</p>
                        <p>职称：主任医师</p>
                        <p>介绍：北京医院肿瘤内科科室主任，党支部书记，副教授，硕士研究生导师，中国老年肿瘤专业委员会肺癌分委会常务委员，北京医学……</p>
                    </div>
                </li>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images/lilin.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：毛永辉</p>
                        <p>科室：肾脏内科</p>
                        <p>职称：主任医师</p>
                        <p>介绍：北京医院肾内科主任，主任医师，硕士研究生导师。1989年毕业于华西医科大学临床医学院，后在北京医院内科、肾内科工作……</p>
                    </div>
                </li>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images//huangcibo.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：黄慈波</p>
                        <p>科室：风湿免疫科</p>
                        <p>职称：主任医师</p>
                        <p>介绍：教授主任医师研究生导师卫生部北京医院风湿免疫科主任，北京大学医学部风湿免疫系副主任；海峡两岸医师交流协会风湿免疫……</p>
                    </div>
                </li>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images/caosuyan.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：曹素艳</p>
                        <p>科室：特需医疗部</p>
                        <p>职称：主任医师</p>
                        <p>介绍：北京医院特需医疗部（健康管理中心）/全科医疗部主任，老年与全科医学中心副主任，主任医师，医学硕士。北京大学医学部硕士……</p>
                    </div>
                </li>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images/chenhaibo.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：陈海波</p>
                        <p>科室：神经内科</p>
                        <p>职称：主任医师</p>
                        <p>介绍：北京医院神经内科主任，主任医师，北京大学医学部神经病学系副主任、教授。中国医师协会神经内科医师分会副会长兼帕金……</p>
                    </div>
                </li>
                <li>
                    <div class="picbox">
                        <a href="">
                            <img src="images/jack.png" alt="">
                        </a>
                    </div>
                    <div class="wordbox">
                        <p>姓名：Jack</p>
                        <p>科室：普通外科</p>
                        <p>职称：主任医师</p>
                        <p>介绍：北京医院普通外科主任，胃肠外科主任，北京大学医学部硕士研究生导师，1985年毕业于白求恩医科大学，从事普外科临床工……</p>
                    </div>
                </li>
            </ul>
         </div>  
        </div> 
    </section>

    <!-- yejiao -->
    <footer>
        <!-- 友情链接 -->
        <div class="friend-links">
            <h3>友情链接</h3>
            <ul>
                <li><a href="">院长信箱</a></li>
                <li><a href="">投诉信箱</a></li>
                <li><a href="">在线调查</a></li>
                <li><a href="">地理位置</a></li>
                <li><a href="">网站图片</a></li>
                <li><a href="">网站帮助</a></li>
                <li><a href="">隐私申明</a></li>
            </ul>
        </div>

        <!-- xiaomiyisheng联系方式 -->
        <address>
            <h3>小米医生</h3>
            <ul>
                <li>地址：北理工国防大厦111号</li>  
                <li>电话：088-88888888</li>
                <li>邮箱：kefu@imooc.com</li>
                <li>邮编：666666</li>
                <li>网址：<a href="imooc.com">//imooc.com</a></li>
                <li>举报热线：088-88888888</li>
            </ul>
        </address>
    </footer>
</body> 
</html>
```

