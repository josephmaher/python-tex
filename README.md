# python-tex
updated python-tex for python3

This is the pip tex python module from:

https://pypi.org/project/tex/

with the minimal changes needed to make it run under python3.  (It now won't run under python2 though.)

Here's the original description:



The python-tex project is obsolete! Please have a look at Texcaller http://www.profv.de/texcaller/.

Python-tex is a convenient interface to the TeX command line tools that handles all kinds of errors without much fuzz.

Temporary files are always cleaned up. The TeX interpreter is automatically re-run as often as necessary, and an exception is thrown in case the output fails to stabilize soon enough. The TeX interpreter is always run in batch mode, so it won’t ever get in your way by stopping your application when there are issues with your TeX source. Instead, an exception is thrown that contains all information of the TeX log.

This enables you to debug TeX related issues directly within your application or within an interactive Python interpreter session.

Example:

```
>>> from tex import latex2pdf
>>> document = ur"""
... \documentclass{article}
... \begin{document}
... Hello, World!
... \end{document}
... """
>>> pdf = latex2pdf(document)
```
```
>>> type(pdf)
<type 'str'>
>>> print "PDF size: %.1f KB" % (len(pdf) / 1024.0)
PDF size: 5.6 KB
>>> pdf[:5]
'%PDF-'
>>> pdf[-6:]
'%%EOF\n'
```
