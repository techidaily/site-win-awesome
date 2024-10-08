---
title: B29] Challenges of Handling Massive File Sizes in EmEditor
date: 2024-10-07T16:56:11.343Z
updated: 2024-10-08T17:41:45.158Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/ab163d296acb79c8d1b99be55f1a9e8dc7788fd98e467de0ef2e0c0cd66b65c3.jpg
---

## B29] Challenges of Handling Massive File Sizes in EmEditor

Viewing 3 posts - 1 through 3 (of 3 total)

* Author  
Posts
* November 7, 2007 at 2:53 pm [#4949](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/ebe87191575d8a3f3b1fb12210cba2f0?s=80&d=identicon&r=g)CaptainFlint](https://www.emeditor.com/forums/users/captainflint/ "View CaptainFlint's profile")  
Participant  
I opened one of my huge SQL-files (\~160 MB; longest line is \~2700 characters) and found the following inconsistencies:  
**1.** Wrapping Mode buttons on the toolbar are disabled both visually and functionally (the first button is shown normally, but cannot be pressed).  
**2.** Option **Highlight (2) -> Strings Enclosed by Quotation Marks -> Continue to Next Line** is not taken into account at all (I have a double-lines string but the first part of it is highlighted only).  
**3.** When I try to search some text in this file, searching is performed twice (at least, it looks so). That is, in the progress dialog I see the line number increasing to the maximum number (1359306 in my case), then it becomes 0 and is growing to the maximum again – and only after this second cycle it stops. If I press Cancel during the first “stage”, the second stage immediately begins and I have to press Cancel again. (Maybe, this is valid not only with large files, but I can’t check it on small files – it’s too fast there.)  
**4.** Searching for **n** is extremely slow! Two tests:  
**a)** Replace every **n** with **n**. In usual file it is done with speed \~1000 occurences per second. In this SQL file it happens just \~100 occurences per second. (The first lines in this SQL file are not long at all – maximum 80 characters, so it cannot be because of the rare appearance of the **n**‘s in the file.)  
**b)** Replace **^.{0,1000}$** with nothing: the speed is \~34000 replaces per second. When I changed the expression to **^.{0,1000}n**, the speed became just \~100 replaces per second!  
November 7, 2007 at 4:52 pm [#4954](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
I opened one of my huge SQL-files (\~160 MB; longest line is \~2700 characters) and found the following inconsistencies:  
 1\. Wrapping Mode buttons on the toolbar are disabled both visually and functionally (the first button is shown normally, but cannot be pressed).  
 This is the specification. In order to improve performance in very large files, wrapping mode is fixed to “No-Wrap” mode in case of very large files. You can change the threshold in the file size in the Advanced tab of the Customize dialog box. The default is 100MB. You can change this value to 200MB if you don’t have problem with opening larger files.  
 2\. Option Highlight (2) -> Strings Enclosed by Quotation Marks -> Continue to Next Line is not taken into account at all (I have a double-lines string but the first part of it is highlighted only).  
 This is also the specification, and it is restricted in larger files. Again, you can change the value above to 200MB if you need this feature.  
 3\. When I try to search some text in this file, searching is performed twice (at least, it looks so). That is, in the progress dialog I see the line number increasing to the maximum number (1359306 in my case), then it becomes 0 and is growing to the maximum again – and only after this second cycle it stops. If I press Cancel during the first “stage”, the second stage immediately begins and I have to press Cancel again. (Maybe, this is valid not only with large files, but I can’t check it on small files – it’s too fast there.)  
 I reproduced this issue, and I will look into that.  
 4\. Searching for n is extremely slow! Two tests:  
 a) Replace every n with n. In usual file it is done with speed \~1000 occurences per second. In this SQL file it happens just \~100 occurences per second. (The first lines in this SQL file are not long at all – maximum 80 characters, so it cannot be because of the rare appearance of the n’s in the file.)  
 b) Replace ^.{0,1000}$ with nothing: the speed is \~34000 replaces per second. When I changed the expression to ^.{0,1000}n, the speed became just \~100 replaces per second!  
 I will further try to optimize find/replace operations.  
 Thanks!  
November 7, 2007 at 5:33 pm [#4956](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/ebe87191575d8a3f3b1fb12210cba2f0?s=80&d=identicon&r=g)CaptainFlint](https://www.emeditor.com/forums/users/captainflint/ "View CaptainFlint's profile")  
Participant  
> This is the specification. In order to improve performance in very large files, wrapping mode is fixed to “No-Wrap” mode in case of very large files. You can change the threshold in the file size in the Advanced tab of the Customize dialog box. The default is 100MB. You can change this value to 200MB if you don’t have problem with opening larger files.  
 OK, I see. Is it anywhere in the Help? I couldn’t find it… :(If no, I think it is worth describing the full list of the functions that do not work with large files.
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
<li><a href="https://digital-screen-recording.techidaily.com/new-in-2024-essential-guide-to-selecting-best-video-grabber-tools/"><u>[New] In 2024, Essential Guide to Selecting Best Video Grabber Tools</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/updated-straightforward-methods-to-save-insta-story-videos-for-2024/"><u>[Updated] Straightforward Methods to Save Insta Story Videos for 2024</u></a></li>
<li><a href="https://win-awesome.techidaily.com/1-troubleshooting-and-resolving-windows-search-problems-a-step-by-step-guide/"><u>1. Troubleshooting and Resolving Windows Search Problems: A Step-by-Step Guide</u></a></li>
<li><a href="https://win-awesome.techidaily.com/10-obstacles-expert-analysis-on-zdnet/"><u>10 Obstacles | Expert Analysis on ZDNET</u></a></li>
<li><a href="https://graphic-issues.techidaily.com/1719817987525-enhance-viewing-quality-instantly/"><u>Enhance Viewing Quality, Instantly!</u></a></li>
<li><a href="https://fake-location.techidaily.com/full-guide-to-fix-itoolab-anygo-not-working-on-lenovo-thinkphone-drfone-by-drfone-virtual-android/"><u>Full Guide to Fix iToolab AnyGO Not Working On Lenovo ThinkPhone | Dr.fone</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-how-to-remove-icloud-from-iphone-14-pro-max-smoothly-by-drfone-ios/"><u>In 2024, How To Remove iCloud From iPhone 14 Pro Max Smoothly</u></a></li>
<li><a href="https://youtube-lab.techidaily.com/24-virtual-victory-channel-over-a-hundred-heroes-rise/"><u>In 2024, Virtual Victory Channel Over a Hundred Heroes Rise</u></a></li>
<li><a href="https://youtube-web.techidaily.com/ssional-audio-tactics-achieving-excellence-without-a-microphone-for-2024/"><u>Professional Audio Tactics Achieving Excellence without a Microphone for 2024</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/top-5-nubia-red-magic-9-pro-bypass-frp-tools-for-pc-that-actually-work-by-drfone-android/"><u>Top 5 Nubia Red Magic 9 Pro Bypass FRP Tools for PC That Actually Work</u></a></li>
<li><a href="https://win-awesome.techidaily.com/top-tech-certification-programs-for-every-professional-level-insights-from-zdnet/"><u>Top Tech Certification Programs for Every Professional Level - Insights From ZDNet</u></a></li>
<li><a href="https://win-awesome.techidaily.com/top-tier-durable-tablet-experience-windows-os-and-precision-stylus-handling-insights-from-a-tech-expert-at-zdnet/"><u>Top-Tier Durable Tablet Experience: Windows OS and Precision Stylus Handling - Insights From a Tech Expert at ZDNet</u></a></li>
<li><a href="https://win-awesome.techidaily.com/unmissable-black-friday-discounts-from-the-microsoft-store-get-your-hands-on-the-300-surface-go-2-plus-a-high-performing-acer-2-in-1-laptop-at-just-230-deal124/"><u>Unmissable Black Friday Discounts From the Microsoft Store: Get Your Hands on the $300 Surface Go 2, Plus a High-Performing Acer 2-in-1 Laptop at Just $230 | Deals and Guides - ZDNet</u></a></li>
<li><a href="https://win-awesome.techidaily.com/unmissable-black-friday-offers-on-tech-gadgets-score-a-steal-with-surface-go-2-and-acer-laptop-from-microsofts-online-store/"><u>Unmissable Black Friday Offers on Tech Gadgets: Score a Steal with Surface Go 2 & Acer Laptop From Microsoft's Online Store!</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<span id="1770526">
					<video width="240" height="480" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1770526.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/20702-1770526">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1770526.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:150px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Ftokenmetrics.sjv.io%2Fc%2F5597632%2F1770526%2F20702'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1770526/20702" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

