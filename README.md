# pre-commit-cpp

This is a set of git [pre-commit framework](https://pre-commit.com/) hooks for C/C++ language. The hooks provided are:

* [cpplint](https://github.com/cpplint/cpplint): style-error detector (or linter) for [Google C++ Style Guide](http://google.github.io/styleguide/cppguide.html)
* [cppcheck](http://cppcheck.sourceforge.net/): static analyzer for C/C++ code

## Installation

### Prerequisites

1. Install pre-commit framework if you haven't done it already. 
2. (Read [https://pre-commit.com/#install](https://pre-commit.com/#install) for more.)

Create `.pre-commit-config.yaml` under the root of your git repository. (Read
[https://pre-commit.com/#plugins](https://pre-commit.com/#plugins) for more.)

Then install pre-commit into your git hooks. (Read [https://pre-commit.com/#usage](https://pre-commit.com/#usage) for more.)

### Python and cpplint

`cpplint` hook requires [cpplint](https://pypi.org/project/cpplint/) Python package, which in turn requires Python.  Once Python is installed on your system, cpplint package will be taken care of.
The installation method of Python can be found here: [https://docs.python-guide.org/starting/installation/](https://docs.python-guide.org/starting/installation/).

### cppcheck

`cppcheck` hook requires cppcheck executable, which is available for macOS, Linux and Microsoft Windows. You can download cppcheck from its official site: [http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/).

### C/C++ hooks

To use the C/C++ hooks, add the following YAML code-block to your `.pre-commit-config.yaml`:

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: master
  hooks:
  - id: cpplint   # linter for Google C++ Style Guide
  - id: cppcheck  # static analyzer for C/C++ code
```

Of course, you don't need to use all the hooks together.
And remember, YAML is indentation sensitive: use the same number of whitespaces for indentation level.

## Usage

Each time you commit to the git repository, the hooks will run automatically. :-)

## References

* [https://pre-commit.com/](https://pre-commit.com/)
* [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
