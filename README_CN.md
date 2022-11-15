# nonestrap

另一个 NoneBot2 项目引导工具。

## 安装

通过以下命令安装 nonestrap：

```console
pip install nonestrap
```

## 用法

```console
# 使用 onebot-v11 适配器将引导文件和虚拟环境安装到 ./mybot/ 中，不使用任何额外插件。
nonestrap -a onebot-v11 mybot

# 使用 onebot-v11 和 ding 适配器将引导文件和虚拟环境安装到 ./mybot/ 中并配置 APScheduler
nonestrap -a onebot-v11 -a ding mybot nonebot-plugin-apscheduler

# 与第一个相同，但使用生产环境 .env 文件。
nonestrap -a onebot-v11 -e prod mybot

# 与第一个相同，但不创建新的虚拟环境。
# 如果您已经准备了虚拟环境，请使用这个。
nonestrap -a onebot-v11 -V mybot

# 如果您想给嵌入式 Python 使用 nonestrap，请使用这个。
# 在此之前请先将 pip 和 setuptools 安装到 Lib/site-packages，
# 并且修改 pth 导入控制文件。
pip install -t Lib/site-packages pip setuptools
nonestrap -a onebot-v11 -VE python.exe mybot
```
