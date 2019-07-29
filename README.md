# pre-commit-cpp

This is a set of git [pre-commit framework](https://pre-commit.com/) hooks for
C/C++ language. The hooks provided are:

* [clang-format](https://clang.llvm.org): formatter of C/C++ code based on a
style guide (Google, LLVM, Mozilla, Webkit, and Chromium available)
* [cpplint](https://github.com/cpplint/cpplint): linter
(or style-error detector) for
[Google C++ Style Guide](http://google.github.io/styleguide/cppguide.html)
* [cppcheck](http://cppcheck.sourceforge.net/): static analyzer of C/C++ code

These hooks require pre-commit framework to be installed on your system
and configured for each git repository. For more information please refer to

* [pre-commit installation](https://pre-commit.com/#install)
* [pre-commit plugins](https://pre-commit.com/#plugins) (`.pre-commit-config.yaml`)
* [pre-commit usage](https://pre-commit.com/#usage)
* [pre-commit hook list](https://pre-commit.com/hooks.html)

## C/C++ Hook Prerequisites

1. clang-format hook in pre-commit-cpp requires `clang-format` executable, which
is available for macOS, Linux and Microsoft Windows. Use brew (on macOS) or apt
(on Ubuntu) can install it. For Windows, please read
[http://releases.llvm.org/download.html](http://releases.llvm.org/download.html)
2. cppcheck hook in pre-commit-cpp requires `cppcheck` executable, which is
available for macOS, Linux and Microsoft Windows. Use brew (on macOS) or apt (on
Ubuntu) to install it. For Windows, please read
[http://cppcheck.sourceforge.net/#download](http://cppcheck.sourceforge.net/#download).

## C/C++ Hook Installation

To use the C/C++ hooks, add the following YAML code block to your
`.pre-commit-config.yaml`:

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: 0.6.0          # use the most recent version
  hooks:
  - id: clang-format  # formatter of C/C++ code based on a style guide (Google, LLVM, Mozilla, Webkit, and Chromium available)
  - id: cpplint       # linter (or style-error checker) for Google C++ Style Guide
  - id: cppcheck      # static analyzer of C/C++ code
```

You don't need to use all the hooks together, i.e. add only the ones that you
need.

And remember, YAML is indentation sensitive: make sure `.pre-commit-config.yaml`
use the same number of whitespaces for indentation after adding the above code
block.

## Usage

Each time you commit to the git repository, the hooks will run automatically.
:-)

## References

* [https://pre-commit.com/](https://pre-commit.com/)
* [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
* [https://clang.llvm.org/docs/ClangFormat.html](https://clang.llvm.org/docs/ClangFormat.html)
* [https://github.com/cpplint/cpplint](https://github.com/cpplint/cpplint)
* [http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/)
