

<div class="outline">
[openGuidePage](#a1)

[openGuideVideo](#a2)

[openGuideRepeatVideo](#a2)
</div>

#**概述**

**概述**

guide 封装了首次下载或者是版本更新后启动应用时的导航页，模块自动记录是否为第一次启动，导航页分为视频、图片两大类。图片导航在最后一个页面点击立即体验会关闭导航页。视频导航仅支持格式为MP4格式，视频播放完后会自动关闭导航页，建议视频不要太大，时间不要太长（太长会影响用户体验效果，建议10s左右）。

## [实例widget下载地址](https://codeload.github.com/xiaoyang521style/guide/zip/master)

##**模块接口**
    
<div id="a1"></div>
#**openGuidePage**

打开图片导航

openGuidePage({params})

##params

imgs：

- 类型：数组
- 描述：导航图片（支持 widget:// fs:// 不支持相对路径）。

point_normal

- 类型：字符串
- 描述：（可选项）普通页面分页控件图片地址（widget:// fs:// 相对路径都是支持），尺寸图片建议30 × 30。

point_select

- 类型：字符串
- 描述：（可选项）当前页面分页控件数图片地址（widget:// fs:// 相对路径都是支持），尺寸图片建议30 × 30。

btnColor

- 类型：字符串
- 描述：（可选项）关闭按钮背景颜色(00FFFF)。

time

- 类型：字符串
- 描述：（可选项）导航页消失的时间，以秒为单位。

##代码示例

```js
var guide = api.require('guide');
guide.openGuidePage({
    imgs: ['widget://image/guide/load_1.jpg', 'widget://image/guide/load_2.jpg', 'widget://image/guide/load_3.jpg'],
    point_normal:'widget://image/guide/point_normal@2x.png',
    point_select:'widget://image/guide/point_select@2x.png',
    btnColor:'00FFFF',
    time:'2'
};
```
##可用性

iOS系统

可提供的1.0.0及更高版本

<div id="a2"></div>
#**openGuideVideo**

打开视频导航

openGuideVideo({params})

##params

path：

- 类型：字符串
- 描述：导航视频本地地址（widget:// fs:// 相对路径都是支持）。

time

- 类型：字符串
- 描述：（可选项）导航页消失的时间。

##代码示例

```js
var guide = api.require('guide');
guide.openGuidePage({
    path: 'widget://video/guide/video.mp4',
    time:'2'
};

##可用性

iOS系统

可提供的1.0.0及更高版本

<div id="a3"></div>
#**openGuideRepeatVideo**

打开循环视频导航

openGuideRepeatVideo({params})

##params

path：

- 类型：字符串
- 描述：导航视频本地地址（widget:// fs:// 相对路径都是支持）。

##代码示例

```js
var guide = api.require('guide');
    guide.openGuideRepeatVideo({
    path: 'widget://video/guide/video.mp4'
};

##可用性

iOS系统

可提供的1.0.0及更高版本




