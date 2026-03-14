# 构建

windows 下构建注意换行符为 LF，而不是 CRLF

## git换行符

``` bash
git config --global core.autocrlf false
git config --show-origin --get-all core.autocrlf
```

## 获取当前代码

``` bash
git clone --recurse-submodules git@github.com:CaiJinHao/linuxdeploy-jinhao.git
```

## 复制文件

``` bash
  cp custom_env/include/bootstrap/ubuntu/* app/src/main/assets/env/include/bootstrap/ubuntu/
  cp custom_env/include/bootstrap/debian/debootstrap/scripts/* app/src/main/assets/env/include/bootstrap/debian/debootstrap/scripts/
```

## 配置环境变量

根目录创建local.properties

``` text
sdk.dir=D\:\\Android\\Sdk
```

## 构建apk

``` bash
# release 使用了debug 签名
.\gradlew.bat clean assembleRelease
```
