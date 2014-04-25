README
======

Many thanks to [Alex Coles](https://github.com/myabc) for the excellent [markdownj](https://github.com/myabc/markdownj).

At [YouCanBook.Me](https://youcanbook.me) we use a slightly adjusted version of markdown.

- All line breaks produce br tags (no need to add two spaces)
- We don't use the ol rule (lines that start with numbers and dots)

The first change was for backwards-compatibility with our pre-markdown system. The second was because we often
need to present date strings on their own on a line, which in some localisations (e.g. Norwegian) looks like this:

    25. april 2014

Which stardard markdown will change to April 1st.

This fork hasn't changed any of the existing files, so the jar file can be used interchangably with the original.
But we added a class so that you have the option of:

    public static String markdown(String string) {
        return (new MarkdownProcessorLineBreaks()).markdown(string);
    }

keith@youcanbook.me

@coderkeith