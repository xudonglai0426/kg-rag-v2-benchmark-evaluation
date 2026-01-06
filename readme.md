# KG-RAG-V2 Benchmark Evaluation

## Links
- apk: https://drive.google.com/drive/folders/1It1hX83IGIaGP12tV_kMwHVh-s3gVUMu?usp=sharing
- intention: https://drive.google.com/drive/folders/1ozPXt2nbKEPCQ8Zo4Hdb-WtsMawN0waI?usp=sharing
- android_automation: https://github.com/xudonglai0426/android_automation

## Notes
- android app 通过apk安装，harmony/ios直接在应用市场安装就行

## Harmony
#### Hdc
Harmony涉及hdc的安装（作用与adb一致）

下载地址：https://developer.huawei.com/consumer/cn/download/  安装Command Line Tools 6.0.1 Release

之后配置环境变量 export PATH=$PATH:/Users/xudonglai/Desktop/command-line-tools/sdk/default/openharmony/toolchains（可参考：https://developer.huawei.com/consumer/cn/doc/harmonyos-guides/hdc ）

安装成功的标志是，连接Harmony手机的情况下，在terminal运行 hdc list targets 显示对应手机的sn号
```python
(base) xudonglai@xudonglaideMacBook-Air ~ % hdc list targets
9CN0223B01031784
```

## Android
#### Apk
包含所有需要的android app的apk安装包
https://drive.google.com/drive/folders/1p-mkBJfkHjhZYqziaU5YYDhSoGCqHnRJ?usp=sharing

在虚拟机上，在terminal可通过adb install /Users/name/Downloads/xxx.apk (具体apk路径) 直接安装

#### Android studio/Adb

需要安装Android studio以及adb，以使用安卓虚拟机

Android Studio: https://developer.android.com/studio?hl=zh-cn

一直点击next，应该会自动安装adb，第一次安装耗时会久一些（安装中如果有问题，可以直接搜索/gpt，相关内容很多）

安装成功后，Android Studio → More Actions → Virtual Device Manager
<div align="center">
  <img src="android_studio_fig_1.png"/>
</div>

在里边添加新的模拟机，选择 Pixel 6机型
<div align="center">
  <img src="android_studio_fig_2.png"/>
</div>

添加成功后，对应的device name会显示在界面上
<div align="center">
  <img src="android_studio_fig_3.png"/>
</div>


启动虚拟机，所有一切都安装成功的标志就是，在terminal运行 adb devices 命令时，显示对应的虚拟机的id（证明adb可以正常连接到手机并使用）
```python
List of devices attached
emulator-5554   device
```

## IOS

## XnViewMP（用于bounding box标注）

Windows/Mac系统都可以下载安装XnViewMP，用免费版即可

用XnViewMP打开图片，移动光标就可以在右下角找到对应X,Y坐标，作为bounding box数据记录

<div align="center">
<p align="center">
  <img src="figure1.png"/>
</p>
</div>

