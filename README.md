# Project Week 7
Time Spent: 3 hours

Objective: Find, study, recreate and document 5 vulnerabilities affecting an old version of WordPress.

#Report


1.
-[x] Summary: XSS Crashing due to YouTube embedded video URL malfunction.
-Vulnerability Type: XSS and Inject
-Tested in version: 4.2.0
-Fixed in version: 4.2.13
-[x] GIF Walkthrough: https://i.imgur.com/zqq6Sju.gifv\
-[x] Steps to recreate:
	-Chose a youtube video and add embed it to the welcome post.
	-insert [embed
	src='https://youtu.be/mThqhAT2Irk onload=while(1)\{alert(document.cookie\};\\x3e'][/embed] onto the post.
	-update the post and click on view post
	-cookie should pop up with the message
	-delete the embed video after.
 - [x] Affected source code:
	[Link 4]: https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8\


2.
-[x] Summary : Creates a pop up when you hover the link on the post.
-Vulnerability types:XSS
-Tested in version:4.0
-Fixed in version: 4.2.3
-[x] GIF Walkthrough: https://i.imgur.com/btyqiJf.gifv
-[x] Steps to recreate:
		-Make a new post on the developer portal
		-insert " <a href="</a><a title=" onmouseover=alert('test') ">link</a> ""
		-into both the name of the post and the comment.
		-update page
should create a pop up saying test after every time you hover over the post\

- [x] Affected source code:
	[Link 3]: {\field{\*\fldinst{HYPERLINK "https://en.forums.wordpress.com/topic/pop-up-image-when-mouse-hovers-over-link"}}{\fldrslt https://en.forums.wordpress.com/topic/pop-up-image-when-mouse-hovers-over-link}}

3.
- [x] Summary:  XSS Vulnerability via Media File Data Attachments.
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.2
- [x] GIF Walkthrough: https://i.imgur.com/zqq6Sju.gifv
- [x] Steps to recreate:
	Go to the comments section of the page.
	Enter in <script>while(1)\{alert(document.cookie);\}</script> in the comments box.  
	Warning once you click submit, the page will refresh and you will have an infinite amount of alert messages.  
	After you are done with this vulnerability, to end the message, go to the info page and delete the comment.
- [x] Affected source code:
	[Link 2]: https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7}
