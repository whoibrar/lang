---
published : true

title : Python Strings
permalink : "/py/strings"
layout : note
excerpt : 

alias : ["Python Strings"]
categories : ["py"]
tags : 

# date : 2022-04-14 00:00:00 +0000

showfooter : 
showgraph : 
---

## Text Processing and [[UNICODE]]
- To decode bytes into graphemes we need to know the original encoding 
- In Unicode grapheme =/= code point =/= byte
- All strings are Unicode in python3, with [[UTF-8]] as default encoding
- Also supports Unicode characters as identifiers (now call your résumé=True)

```python
>>> "\N{GREEK CAPITAL LETTER DELTA}"  # Using the character name
'\u0394'
>>> "\u0394"                          # Using a 16-bit hex value
'\u0394'
>>> "\U00000394"                      # Using a 32-bit hex value
'\u0394'

```

### Unicode Aware [[vs]] Unicode Unaware 
```python

#Unicode Unaware code
>>> s = "👍"
>>> len(s) #4
>>> s[0] #'\xf0'
>>> s[1] #'\x9f'
>>> s[2] #'\x91'

#Unicode Aware code
>>> s = "👍"
>>> len(s) #1
>>> s[0] #u'\U001f44d'

```

- To learn more
	- [Unicode HOWTO — Python 3.10.2 documentation](https://docs.python.org/3/howto/unicode.html)
	- [Processing Text Files in Python 3 — Nick Coghlan's Python Notes 1.0 documentation](https://python-notes.curiousefficiency.org/en/latest/python3/text_file_processing.html)
	- [PyVideo.org · The Guts of Unicode in Python](https://pyvideo.org/pycon-us-2013/the-guts-of-unicode-in-python.html)
	- [Pragmatic Unicode | Ned Batchelder](https://nedbatchelder.com/text/unipain.html)


---

Return to [[py.python|python]]

---
