DetectHtml
==========

A Java static method to detect text that has been marked up with HTML tags
or entities.

I needed to detect self-contained HTML tags or entities in user supplied data
to make formatting determinations.  After searching the Internet I found a
few examples as regular expressions.  Most of the example failed by initial
test cases and didn't handle conditions such as test without tags that
contained HTML entity escape codes.

I continue to refine the regular expression until I came up with a good meta
expression that handled:

- Start and End tag combinations in single or multi-line text values.
- Text marked up with self-closing tags such as <br/> or <hr/>
- Text marked up with HTML entity escape sequences like &lt; or &frac12;

I also wanted to make sure that it didn't match other common text phrases
that may be misinterpreted as HTML.

- Logic expressions such as:  "If A<B then B>A"
- Ampersand usage:  AT&T,  D&B, etc...
- Malformed or partial HTML: </body></html>

No dependencies required.  Just refactor the class into your project and
you're done.

--Dave

