# Markdown and BB-codes for sites — Discuss.Moe
For discuss.moe

This script installed by [Tapermonkey](http://tampermonkey.net/) addon into page and executing.
Script is universal in mean how to work on any site, but it require some special remarks _(for all sites: #identificator or .class where text need to mark, also: somewere add CSS rules, somewhere disable some markdown, somewhere edit regex to accurate pasting html code)_ to compleately work without issues.

Markdown is based on Github markdown and [this article](https://daringfireball.net/projects/markdown/syntax) for exception markdown with spaces, because vk.com delete it from text.

# Available markdown (for D.M.)

```
~~strikeout~~, [o]overline[/o] (no md)
[sup]superscript[/sup], [sub]subtitle[/sub]
{#anchor} (test it by clicking [on this link](#anchor))
spoiler(hide text under white blurred background): %%spoiler%%
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

Compleate list:
- [x] this is a complete item
- [ ] this is an incomplete item

Table:
First Header | Second Header | Third header
------------ | ------------- | ------------
Content from cell 1 | Content from cell 2 | Some blah blah blah
Content in the first column | Content in the second column | Another content\nwith force newline

newline
[hr]

text alighned left, [c]centered text[/c] or [r]right-alighned text[/r]
[j]also justifyed text[/j]

YouTube embeding:
ID only: [yt]00000000000[/yt] Short: [yt]https://youtu.be/00000000000[/yt] Full: [yt]https://www.youtube.com/watch?v=00000000000[/yt]
[font=Arial]Arial font[/font], also may be [font="Lucide Consoles"]font in quotation[/font] (any font possible to use)
Some sizing: [size=1em]1[/size][size=10pt]2[/size][size=11px]3[/size][size=12px]4[/size][size=27mm]5[/size][size=5cm]6[/size][size=1vh]7[/size][size=1vw]8[/size]
Shadowing text [glow=0,0,8,darkgreen]text[/glow] or [shadow=1,1,2,black]text[/shadow] (use same CSS effect: text-shadow)
"\n" force newline character
[raw][/raw] or [html][/html] for paste html code by itself (need to replace < to &lt;)

-------------
Combinations (some test examples I use):
> *text* ~~in quote~~
> > quote in quote
> > multiline too

> some `inline code` too

also
> [yt]TPFQ49rDaiw[/yt]

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
- [spoiler]item 2[/spoiler]

This will use CSS: word-break: break-all; word-wrap: break-word; and max-height (add vertical scroll bar)
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
Control post...
[raw]&lt;input id="sepialevel" type="range" min="0" max="100" step="1" value="0" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: sepia(' + val + '); -webkit-filter: sepia(' + val + '); }'; document.body.appendChild(sheet);"> Sepia<br>
&lt;input id="sepialevel" type="range" min="0" max="200" step="2" value="100" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: brightness(' + val + ');  -webkit-filter: brightness(' + val + '); }'; document.body.appendChild(sheet);"> Brightness<br>
&lt;input id="sepialevel" type="range" min="0" max="200" step="2" value="100" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: contrast(' + val + '); -webkit-filter: contrast(' + val + '); }'; document.body.appendChild(sheet);"> Contrast<br>
&lt;input id="sepialevel" type="range" min="0" max="100" step="1" value="0" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: grayscale(' + val + '); -webkit-filter: grayscale(' + val + '); }'; document.body.appendChild(sheet);"> Grayscale<br>
&lt;input id="sepialevel" type="range" min="0" max="360" step="5" value="0" oninput="let val = this.value; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: hue-rotate(' + val + 'deg); -webkit-filter: hue-rotate(' + val + 'deg); }'; document.body.appendChild(sheet);"> HUE rotate<br>
&lt;input id="sepialevel" type="range" min="0" max="100" step="1" value="0" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: invert(' + val + '); -webkit-filter: invert(' + val + '); }'; document.body.appendChild(sheet);"> Invert<br>
&lt;input id="sepialevel" type="range" min="0" max="100" step="1" value="100" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: opacity(' + val + '); -webkit-filter: opacity(' + val + '); }'; document.body.appendChild(sheet);"> Opacity<br>
&lt;input id="sepialevel" type="range" min="0" max="200" step="2" value="100" oninput="let val = this.value / 100; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: saturate(' + val + '); -webkit-filter: saturate(' + val + '); }'; document.body.appendChild(sheet);"> Saturate<br>
&lt;input id="sepialevel" type="range" min="0" max="40" step="1" value="0" oninput="let val = this.value; var sheet = document.createElement('style'); sheet.innerHTML = '.cooked { filter: blur(' + val + 'px); -webkit-filter: blur(' + val + 'px); }'; document.body.appendChild(sheet);"> Blur<br>
[/raw]
e.t.c.
```
