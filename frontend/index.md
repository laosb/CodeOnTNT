# CodeOnTNT - 前端

![img](%E6%B6%82%E9%B8%A6_Screenshot_2018-11-22-19-39-06-540_1.jpg)

经过连续一段时间的摸索，本人倒腾出了一种可用的在 TNT 上进行前端开发的方式。

终端/基本工具环境：Termux
编辑器/文件树：cloudcmd（Emacs、Vim 亦可）

### 已知问题
- node-sass 因为 arm64 平台的限制无法在 Termux 中编译，因此项目不可依赖 node-sass。

## Getting Started

从 Play Store 安装 Termux。打开 Termux，它会自动安装基本 Linux 环境组件。之后安装一些基本工具：

```sh
pkg install git
pkg install node
pkg install yarn
pkg install g++ make python2 # 或 python，视依赖而定。部分依赖由于无 arm64 平台的二进制预编译文件可能需要编译，因此准备工具链。本命令可选。
```

然后安装 cloudcmd 和编辑器（高阶用户请忽略）：

```sh
yarn global add cloudcmd deepword
```

至此基本环境安装完毕，可以开始尝试项目了。用 git 克隆项目后按常规使用 yarn 或 npm 安装依赖，并启动调试服务器（通常是 yarn start / yarn serve/ yarn dev）。

Termux 上从左边缘右滑打开抽屉，选择 New Session 创建新的 Termux 会话，在会话中启动 cloudcmd 环境：

```sh
cloudcmd --root=. --editor=deepword
```

这会自动打开一个浏览器窗口，就是 cloudcmd 的环境。打开项目的调试服务器的页面，就可以一边看着预览一边开发了！

## 授权

CC-BY-NC-SA 4.0.
