# pre-commit-cpp

This is a set of git [pre-commit framework](https://pre-commit.com/) hooks for C/C++ language. The hooks provided are:

* [cpplint](https://github.com/cpplint/cpplint): A style-error detector (or linter) for [Google C++ Style Guide](http://google.github.io/styleguide/cppguide.html)
* [cppcheck](http://cppcheck.sourceforge.net/): A static analyzer for C/C++ code

## Installation

### Prerequisites

Install pre-commit framework if you haven't done it already. (Please read [https://pre-commit.com/#install](https://pre-commit.com/#install) for more information.)

Change to your git repository and create `.pre-commit-config.yaml` under the root of the repository. (Please read
[https://pre-commit.com/#plugins](https://pre-commit.com/#plugins) for more information.)

Then install pre-commit into your git hooks. (Please read [https://pre-commit.com/#usage](https://pre-commit.com/#usage) for more information.)

### C/C++ hooks

To use the C/C++ hooks, add the following YAML code-block to your `.pre-commit-config.yaml`:

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: master
  hooks:
  - id: cpplint   # a linter for Google C++ Style Guide
  - id: cppcheck  # a static analyzer for C/C++ code
```

Of course, you don't need to use all the hooks together.
And remember, YAML (i.e. `.pre-commit-config.yaml`) is indentation sensitive.

## External tools

### cpplint

`cpplint` hook requires [cpplint](https://pypi.org/project/cpplint/) Python package, which in turn requires Python.  Once Python is installed on your system, cpplint package will be taken care of.

The installation method of Python can be found here: [https://docs.python-guide.org/starting/installation/](https://docs.python-guide.org/starting/installation/).

### cppcheck

`cppcheck` hook requires cppcheck executable, which is available for macOS, Linux and Microsoft Windows. You can download cppcheck from its official site: [http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/).

## References

* [https://pre-commit.com/](https://pre-commit.com/)
* [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
