# FEmirror 云更新

`FEmirror 云更新` 是一个自动化更新平台,无需后端也可以完成 app 日常更新.

<img  :src="$withBase('/h2.png')" alt="foo">

## [访问网站](https://hotfix.femirror.com/)

## 使用指南

### 注册

使用`Github`授权登录.

### 上传更新包

点击左侧`点击/拖动上传升级包`按钮上传升级文件.

可以上传`apk`,`wgt`两种类型的文件.

文件上传成功后在`应用管理`列表中会出现您刚刚上传的更新包信息.

<img  :src="$withBase('/h3.png')" alt="foo">

### wgt 热更新的发布

点击`发布`按钮,如下图,提供几种参数供您选择.

<img :src="$withBase('/h1.png')" alt="foo">
#### 更新方式的选择

1.  静默更新 : 使用`checkUpdate`方法后检查更新,如果有更新会自动下载 app,整个过程没有任何提示,用户第二次打开 app 就会出现更新后的效果.
2.  提示更新 : 使用`checkUpdate`方法后检查更新,如果有则会弹出确认框,用户确认后会提示正在下载,正在安装,安装完成重启,更新完成等提示.

#### 更新平台的选择

如果只需要某一个平台更新,可以根据需求选择

| iphone 效果如下                                                  | 安卓效果如下                                                          |
| ---------------------------------------------------------------- | --------------------------------------------------------------------- |
| <img   width="380"  :src="$withBase('/IMG_0040.PNG')" alt="foo"> | <img   width="380"  :src="$withBase('/S80805-211149.jpg')" alt="foo"> |

### app 更新的发布

app 更新只适用于`安卓 apk` 类型,也就是下载更新包后执行安装.

### 关闭更新

在应用详情的右上角可以关闭更新,关闭更新后用户检查更新后不会作处理

## 常见问题

### 提示版本不一致

在调试热更新的时候必须使用自定义基座,否则得到的版本是 `Hbuilder H5+ App` 的版本.

### 更新替换

由于这种热更新是替换更新,新的热更新包如果有问题,可能导致 app 无法使用,请测试成功后再发布,或者您上传一个专用于测试的 app
