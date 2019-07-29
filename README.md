# pre-commit-cpp

This is a set of git [pre-commit framework](https://pre-commit.com/) hooks for C/C++ language. The hooks provided are:

* [cpplint](https://github.com/cpplint/cpplint): style-error detector (or linter) for [Google C++ Style Guide](http://google.github.io/styleguide/cppguide.html)
* [cppcheck](http://cppcheck.sourceforge.net/): static analyzer for C/C++ code

## Prerequisites

1. Install pre-commit framework if you haven't done it already. 
(Read [https://pre-commit.com/#install](https://pre-commit.com/#install) for more.)
2. Create `.pre-commit-config.yaml` under the root of your git repository.
(Read [https://pre-commit.com/#plugins](https://pre-commit.com/#plugins) for more.)
3. Install pre-commit into your git hooks. 
(Read [https://pre-commit.com/#usage](https://pre-commit.com/#usage) for more.)
4. Install `cppcheck`, which is available for macOS, Linux and Microsoft Windows. 
You can download cppcheck from its official site: 
[http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/).

## C/C++ Hook Installation

To use the C/C++ hooks, add the following YAML code-block to your `.pre-commit-config.yaml`:

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: 0.5.0
  hooks:
  - id: cpplint   # linter for Google C++ Style Guide
  - id: cppcheck  # static analyzer for C/C++ code
```

Of course, you don't need to use all the hooks together, i.e.
you only add hooks that you want to use.

Remember, YAML is indentation sensitive: use the same number of whitespaces for 
each indentation level.

## Usage

Each time you commit to the git repository, the hooks will run automatically. :-)

## References

* [https://pre-commit.com/](https://pre-commit.com/)
* [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
