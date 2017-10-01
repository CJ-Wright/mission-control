# Notes for using rever
Rever is a very powerful versioning and release tool. Like all good tools there are procedures to maximizing your productivity.

1. You will need to install `rever` (use `conda`)
1. You will need a `rever.xsh` file. (see this dir for an example)
1. You will need to change the docs `conf.py` to use the version by importing it from the top most `__init__.py` file.
1. Always commit all changes before versioning/tagging the code, since rever will commit any changes. While rever can undo the changes it makes all non version changes will be lost upon a rever undo!
1. You can undo a rever command by `rever $version -u command1,command2`
1. You will need to insert a `__version_=='a.b.c'` in the top most `__init__.py` file.
```python
# The short X.Y version.
version = REVER_VERSION.rsplit('.',1)[0]

# The full version, including alpha/beta/rc tags.
release = REVER_VERSION
```