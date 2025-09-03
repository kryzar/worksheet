# Worksheet

LaTeX template for the UCalgary Math211 weekly worksheets. Work in progress.

## Basics

See the [example.tex](/example/example.tex) as an example, and the resulting
PDF files [example.pdf](/example/example.pdf) and
[example.SOLUTIONS.pdf](/example/example.SOLUTIONS.pdf).

## Automatic compilation

The script [`worksheet`](/worksheet) will automatically compile two versions of your
worksheet: one with, and one without solutions. For example:

```
worksheet my_worksheet.tex
```

will create the two following files:
```
my_worksheet.pdf
my_worksheet.SOLUTIONS.pdf
```

> [!NOTE]  
> Compilation happens in a single working directory in `/tmp` dedicated solely
> to the input file. With that, and the use of `latexmk`, the file is compiled
> only if it has been modified.

> [!WARNING]  
> Might not work for Windows.

If you can't use that, simply add or remove the `solution` option to the
document class.

## TODO

Here are some things that should be done:

- Add default values for `coursename`, etc.
- A `questions` (resp. `answers`) environment in an `exercise` (resp.
  `solution`) environment, without preliminary text, looks ugly.
- Add a general environment `comment` without counter for general comments in a
  solution.
- Add a point after the `question` (resp. `answer`) counter. (This sounds easy,
  but with the use of `csname`, I always get a whitespace. I assume an
  `\hspace` with a well chosen value would do the trick...)
