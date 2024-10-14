---
title: How to Use the GetLine Feature for Selective Text Retrieval in EmEditor Text Editor
date: 2024-10-08T07:02:56.663Z
updated: 2024-10-14T05:39:35.612Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/192f81e62d92a192c6756d4acefa6e25619bd0109c72bd43d2bf00cf25a87ef6.png
---

## How to Use the GetLine Feature for Selective Text Retrieval in EmEditor Text Editor

Viewing 3 posts - 1 through 3 (of 3 total)

* Author  
Posts
* February 18, 2012 at 7:56 pm [#10040](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/f29c043a3cc5c5dac8db4e62939893e9?s=80&d=identicon&r=g)Stefan](https://www.emeditor.com/forums/users/Stefan/ "View Stefan's profile")  
Participant  
This is 11.0.5, 32-bit portable on XP SP3  
> GetLine Method  
> Retrieves the text on the specified line.  
> \[JavaScript\] str = document.GetLine(yLine \[, nFlags \]);  
> \[VBScript\] str = document.GetLine(yLine \[, nFlags \])  
 But i wonder why GetLine returns the selected part only  
 instead of the whole line?  
 Back ground:  
 in an macro i walk through all selected lines and wanted to get the text of the WHOLE line.  
FOR y = 1 to 3  
	  'Retrieves the text on the specified line.  
	  str = document.GetLine(y)  
	NEXT  
 Instead i get the selected part of that lines only.  
 Why?  
 How can i get the whole line at easy?  
 Do i really have to use something like:  
FOR y = 1 to 3  
	  'Sets the cursor position.  
	  document.selection.SetActivePoint eePosLogical, 1, y, false  
	    
	  'Selects a line at the cursor.  
	  document.selection.SelectLine  
	    
	  'Retrieves the text on the specified line.  
	  str = document.GetLine(y)  
	NEXT  
 Question:  
 Can GetLine() be extended by an flag to get the whole line always, no matter of the selection?  
 If not, should the help wrote  
 “Retrieves the selected text on the specified line.”  
 instead of  
 “Retrieves the text on the specified line.”  
 Or is there an other method?  
February 20, 2012 at 7:02 pm [#10048](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
Hello,  
 I couldn’t reproduce this issue. Can you show me or send me a sample file? Can you write how the file was selected when you run this macro?  
 Thank you,  
February 20, 2012 at 8:47 pm [#10050](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/f29c043a3cc5c5dac8db4e62939893e9?s=80&d=identicon&r=g)Stefan](https://www.emeditor.com/forums/users/Stefan/ "View Stefan's profile")  
Participant  
Your answer implies that GetLine() returns the whole line already.  
 That was not clear to me because i saw different results (to my failure as i see now)  
 Today i saw by an another test that GetLine() returns the whole line indeed:  
    
	#language = "VBScript"  
	    
	'Returns the line number of the top of the selection.  
	SelLineFirst = document.selection.GetTopPointY(eePosView)  
		    
	'Returns the line number of the bottom of the selection.  
	SelLinesLast = document.selection.GetBottomPointY(eePosView)  
	    
	    
	For LineNumber = SelLineFirst to SelLinesLast  
	    
		'Retrieves the text on the specified line "LineNumber"  
		Line = document.GetLine(LineNumber)  
		    
		'Show line content:  
		alert Line  
	    
	        'here is my failure  
	        'document.selection.Text = newtext & Line  
	    
	Next 'LineNumber  
	 Now that i know that GetLine() returns the whole line content  
 i know i did something wrong.  
 My problem was that i wanted not to select the whole lines  
 (in front of executing my script)  
 but start selection at some signs behind SOL at first line  
 and end at some position before EOL at the last line.  
 BUT then, silly me, i used **document.selection.Text = newtext**  
 and was wondering why GetLine() didn’t returns the whole line,  
 now i see i was to silly to get what happens… sorry.  
 (only the selected text was altered, of course)  
 No i use something like  
For LineNumber = SelLineFirst to SelLinesLast  
	    
		'Retrieves the text on the specified line "LineNumber"  
		Line = document.GetLine(LineNumber)  
		    
		'Selects a line at the cursor.  
		document.selection.SelectLine  
	    
	        'overwrite this line with new text  
	        document.selection.Text = newtext & Line  
	    
	Next 'LineNumber  
	 The additional **document.selection.SelectLine**  
 extends at real time the selection to the whole line  
 and so my replacement replaces the whole line as wanted.  
 Issue solved.  
 Thanks Yutaka! Thank you for your endurance and support!
* Author  
Posts

Viewing 3 posts - 1 through 3 (of 3 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://facebook-video-footage.techidaily.com/new-echoes-of-amusement-comical-tune-transformations-for-2024/"><u>[New] Echoes of Amusement Comical Tune Transformations for 2024</u></a></li>
<li><a href="https://snapchat-videos.techidaily.com/new-in-2024-amplify-your-snapchat-experience-with-easy-voice-customization/"><u>[New] In 2024, Amplify Your Snapchat Experience with Easy Voice Customization</u></a></li>
<li><a href="https://instagram-video-recordings.techidaily.com/new-in-2024-from-blurry-beginnings-transforming-your-videography-with-instagram-techniques/"><u>[New] In 2024, From Blurry Beginnings Transforming Your Videography with Instagram Techniques</u></a></li>
<li><a href="https://win-awesome.techidaily.com/1-year-subscription-pass-for-emeditor-professional-text-editing-software/"><u>1-Year Subscription Pass for EmEditor - Professional Text Editing Software</u></a></li>
<li><a href="https://win-awesome.techidaily.com/b29-challenges-of-handling-massive-file-sizes-in-emeditor/"><u>B29] Challenges of Handling Massive File Sizes in EmEditor</u></a></li>
<li><a href="https://win-awesome.techidaily.com/efficient-coding-with-emeditor-a-fast-and-feature-rich-text-editing-solution/"><u>Efficient Coding with EmEditor - A Fast and Feature-Rich Text Editing Solution</u></a></li>
<li><a href="https://win-awesome.techidaily.com/emeditor-text-editor-master-your-coding-sessions-with-the-power-of-code-folding/"><u>EmEditor Text Editor: Master Your Coding Sessions with the Power of Code Folding</u></a></li>
<li><a href="https://program-issues.techidaily.com/1722993013472-resolving-rainbow-six-sieges-error-code-3-0x0001000b-a-comprehensive-guide/"><u>Resolving Rainbow Six Siege's Error Code 3-0X0001000B: A Comprehensive Guide</u></a></li>
<li><a href="https://win-awesome.techidaily.com/understanding-text-file-encoding-in-emeditor-why-reloading-wont-change-it/"><u>Understanding Text File Encoding in EmEditor - Why Reloading Won't Change It</u></a></li>
<li><a href="https://screen-capture.techidaily.com/virtual-voyage-unlimited-the-ultimate-selection-of-free-roleplayers/"><u>Virtual Voyage Unlimited The Ultimate Selection of Free Roleplayers</u></a></li>
<li><a href="https://ios-location-track.techidaily.com/ways-to-stop-parent-tracking-your-apple-iphone-xs-drfone-by-drfone-virtual-ios/"><u>Ways to stop parent tracking your Apple iPhone XS | Dr.fone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://imp.i357552.net/c/5597632/863035/11832" target="_top" id="863035">
  <img src="//a.impactradius-go.com/display-ad/11832-863035" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://imp.i357552.net/i/5597632/863035/11832" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

