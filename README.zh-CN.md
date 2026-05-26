# python-showcase

[English](README.md) | [中文](README.zh-CN.md)

Python 脚本合集，用于学习和快速参考。每个示例演示不同的实际应用场景。

## 脚本列表

### CodeyMining

自动完成 Codey 论坛的每日签到和矿场收益领取。使用 `requests` 进行会话管理，通过正则提取 form hash，并自动处理 cookie。

```bash
# 先在 CodeyMining.py 中修改用户名和密码
python3 CodeyMining.py
```

可通过 crontab 设置每日定时执行：

```
01 06 * * * python3 /path/to/CodeyMining.py
```

详见 [`codeymining/README.md`](codeymining/README.md)。采用 Apache 2.0 许可证。

### lcysign

自动完成良辰云每日签到以获取流量配额。通过邮箱和密码登录，解析 HTML 判断签到状态，未签到则自动执行签到。

```bash
# 先在 sign.py 中修改邮箱和密码
python3 sign.py
```

可通过 crontab 设置每日定时执行：

```
01 06 * * * python3 /path/to/sign.py
```

详见 [`lcysign/README.md`](lcysign/README.md)。采用 Apache 2.0 许可证。

### OSTEP Crawler

批量下载 [OSTEP（Operating Systems: Three Easy Pieces）](http://pages.cs.wisc.edu/~remzi/OSTEP/Chinese/) 中文翻译版 PDF 文件。

```bash
cd ostepcrawler
python3 ostepcrawler.py
```

PDF 文件以 `00.pdf`、`01.pdf`、... 的命名保存在当前目录。

## 环境要求

- Python 3.x
- `requests` 库（用于 CodeyMining 和 lcysign）
