<div align=center>
<img width=64 src="resources/delegateui_icon.svg">

# 「 DelegateUI 」 Modern UI for Qml 

Ant Design component library for Qt Qml

If you need Qt5 impl [DelegateUI for Qt5](https://github.com/mengps/QmlControls)

</div>

<div align=center>

![win-badge] ![linux-badge] [![Issues][issues-image]][issues-url] [![QQGroup][qqgroup-image]][qqgroup-url]

English | [中文](./README-zh_CN.md)

</div>

[win-badge]: https://img.shields.io/badge/Windows-passing-brightgreen?style=flat-square
[linux-badge]: https://img.shields.io/badge/Linux-passing-brightgreen?style=flat-square

[issues-image]: https://flat.badgen.net/github/label-issues/mengps/DelegateUI/open
[issues-url]: https://github.com/mengps/DelegateUI/issues

[qqgroup-image]: https://img.shields.io/badge/QQGroup-490328047-f74658?style=flat-square
[qqgroup-url]: https://qm.qq.com/q/cMNHn2tWeY

<div align=center>

## 🌈 Gallery Preview

<img width=800 height=500 src="preview/light.png">
<img width=800 height=500 src="preview/dark.png">
<img width=800 height=500 src="preview/doc.png">

</div>

## ✨ Features

- 📦 A set of high-quality Qml components out of the box.
- 🎨 Powerful theme customization system.
- 💻 Based on Qml, completely cross platform.

## 🗺️ Roadmap

The development plan can be found here: [Component Roadmap](https://github.com/mengps/DelegateUI/discussions/5).

Anyone can discuss through issues, QQ groups, or WeChat groups, and ultimately meaningful components/functions will be added to the development plan.

## 🔨 How to Build

- Clone
```auto
git clone --recursive https://github.com/mengps/DelegateUI.git
```
- Build
```cmake
cd DelegateUI
cmake -S . -B build 
cmake --build build --config Release --target all --parallel
```
By default, the `plugin` will be builded in the `[QtDir]/[QtVersion]/[Kit]/qml/DeleagetUI` directory.

- Install
```cmake
cmake --install --prefix <install_dir>
```
The installation directory structure
```auto
──<install_dir>
    ├─include
    │   *.h
    ├─bin
    │   *.dll/so
    ├─lib
    │   *.lib
    └─imports
        └─DeleagetUI
```
- Usage
  - Link the `<install_dir>/lib`.
  - Include the `<install_dir>/include`.
  - Copy the `<install_dir>/bin/DeleagetUI.[dll/so]` to `[QtDir]/[QtVersion]/[Kit]/bin`.
  - Copy the `<install_dir>/imports/DeleagetUI` to `[QtDir]/[QtVersion]/[Kit]/qml`.

## 📦 Get started 

 - Create QtQuick application `QtVersion >= 6.5`
 - Add the following cmake command to your project `CMakeLists.txt`
 ```cmake
  target_include_directories(<your_target> PRIVATE DelegateUI/include)
  target_link_directories(<your_target> PRIVATE DelegateUI/lib)
  target_link_libraries(<your_target> PRIVATE DelegateUI)
 ```
 - Add the following code to your `main.cpp`
 ```cpp
  #include "delapp.h"

  int main(int argc, char *argv[])
  {
      ...
      QQuickWindow::setGraphicsApi(QSGRendererInterface::OpenGL);
      QQuickWindow::setDefaultAlphaBuffer(true);
      ...
      QGuiApplication app(argc, argv);
      QQmlApplicationEngine engine;
      DelApp::initialize(&engine);
      ...
  }
 ```
- Add the following code to your `.qml`
 ```qml
  import DelegateUI
  DelWindow { 
    ...
  }
 ```
 Alright, you can now enjoy using DelegateUI.

## 🚩 Reference

- Ant-d Components: https://ant-design.antgroup.com/components/overview
- Ant Design: https://ant-design.antgroup.com/docs/spec/introduce

## 💓 LICENSE

Use `MIT LICENSE`

## 🌇 Environment

Windows 11 / Ubuntu 24.04.2, Qt Version >= 6.7

## 🎉 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=mengps/DelegateUI&type=Date)](https://star-history.com/#mengps/DelegateUI&Date)