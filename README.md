# TypograPy

## Purpose

For people used to code, formats like Markdown, Textile, AsciiDoc and all wiki-like tools are great when it comes to write. Furthermore, they bring an ease of editing previously unknown (e.g. write a sentence per line, and rearranging will be only easier).

However, if you are a bit into writing, you know those are not enough. Indeed, typography rules are numerous (well, depending on the language at least), and these formats rarely provide the tools to handle all this.

This projects aims at filling the gaps, by allowing the writer to design a set of rules for automatic replacements upon calling a command line.

## Roadmap

* [ ] Create a Python project (Typogra**Py**; will give me the opportunity to work a bit with that language)
* [ ] First version will be CLI only; if works well, a GUI should be studied
* [ ] Works with rule files:
  * The rule file contains:
    * rule name;
    * matching pattern;
    * replacement.
  * Default rule files come included with the application, but custom rule files can be created.
  * This implies creating an engine based on regular expressions, with both its flexiblity and its limitations.
* [ ] Run by providing a config file specifying:
  * the rule file to use
  * the rules to be active (all if nothing specified)
  * the files to typograpy (to run without argument; otherwise, the file(s) can be passed as command-line arguments)
* [ ] Offer a summary of replacements for user to confirm before they are made (kind of the interactive rebase of Git). An option should allow to bypass confirmation and always replace everything.

## Rules to implement

### French

(Replacements will be written `sed`-style when possible for concision)

* `s/ \s+/ /` (no double space)
* Use ellipses instead of `...`.
* Use French quotes (`«»`).
* Use unbreakable space before `?!;:` and so on.
* Begin sentences with an uppercase character (allow writer to use letters with accents and TypograPy move it to upper case, since having uppercase with accents is not always easy)
