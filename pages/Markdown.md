## Markdown

So far we've only talked about code cells, but there are other kinds of cells as well. The main other kind of cell you should know about is **markdown**. This cell is actually a markdown cell. You can double click it to see and edit the raw markdown, then run the cell again to see the markdown rendered.

When you're using notebooks to write reports, you want to be able to include prose that isn't very appropriate for code comments. Markdown is useful for this.

By default every new cell is a code cell. To convert a cell to markdown, highlight the cell, make sure it's inactive, and type 'm'. It's that simple.

Jupyter supports full markdown so you can do all sorts of things, like

_Italics_

__Bold__

# Big Headers

#### And small headers

both `inline` code

```python
# And syntax-highlighted
multiline()
codeblock = "samples"
```

Embedded HTML like <kbd>key</kbd> tags and <span style="color:red;">tags with custom CSS</span>.

And LaTeX style equations: $e^{i\pi} + 1 = 0$

Probably most usefully, you have [links](http://jupyter-notebook.readthedocs.io/en/latest/notebook.html).

That link above is the nice and readable documentation for Jupyter. It's worth looking through if you have any further questions about notebooks. For more detail on markdown specifically, [see here](http://jupyter-notebook.readthedocs.io/en/latest/examples/Notebook/Working%20With%20Markdown%20Cells.html). 

And look, our code still works, and `message` is still defined :)
