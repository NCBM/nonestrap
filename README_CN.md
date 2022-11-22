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

# 与第一个类似，但使用生产环境 .env 文件。
nonestrap -a onebot-v11 -e prod mybot

# 与第一个类似，但不创建新的虚拟环境。
# 如果您已经准备了虚拟环境，请使用这个。
nonestrap -a onebot-v11 -V mybot

# 与第一个类似，但保留 bot.py 而非 bot.pyc。
nonestrap -a onebot-v11 -C mybot
```
