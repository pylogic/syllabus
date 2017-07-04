# pep8

标签（空格分隔）： 未分类

---
**install (2 ways):**

    pip install pep8
    sudo apt-get install pep8

**check:**

    pep8 --first test.py
    pep8 --show-source --show-pep8 test.py

**write test program(CodeStyle.py):**

    import pep8
    python_code_style_checker = pep8.Checker('test.py', show_source=True)
    file_errors = python_code_style_checker.check_all()
    print("Found %s errors (and warnings)" % file_errors)

**help:**

    pep8 -h


----------


***reference:***
[PEP8 Python 编码规范][1]

***tool:***
[PEP8 online][2]


  [1]: http://www.jianshu.com/p/52f4416c267d
  [2]: http://pep8online.com/