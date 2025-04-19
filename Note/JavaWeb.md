# 前端学习

## HTML-CSS

### Vscode开发工具

meta标签

> <meta> 是 HTML 中的一个元数据标签，用于提供关于 HTML 文档的元信息，这些信息不会直接显示在页面上，但对于浏览器和搜索引擎等工具来说非常重要。<meta> 标签通常位于 HTML 文档的 <head> 部分。

代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- 字符集 -->
    <meta charset="UTF-8">
    <!-- 在移动设备的显示和缩放比例 -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
   <body>
        <h1>Html快速入门</h1>
        <!-- alt描述,width,height设置长宽 -->
        <img src="Picture/cuixingshi.png" alt="cuixingshi" width="300" height="300">
        <h1>我是一级标题</h1>
   </body>
</html>
```

### 常见标签和样式-央视新闻-标题-排版

html在渲染时，从上往下逐行解析展示的

**只有h1-h6没有多余的**

### 常见标签和样式-央视新闻-标题-样式

#### CSS 引入方式

- **行内样式**：写在标签的`style`属性中（配合 JavaScript 使用）
- **内部样式**：写在`<style>`标签中（可以写在页面任何位置，但通常约定写在`<head>`标签中）
- **外部样式**：写在一个单独的`.css`文件中（需要通过`<link>`标签在网页中引入）

![image-20250209121544712](./picture/image-20250209121544712.png)

![image-20250213162314474](./picture/image-20250213162314474.png)

### 常见标签和样式-央视新闻-标题-样式(选择器)

> CSS选择器是用来选取需要设置样式的元素(标签)的

| 选择器     | 写法                | 示例       | 示例说明                               |
| ---------- | ------------------- | ---------- | -------------------------------------- |
| **元素选择器** | 元素名称 {...}      | h1 {...}   | 选择页面上所有的<h1>标签               |
| **类选择器** | .class 属性值 {...} | .cls {...} | 选择页面上所有 class 属性为 cls 的标签 |
| **id 选择器** | #id 属性值 {...}    | #hid {...} | 选择页面上 id 属性为 hid 的标签        |
|分组选择器|选择器1,选择器2 {...}|h1,h2 {...}|选择页面上所有的<h1>和<h2>标签|
|属性选择器|元素名称[属性] {...}|input[type] {...}|选择页面上有type属性的<input>标签|
|属性选择器|元素名称[属性名="值"] {...}|input[type="text"] {...}|选择页面上type属性为text的<input>标签|
|后代选择器|元素1 元素2 {...}|form input {...}|选择<form>标签内的所有<input>标签|

### 常见标签和样式-央视新闻-正文-排版

代码

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</title>
        <style>
          #time{
            color: #b2b2b2;
          }    
          a{
            /* 去除超链接下的下划线 */
            text-decoration:none;
          }
        </style>
        <!-- 方式3：外部样式 -->
        <!-- <link rel="stylesheet" href="./css/news.css"> -->
    </head>
    <body>
        <!--  -------------------新闻标题-------------------- -->
        <h1>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</h1>
      
        <a href="https://www.cctv.com" target="_blank" >央视网</a> 
        <!-- 发布时间 -->
        <span id="time">2024年05月15日 20:07</span>
        <br>
        <!--  -------------------新闻主体-------------------- -->
        <!-- 引入一个视频,路径为./video/video.mp4,controls表示显示控件-->
         <!-- video标签属性
          src-视频路径
          controls-显示控件
          autoplay-自动播放
          width-宽度
          height-高度,建议只设置一个,另一个会自动适应
            px：像素
            百分比：相对于父元素的宽度
            自动：根据视频的宽度自动调整
          loop-循环播放
          poster-封面图片
          muted-静音
          preload-预加载
         -->
        <video src="./video/news.mp4" controls width="80%"></video>
        <!-- <audio src="./audio/news_1739964534813.mp3" controls></audio> -->
        <p>央视网消息（新闻联播）：作为共抓长江大保护的标志性工程，长江十年禁渔今年进入第四年。习近平总书记指出，长江禁渔是为全局计、为子孙谋的重要决策。牢记总书记嘱托，沿江省市持续推进长江水生生物多样性恢复，努力保障退捕渔民就业生活。这段时间，记者深入长江两岸，记录下禁渔工作取得的重要阶段性成效和广大干部群众坚定不移推进长江十年禁渔的扎实行动。</p>
        <p>行走在长江沿线，科研人员发现很多可喜现象。</p>
        <!-- 引入一张gif，在./Picture目录下 -->
        <!-- img标签属性
        src-访问路径
        1.绝对路径
          1.1绝对磁盘路径:C:\Users\Administrator\Desktop\Study\Picture\1_1739964534896.gif
          1.2绝对网络路径:https://www.baidu.com/img/bd_logo1.png
        2.相对路径
          2.1./表示当前目录(可以省略)
          2.2../表示上一级目录
         
        alt-图片描述
        width-宽度
        height-高度,建议只设置一个,另一个会自动适应
        px：像素
        百分比：相对于父元素的宽度
        自动：根据图片的宽度自动调整 -->
        <img src="./Picture/1_1739964534896.gif" alt="gif" width="80%"></img>
        <p>在长江南源，一处小头裸裂尻鱼新的栖息地被发现，鱼的数量大约超3万尾，为水生态保护提供了珍贵数据。</p>
        <br>
        <p>在长江中游，追踪显示，人工增殖放流的中华鲟成功入海率已经从45%左右提升至60%以上；鄱阳湖鱼类小型化、低龄化趋势得到遏制，栖息地生存环境得以改善。</p>
        <br>
        <p>在长江下游，今年3月起，南京秦淮河入江口首次出现野生中华绒螯蟹大规模洄游现象，种群数量明显增加。</p>
        
        <img src="./Picture/2_1739964534978.jpg" width="80%">
        <p>水生生物资源恢复向好，见证了长江十年禁渔三年多来的阶段性成果。</p>
        <br>
        <p>实施长江十年禁渔，是以习近平同志为核心的党中央从中华民族长远利益出发作出的重要决策。党的十八大以来，总书记多次深入长江沿线考察调研，详细了解长江十年禁渔的实施情况，他指出，要坚定推进长江十年禁渔，巩固好已经取得的成果。</p>
        
        <img src="./Picture/3_1739964535067 (1).jpg" width="80%">
        <p>按照部署，自2021年1月1日起，在长江干流、大型通江湖泊、重要支流和长江口部分海域实行为期十年的禁渔，常年禁止天然渔业资源的生产性捕捞。禁渔三年多来，相关评估显示，长江干流和鄱阳湖、洞庭湖水生生物完整性指数由禁渔前最差的“无鱼”提升了两个等级。2022年，长江江豚数量达到1249头，实现历史性止跌回升。长江干流水质连续4年全线保持Ⅱ类。</p>
        <br>
        <p>实施长江十年禁渔，解决好渔民上岸后的生产生活问题，禁渔才有稳定扎实的社会基础。</p>
        
        <img src="./Picture/4_1739964535156.jpg (1).jpg" width="80%">
        <p>安徽退捕转产的3万多名渔民，在政府的引导下接受就业培训。在当涂县，免费学习养殖技术，养殖生态螃蟹成了退捕渔民的新选择。</p>
        <br>
        <p>在拥有洞庭湖超六成水域的湖南岳阳，政府帮扶上岸渔民建起养殖场，发展风干鱼产业，还带领他们学习直播带货，拓宽销路。</p>
        <br>
        <p>在渔民退捕上岸的鄱阳湖棠荫岛，当地在继续保护好生态的前提下，正探索规划利用独特的自然资源发展旅游产业。禁渔三年多来，有关部门对23.1万退捕渔民逐一建档立卡，多渠道提升就业、社保水平。</p>

        <img src="./Picture/5_1739964535235.jpg" width="80%">
        <p>长江十年禁渔实施以来，沿江省市合力攻坚、久久为功，长江大保护不断向纵深推进，持续巩固禁渔成果。下一步，沿江省市还将加强水生生物重要栖息地修复，建立退捕渔民动态精准帮扶服务，完善跨区域、跨部门执法合作机制，确保一江清水绵延后世、惠泽人民。</p>
    </body>
</html>
```

### 常见标签和样式-央视新闻-正文-样式

代码

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</title>
        <style>
          #time{
            color: #b2b2b2;
          }    
          a{
            /* 去除超链接下的下划线 */
            text-decoration:none;
          }
          p{
            /* 首行缩进 */
            text-indent: 2em;
            /* 行高 */
            line-height: 2;/* 行高为字体大小的2倍 */
          }
        </style>
        <!-- 方式3：外部样式 -->
        <!-- <link rel="stylesheet" href="./css/news.css"> -->
    </head>
    <body>
        <!--  -------------------新闻标题-------------------- -->
        <h1>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</h1>
      
        <a href="https://www.cctv.com" target="_blank" >央视网</a> 
        <!-- 发布时间 -->
        <span id="time">2024年05月15日 20:07</span>
        <br>
        <!--  -------------------新闻主体-------------------- -->
        <!-- 引入一个视频,路径为./video/video.mp4,controls表示显示控件-->
         <!-- video标签属性
          src-视频路径
          controls-显示控件
          autoplay-自动播放
          width-宽度
          height-高度,建议只设置一个,另一个会自动适应
            px：像素
            百分比：相对于父元素的宽度
            自动：根据视频的宽度自动调整
          loop-循环播放
          poster-封面图片
          muted-静音
          preload-预加载
         -->
        <video src="./video/news.mp4" controls width="80%"></video>
        <!-- <audio src="./audio/news_1739964534813.mp3" controls></audio> -->
        <p><!-- &nbsp;表示一个空格字符 -->
          <b>央视网消息</b>
          （新闻联播）：作为共抓长江大保护的标志性工程，长江十年禁渔今年进入第四年。习近平总书记指出，长江禁渔是为全局计、为子孙谋的重要决策。牢记总书记嘱托，沿江省市持续推进长江水生生物多样性恢复，努力保障退捕渔民就业生活。这段时间，记者深入长江两岸，记录下禁渔工作取得的重要阶段性成效和广大干部群众坚定不移推进长江十年禁渔的扎实行动。
        </p>
        <p>行走在长江沿线，科研人员发现很多可喜现象。</p>
        <!-- 引入一张gif，在./Picture目录下 -->
        <!-- img标签属性
        src-访问路径
        1.绝对路径
          1.1绝对磁盘路径:C:\Users\Administrator\Desktop\Study\Picture\1_1739964534896.gif
          1.2绝对网络路径:https://www.baidu.com/img/bd_logo1.png
        2.相对路径
          2.1./表示当前目录(可以省略)
          2.2../表示上一级目录
         
        alt-图片描述
        width-宽度
        height-高度,建议只设置一个,另一个会自动适应
        px：像素
        百分比：相对于父元素的宽度
        自动：根据图片的宽度自动调整 -->
        <img src="./Picture/1_1739964534896.gif" alt="gif" width="80%"></img>
        <p>在长江南源，一处小头裸裂尻鱼新的栖息地被发现，鱼的数量大约超3万尾，为水生态保护提供了珍贵数据。</p>
        <br>
        <p>在长江中游，追踪显示，人工增殖放流的中华鲟成功入海率已经从45%左右提升至60%以上；鄱阳湖鱼类小型化、低龄化趋势得到遏制，栖息地生存环境得以改善。</p>
        <br>
        <p>在长江下游，今年3月起，南京秦淮河入江口首次出现野生中华绒螯蟹大规模洄游现象，种群数量明显增加。</p>
        
        <img src="./Picture/2_1739964534978.jpg" width="80%">
        <p>水生生物资源恢复向好，见证了长江十年禁渔三年多来的阶段性成果。</p>
        <br>
        <p>实施长江十年禁渔，是以习近平同志为核心的党中央从中华民族长远利益出发作出的重要决策。党的十八大以来，总书记多次深入长江沿线考察调研，详细了解长江十年禁渔的实施情况，他指出，要坚定推进长江十年禁渔，巩固好已经取得的成果。</p>
        
        <img src="./Picture/3_1739964535067.jpg" width="80%">
        <p>按照部署，自2021年1月1日起，在长江干流、大型通江湖泊、重要支流和长江口部分海域实行为期十年的禁渔，常年禁止天然渔业资源的生产性捕捞。禁渔三年多来，相关评估显示，长江干流和鄱阳湖、洞庭湖水生生物完整性指数由禁渔前最差的“无鱼”提升了两个等级。2022年，长江江豚数量达到1249头，实现历史性止跌回升。长江干流水质连续4年全线保持Ⅱ类。</p>
        <br>
        <p>实施长江十年禁渔，解决好渔民上岸后的生产生活问题，禁渔才有稳定扎实的社会基础。</p>
        
        <img src="./Picture/4_1739964535156.jpg" width="80%">
        <p>安徽退捕转产的3万多名渔民，在政府的引导下接受就业培训。在当涂县，免费学习养殖技术，养殖生态螃蟹成了退捕渔民的新选择。</p>
        <br>
        <p>在拥有洞庭湖超六成水域的湖南岳阳，政府帮扶上岸渔民建起养殖场，发展风干鱼产业，还带领他们学习直播带货，拓宽销路。</p>
        <br>
        <p>在渔民退捕上岸的鄱阳湖棠荫岛，当地在继续保护好生态的前提下，正探索规划利用独特的自然资源发展旅游产业。禁渔三年多来，有关部门对23.1万退捕渔民逐一建档立卡，多渠道提升就业、社保水平。</p>

        <img src="./Picture/5_1739964535235.jpg" width="80%">
        <p>长江十年禁渔实施以来，沿江省市合力攻坚、久久为功，长江大保护不断向纵深推进，持续巩固禁渔成果。下一步，沿江省市还将加强水生生物重要栖息地修复，建立退捕渔民动态精准帮扶服务，完善跨区域、跨部门执法合作机制，确保一江清水绵延后世、惠泽人民。</p>
    </body>
</html> 
```

![image-20250222135623696](./picture/image-20250222135623696.png)

### 常见标签和样式-央视新闻-整体样式

代码

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</title>
        <style>
          #time{
            color: #b2b2b2;
          }    
          a{
            /* 去除超链接下的下划线 */
            text-decoration:none;
          }
          p{
            /* 首行缩进 */
            text-indent: 2em;
            /* 行高 */
            line-height: 2;/* 行高为字体大小的2倍 */
          }
          #page{
            width: 70%;/* 上下外边距为0，左右外边距自动，实现居中显示 */
            margin-left: auto;
            margin-right: auto;
          }
        </style>
        <!-- 方式3：外部样式 -->
        <!-- <link rel="stylesheet" href="./css/news.css"> -->
    </head>
    <body>
      <div id="page">
       
        <!--  -------------------新闻标题-------------------- -->
        <h1>【新思想引领新征程】推进长江十年禁渔 谱写长江大保护新篇章</h1>
      
        <a href="https://www.cctv.com" target="_blank" >央视网</a> 
        <!-- 发布时间 -->
        <span id="time">2024年05月15日 20:07</span>
        <br>
        <!--  -------------------新闻主体-------------------- -->
        <!-- 引入一个视频,路径为./video/video.mp4,controls表示显示控件-->
         <!-- video标签属性
          src-视频路径
          controls-显示控件
          autoplay-自动播放
          width-宽度
          height-高度,建议只设置一个,另一个会自动适应
            px：像素
            百分比：相对于父元素的宽度
            自动：根据视频的宽度自动调整
          loop-循环播放
          poster-封面图片
          muted-静音
          preload-预加载
         -->
        <video src="./video/news.mp4" controls width="100%"></video>
        <!-- <audio src="./audio/news_1739964534813.mp3" controls></audio> -->
        <p><!-- &nbsp;表示一个空格字符 -->
          <b>央视网消息</b>
          （新闻联播）：作为共抓长江大保护的标志性工程，长江十年禁渔今年进入第四年。习近平总书记指出，长江禁渔是为全局计、为子孙谋的重要决策。牢记总书记嘱托，沿江省市持续推进长江水生生物多样性恢复，努力保障退捕渔民就业生活。这段时间，记者深入长江两岸，记录下禁渔工作取得的重要阶段性成效和广大干部群众坚定不移推进长江十年禁渔的扎实行动。
        </p>
        <p>行走在长江沿线，科研人员发现很多可喜现象。</p>
        <!-- 引入一张gif，在./Picture目录下 -->
        <!-- img标签属性
        src-访问路径
        1.绝对路径
          1.1绝对磁盘路径:C:\Users\Administrator\Desktop\Study\Picture\1_1739964534896.gif
          1.2绝对网络路径:https://www.baidu.com/img/bd_logo1.png
        2.相对路径
          2.1./表示当前目录(可以省略)
          2.2../表示上一级目录
         
        alt-图片描述
        width-宽度
        height-高度,建议只设置一个,另一个会自动适应
        px：像素
        百分比：相对于父元素的宽度
        自动：根据图片的宽度自动调整 -->
        <img src="./Picture/1_1739964534896.gif" alt="gif" width="100%"></img>
        <p>在长江南源，一处小头裸裂尻鱼新的栖息地被发现，鱼的数量大约超3万尾，为水生态保护提供了珍贵数据。</p>
        <br>
        <p>在长江中游，追踪显示，人工增殖放流的中华鲟成功入海率已经从45%左右提升至60%以上；鄱阳湖鱼类小型化、低龄化趋势得到遏制，栖息地生存环境得以改善。</p>
        <br>
        <p>在长江下游，今年3月起，南京秦淮河入江口首次出现野生中华绒螯蟹大规模洄游现象，种群数量明显增加。</p>
        
        <img src="./Picture/2_1739964534978.jpg" width="100%">
        <p>水生生物资源恢复向好，见证了长江十年禁渔三年多来的阶段性成果。</p>
        <br>
        <p>实施长江十年禁渔，是以习近平同志为核心的党中央从中华民族长远利益出发作出的重要决策。党的十八大以来，总书记多次深入长江沿线考察调研，详细了解长江十年禁渔的实施情况，他指出，要坚定推进长江十年禁渔，巩固好已经取得的成果。</p>
        
        <img src="./Picture/3_1739964535067.jpg" width="100%">
        <p>按照部署，自2021年1月1日起，在长江干流、大型通江湖泊、重要支流和长江口部分海域实行为期十年的禁渔，常年禁止天然渔业资源的生产性捕捞。禁渔三年多来，相关评估显示，长江干流和鄱阳湖、洞庭湖水生生物完整性指数由禁渔前最差的“无鱼”提升了两个等级。2022年，长江江豚数量达到1249头，实现历史性止跌回升。长江干流水质连续4年全线保持Ⅱ类。</p>
        <br>
        <p>实施长江十年禁渔，解决好渔民上岸后的生产生活问题，禁渔才有稳定扎实的社会基础。</p>
        
        <img src="./Picture/4_1739964535156.jpg" width="100%">
        <p>安徽退捕转产的3万多名渔民，在政府的引导下接受就业培训。在当涂县，免费学习养殖技术，养殖生态螃蟹成了退捕渔民的新选择。</p>
        <br>
        <p>在拥有洞庭湖超六成水域的湖南岳阳，政府帮扶上岸渔民建起养殖场，发展风干鱼产业，还带领他们学习直播带货，拓宽销路。</p>
        <br>
        <p>在渔民退捕上岸的鄱阳湖棠荫岛，当地在继续保护好生态的前提下，正探索规划利用独特的自然资源发展旅游产业。禁渔三年多来，有关部门对23.1万退捕渔民逐一建档立卡，多渠道提升就业、社保水平。</p>

        <img src="./Picture/5_1739964535235.jpg" width="100%">
        <p>长江十年禁渔实施以来，沿江省市合力攻坚、久久为功，长江大保护不断向纵深推进，持续巩固禁渔成果。下一步，沿江省市还将加强水生生物重要栖息地修复，建立退捕渔民动态精准帮扶服务，完善跨区域、跨部门执法合作机制，确保一江清水绵延后世、惠泽人民。</p>
        </div>
      </body>
</html>
```

#### 盒子模型

![image-20250222141039980](./picture/image-20250222141039980.png)

![image-20250222141812856](./picture/image-20250222141812856.png)

代码

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    #div1{
      width: 400px;/*默认是内容展示区域的宽度*/
      height: 400px;
      background-color: pink;
      padding: 30px;
      box-sizing: border-box;/*属性值改为这个就会让盒子外面变成400,300而不是内容显示区域*/
      /* 设置边框 */
      border: 10px solid red;
      /* 设置外边距 */
      margin: 30px auto; /*上下外边距为30,左右外边距自动,实现居中显示*/
    }
  </style>
</head>
<body>
    <div id="div1">
        A A A A A A A A A A A A A A A A
    </div>
</body>
</html>
```

效果:

![image-20250222143103150](./picture/image-20250222143103150.png)

总结

![image-20250222143113397](./picture/image-20250222143113397.png)

### 常见标签和样式-tlias案例-顶部导航栏

页面原型:是在应用程序开发初期，由产品经理制作的早期项目模型，主要用于展示页面的基本布局、功能以及交互设计，其作用是帮助设计师、开发者等更好地理解和讨论最终产品的外观和行为 。

现在我们需要认识到<strong>提示词</strong>的重要性质



#### Flex弹性布局




![image](./picture/image-20250227221627353.png)

body标签自带的8px的外边距

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        /* body {
            margin: 0;
        } */

        #container {
            width: 500px;
            height: 300px;
            background-color: blue;
            display: flex;
            /* 弹性布局 */
            flex-direction: row;
            /* 垂直排列 */
            justify-content: space-between;
            /*解释justify-content每一个参数的含义*/
            /* flex-start: 从容器的起始位置开始排列 */
            /* flex-end: 从容器的结束位置开始排列 */
            /* center: 居中排列 */
            /* space-between: 均匀排列，第一个元素在容器的起始位置，最后一个元素在容器的结束位置 */
            /* space-around: 均匀排列，每个元素周围都有相同的空间 */
            /* space-evenly : 均匀排列，每个元素之间的空间相等 */

        }

        .box {
            width: 50px;
            height: 50px;
            background-color: red;
            border: 1px solid black;
        }
    </style>
</head>

<body>


    <div id="container">
        <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
    </div>
</body>
```
效果图
![image](./picture/image.png)

### HTML-CSS-常见标签和样式-表单标签



![image1](./picture/image-1.png)


- get:将表单数据拼接在url后面,不安全,但是可以被缓存(默认)*,例如: /save?name=zhangsan&age=18 */
> 如果是隐私数据，就不推荐使用GET
在浏览器中GET请求大小有限制,不适合大数据的表单

- post:将表单数据放在请求体中,安全,但是不可以被缓存*/ 例如: /save -->
> 如果是隐私数据，就推荐使用POST
请求大小没有限制

效果图:
![alt text](image.png)
代码
```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <!-- /*form表单元素*/
    /*form表单元素的作用：收集用户输入的数据*/
    /*form表单元素的属性：action,method,target*/
    /*action:表单提交的地址*/ -->
    <!-- /*method:表单提交的方式*/
    /*get:将表单数据拼接在url后面,不安全,但是可以被缓存(默认)*,例如: /save?name=zhangsan&age=18 */
    /*post:将表单数据放在请求体中,安全,但是不可以被缓存*/ 例如: /save -->
    <!-- 表单项要能够采集数据，就要设置name属性,表示当前表单项的名字 -->
    <form action="/save" method="post">
        姓名: <input type="text" name="name">
        年龄: <input type="number" name="age">
        <input type="submit" value="提交">
        
    </form>
</body>

</html>
```

### HTML-CSS-常见标签和样式-表单项标签


![image](./picture/image-3.png)

代码:POST请求

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <form action="/save" method="post">
        姓名: <input type="text" name="name"><br>

        年龄: <input type="number" name="age"><br>

        密码:
        <input type="password" name="password"><br>
        男<input type="radio" name="sex" value="male">
        女<input type="radio" name="sex" value="female"><br>


        选择学历:
        <select name="select">
            <option value="">-------------请选择-------------</option>
            <option value="大学">大学</option>
            <option value="中学">中学</option>
            <option value="初中">初中</option>
        </select><br>
        爱好:
        <input type="checkbox" name="hobby" value="Java">Java
        <input type="checkbox" name="hobby" value="Python">Python
        <input type="checkbox" name="hobby" value="跑步">跑步
        <br>
        个人简介:
        <textarea name="desc" id="1" cols="4" rows="4"></textarea><br>
        文件上传
        <input type="file" name="file"><br>
        时间:
        <input type="date" name="date"><br>

        <!-- 表单常见按钮 -->
        <input type="submit" value="提交">
        <input type="reset" value="重置">
        <input type="button" value="按钮">




    </form>
</body>

</html>
```




![image](./picture/image-4.png)


label标签
> 可以让被标签包裹的字被点击时也选中，而不是必须要点击圆圈

总结
![image](./picture/image-5.png)


### HTML-CSS-常见标签和样式-tlias案例-搜索表单区域
skip





## JS-介绍
什么是 Javascript

Web 标准也称网页标准，由一系列的标准组成，大部分由 W3C (WorldWideWebConsortium, 万维网联盟) 负责制定。
三个组成部分:
- HTML: 负责网页的结构 (页面元素和内容)。
- CSS: 负责网页的表现 (页面元素的外观、位置等页面样式，如：颜色、大小等)。
- Javascript: 负责网页的行为 (交互效果)。



简介

>Javascript(简称:JS)是一门跨平台、面向对象的脚本语语言,是用来控制网页行为,实现页面的交互效果。
Javascript和Java是完全不同的语言,不论是概念还是概念还是设计。但是基础语法类似。

组成:
- ECMAScript:规定了JS基础语法核心知识,包括变量、数据类型、流程控制、函数、对象等。
- BOM:浏览器对象模型,用于操作浏览器本身,如:页面弹窗、地址栏操作、关闭窗口等。
- DOM:文档对象模型,用于操作HTML文档,如:改变标签内内的内容、改变标签内字体样式等。


### JS核心语法-引入方式

![alt text](./picture/image-6.png)

![alt text](./picture/image-7.png)



1. JS 引入方式
内部脚本：将 JS 代码定义在 HTML 页面的<script></script>中 (<:body> 的底部)
外部脚本：将 JS 代码定义在 JS 文件中，通过 < scriptsrc=""></script>标签引入
2. JS 书写规范
结束符：每行结尾以分号结尾，结尾分号可有可无

### JS 核心语法-变量&数据类型

> JS 中用 let 关键字来声明变量 (弱类型语言，变量可以存存放不同类型的值)。
变量名需要遵循如下规则:

- 只能用字母、数字、下划线 (_)、美元符号 ($) 组成，且数字不能开头

- 变量名严格区分大小写，如 name 和 Name 是不同的变量

- 不能使用关键字，如:let、var、if、for 等

JS 中用 const 关键字来声明常量。
一旦声明，常量的值就不能改变 (不可以重新赋值)

```javascript
    // 1. 变量的声明
    let a = 10;

    let b = "HelloWorld";
    //2.常量的声明
    const PI = 3.14;
    // PI = 12;
    alert(b)//弹出窗口
    console.log(PI)//输出到控制台
    document.write("你好")//直接写在body区域
```

JavaScript 的数据类型分为：基本数据类型和引用数据类型 (对象)。
基本数据类型:
- number: 数字 (整数、小数、NaN (Not a Number))
- boolean: 布尔。true,false
- null: 对象为空。Javascript 是大小写敏感的，因此 null、Null、Nu11、NULL 是完全不同的
- undefined: 当声明的变量未初始化时，该变量的默认值是 undefined
-  string: 字符串，单引号、双引号、反引号皆可，推荐使用单引号

使用typeof可以查看数据的类型
```js
typeof 变量
```


数据类型
模板字符串语法:
(反引号，英文输入模式下按键盘的 tab 键上方波浪线～那个个键
内容拼接变量时，使用 ${} 包住变量
```js
let str = 'Fuck';
console.log(`${str}you`)
```

 ### JS 核心语法-函数

 ![image](./picture/image%20copy.png)

![image](./picture/image%20copy%202.png)

实例代码
```html
<script>
    //1.函数的定义和调用
    function add(a, b) {//-具名函数
      return a + b;
    }
    let result = add(12, 10);
    alert(result)


    //2.1
    //函数表达式
    let func = function (a, b) {
      return a * b;
    }
    //2.2
    // 箭头函数
    let a = (a, b) => {
      return a + b;
    }
    alert(a(2, 3))
  </script>

```

 ### JS-核心语法-自定义对象&JSON

#### 自定义对象
![image](./picture/image%20copy%203.png)

调用方式:

- 调用属性
> 对象名.属性名;

- 调用方法
> 对象名.方法名

注意尽量不要用箭头函数
```js
let user = {
      name: 'hexiaolei',
      age: 18,
      address: '苏州',
      say: function (str) {
        alert(str);
      },
      //也可以
      sayA(str2) {
        alert(str2)
      },
      //在箭头函数中，this并不指向当前对象，指向的是当前元素的上级
      sayB: () => {
        alert(this + 'hello')
      }
    }
    user.say('Hello');
    user.sayA('helloAgain')
    user.sayB()

```
因为`sayB`方法中的this,指向的是object window,而不是当前对象

#### JSON

概念:JavaScript Object Notation,JavaScript对象标记法(JS对象标记法书写的文本)

由于语法简单，层次结构鲜明，所以常用于数据载体，在网络中进行传输



JSON格式:`{key:value,key1:value,key2:value}`
z
```js
//讲js对象转化为字符串,JSON.stringify()
    let user = {
      name: 'hexiaolei',
      age: '18',
      addresss: '苏州',
    }
    //js->json
    console.log(JSON.stringify(user))

    //json->js
    let jsonString = '{"name":"hexiaolei","age":18,"address":"Suzhou"}'
    alert(JSON.parse(jsonString).name)
```



### JS-核心语法-DOM

概念:Document Object Model,文档对象模型

将标记语言的各个组成部分分装为对应的对象:
- Document:整个文档对象
- Element:元素对象
- Attribute:属性对象
- Text:文本对象
- Cpmment:注释对象


![image](./picture/image%20copy%204.png)

JavaScritp通过DOM，可以对html进行以下更改
- 改变html元素内容
- 改变html元素样式(css)
- 对html DOM时间做出反应
- 添加或者删除html元素

DOM操作核心思想: 将网页中所有元素当作对象处理，（标签的所有属性在该对象上都可以找到）

操作步骤:
- 获取要操作的DOM对象
- 操作DOM对象的属性和方法

获取DOM对象
- 根据CSS选择器来选择DOM元素，获取匹配到的第一个元素:document.querySelector('选择器')
- 根据CSS选择器来选择DOM元素，获取匹配到的第一个元素:document.querySelectorAll('选择器')//标签选择器span,类选择器.xxx,id选择器#xxx
！！！：得到的是NodeList节点集合，是一个伪数组(有长度，有索引的数组)



练习小代码
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JS-DOM</title>
</head>

<body>

  <h1 id="title1">11111</h1>
  <h1>22222</h1>
  <h1>33333</h1>

  <script>
    //修改第一个h1标签的内容

    let h = document.querySelector('h1');
    h.innerHTML = '48123428-1039';
    // document.querySelectorAll('h1')[1].innerHTML = '555555';

    let all = document.querySelectorAll('h1');

    for (let i = 0; i < all.length; i++) {
      all[i].innerHTML = '666666';
    }

  </script>
</body>

</html>


```

### JS-核心语法-事件监听

事件:HTML事件是发生在HTML元素上的事情,例如
- 按钮被点击
- 鼠标移动要元素上
- 按下键盘按键

事件监听:JavaScript可以在事件触发时，就立刻调用一个函数，也称为事件绑定或注册事件.

语法:`事件源.addEventListener('事件类型',事件触发执行的函数)`
事件监听三要素:
- 事件源：哪个dom元素出发了事件，要获取dom元素
- 事件类型:用什么方式出发，比如：鼠标单击click
- 事件触发执行的函数:要做什么事情 
 

练习代码
```html

<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Tlias智能学习辅助系统</title>
    <style>
        /* 导航栏样式 */
        .navbar {
            background-color: #b5b3b3;
            /* 灰色背景 */

            display: flex;
            /* flex弹性布局 */
            justify-content: space-between;
            /* 左右对齐 */

            padding: 10px;
            /* 内边距 */
            align-items: center;
            /* 垂直居中 */
        }

        .navbar h1 {
            margin: 0;
            /* 移除默认的上下外边距 */
            font-weight: bold;
            /* 加粗 */
            color: white;
            /* 设置字体为楷体 */
            font-family: "楷体";
        }

        .navbar a {
            color: white;
            /* 链接颜色为白色 */
            text-decoration: none;
            /* 移除下划线 */
        }

        /* 搜索表单样式 */
        .search-form {
            display: flex;
            flex-wrap: nowrap;
            align-items: center;
            gap: 10px;
            /* 控件之间的间距 */
            margin: 20px 0;
        }

        .search-form input[type="text"],
        .search-form select {
            padding: 5px;
            /* 输入框内边距 */
            width: 260px;
            /* 宽度 */
        }

        .search-form button {
            padding: 5px 15px;
            /* 按钮内边距 */
        }

        /* 表格样式 */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        th,
        td {
            border: 1px solid #ddd;
            /* 边框 */
            padding: 8px;
            /* 单元格内边距 */
            text-align: center;
            /* 左对齐 */
        }

        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }

        .avatar {
            width: 30px;
            height: 30px;
        }

        /* 页脚样式 */
        .footer {
            background-color: #b5b3b3;
            /* 灰色背景 */
            color: white;
            /* 白色文字 */
            text-align: center;
            /* 居中文本 */
            padding: 10px 0;
            /* 上下内边距 */
            margin-top: 30px;
        }

        #container {
            width: 80%;
            /* 宽度为80% */
            margin: 0 auto;
            /* 水平居中 */
        }
    </style>
</head>

<body>
    <div id="container">
        <!-- 顶部导航栏 -->
        <div class="navbar">
            <h1>Tlias智能学习辅助系统</h1>
            <a href="#">退出登录</a>
        </div>

        <!-- 搜索表单区域 -->
        <form class="search-form" action="/search" method="post">
            <label for="name">姓名：</label>
            <input type="text" id="name" name="name" placeholder="请输入姓名">

            <label for="gender">性别：</label>
            <select id="gender" name="gender">
                <option value=""></option>
                <option value="1">男</option>
                <option value="2">女</option>
            </select>

            <label for="position">职位：</label>
            <select id="position" name="position">
                <option value=""></option>
                <option value="1">班主任</option>
                <option value="2">讲师</option>
                <option value="3">学工主管</option>
                <option value="4">教研主管</option>
                <option value="5">咨询师</option>
            </select>

            <button type="submit">查询</button>
            <button type="reset">清空</button>
        </form>

        <!-- 表格展示区 -->
        <table>
            <!-- 表头 -->
            <thead>
                <tr>
                    <th>姓名</th>
                    <th>性别</th>
                    <th>头像</th>
                    <th>职位</th>
                    <th>入职日期</th>
                    <th>最后操作时间</th>
                    <th>操作</th>
                </tr>
            </thead>

            <!-- 表格主体内容 -->
            <tbody>
                <tr>
                    <td>令狐冲</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="令狐冲"></td>
                    <td>讲师</td>
                    <td>2021-06-15</td>
                    <td>2024-09-16 15:30</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>任盈盈</td>
                    <td>女</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="任盈盈"></td>
                    <td>咨询师</td>
                    <td>2021-07-20</td>
                    <td>2024-09-17 09:00</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>向问天</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>班主任</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>任我行</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>教研主管</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>田伯光</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="令狐冲"></td>
                    <td>班主任</td>
                    <td>2021-06-15</td>
                    <td>2024-09-16 15:30</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>不戒</td>
                    <td>女</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="任盈盈"></td>
                    <td>班主任</td>
                    <td>2021-07-20</td>
                    <td>2024-09-17 09:00</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>左冷禅</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>班主任</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>定逸</td>
                    <td>女</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>班主任</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>东方兄弟</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>讲师</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
                <tr>
                    <td>金庸</td>
                    <td>男</td>
                    <td><img class="avatar" src="https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg"
                            alt="向问天"></td>
                    <td>咨询师</td>
                    <td>2021-05-01</td>
                    <td>2024-09-15 17:45</td>
                    <td class="action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
            </tbody>
        </table>

        <!-- 页脚版权区域 -->
        <footer class="footer">
            <p>江苏传智播客教育科技股份有限公司</p>
            <p>版权所有 Copyright 2006-2024 All Rights Reserved</p>
        </footer>
    </div>

    <script>
        //通过JS为上述的表格中数据行添加事件监听, 实现鼠标进入后, 背景色#f2e2e2; 鼠标离开后, 背景色需要设置为#fff; (JS新版本的语法)
        //两个标签选择器之间用逗号隔开,然后再用forEach方法遍历
        //forEach方法的参数是一个函数,这个函数有一个参数,这个参数就是当前遍历到的元素
        document.querySelectorAll('tbody tr').forEach((tr) => {
            tr.addEventListener('mouseenter', () => {
                tr.style.backgroundColor = '#f2e2e2';
            });
            tr.addEventListener('mouseleave', () => {
                tr.style.backgroundColor = '#fff';
            });
        });
    </script>
</body>

</html>

```


常见事件

|鼠标事件|键盘事件|焦点事件|表单事件|
|:-:|:-:|:-:|:-:|
|click(鼠标点击)|keydown(按下触发)|focus(获取焦点触发)|input(输入时触发)|
|mouseenter(鼠标移入)|keyup(抬起触发)|blur(失去焦点)|submit(提交时触发)|
|mouseleave(鼠标移出)|


### JS-核心语法-事件监听（优化）

JS模块化(export,import)

## Vue快速入门

什么是Vue?

Vue是一个用于**构建用户界面**的**渐进式**JavaScript**框架**。


Vue是一个生态系统，包含了Vue.js、Vue Router、Vuex等多个组件。


框架：就是一套完整的项目解决方案，用于快速构建项目。

优点：大大提升前端项目的开发效率
。
缺点：需要理解记忆框架的使用规则。（参照官网）

基于数据渲染出用户看到的界面

数据驱动视图
### Vue-常见指令的使用

![image](./picture/image%20copy%205.png)


案例
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Tlias智能学习辅助系统</title>
    <style>
        /* 导航栏样式 */
        .navbar {
            background-color: #b5b3b3;
            /* 灰色背景 */

            display: flex;
            /* flex弹性布局 */
            justify-content: space-between;
            /* 左右对齐 */

            padding: 10px;
            /* 内边距 */
            align-items: center;
            /* 垂直居中 */
        }

        .navbar h1 {
            margin: 0;
            /* 移除默认的上下外边距 */
            font-weight: bold;
            /* 加粗 */
            color: white;
            /* 设置字体为楷体 */
            font-family: "楷体";
        }

        .navbar a {
            color: white;
            /* 链接颜色为白色 */
            text-decoration: none;
            /* 移除下划线 */
        }

        /* 搜索表单样式 */
        .search-form {
            display: flex;
            flex-wrap: nowrap;
            align-items: center;
            gap: 10px;
            /* 控件之间的间距 */
            margin: 20px 0;
        }

        .search-form input[type="text"],
        .search-form select {
            padding: 5px;
            /* 输入框内边距 */
            width: 260px;
            /* 宽度 */
        }

        .search-form button {
            padding: 5px 15px;
            /* 按钮内边距 */
        }

        /* 表格样式 */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        th,
        td {
            border: 1px solid #ddd;
            /* 边框 */
            padding: 8px;
            /* 单元格内边距 */
            text-align: center;
            /* 左对齐 */
        }

        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }

        .avatar {
            width: 30px;
            height: 30px;
        }

        /* 页脚样式 */
        .footer {
            background-color: #b5b3b3;
            /* 灰色背景 */
            color: white;
            /* 白色文字 */
            text-align: center;
            /* 居中文本 */
            padding: 10px 0;
            /* 上下内边距 */
            margin-top: 30px;
        }

        #container {
            width: 80%;
            /* 宽度为80% */
            margin: 0 auto;
            /* 水平居中 */
        }
    </style>
</head>

<body>
    <div id="container">
        <!-- 顶部导航栏 -->
        <div class="navbar">
            <h1>Tlias智能学习辅助系统</h1>
            <a href="#">退出登录</a>
        </div>

        <!-- 搜索表单区域 -->
        <form class="search-form" action="/search" method="post">
            <label for="name">姓名：</label>
            <input type="text" id="name" name="name" placeholder="请输入姓名">

            <label for="gender">性别：</label>
            <select id="gender" name="gender">
                <option value=""></option>
                <option value="1">男</option>
                <option value="2">女</option>
            </select>

            <label for="position">职位：</label>
            <select id="position" name="position">
                <option value=""></option>
                <option value="1">班主任</option>
                <option value="2">讲师</option>
                <option value="3">学工主管</option>
                <option value="4">教研主管</option>
                <option value="5">咨询师</option>
            </select>

            <button type="submit">查询</button>
            <button type="reset">清空</button>
        </form>

        <!-- 表格展示区 -->
        <table>
            <!-- 表头 -->
            <thead>
                <tr>
                    <th>序号</th>
                    <th>姓名</th>
                    <th>性别</th>
                    <th>头像</th>
                    <th>职位</th>
                    <th>入职日期</th>
                    <th>最后操作时间</th>
                    <th>操作</th>
                </tr>
            </thead>

            <!-- 表格主体内容 -->
            <tbody>
                <!-- key唯一标识符, -->
                <tr v-for="(item,index) in empList" :key="item.id">
                    <td>{{index + 1 }}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.gender == 1 ? '女':'男'}}</td>
                    <!-- 插值表达式不可以出现在标签内部 -->
                    <td><img class="avatar" src="{{item.image}}" alt={{item.name}}></td>
                    <td>{{item.job}}</td>
                    <td>{{item.entrydate}}</td>
                    <td>{{item.updatetime}}</td>
                    <td class=" action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
            </tbody>
        </table>

        <!-- 页脚版权区域 -->
        <footer class="footer">
            <p>江苏传智播客教育科技股份有限公司</p>
            <p>版权所有 Copyright 2006-2024 All Rights Reserved</p>
        </footer>
    </div>


    <script type="module">
        import { createApp } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'

        createApp({
            data() {
                return {
                    empList: [
                        {
                            "id": 1,
                            "name": "谢逊",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/4.jpg",
                            "gender": 1,
                            "job": "1",
                            "entrydate": "2023-06-09",
                            "updatetime": "2024-09-30T14:59:38"
                        },
                        {
                            "id": 2,
                            "name": "韦一笑",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg",
                            "gender": 1,
                            "job": "1",
                            "entrydate": "2020-05-09",
                            "updatetime": "2024-09-01T00:00:00"
                        },
                        {
                            "id": 3,
                            "name": "黛绮丝",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/2.jpg",
                            "gender": 2,
                            "job": "2",
                            "entrydate": "2021-06-01",
                            "updatetime": "2024-09-01T00:00:00"
                        }
                    ]
                }
            }
        }).mount('#container')
    </script>

</body>

</html>
```



![image](./picture/image%20copy%206.png)



### Vue-常用指令-v-model与v-on

v-bind作用
- 动态威HTML标签绑定属性值，如href,src,style样式等
- 语法: v-bind:属性名="属性值"
- 简化: :属性名="属性值"

动态为标签的属性绑定值，不能使用插值表达式，得使用v-bind命令。且绑定的数据,必须在data中定义

v-if & v-show

- 作用:这两个指令，都是用来控制元素的显示和隐藏的
- v-if
    - 语法:v-if="表达式",为true，显示，false，不显示
    - 原理:基于条件判断，来控制创建或移除元素节点（条件渲染）
    - 场景:要么显示,要么不显示，切换不频繁的场景
- v-show
    - 语法:v-show="表达式",为true，显示，false，隐藏
    - 原理:基于css演示display来控制显示和隐藏
    - 场景：频繁切换显示隐藏的场景

注意：
v-else-if必须出现在v-if之后，可以出现多个;
v-else必须出现在v-if/v-else-if之后。

练习代码
```html

<tbody>
                <!-- key唯一标识符, -->
                <tr v-for="(item,index) in empList" :key="item.id">
                    <td>{{index + 1 }}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.gender == 1 ? '女':'男'}}</td>
                    <!-- 插值表达式不可以出现在标签内部 -->
                    <td><img class="avatar" v-bind:src="item.image" alt=1></td>
                    <td>
                        <span v-if="item.job==1">班主任</span>
                        <span v-else-if="item.job==2">讲师</span>
                        <span v-else-if="item.job==3">学工主管</span>
                        <span v-else-if="item.job==4">教研主管</span>
                        <span v-else-if="item.job==5">咨询师</span>
                        <span v-else>其他</span>
                    </td>
                    <td>{{item.entrydate}}</td>
                    <td>{{item.updatetime}}</td>
                    <td class=" action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
            </tbody>

```
v-show就是把v-if替换，显示时依靠display属性

1.v-if 与 v-show的作用?
根据条件判断，是否展示某元素
2. v-if 与 v-show的区别?
v-if：条件不成立，直接不渲染这个元素（不频繁切换的场景）
V-show:通过css样式，来控制元素的展示与隐藏（频繁切换的场景)

### Vue-常用指令-v-model与v-on

采集表单项数据: v-model
事件绑定:v-on

作用: 在表单元素上使用,双向数据绑定。可以方便获取 或 设置 表单项数据
语法：v-model="变量名"
 

 v-on
 - 作用：为html标签绑定事件(添加事件监听)
 - 语法：
    - v-on:事件名="方法名"
    - 简写为@事件名="..."


练习代码
```html
<!DOCTYPE html>
<html lang="zh-CN">

<head>
    <meta charset="UTF-8">
    <title>Tlias智能学习辅助系统</title>
    <style>
        /* 导航栏样式 */
        .navbar {
            background-color: #b5b3b3;
            /* 灰色背景 */

            display: flex;
            /* flex弹性布局 */
            justify-content: space-between;
            /* 左右对齐 */

            padding: 10px;
            /* 内边距 */
            align-items: center;
            /* 垂直居中 */
        }

        .navbar h1 {
            margin: 0;
            /* 移除默认的上下外边距 */
            font-weight: bold;
            /* 加粗 */
            color: white;
            /* 设置字体为楷体 */
            font-family: "楷体";
        }

        .navbar a {
            color: white;
            /* 链接颜色为白色 */
            text-decoration: none;
            /* 移除下划线 */
        }

        /* 搜索表单样式 */
        .search-form {
            display: flex;
            flex-wrap: nowrap;
            align-items: center;
            gap: 10px;
            /* 控件之间的间距 */
            margin: 20px 0;
        }

        .search-form input[type="text"],
        .search-form select {
            padding: 5px;
            /* 输入框内边距 */
            width: 260px;
            /* 宽度 */
        }

        .search-form button {
            padding: 5px 15px;
            /* 按钮内边距 */
        }

        /* 表格样式 */
        table {
            width: 100%;
            border-collapse: collapse;
        }

        th,
        td {
            border: 1px solid #ddd;
            /* 边框 */
            padding: 8px;
            /* 单元格内边距 */
            text-align: center;
            /* 左对齐 */
        }

        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }

        .avatar {
            width: 30px;
            height: 30px;
        }

        /* 页脚样式 */
        .footer {
            background-color: #b5b3b3;
            /* 灰色背景 */
            color: white;
            /* 白色文字 */
            text-align: center;
            /* 居中文本 */
            padding: 10px 0;
            /* 上下内边距 */
            margin-top: 30px;
        }

        #container {
            width: 80%;
            /* 宽度为80% */
            margin: 0 auto;
            /* 水平居中 */
        }
    </style>
</head>

<body>
    <div id="container">
        <!-- 顶部导航栏 -->
        <div class="navbar">
            <h1>Tlias智能学习辅助系统</h1>
            <a href="#">退出登录</a>
        </div>
        {{searchForm}}
        <!-- 搜索表单区域 -->
        <form class="search-form">
            <label for="name">姓名：</label>
            <input type="text" id="name" name="name" placeholder="请输入姓名" v-model="searchForm.name">
            <label for="gender">性别：</label>
            <select id="gender" name="gender" v-model="searchForm.gender">
                <option value="1">男</option>
                <option value="2">女</option>
            </select>

            <label for="position">职位：</label>
            <select id="position" name="position" v-model="searchForm.job">

                <option value="1">班主任</option>
                <option value="2">讲师</option>
                <option value="3">学工主管</option>
                <option value="4">教研主管</option>
                <option value="5">咨询师</option>
            </select>

            <button type="submit" v-on:click="search">查询</button>
            <button type="reset" v-on:click="reset">清空</button>
        </form>

        <!-- 表格展示区 -->
        <table>
            <!-- 表头 -->
            <thead>
                <tr>
                    <th>序号</th>
                    <th>姓名</th>
                    <th>性别</th>
                    <th>头像</th>
                    <th>职位</th>
                    <th>入职日期</th>
                    <th>最后操作时间</th>
                    <th>操作</th>
                </tr>
            </thead>

            <!-- 表格主体内容 -->
            <tbody>
                <!-- key唯一标识符, -->
                <tr v-for="(item,index) in empList" :key="item.id">
                    <td>{{index + 1 }}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.gender == 1 ? '女':'男'}}</td>
                    <!-- 插值表达式不可以出现在标签内部 -->
                    <td><img class="avatar" v-bind:src="item.image" alt=1></td>
                    <td>
                        <span v-if="item.job==1">班主任</span>
                        <span v-else-if="item.job==2">讲师</span>
                        <span v-else-if="item.job==3">学工主管</span>
                        <span v-else-if="item.job==4">教研主管</span>
                        <span v-else-if="item.job==5">咨询师</span>
                        <span v-else>其他</span>
                    </td>
                    <td>{{item.entrydate}}</td>
                    <td>{{item.updatetime}}</td>
                    <td class=" action-buttons">
                        <button type="button">编辑</button>
                        <button type="button">删除</button>
                    </td>
                </tr>
            </tbody>
        </table>

        <!-- 页脚版权区域 -->
        <footer class="footer">
            <p>江苏传智播客教育科技股份有限公司</p>
            <p>版权所有 Copyright 2006-2024 All Rights Reserved</p>
        </footer>
    </div>


    <script type="module">
        import { createApp } from 'https://unpkg.com/vue@3/dist/vue.esm-browser.js'

        createApp({
            data() {
                return {
                    searchForm://用来封装用户输入的查询条件
                    {
                        name: '',
                        gender: '',
                        job: ''
                    },

                    empList: [
                        {
                            "id": 1,
                            "name": "谢逊",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/4.jpg",
                            "gender": 1,
                            "job": "1",
                            "entrydate": "2023-06-09",
                            "updatetime": "2024-09-30T14:59:38"
                        },
                        {
                            "id": 2,
                            "name": "韦一笑",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/1.jpg",
                            "gender": 1,
                            "job": "7",
                            "entrydate": "2020-05-09",
                            "updatetime": "2024-09-01T00:00:00"
                        },
                        {
                            "id": 3,
                            "name": "黛绮丝",
                            "image": "https://web-framework.oss-cn-hangzhou.aliyuncs.com/2023/2.jpg",
                            "gender": 2,
                            "job": "2",
                            "entrydate": "2021-06-01",
                            "updatetime": "2024-09-01T00:00:00"
                        }
                    ]
                }
            }
            ,
            //方法
            methods: {
                search(event) {
                    event.preventDefault();//阻止表单的默认提交行为
                    console.log(this.searchForm);
                },
                reset() {
                    this.searchForm = {
                        name: '',
                        gender: '',
                        job: ''
                    }
                }
            }
        }).mount('#container')
    </script>

</body>

</html>
```


## Ajax

### Ajax快速入门

什么是Ajax
- 介绍:Asynchronous JavaScript And XML,异步的JavaScript和XML
- 作用
    - 数据交换:通过Ajax可以给服务器发送请求，并获取服务器响应数据.
    - 异步交互：可以在**不重新加载整个页面**的情况下，与服务器交换数据并**更新部分网页**的技术，如果搜索用户名是否可用等.
Axios
- 介绍：Axios 对原生Ajax进行封装，简化书写，快速开发
- 步骤：
    - 引入js文件
    - 使用Axios发送请求，并获取响应结果
 

XML:`Extensible Markup Language`,**可扩展标记语言,本质是一种数据格式,可以用来存储复杂的数据结构**



简单代码演示
```html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Axios入门程序</title>
</head>
<body>

  <button id="getData">GET</button>
  <button id="postData">POST</button>
  
  <script src="https://unpkg.com/axios/dist/axios.min.js"></script>
  <script>
    //GET请求
    document.querySelector('#getData').onclick = function() {
      axios({
        url:'https://mock.apifox.cn/m1/3083103-0-default/emps/list',
        method:'get'
      }).then(function(res) {
        console.log(res.data);
      }).catch(function(err) {
        console.log(err);
      })
    }
    
    //POST请求
    document.querySelector('#postData').onclick = function() {
      axios({
        url:'https://mock.apifox.cn/m1/3083103-0-default/emps/update',
        method:'post'
      }).then(function(res) {
        console.log(res.data);
      }).catch(function(err) {
        console.log(err);
      })
    }
  </script>
</body>
</html>
```


简化方式-Axios请求方法别名
方法  描述
axios.get(url [, config])   发送get请求
axios.delete(url [, config])    发送delete请求
axios.post(url [, data[, config]])  发送post请求
axios.put(url [, data[, config]])   发送put请求

get请求:`axios.get("https://mock.apifox.cn/m1/3083103-0-default/emps/list").then(result => {
    console.log(result.data);
})`


post请求:`axios.post("https://mock.apifox.cn/m1/3083103-0-default/emps/update","id=1").then(result => {
    console.log(result.data);
})`


method:请求方式
url:路径
date:请求数据(POST)
params:发送请求是携带的url参数，如...?key=value




async & await 
可以通过async,awit可以使异步变为同步操作。async就是来声明一个异步方法，await是用来等待异步任务执行
await关键字只在async函数内有效，await关键字取代then函数，等待获取到请求成功的结果值

Vue 的生命周期
生命周期: 指一个对象从创建到销毁的整个过程
生命周期的八个阶段：没出发一个生命周期，会自动执行一个生命周期方法（钩子）



## Maven


### Maven课程介绍
Maven是一款用于管理和构建Java项目的工具,是apache旗下的一个开源项目


### Maven-概述-介绍&安装
[Maven官网](http://maven.apache.org/)

Maven是一款用于管理和构建Java项目的工具，基于项目对象模型(POM project object model) -> pom.xml,的概念，通过一小段描述信息来管理项目的构建

有本地仓库->私有仓库->中央仓库


#### 安装

1. 解压apache-maven-x.x.x-bin.zip
2. 配置本地仓库:修改conf/settings.xml中的<localRepository>为指定一个目录
3. 配置阿里云私服
```xml
     <mirror>
        <id>alimaven</id>
        <name>aliyun maven</name>
        <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
        <mirrorOf>central</mirrorOf>
    </mirror>
```
MAVEN_HOME
%MAVEN_HOME%\bin
将以上代码添加到mirrors中
添加环境变量，与java类似




### Maven-IDEA集成


配置Maven环境(全局)
找到设置，构建工具设置为自己配置的maven地址
设置java版本和jre版本

#### 创建Maven项目
1. 创建模块，选择New Module，填写模块信息，选择构建工具为Maven，点击create，创建完成
2. 编写HelloWorld,并运行

Maven坐标
- 什么是坐标
    - Maven 中的坐标是资源(jar)的唯一标识,通过该坐标可以唯一定位资源位置
    - 使用坐标来定义项目或引入项目中需要的依赖

Maven坐标主要构成
    - groupId:定义当前Maven项目隶属组织名称(通常是域名反写如,com.itheima)
    - artifactId:定义当前Maven项目名称(通常是模块名称,例如:goods-service)
    - version:定义当前版本号
        - SNAPSHOT:功能不稳定，尚处于开发过程中,即快照版本
        - RELEASE:功能趋于稳定，当前更新停止，可以用于发行的版本

```xml
    <groupId>org.example</groupId>
    <artifactId>maven-project-01</artifactId>
    <version>1.0-SNAPSHOT</version>
```
导入依赖例子
```xml
<dependencies>
    <dependency>
        <groupId>cn.hutool</groupId>
        <artifactId>hutool-all</artifactId>
        <version>5.8.21</version>
    </dependency>
</dependencies>
```

导入Maven项目
- 方式一:File -> Project Structure -> Modules -> Import Module -> 选择Maven项目的pom.xml


导入Maven项目
- 建议将要导入的maven项目复制到你的目录下
- 建议选择maven项目的pom.xml文件进行导入


### Maven-依赖管理


依赖:指当前项目运行所需要的jar包，一个项目中可以引入多个依赖。
配置:
1. 在pom.xml中编写<dependencies>标签
2. 在<dependencies>标签中使用<dependency>引入坐标
3. 定义坐标的groupId,artifactId,version
4. 点击刷新按钮，引入最新加入的坐标

排除依赖
> 指主动断开依赖的资源，被派出的资源无需执行版本


```xml

        <dependencies>
            <dependency>
                <groupId>org.springframework</groupId>
                <artifactId>spring-context</artifactId>
                <version>7.0.0-M3</version>
                <exclusions>
                    <exclusion>
                        <groupId>io.micrometer</groupId>
                        <artifactId>micrometer-observation</artifactId>
                    </exclusion>
                </exclusions>
            </dependency>
        </dependencies>
```

注意事项:
- 一旦依赖配置变更了，记得重新加载
- 引入的依赖本地仓库不存在，记得联网


### Maven生命周期

Maven的生命周期就是为了对所有的maven项目构建过程进行抽象和统一

Maven中有三套生命周期**相互独立**
- clean:清理工作
- default:核心工作，如：编译，测试，打包，安装，部署等
- site:生成报告，发布站点等

生命周期阶段
- clean：移除上一次构建生成的文件
- compile：编译项目源代码
- test：使用合适的单元测试框架运行测试(junit)
- package：将编译后的文件打包，如：jar、war等
- install：安装项目到本地仓库 

install时不会执行clean,因为不是同一套生命周期

执行生命周期的方式
- 在idea中，右侧的maven工具栏，点击选择
- 命令行



### 测试

测试：是一种用来促进,鉴定软件的正确性，完整性，安全性和质量的过程

阶段划分：单元测试，集成测试，系统测试，验收测试

|测试类型|介绍|目的|测试人员|
| ---- | ---- | ---- | ---- |
|单元测试|对软件的基本组成单位进行测试，最小测试单位|检验软件基本组成单位的正确性|开发人员|
|集成测试|将已分别通过测试的单元，按设计要求组合成系统或子系统，再进行的测试|检查单元之间的协作是否正确|开发人员|
|系统测试|对已经集成好的软件系统进行彻底的测试|验证软件系统的正确性、性能是否满足指定的要求|测试人员|
|交付测试|针对用户需求、业务流程进行的正式的测试|验证软件系统是否满足验收标准|客户/需求方| 


测试方法：白盒，黑盒，灰盒测试

白盒：
清除软件内部结果，代码逻辑。
用于验证代码，逻辑正确性

黑盒：
不清除软件内部结构，代码逻辑
用于验证软件的功能，兼容性等方面

灰盒：
两者兼有

JUnit:最流行的Java测试框架之一，提供了一些功能，方便程序进行单元测试（第三方公司提供
）
测试代码与源代码分开，便于维护
可根据需要进行自动化测试
可自动分析结果，产出测试报告

案例：使用JUnit，对UserService中的业务方法进行单元测试
1.在pom.xml中，引入JUnit依赖

```xml
<dependency>
        <groupId>org.junit.jupiter</groupId>
        <artifactId>junit-jupiter</artifactId>
        <version>5.9.1</version>
        <scope>test</scope>
    </dependency>
```

2. 在test/java目录下，创建测试类，并编写对应的测试方法，并在方法上声明@Test注解


例子:
```java
import com.example.UserService;
import org.junit.jupiter.api.Test;

public class UserServiceTest {
    @Test
    public void testGetAge(){
        Integer age = new UserService().getAge("320505200701261511");
        System.out.println("age = " + age);
    }
}

```

JUnit单元测试类命名规范：XxxxxTest[规范].JUnit单元测试方法，必须声明为public void[规定]

JUnit提供了一些辅助方法，用来帮我们确定被测试的方法是否按照预期的效果正常工作，这种方式称为断言


| 断言方法 | 描述 |
| --- | --- |
| `Assertions.assertEquals(Object exp, Object act, String msg)` | 检查两个值是否相等，不相等就报错。 |
| `Assertions.assertNotEquals(Object unexp, Object act, String msg)` | 检查两个值是否不相等，相等就报错。 |
| `Assertions.assertNull(Object act, String msg)` | 检查对象是否为null，不为null，就报错。 |
| `AssertionsassertNotNull(Object act, String msg)` | 检查对象是否不为null，为null，就报错。 |
| `Assertions.assertTrue(boolean condition, String msg)` | 检查条件是否为true，不为true，就报错。 |
| `Assertions.assertFalse(boolean condition, String msg)` | 检查条件是否为false，不为false，就报错。 |
| `Assertions. assertThrows(class expType, Executable exec, String msg)` | 检查两个对象引用是否相等，不相等，就报错。 | 

参数msg了可以写，也可以不写


在JUnit中还提供了一些其他注解，还增强其功能，常见的注解有以下几个
| 注解             | 说明                                                         | 备注               |
| ---------------- | ------------------------------------------------------------ | ------------------ |
| `@Test`          | 测试类中的方法用它修饰才能成为测试方法，才能启动执行         | 单元测试           |
| `@ParameterizedTest` | 参数化测试的注解（可以让单个测试运行多次，每次运行时仅参数不同） | 用了该注解，就不需要`@Test`注解了 |
| `@ValueSource`   | 参数化测试的参数来源，赋予测试方法参数                       | 与参数化测试注解配合使用 |
| `@DisplayName`   | 指定测试类、测试方法显示的名称 （默认为类名、方法名）        |                    |
| `@BeforeEach`    | 用来修饰一个实例方法，该方法会在每一个测试方法执行之前执行一次。 | 初始化资源(准备工作） |
| `@AfterEach`     | 用来修饰一个实例方法，该方法会在每一个测试方法执行之后执行一次。 | 释放资源(清理工作） |
| `@BeforeAll`     | 用来修饰一个静态方法，该方法会在所有测试方法之前只执行一次。  | 初始化资源(准备工作） |
| `@AfterAll`      | 用来修饰一个静态方法，该方法会在所有测试方法之后只执行一次。  | 释放资源(清理工作） | 

1. JUnit单元测试的方法，是否可以声明形参?
- 可以，参数化测试
- @ParameterizedTest + @ValueSource
2. 如何实现在单元测试方法运行之前，做一些初始化操作？
- `@BeforeEach`、`@BeforeAll`
3. 如何实现在单元测试方法运行之后，释放对应的资源？
- `@AfterEach`、`@AfterAll` 

### 单元测试-Maven依赖范围
1. 在maven项目中，test目录存放单元测试的代码，是否可以在main目录中编写单元测试呢?
可以但是不推荐，不符合标准

依赖的jar包，默认情况下，可以在任何地方使用，可以通过<scope></scope>设置其作用范围
作用范围:
- 主程序范围有效.(main文件夹范围内)
- 测试程序范围有效.(test文件夹范围内)
- 是否参与打包运行(package指令范围内)

| scope值 | 主程序 | 测试程序 | 打包（运行） | 范例 |
| ---- | ---- | ---- | ---- | ---- |
| compile（默认） | Y | Y | Y | log4j |
| test | - | Y | - | junit |
| provided | Y | Y | - | servlet-api |
| runtime | - | Y | Y | jdbc驱动 | 

### Maven常见问题解决方式

依赖报红，一直下载一直失败
产生原因：由于网络问题，依赖没有下载完成导致的，在maven仓库中生成了xxx.lastUpdated文件，如果不删除就不会重新下载

解决方式:
1. 根据maven依赖的坐标,找到对应仓库的xxx.lastUpdated文件，删除，删除后重新加载项目
2. 通过命令`del /s *.lastUpdated`批量递归删除


## Web基础


### SpringBoot入门程序剖析
为什么一个main方法就把web应用启动了
起步依赖:
- spring-boot-starter-web: 包含了web应用开发所需要的常见依赖。
- spring-boot-starter-test: 包含了单元测试所需要的常见依赖。
- 官方提供的starter: [https://docs.spring.io/spring-boot/docs/3.1.3/reference/htmlsingle/#using.build-systems.starters](https://docs.spring.io/spring-boot/docs/3.1.3/reference/htmlsingle/#using.build-systems.starters) 


### HTTP协议

概念:Hyper Text Transfer Protocol,超文本传输协议，规定了浏览器和服务器之间数据传输的规则

特点:
1. 基于TCP协议：面向连接，安全
2. 基于请求-响应模型：一次请求对应一次响应
3. HTTP协议是无状态的协议：对于事务没有记忆能力，每次请求-响应都是独立的。
    - 缺点：多次请求不能共享数据
    - 优点：速度快


### HTTP请求协议


#### 请求数据格式

请求行：请求数据第一行（请求方式，资源路径，协议）
`GET /hello?str=Itheima HTTP/1.1`
请求头：第二行开始，格式key:value
`
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br, zstd
Accept-Language: en
Cache-Control: max-age=0
Connection: keep-alive
Host: localhost:8080
Sec-Fetch-Dest: document
Sec-Fetch-Mode: navigate
Sec-Fetch-Site: none
Sec-Fetch-User: ?1
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/135.0.0.0 Safari/537.36
sec-ch-ua: "Google Chrome";v="135", "Not-A.Brand";v="8", "Chromium";v="135"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
`

请求体：POST请求，存放请求参数

请求方式-GET:请求参数在请求行中，没有请求体，如localhost:8080/hello?str=xxxx，大小有限制
请求方式-POST:请求参数在请求体中，POST请求大小没有限制


Web 服务器 (Tomcat) 对 HTTP 协议的请求数据进行解析，并进行了封装 (HttpServletRequest), 在调用 Controlller 方
法的时候传递给了该方法。这样，就使得程序员不必直接对协办议进行操作，让 Web 开发更加便捷。




```java

package cloud.hexiaolei.demo;

import jakarta.servlet.http.HttpServletRequest;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class RequestController {

    @RequestMapping("/request")
    public String request(HttpServletRequest http) {
        //请求方式
        System.out.println("请求方式：" + http.getMethod());
        //获取请求的url地址
        System.out.println("请求的url地址："+http.getRequestURL().toString());
        System.out.println("请求的uri地址："+http.getRequestURI());
        //获取请求协议
        System.out.println("请求协议："+http.getProtocol());
        //获取请求参数
        System.out.println("请求参数name："+http.getParameter("name"));
        System.out.println("请求参数age："+http.getParameter("age"));
        //获取请求头
        System.out.println("请求头："+http.getHeader("Accept"));
        return "OK";
    }
}

```



控制台输出
请求方式：GET
请求的url地址：http://localhost:8080/request
请求的uri地址：/request
请求协议：HTTP/1.1
请求参数name：hexiaolei
请求参数age：18
请求头：text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7


1. **HTTP请求数据需要程序员自己解析吗？**
   - 不需要，web服务器负责对HTTP请求数据进行解析，并封装为了请求对象`HttpServltetRequest`。
2. **如何获取请求数据？**
   - HttpServletRequest对象里面封装了所有的请求信息。 


#### 响应数据格式

例如
```
HTTP/1.1 200
Content-Type: text/html;charset=UTF-8
Content-Length: 2
Date: Sat, 19 Apr 2025 07:13:48 GMT
Keep-Alive: timeout=60
Connection: keep-alive
```

响应头： 第一行协议，状态码，描述
响应头：第二行开始格式key：value
响应体：最后一部分，存放响应数据


[常见状态码](https://it-tools.tech/http-status-codes)

| 响应头字段 | 说明 |
| ---- | ---- |
| Content-Type | 响应内容类型  |
| Content-Length | 响应内容长度（字节数）  |
| Content-Encoding | 响应压缩算法  |
| Cache-Control | 客户端缓存策略指示  |
| Set-Cookie | 浏览器设置cookie指令  | 

响应数据设置
Web 服务器对 HTTP 协议的响应数据进行了封装 (HttpServletRespoonse), 并在调用 Controller 方法的时候传递给
了该方法，这样，就使得程序员不必直接对协议进行操作，让 Web 开发更加便捷



手动设置方式
1
```java
/**
     * 方式1: 通过HttpServletResponse设置响应信息
     * @param response
     * @throws IOException
     */

    @RequestMapping("/response")
    public void response(HttpServletResponse response) throws IOException {
        //设置响应状态码
        response.setStatus(HttpServletResponse.SC_NOT_FOUND);
        //设置响应头
        response.setHeader("Content-Type","text/html;charset=utf-8");
        //设置响应体
        response.getWriter().write("<h1>Fuck you</h1>");
    }


```

2.
```java
/**
     * 方式2: 通过ResponseEntity设置响应信息
     * @return
     */
    @RequestMapping("/response2")
    public ResponseEntity<String> response2(){
        return ResponseEntity.status(404).header("name","javaweb").body("<h1>Fuck you</h1>");
    }

```


开发web程序,完成用户列表渲染展示
