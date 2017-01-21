[`rstcheck`](https://github.com/myint/rstcheck) is a tool that checks the
syntax of code blocks nested within reStructuredText. Currently, the Sphinx
support in `rstcheck` is minimal. This results in
[false positives](https://github.com/myint/rstcheck/issues/19).

It would be interesting to experiment with an alternative `rstcheck` mode that
uses `sphinx-build` instead of `docutils` directly. This would allow `rstcheck`
to parse Sphinx documents exactly the same way Sphinx does.

* `rstcheck` = `docutils` + code block linting
* `rstcheck-sphinx` = `sphinx-build` + code block linting

#### Milestones

##### GSOC 2017 CODING STARTS

* Be familiar what `rstcheck` does and how it does it.
* Be familiar with how to extend Sphinx. Particularly, learn how to parse code
  blocks.

##### GSOC 2017 MIDTERM

* Create a new front end, `rstcheck-sphinx` with first class Sphinx support.
  It should use the `sphinx-build` infrastructure to parse the code.
* Support parsing code blocks using this new `sphinx-build` based front end.
  And use the existing `rstcheck` checkers to lint the code blocks.
* Write unit tests to demonstrate the above functionality.

##### GSOC 2017 FINAL

* Write scripts to automatically test against existing Sphinx projects to check
  for false positives in `rstcheck-sphinx`.
* Integrate with the main `rstcheck` script if appropriate.
* Add additional linting support if time permits. This could involve linting
  more kinds of languages in code blocks. Or it could involve making the
  language support more extendable.
* Integrate with `coala` in the same way the main `rstcheck` script is
  integrated.