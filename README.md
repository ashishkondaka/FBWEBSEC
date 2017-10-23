{\rtf1\ansi\ansicpg1252\cocoartf1561
{\fonttbl\f0\fswiss\fcharset0 Helvetica;\f1\froman\fcharset0 Times-Roman;}
{\colortbl;\red255\green255\blue255;\red0\green0\blue0;}
{\*\expandedcolortbl;;\cssrgb\c0\c0\c0;}
{\*\listtable{\list\listtemplateid1\listhybrid{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{circle\}}{\leveltext\leveltemplateid1\'01\uc0\u9702 ;}{\levelnumbers;}\fi-360\li720\lin720 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{hyphen\}}{\leveltext\leveltemplateid2\'01\uc0\u8259 ;}{\levelnumbers;}\fi-360\li1440\lin1440 }{\listlevel\levelnfc23\levelnfcn23\leveljc0\leveljcn0\levelfollow0\levelstartat1\levelspace360\levelindent0{\*\levelmarker \{hyphen\}}{\leveltext\leveltemplateid3\'01\uc0\u8259 ;}{\levelnumbers;}\fi-360\li2160\lin2160 }{\listname ;}\listid1}}
{\*\listoverridetable{\listoverride\listid1\listoverridecount0\ls1}}
\margl1440\margr1440\vieww16560\viewh20700\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Project Week 7\
Time Spent: 3 hours\
\
Objective: Find, study, recreate and document 5 vulnerabilities affecting an old version of WordPress.\
\
#Report\
\
\
1.\
-[x] Summary: XSS Crashing due to YouTube embedded video URL malfunction. \
-Vulnerability Type: XSS and Inject\
-Tested in version: 4.2.0\
-Fixed in version: 4.2.13\
-[x] GIF Walkthrough: https://i.imgur.com/zqq6Sju.gifv\
-[x] Steps to recreate:\
	-Chose a youtube video and add embed it to the welcome post.\
	-insert [embed 
\f1 \cf2 \expnd0\expndtw0\kerning0
src='https://youtu.be/mThqhAT2Irk onload=while(1)\{alert(document.cookie\};\\x3e'][/embed] onto the post.\
	-update the post and click on \'91view post\'92\
	-cookie should pop up with the message\
	-delete the embed video after.\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0 \cf0 \kerning1\expnd0\expndtw0 - [x] Affected source code:\
	[Link 4]: https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 \
\
2.\
-[x] Summary : Creates a pop up when you hover the link on the post.\
\pard\tx220\tx720\pardeftab720\li720\fi-720\partightenfactor0
\ls1\ilvl0\cf0 -Vulnerability types:XSS\
-Tested in version:4.0\
-Fixed in version: 4.2.3\
-[x] GIF Walkthrough: https://i.imgur.com/btyqiJf.gifv\
-[x] Steps to recreate: \
\pard\tx1660\tx2160\pardeftab720\li2160\fi-2160\partightenfactor0
\ls1\ilvl2\cf0 {\listtext	\uc0\u8259 	}Make a new post on the developer portal\
{\listtext	\uc0\u8259 	}insert " <a href="</a><a title=" onmouseover=alert('test') ">link</a> ""\
{\listtext	\uc0\u8259 	}into both the name of the post and the comment.\
{\listtext	\uc0\u8259 	}update page\
{\listtext	\uc0\u8259 	}should create a pop up saying test after every time you hover over the post\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 - [x] Affected source code:\
	[Link 3]: {\field{\*\fldinst{HYPERLINK "https://en.forums.wordpress.com/topic/pop-up-image-when-mouse-hovers-over-link"}}{\fldrslt https://en.forums.wordpress.com/topic/pop-up-image-when-mouse-hovers-over-link}}\
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0
\cf0 \
3.\
- [x] Summary:  XSS Vulnerability via Media File Data Attachments. \
- Vulnerability types: XSS\
- Tested in version: 4.2\
- Fixed in version: 4.2\
- [x] GIF Walkthrough: https://i.imgur.com/zqq6Sju.gifv \
- [x] Steps to recreate: \
	Go to the comments section of the page.\
	Enter in <script>while(1)\{alert(document.cookie);\}</script> in the comments box.  \
	Warning once you click submit, the page will refresh and you will have an infinite amount of alert messages.  \
	After you are done with this vulnerability, to end the message, go to the info page and delete the comment.\
- [x] Affected source code:\
	[Link 2]: https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7}