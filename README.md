# Markdown and BB-codes for sites — VK
For vk.com

This script installed by [Tapermonkey](http://tampermonkey.net/) addon into page and executing.
Script is universal in mean how to work on any site, but it require some special remarks _(for all sites: #identificator or .class where text need to mark, also: somewere add CSS rules, somewhere disable some markdown, somewhere edit regex to accurate pasting html code)_ to compleately work without issues.

Markdown is based on Github markdown and [this article](https://daringfireball.net/projects/markdown/syntax) for exception markdown with spaces, because vk.com delete it from text.

# Available markdown (for VK)

```
normal, *italic* or _italic_ or [i]italic[/i], **bold** or [b]bold[/b], ***b+i*** or _**b+i**_ or [b][i]b+i[/i][/b]
__underline__ or [u]underline[/u], ~~strikeout~~ or [s]strikeout[/s], [o]overline[/o] (no md)
[sup]superscript[/sup], [sub]subtitle[/sub]
{#anchor} (test it by clicking [on this link](#anchor))
`inline code`
\```multiline code\``` or [code]also code[/code]
> quote (blockquote)
also
> line 1 of blockquote (merged with line 2)
> line 2
also
[quote]blockquote[/quote]
spoiler(hide text under black background): %%spoiler%% or [spoiler]spoiler[/spoiler]
%highlighting%

Lists:
* list item 1
* list item 2
** sublist 1 (WIP)
** sublist 2
* list item 3
also
[list]
[*]item 1
[*]item 2
[*]item 3
[/list]
also
1. numered item 1
2. numered item 2
3. numered item 3
also
[list]
[1]item 1
[2]item 2
[3]item 3
[/list]
named link: [GitHub](http://github.com)
# h1

## h2

### h3

#### h4

##### h5

###### h6

![Embed image](https://site.com/image.jpg)

Compleate list:
- [x] this is a complete item
- [ ] this is an incomplete item

Table:
First Header | Second Header | Third header
------------ | ------------- | ------------
Content from cell 1 | Content from cell 2 | Some blah blah blah
Content in the first column | Content in the second column | Another content\nwith force newline

@XCanG - mention
***
newline
also:
---
or:
[hr]

text alighned left, [c]centered text[/c] or [r]right-alighned text[/r]
[j]also justifyed text[/j]

YouTube embeding:
ID only: [yt]00000000000[/yt] Short: [yt]https://youtu.be/00000000000[/yt] Full: [yt]https://www.youtube.com/watch?v=00000000000[/yt]
[font=Arial]Arial font[/font], also may be [font="Lucide Consoles"]font in quotation[/font] (any font possible to use)
Colors short/full hex: [color=#000]text[/color] or rgb(a)/hsl(a), also [color="Azure"]coloring by name[/color]
Some sizing: [size=1em]1[/size][size=10pt]2[/size][size=11px]3[/size][size=12px]4[/size][size=27mm]5[/size][size=5cm]6[/size][size=1vh]7[/size][size=1vw]8[/size]
Shadowing text [glow=0,0,8,darkgreen]text[/glow] or [shadow=1,1,2,black]text[/shadow] (use same CSS effect: text-shadow)
"\n" force newline character

-------------
Combinations (some test examples I use):
> *text* ~~in quote~~
> > quote in quote
> > multiline too
> some `inline code` too
also
> [yt]00000000000[/yt]
[c]Centered table
Some | Table
---- | -----
Here | .
[/c]

# Mark text %in title%

%%and have *some* markdown __in spoiler too__%%

%%
- [ ] Trying to spoilering to-do list
[Go to #](#) also hided
%%

- list *with* markdown [o]too[/o]
- item 2

This will use CSS: word-break: break-all; word-wrap: break-word; and max-height (add vertical scroll bar) for convinient view
\```
long
code
block
looongliiineheeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeereeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee
1
2
3
4
5
6
7
8
9
0
1
2
3
4
5
6
7
8
9
0
\```
[quote]
long
quote
block
looongliiineheeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeereeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee
1
2
3
4
5
6
7
8
9
0
1
2
3
4
5
6
7
8
9
0
[/quote]
e.t.c.
```
