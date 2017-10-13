Test case for putative uncss 0.15.0 bug.

"With -n avoid injecting blank lines (and unnecessary newlines)"

https://github.com/giakki/uncss/issues/331

> It seems a shame when trimming the CSS to a minimum to leave in (in fact, add!) redundant blank lines and newlines; all the filtered CSS should be on a single line with no breaks.
> 
> (Thanks for an interesting tool: I'm writing up my comparison for my site against purifycss here: http://www.earth.org.uk/note-on-site-technicals-4.html#uncss )


Example of spurious linebreaks left/inserted in output, currently partially removed with a separate tool downstream:

    % cat .note-on-carbon-cost-of-CDN.html | uncss -t 0 -n -m screen,print -i .container,.sidebar,.sml,.noprint,.ad -s img/css/base-20171001.css,img/css/desktop-20170906.css,img/css/fullw-20170606.css,img/css/table-20170622.css
    h1,h2,h3{font-family:sans-serif}.sidebar{color:#000;background-color:#cfc;margin:1em 0}.sml{font-size:small}.pgdescription{font-weight:700;margin:1em 0}.ad{border:1px dotted red;margin:1em;padding:3px}.resp{max-width:100%;height:auto}.respfloatr{float:right;clear:right;height:auto;margin:1em 0 1em 1.5em}.respfloatr{max-width:50%}.respfloatr{border-radius:4px}@media screen and (min-width:640px){.container{max-width:800px;margin:auto}}@media print{.ad,.noprint{display:none!important}} 
    @media screen and (min-width:800px){.container{font-size:1.2rem}}
    
    .fullwcdisp{width:100%;width:100vw;position:relative;left:50%;right:50%;margin-left:-50%;margin-left:-50vw;margin-right:-50%;margin-right:-50vw}.fullwcdisp{clear:both;text-align:center}
    
    table.tb1,table.tb1 td,table.tb1 th{border:1px solid}
