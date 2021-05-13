# purewriter-desktop-liaronce-build
Pure Writer Desktop (LiarOnce Build) for other platform.

## 改动

从 1.x 开始纯纯写作的桌面版不再开源，从今天开始改为打包 AppImage 版本，目前该版本从 .deb 解包而来

## 打包

请确保系统为 Debian 系 Linux 发行版（如 Debian、Ubuntu 等，本配置文件在 Lubuntu 环境下测试通过）

```bash
# 安装相关依赖
sudo apt install -y python3-pip python3-setuptools patchelf desktop-file-utils libgdk-pixbuf2.0-dev fakeroot strace
sudo wget https://github.com/AppImage/AppImageKit/releases/download/continuous/appimagetool-x86_64.AppImage -O /usr/local/bin/appimagetool
sudo chmod +x /usr/local/bin/appimagetool

# 安装 appimage-builder
sudo pip3 install appimage-builder

# 获取仓库并开始打包
git clone https://github.com/LiarOnce/purewriter-desktop-liaronce-build
cd purewriter-desktop-liaronce-build
# 目前版本为 1.3.3，后续更新请修改为对应版本链接
curl -O https://github.com/PureWriter/desktop/releases/download/1.3.3/PureWriter-1.3.3-Linux-amd64.deb

# 如后续版本有更新，请修改 AppImageBuilder.yml 第 5 行和第 22 行的版本号（如 1.3.3） 为新版本号
# 进行打包
appimage-builder
```

## 作者原话

**纯纯写作桌面版本身完全免费、完全开源，它当前非常初级，只提供了双向实时同步编辑当前文章这个功能，甚至它可能对您来说完全不能用 ⚠️⚠️⚠️。如果您打算 仅仅 因为这个桌面版而付费，我强烈建议您重新考虑这件事情。**      --来源：[纯纯写作桌面版](https://writer.drakeet.com/desktop)

<details>
 <summary>过时内容</summary>

此处用于存放我个人编译版本，Drakeet 未提供的版本可以从此处获取。

此处的编译版本个人保证不会对程序本身进行任何修改（因为我不会 Java 和 Kotlin 啊，~~大二的时候学的也是 JavaScript~~）

目前我个人的修改可在此处查看：[查看记录](https://github.com/LiarOnce/desktop/commits/master)

## 目前提供的包

 - [Linux 64 Bit x86](https://purewriter.liaronce.com/#/linux86)（zip，如需 deb 或 AppImage 需自行解决）
 > 用于编译的系统环境：64-bit: Manjaro 20.0 Lysia (个人自用物理机)
 - [Windows 32 Bit](https://purewriter.liaronce.com/#/windowsx86)
 > 用于编译的系统环境：32-bit: Windows 7 Professional (虚拟机) (镜像: 7601.24540 Professional 7 SP1 x86 ZH-CN SM.iso)
 - [Single JAR file](https://purewriter.liaronce.com/#/jarfile)
 > 适用于任何 32-bit x86 系统，如 32 位 Linux 发行版以及 Windows 32 位，但该版本更干净
 
## 已知问题

由于种种原因（穷），未测试 Surface Pro X、Matebook E 2019 等搭载 Windows 10 ARM64 系统的设备是否可以正常运行。[issue#1](https://github.com/LiarOnce/purewriter-desktop-liaronce-build/issues/1)

## 更多

了解更多信息，请访问：[https://purewriter.liaronce.com](https://purewriter.liaronce.com)

捐赠：[https://purewriter.liaronce.com/#/donate](https://purewriter.liaronce.com/#/donate)
</details>
