Converting readme.md into a website
===================================
Windows 10
----------

`shell`
```shell
$ cd project
$ python -m venv sphinx-env
$ sphinx-env\Scripts\activate.bat
(sphinx-env) $ python -m pip install -U pip
(sphinx-env) $ python -m pip install sphinx
(sphinx-env) $ python -m pip install sphinx_rtd_theme
(sphinx-env) $ python -m pip install myst_parser
```

`conf.py`
```
extensions = [ 
  'sphinx.ext.intersphinx',
  'myst_parser',
]

html_theme = 'sphinx_rtd_theme'
```

Rename source/index.rst to source/index.md, copy the contents of your readme.md into this file or link toctree as you need.


`shell`
```shell
(sphinx-env) $ make html
``` 

**Important!** 

If using GH-Pages, make sure to create a .nojekyll file. Otherwise your css/js will not work! 