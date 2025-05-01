---
title: "模型替身"
upstreamCommit: eeb79828b79a3f4298f892c061142e2ab0871b3c
---

# 模型替身
## 什么是模型替身
模型替身是你模型的替身。 他将在别的玩家因为某些原因看不到你的原模型时出现。譬如你的模型是PC端的但是你的朋友正在使用Quest端时。一般来说, 你的朋友会看到你的备用模型或者机器人模型,创建模型替身将使你保持你原来的外观。

## 创建模型替身
你只能为你[拥有或者是已上传](/creators.vrchat.com/avatars/creating-your-first-avatar)的模型创建模型替身,模型替身目前只支持人形模型。

创建你的第一个模型替身:

1. 登录vrchat网页。

2. 转到"Avatars", 然后点击"My Avatars", 然后点击你想要创建模型替身的模型的名称或图标。

3. 点击"Generate Impostors"/"Regenerate Impostors"(当这个模型已经有替身但是你打算更新时)
4. 稍等片刻

5. 刷新页面, 过一段时间之后你就能看到你的模型成功创建了适配PC/Quest平台的替身。

![image](/creators.vrchat.com/images/avatars/impostors/generation.png)

 你可以打开或者关闭模型替身. 关闭时，将展示你的备用模型.


## 预览模型替身
创建了模型替身后, 你可能会迫不及待的想要看到它长啥样。

1. 登录VRChat。

2. 通过主菜单打开模型菜单。

3. 点击你创建了替身的模型。

4. 你应该注意到模型的"特性"栏现在包括了"模型替身"。 

![image](/creators.vrchat.com/images/avatars/impostors/features-row.png)

你应该也能看到一个在模型预览下面的新按钮，允许你在模型替身和一般模型的预览中切换。



::: info 笔记
**在菜单里展示的模型替身可能会有一些其他玩家看不到的bug**
:::
![image](/creators.vrchat.com/images/avatars/impostors/preview-avatar.png)
![image](/creators.vrchat.com/images/avatars/impostors/preview-impostor.png)

## 自定义模型替身
模型替身的默认效果就很不错了, 但是复杂的模型可能会从使用VRChat SDK自定义中受益。

在上传前将VRCImpostorSettings脚本加到你的模型上来自定义模型替身。

## VRCImpostorSettings(VRC模型替身设置)

### 分辨率缩放
调整该身体部位在替身纹理图集中占用的空间比例。

例如：将此脚本放置在头部骨骼时，可通过调整该值控制头部在图集中的占比，从而提升或降低该部位的纹理质量。注意调整可能导致图集中其他身体部位的占比被压缩。

_该设置基于VRCImpostorSettings脚本所绑定的骨骼生效。_



### 需忽略的变换
在替身数据采集时忽略指定的变换节点。这些变换将在最终结果中被隐藏。

_该设置独立于VRCImpostorSettings脚本所绑定的骨骼生效。_

### 额外子级变换
适用于翅膀、尾巴等部位。启用后将为当前脚本所在的骨骼生成独立子画面。

不建议对手指等细小部位使用此功能，因为所有子画面共享同一纹理图集。启用可能降低其他部位的纹理质量。

_该设置独立于VRCImpostorSettings脚本所绑定的骨骼生效。_

### 重新设置父级
将其他骨骼设置为当前替身子画面的子级。该骨骼将与当前身体部位共同进行替身化处理，成为子画面的一部分。

例如：若希望翅膀成为上半身的一部分，可使用此功能在替身化过程中将翅膀根部骨骼重新父级到胸部骨骼。

_该设置基于VRCImpostorSettings脚本所绑定的骨骼生效。_

## 什么时候会看到模型替身?
目前, 只有三种情况会看到模型替身:

- 模型预览界面

- 性能阻止 (例如，模型等级是"very poor"但是你将性能限制开到了"medium")

- 平台不匹配 (例如，模型是PC模型, 但是你在玩Quest平台)


::: info 信息
**自动生成模型替身和对非人形模型的支持将在未来推送！**
:::