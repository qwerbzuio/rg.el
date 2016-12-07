# rg.el

[![License GPL 3](https://img.shields.io/badge/license-GPL_3-green.svg?style=flat)](LICENSE)

Use [ripgrep](https://github.com/BurntSushi/ripgrep) in Emacs.

Ripgrep is a replacement for both grep like (search one file) and ag
like (search many files) tools. It's fast and versatile and written in
Rust. For some introduction and benchmarks, see
[ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}](http://blog.burntsushi.net/ripgrep/).

This package let you run ``ripgrep`` like ``grep`` from within Emacs.

## Usage

Invoke by <kbd>M-x rg</kbd>. This works the same way as <kbd>M-x rgrep</kbd>,
i.e. you get an interactive prompt to enter search details. Universal
argument can be used as for ``rgrep``.

## Customize

[ripgrep](https://github.com/BurntSushi/ripgrep) has its own builtin
mappings from type names to file name patterns that can be selected
from rg.el on invocation of ``rg``.
It's also possible to add custom patterns by customizing
``rg-custom-type-flags``.

```el
(setq rg-custom-type-flags
  '(("foo" .    "*.foo *.bar")
    ("baz" .    "*.baz *.qux")))
```

## License

See [LICENSE](LICENSE).
