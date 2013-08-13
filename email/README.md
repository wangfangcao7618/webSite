﻿# email 文件夹下为发送邮件的html文件 其中分为功能性和活动性两类Email. 功能性包括注册验证邮件,订单通知邮件等,在function子文件夹下. 活动类邮件只针对某一次性的活动,直接放到了email文件夹下


# edm制作注意事项：

## 一、EDM邮件图片要求规范

1. 尽量避免全部是图片.注意平衡图片和文字的比例。

2. 整页图片控制在20张以内.每张图片最大不能超过20kb。

3. 图片地址请不要写成本地路怪，例如:`<img src="image/menu-5.gif" alt="" />`，(这样发送出去的邮件，收件人没办法看到您的图片)。正确的写法应该是:`<img src="http://放置图片的网络空间绝对地址/menu-5.gif" alt="" />`。

4. 图片名称尽量减少特殊字符命名,避免用汉字命名。后缀如.jpg不能大写，否则某些邮箱无法识别会造成图片不显示。另外，图片名称不能含有ad字符，否则图片上传后会显示成“被过滤广告”。

5. 在Photoshop中，不要把一张整图道接切成过多的小图，然后道接存储为web格式，这种模板在邮箱中显示效果不正常同时进入垃圾箱的风险也极高。


## 二、EDM邮件设计编码规范

1. 页面宽度请设定在600到800px(像素)以内.长度1024px以内。 

2. Html编码请使用utf-8。

3. HTML代码在15kb以内。(各个邮箱的收件标准不一样，如果超出15kb您的邮件很有可能会进入垃圾邮件箱。

4. 请使用table表格来布局。同一个`<td>`里只放一张图片，如`<td><img src="photo.jpg" ></td>`所有的图片都要定义高和宽。同一段文字放在同一`<td>`里，每个img标签里都必须声明style="display:block,border:0",以防止出现图片间隙及图片边框，如果结构比较繁杂出现图片间隙的时候，可以考虑在tr里写上style="line-height:1px"；每个table都要重置border="0" cellpadding="0" cellspacing="0"，以避免图片出现间隙。

5. 如果需要邮件居中显示，请在table里设定align ="center"。

6. 不可将word类文件道接转换为html格式.否则会造成编码不规范，如果使用ps导出网页，请把注释内容去掉，有些情况下会影响邮件的显示。

7. 不要使用外链的css样式定义文字和图片(外链的css样式在邮件里将不能被读取，所以发送出去的邮件因为没有链接到样式，将会使你的邮件内容样式丢失)，正确的写法:`<td style="font-family:Arial,Helvetica, sans-serif; font-size, 12px;color:#000000;">文字</td>”<font style="font-family:Arial，Helvetica, sans-serif; font-size, 12px;color:#000000;">文字</font>`。

8. 不使用Flash, Java, Javascript, frames, i-frames, ActiveX以及HTML，如果页面中的图片一定要是动态的，请将FLASH文件转换成GIF动画使用，但在Outlook 2007里.GIF将不能正常显示.因为Outlook 2007限制GIF动画。

9. 不要使用`<table></table>`以外的body, meta和html之类的标签.部分邮箱系统会把这些过滤掉。

10. 背景图片代码写法如一:`<table background="background.gif" cellspacing="0″ cellpadding="0″>`，但请注意, outlook对背景图片不识别。如果需要书写背景图片的样式，则需要先写背景图.然后在style里申明背景图的重复样式。正确写法如`<td background="1.jpg" style="background-repeat:no-repeat"></td>`,或者用插入图片加背景颜色来完成背景图片的效果。

11. 不要出现"onMouseOut"、"onMouseOver"，即使在<td>里设置了，发送到邮箱后也将被过滤，无法显示设定鼠标经过所显示的内容。

12. 若邮件模板内侧边或者上下有空白间距.不要用padding，必须得用标准的td来设定空白间距，否则会导致各个邮箱解析不同。

13. 在yahoo邮箱里line-height要定义时的注意事项:需在块元素里定义line-height.如果td里有<p>标签，则line-height也必须在P里定义。无论是td还是P，如果有超链接，则都必须在a便签里面定义line-height。如果只是在td或者p里面定义line-height的话，那yahoo邮箱将无法识别a里面的行高。


## 三、EDM邮件设计链接要求

1. 链接数量不能超过10个，如果所有图片的链接地址一样，请将所有的小图合并成一张大图。

2. 链接请写成绝对地址，例如:`<a href="http://www.muyingzhijia.com">文字或图片</a>`,(以确保收信人在点击链接时能够正常浏览您的内容)。

3. 链接地址的长度不能超过255个字符，会导致无法追踪或链接错误。

4. 尽且不要使用地图功能(map)链接图片，此功能会使邮件被多数邮箱划分为垃圾邮件。

5. 为避免用户收到的邮件图片无法浏览，请制作一份和邮件内容一样的web页面，然后在邮件顶部写一句话:“如果您无法查看邮件内容，请点击这里”，链接到放有同样内容的web页面。

6. 文字中出现网站地址链接被屏蔽为垃圾邮件的风险是极高的，例如:http://www.muyingzhijia.com 此类链接.建议写成“母婴之家”文字加链接，或是将网址做成图片加链接。


## 四、EDM邮件设计文字规范

1. 邮件主题控制在18个字以内，避免使用—!……等符号.容易产生乱码。

2. 邮件主题和内容都不要加入带有网站地址的信息，比如“www.muyingzhijia.com 或者 XXX公司祝您新年好”。如果客户的品牌知名度比较高，主题上可加入一下公司的名称.比如:“母婴之家奶粉周”。

3. 文字内容、版面尽且简洁，突出主题.以达到更高的点击率。

4. 不使用类似如下敏感及带促销类的文字:免费、优惠、特惠、特价、低价、便宜、廉价、视频、赚钱、群发、发财、致富、代开、薪水、交友、支付、商机、法宝、宝典、秘密、情报、机密、保密、绝密、神秘、秘诀等。如果一定需要请把敏感字制作成图片。

5. 如果发送超过20万封.主题内容要更换.发送超过200万封.要考虑重新设计。