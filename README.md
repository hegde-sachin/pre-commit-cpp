# pre-commit-cpp

This is a set of git [pre-commit framework](https://pre-commit.com/) hooks for C/C++ language. The hooks provided are:

* [cpplint](https://github.com/cpplint/cpplint): style-error detector (or linter) for [Google C++ Style Guide](http://google.github.io/styleguide/cppguide.html)
* [cppcheck](http://cppcheck.sourceforge.net/): static analyzer for C/C++ code

## Prerequisites

1. Install pre-commit framework if you haven't done it already.  For more 
information please read
[https://pre-commit.com/#install](https://pre-commit.com/#install).
2. Create `.pre-commit-config.yaml` under the root of your git repository if you
don't have one.  For more information please read
[https://pre-commit.com/#plugins](https://pre-commit.com/#plugins).
3. Install pre-commit into your git hooks if you haven't done it already. For 
more information please read 
[https://pre-commit.com/#usage](https://pre-commit.com/#usage).
4. cppcheck hook in pre-commit-cpp requires `cppcheck` executable, which is 
available for macOS, Linux and Microsoft Windows. You can download it from its 
official site: 
[http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/).

## C/C++ Hook Installation

To use the C/C++ hooks, add the following YAML code-block to your 
`.pre-commit-config.yaml`:

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: 0.5.0      # use the most recent version
  hooks:
  - id: cpplint   # linter for Google C++ Style Guide
  - id: cppcheck  # static analyzer for C/C++ code
```

You don't need to use all the hooks together, i.e.
add hooks that you want to use.

And remember, YAML is indentation sensitive: make sure `.pre-commit-config.yaml` 
uses the same number of whitespaces for indentation level after adding the
above code block.

## Usage

Each time you commit to the git repository, the hooks will run automatically. :-)

## References

* [https://pre-commit.com/](https://pre-commit.com/)
* [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
