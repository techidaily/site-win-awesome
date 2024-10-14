---
title: B29] Challenges of Handling Massive File Sizes in EmEditor
date: 2024-10-07T04:33:59.198Z
updated: 2024-10-14T02:24:16.093Z
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
<li><a href="https://facebook-video-content.techidaily.com/new-2024-approved-make-facebook-videos-extend-the-wallpaper/"><u>[New] 2024 Approved Make Facebook Videos Extend the Wallpaper</u></a></li>
<li><a href="https://fox-links.techidaily.com/new-the-complete-picture-toolwizs-app-masterclass-for-2024/"><u>[New] The Complete Picture Toolwiz's App Masterclass for 2024</u></a></li>
<li><a href="https://win-awesome.techidaily.com/1-year-subscription-pass-for-emeditor-professional-text-editing-software/"><u>1-Year Subscription Pass for EmEditor - Professional Text Editing Software</u></a></li>
<li><a href="https://win-awesome.techidaily.com/1-enhance-text-editing-with-emeditor-api-wrapper-add-on/"><u>1. Enhance Text Editing with EmEditor API Wrapper Add-On</u></a></li>
<li><a href="https://win-awesome.techidaily.com/advanced-text-editor-explore-the-capabilities-of-emeditor-by-eaglesoft/"><u>Advanced Text Editor: Explore the Capabilities of EmEditor by EagleSoft</u></a></li>
<li><a href="https://win-answers.techidaily.com/beat-cant-start-maplestory-essential-solutions-to-get-your-favorite-game-running-smoothly-again/"><u>Beat 'Can't Start Maplestory': Essential Solutions to Get Your Favorite Game Running Smoothly Again</u></a></li>
<li><a href="https://win-awesome.techidaily.com/enhance-your-coding-experience-with-emeditors-minimalzen-color-theme-for-text-editors/"><u>Enhance Your Coding Experience with EmEditor's MinimalZen Color Theme for Text Editors</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-use-special-features-virtual-location-on-vivo-s17-drfone-by-drfone-virtual-android/"><u>How To Use Special Features - Virtual Location On Vivo S17? | Dr.fone</u></a></li>
<li><a href="https://win-awesome.techidaily.com/how-to-use-the-getline-feature-for-selective-text-retrieval-in-emeditor-text-editor/"><u>How to Use the GetLine Feature for Selective Text Retrieval in EmEditor Text Editor</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-how-to-sharefake-location-on-whatsapp-for-realme-12-proplus-5g-drfone-by-drfone-virtual-android/"><u>In 2024, How to Share/Fake Location on WhatsApp for Realme 12 Pro+ 5G | Dr.fone</u></a></li>
<li><a href="https://unlock-android.techidaily.com/in-2024-how-to-show-wi-fi-password-on-tecno-camon-20-premier-5g-by-drfone-android/"><u>In 2024, How to Show Wi-Fi Password on Tecno Camon 20 Premier 5G</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/in-2024-revolutionizing-vr-experiences-with-newest-game-engines/"><u>In 2024, Revolutionizing VR Experiences with Newest Game Engines</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-what-does-enter-puk-code-mean-and-why-did-the-sim-get-puk-blocked-on-motorola-moto-g-stylus-5g-2023-device-by-drfone-android/"><u>In 2024, What Does Enter PUK Code Mean And Why Did The Sim Get PUK Blocked On Motorola Moto G Stylus 5G (2023) Device</u></a></li>
<li><a href="https://win-awesome.techidaily.com/maintaining-concentration-with-emeditor-solutions-for-post-output-distraction-issues/"><u>Maintaining Concentration with EmEditor - Solutions for Post-Output Distraction Issues</u></a></li>
<li><a href="https://win-awesome.techidaily.com/mastering-plugin-functions-running-individual-commands-via-emeditor-macros-on-macos/"><u>Mastering Plugin Functions: Running Individual Commands via EmEditor Macros on MacOS</u></a></li>
<li><a href="https://win-awesome.techidaily.com/troubleshooting-file-extension-issues-in-vista-x64-using-emeditor/"><u>Troubleshooting File Extension Issues in Vista X64 Using EmEditor</u></a></li>
<li><a href="https://tech-hub.techidaily.com/what-is-codegpt-and-can-it-really-write-code/"><u>What Is CodeGPT and Can It Really Write Code?</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2082520/7443" target="_top" id="2082520">
  <img src="//a.impactradius-go.com/display-ad/7443-2082520" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2082520/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

