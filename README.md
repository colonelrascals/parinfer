# Parinfer [![Build Status](https://travis-ci.org/shaunlebron/parinfer.svg?branch=master)](https://travis-ci.org/shaunlebron/parinfer)

This is an experiment that tries to demonstrate a possible replacement for
[paredit] as a simpler and more natural way to write Lisp code.

[paredit]:http://danmidwood.com/content/2014/11/21/animated-paredit.html

## Formatter

| File  | Description  | Details | Tests |
|------:|:-------------|---------|-------|
| [`reader.cljc`] | clojure reader for tracking parens and token states |  |  |
| [`infer.cljc`] | infers parens based on indentation | [details][infer-details] | [tests][infer-tests] |
| [`prep.cljc`] | preps file by correcting indentation based on parens | [details][prep-details] | [tests][prep-tests] |

Run tests with:

```
lein cljsbuild test
```

[`reader.cljc`]:src/parinfer/format/reader.cljc
[`infer.cljc`]:src/parinfer/format/infer.cljc
[`prep.cljc`]:src/parinfer/format/prep.cljc

[overview]:doc/overview.md
[prep-details]:doc/prep-details.md
[prep-tests]:doc/prep-tests.md
[infer-details]:doc/infer-details.md
[infer-tests]:doc/infer-tests.md

## Presentation Page (w/ CodeMirror)

| File  | Description  |
|------:|:-------------|
| [`core.cljs`] | entry point |
| [`editor.cljs`] | glues formatter to CodeMirror |
| [`state.cljs`] | state of each editor |
| [`vcr.cljs`] | editor recording and playback |
| [`vcr_data.cljs`] | editor animation data |

[`core.cljs`]:src/parinfer/core.cljs
[`editor.cljs`]:src/parinfer/editor.cljs
[`state.cljs`]:src/parinfer/state.cljs
[`vcr.cljs`]:src/parinfer/vcr.cljs
[`vcr_data.cljs`]:src/parinfer/vcr_data.cljs

## Running

```
lein figwheel dev
open http://localhost:3449
```
