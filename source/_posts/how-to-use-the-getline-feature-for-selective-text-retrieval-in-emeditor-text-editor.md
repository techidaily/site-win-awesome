---
title: How to Use the GetLine Feature for Selective Text Retrieval in EmEditor Text Editor
date: 2024-10-06T16:34:42.172Z
updated: 2024-10-08T17:39:03.426Z
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
<li><a href="https://screen-mirroring-recording.techidaily.com/new-2024-approved-finding-the-perfect-recorders-outside-microsofts-ecosystem/"><u>[New] 2024 Approved Finding the Perfect Recorders Outside Microsoft's Ecosystem</u></a></li>
<li><a href="https://youtube-tips.techidaily.com/treamlining-content-creation-with-youtube-rules/"><u>[New] Streamlining Content Creation with YouTube Rules</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-5-ways-to-record-league-of-legends-lol-games/"><u>[Updated] 5 Ways to Record League of Legends (LOL) Games</u></a></li>
<li><a href="https://fox-glue.techidaily.com/updated-skys-the-limit-for-your-shots-blend-free-space-and-premium-subscriptions-for-2024/"><u>[Updated] Sky's the Limit for Your Shots Blend Free Space and Premium Subscriptions for 2024</u></a></li>
<li><a href="https://buynow-tips.techidaily.com/alexa-or-siri-showdown-a-deep-dive-into-echo-dot-vs-homepod-mini/"><u>Alexa or Siri Showdown: A Deep Dive Into Echo Dot Vs. HomePod Mini</u></a></li>
<li><a href="https://win-awesome.techidaily.com/avoid-the-hurdles-of-windows-11-update-a-user-friendly-guide-to-enhance-your-pcs-performance-zdnet/"><u>Avoid the Hurdles of Windows 11 Update - A User-Friendly Guide to Enhance Your PC's Performance | ZDNet</u></a></li>
<li><a href="https://buynow-marvelous.techidaily.com/comprehensive-review-unpacking-the-performance-of-chargetechs-high-capacity-27000mah-battery-pack/"><u>Comprehensive Review: Unpacking the Performance of ChargeTech's High-Capacity 27000mAh Battery Pack</u></a></li>
<li><a href="https://fake-location.techidaily.com/dose-life360-notify-me-when-someone-checks-my-location-on-oppo-reno-8t-5g-drfone-by-drfone-virtual-android/"><u>Dose Life360 Notify Me When Someone Checks My Location On Oppo Reno 8T 5G? | Dr.fone</u></a></li>
<li><a href="https://win-awesome.techidaily.com/experience-improved-durability-on-your-surface-duo-2-with-the-new-pen-cover-and-wireless-charging-capabilities-zdnet-exclusive-test/"><u>Experience Improved Durability on Your Surface Duo 2 with the New Pen Cover and Wireless Charging Capabilities - ZDNet Exclusive Test!</u></a></li>
<li><a href="https://win-awesome.techidaily.com/get-your-professional-microsoft-project-and-visio-licenses-today-at-only-20-special-deal-from-zdnet/"><u>Get Your Professional Microsoft Project & Visio Licenses Today at Only $20 - Special Deal From ZDNet!</u></a></li>
<li><a href="https://some-knowledge.techidaily.com/in-2024-in-depth-review-of-dji-mavic-pro-eyewear-tech/"><u>In 2024, In-Depth Review of DJI Mavic Pro Eyewear Tech</u></a></li>
<li><a href="https://win-awesome.techidaily.com/microsoft-to-do-evaluation-is-this-task-management-tool-overwhelming-users-techspot/"><u>Microsoft To Do Evaluation: Is This Task Management Tool Overwhelming Users? | TechSpot</u></a></li>
<li><a href="https://win-awesome.techidaily.com/new-microsoft-announcement-pay-for-updates-coming-what-it-costs-you/"><u>New Microsoft Announcement: Pay-for-Updates Coming - What It Costs You</u></a></li>
<li><a href="https://win-awesome.techidaily.com/paying-for-windows-10-updates-microsoft-announces-new-fees-starting-next-year-what-you-need-to-know/"><u>Paying for Windows 10 Updates: Microsoft Announces New Fees Starting Next Year – What You Need to Know</u></a></li>
<li><a href="https://win-awesome.techidaily.com/redefining-innovation-my-take-on-microsofts-encouragement-to-think-outside-the-box-with-excel-analysis-by-zdnet/"><u>Redefining Innovation: My Take on Microsoft's Encouragement to Think Outside the Box with Excel | Analysis by ZDNet</u></a></li>
<li><a href="https://win-awesome.techidaily.com/revolutionizing-the-arm-landscape-exciting-new-microsoft-windows-applications-set-to-launch/"><u>Revolutionizing the ARM Landscape: Exciting New Microsoft Windows Applications Set to Launch</u></a></li>
<li><a href="https://win11.techidaily.com/unravel-complex-windows-issues-help-at-hand/"><u>Unravel Complex Windows Issues: Help at Hand!</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1918703/19272" target="_top" id="1918703">
  <img src="//a.impactradius-go.com/display-ad/19272-1918703" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1918703/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

