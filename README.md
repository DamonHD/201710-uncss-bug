Test case for putative uncss 0.15.0 bug.

"With -n avoid injecting blank lines (and unnecessary newlines)"

https://github.com/giakki/uncss/issues/331#issuecomment-335873476

It seems a shame when trimming the CSS to a minimum to leave in (in fact, add!) redundant blank lines and newlines; all the filtered CSS should be on a single line with no breaks.

(Thanks for an interesting tool: I'm writing up my comparison for my site against purifycss here: http://www.earth.org.uk/note-on-site-technicals-4.html#uncss )
