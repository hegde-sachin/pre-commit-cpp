# pre-commit-cpp

pre-commit framework hook for C/C++ language

## Hooks

```yaml
- repo: https://gitlab.com/daverona-env/pre-commit-cpp
  rev: 1.0.0
  hooks:
  - id: cpplint
  - id: cppcheck
```

## External tools

<!--
### clang-format

```bash
brew install clang-format
```
-->

### cppcheck

The installation method for macOS, Linux and Microsoft Windows is explained on its official site: [http://cppcheck.sourceforge.net/](http://cppcheck.sourceforge.net/).

<!--
### oclint

```bash
brew install oclint
```

The installation method for Linux is described on its official site: [http://docs.oclint.org/en/stable/intro/installation.html](http://docs.oclint.org/en/stable/intro/installation.html),
-->

## References

* [https://github.com/caramelomartins/awesome-linters#cc](https://github.com/caramelomartins/awesome-linters#cc)
