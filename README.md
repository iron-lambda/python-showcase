# python-showcase

![Language](https://img.shields.io/badge/language-Python-yellow)  [![English](https://img.shields.io/badge/lang-English-blue)](README.md) [![中文](https://img.shields.io/badge/lang-中文-red)](README.zh-CN.md)


A collection of Python scripts for learning and quick reference. Each example demonstrates a different practical use case.

## Scripts

### CodeyMining

Automates daily check-in and mining reward collection for the Codey BBS forum. Uses `requests` with session management, form hash extraction via regex, and cookie handling.

```bash
# Edit username and password in CodeyMining.py first
python3 CodeyMining.py
```

Can be scheduled with crontab for daily execution:

```
01 06 * * * python3 /path/to/CodeyMining.py
```

See [`codeymining/README.md`](codeymining/README.md) for details. Licensed under Apache 2.0.

### lcysign

Automates daily check-in for Liangchenyun (良辰云) to earn traffic quota. Logs in via email/password, checks sign-in status by parsing HTML, and performs the check-in if needed.

```bash
# Edit email and password in sign.py first
python3 sign.py
```

Can be scheduled with crontab for daily execution:

```
01 06 * * * python3 /path/to/sign.py
```

See [`lcysign/README.md`](lcysign/README.md) for details. Licensed under Apache 2.0.

### OSTEP Crawler

Batch downloads the Chinese-translated PDF files of [OSTEP (Operating Systems: Three Easy Pieces)](http://pages.cs.wisc.edu/~remzi/OSTEP/Chinese/) from the University of Wisconsin website.

```bash
cd ostepcrawler
python3 ostepcrawler.py
```

PDFs are saved as `00.pdf`, `01.pdf`, ... in the current directory.

## Requirements

- Python 3.x
- `requests` library (for CodeyMining and lcysign)
