# Pica Comic

[![flutter](https://img.shields.io/badge/flutter-3.27.1-blue)](https://flutter.dev/)
[![License](https://img.shields.io/github/license/Pacalini/PicaComic)](https://github.com/Pacalini/PicaComic/blob/master/LICENSE)
[![Download](https://img.shields.io/github/v/release/Pacalini/PicaComic)](https://github.com/Pacalini/PicaComic/releases)
[![stars](https://img.shields.io/github/stars/Pacalini/PicaComic)](https://github.com/Pacalini/PicaComic/stargazers)

A comic app with multiple sources built with flutter.

## 当前问题

flutter版本不兼容。预测使用的Flutter=3.27.1，Gradle=gradle-8.10.2-all，其它依赖未知
墨水屏版本需求：
- [] 低刷新甚至不刷新
- [] 滑动浏览模式改为翻页浏览
- [] 修改显示分辨率

## 本地编译过程（只包含Windows@AndroidStudio->Android）端
- 环境1 AS安装，使用版本24.1.2，插件包括Dart，Flutter，Gradle，均为最新版，AndroidSDK包括35/34/33/NDK25.1/，BuildTool35/34/33，CLI16.0，CMake4/USBdriver/SDK-PT
- Flutter=3.27.1，安装后修改两个文件换源，并运行`flutter doctor`和`flutter doctor --android-licenses`
- 环境变量，设置`GRADLE_USER_HOME`为和项目文件同盘符的文件夹，用于系统放置所有编译文件
- 环境变量，设置`GRADLE_HOME`为该版本gradle文件目录`*\gradle-8.10.2`
- 环境变量，`JAVA_HOME`为java17的母目录
- 环境变量，`PUB_CACHE`为和项目文件同盘符的文件夹
- AS打开项目，打开`pubspec.yaml`文件，`upgrade`依赖
- AS打开安卓子项目，修改app/build.gradle，版本号统一改为java1.8，自动下载依赖和编译，生成编译文件
- 生成后打开\pub_cache\hosted\pub.flutter-io.cn\shared_preferences_android-2.4.7\android\build.gradle，同样统一为java1.8
- 回到项目，连接设备，编译

**Forked from [nyne](https://github.com/wgh136), provide extended support & fix, no guaranteed roadmap.**

## Download

<a href="https://github.com/Pacalini/PicaComic/releases">
<img src="https://user-images.githubusercontent.com/69304392/148696068-0cfea65d-b18f-4685-82b5-329a330b1c0d.png"
alt="Get it on GitHub" align="center" height="80" /></a>

<a href="https://github.com/Pacalini/PicaComic/blob/master/INSTALL.md#obtainium">
<img src="https://github.com/ImranR98/Obtainium/blob/main/assets/graphics/badge_obtainium.png"
alt="Get it on Obtainium" align="center" height="54" />
</a>

An [AUR package](https://aur.archlinux.org/packages/pica-comic-bin) is packed by [Lilinzta](https://github.com/Lilinzta):
```shell
paru -S pica-comic-bin
```

## Build

1. Clone the repository
```shell
git clone https://github.com/Pacalini/PicaComic
```
2. Install flutter: https://docs.flutter.dev/get-started/install
3. Build Application: https://docs.flutter.dev/deployment

## Introduction

### Built-in Comic Source

Currently, Pica Comic has 5 built-in comic sources:
- picacg
- e-hentai/exhentai
- jmcomic
- hitomi
- htcomic
- nhentai

### Features

- Browse manga
- Online reading
- Download manga
- Manage local favorites and network favorites
- Data sync(using webdav)
- Reading history

### History

This project initially started as an unofficial app for picacg
and later evolved into an app that supports multiple comic sources.

## Thanks

### Projects
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=tonquer&repo=JMComic-qt)](https://github.com/tonquer/JMComic-qt)

The image restructuring algorithm used to display jm images is from this project.

### Tags Translation
[![Readme Card](https://github-readme-stats.vercel.app/api/pin/?username=EhTagTranslation&repo=Database)](https://github.com/EhTagTranslation/Database)

The Chinese translation of the manga tags is from this project.
