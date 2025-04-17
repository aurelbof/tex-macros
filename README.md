To use these macros in your project, create a symbolic link to `tex-macros` in the same directory as your main `.tex` file:

```
ln -s PATH/TO/REPO/tex-macros ./tex-macros
```

Then you can \input any of the files, e.g.

```
\input{tex-macros/article-preamble}
\begin{document}
...
\end{document}
```

The tikz figures are designed to be either compiled as standalone files or included with `\include`, with an optional global variable `\scale` defined, e.g. `\def\scale{1.5}`.
This is automatically done by a locally defined function `\includetikz`, used like so:
```
\includetikz[scale=0.8]{poseidon}
```
It will automatically find `poseidon.tex` inside of `tex-macros/tikz-figures`.
