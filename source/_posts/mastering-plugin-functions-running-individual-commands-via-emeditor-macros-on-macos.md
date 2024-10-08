---
title: "Mastering Plugin Functions: Running Individual Commands via EmEditor Macros on MacOS"
date: 2024-10-02T17:01:38.265Z
updated: 2024-10-08T17:32:39.898Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/9cc152d1aca0892df1ca5596ac3ad03cce388893be920721cefd3090f694d72e.png
---

## Mastering Plugin Functions: Running Individual Commands via EmEditor Macros on MacOS

Viewing 4 posts - 1 through 4 (of 4 total)

* Author  
Posts
* October 12, 2008 at 4:16 pm [#6391](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d73fc2c7bd494149d303a2b87aa5a6d5?s=80&d=identicon&r=g)dreftymac](https://www.emeditor.com/forums/users/dreftymac/ "View dreftymac's profile")  
Participant  
PROBLEM:  
 I would like to be able to run all available plugin commands from an emeditor macro. The problem is, ExecuteCommandByID does not seem to know what all the ID numbers are for every single plugin action.  
 QUESTION:  
 Is ExecuteCommandByID capable of finding and running all of the commands that are defined in every plugin? If not, is there another way to tell a macro to run any arbitrary command from any arbitrary plugin?  
 Thanks for any help or info  
October 12, 2008 at 5:46 pm [#6392](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> dreftymac wrote:  
> PROBLEM:  
> I would like to be able to run all available plugin commands from an emeditor macro. The problem is, ExecuteCommandByID does not seem to know what all the ID numbers are for every single plugin action.  
>  
> QUESTION:  
> Is ExecuteCommandByID capable of finding and running all of the commands that are defined in every plugin? If not, is there another way to tell a macro to run any arbitrary command from any arbitrary plugin?  
>  
> Thanks for any help or info  
 You can use QueryStringByID Method to figure out which plug-in corresponds to which ID.  
October 13, 2008 at 4:44 am [#6393](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/d73fc2c7bd494149d303a2b87aa5a6d5?s=80&d=identicon&r=g)dreftymac](https://www.emeditor.com/forums/users/dreftymac/ "View dreftymac's profile")  
Participant  
You can use QueryStringByID Method to figure out which plug-in corresponds to which ID  
 Yes, thank you for this, but that was not actually the question. The question is not how to run any plugin, but the question was how to run any specific \*command\* inside of any specific plugin.  
 For example:  
    
	        /// we know we can do this for any plugin ...  
	        var idd  =  5637;                /// QueryStringByID found this for us  
	        editor.ExecuteCommandByID(idd);  /// activate the "outline" plugin  
	            
	        /// but can you do *this* for any plugin ...  
	        /*  
	        var oPlugin =   editor.GetPluginByID(idd);  /// <-- how can you do this?  
	        oPlugin.doCommand('CollapseAll');           /// <-- or this?  
	        oPlugin.doCommand('ExpandAll');             /// <-- or this?  
	        oAnyPlugin.doCommand('AnyCommandYouWant');  /// <-- or even this?  
	        */  
	October 13, 2008 at 5:13 am [#6394](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")  
Keymaster  
> dreftymac wrote:  
>  
> You can use QueryStringByID Method to figure out which plug-in corresponds to which ID  
>  
> Yes, thank you for this, but that was not actually the question. The question is not how to run any plugin, but the question was how to run any specific \*command\* inside of any specific plugin.  
>  
> For example:  
>  
>  
>  
>         /// we know we can do this for any plugin ...  
>  
>         var idd  =  5637;                /// QueryStringByID found this for us  
>  
>         editor.ExecuteCommandByID(idd);  /// activate the "outline" plugin  
>  
>  
>  
>         /// but can you do *this* for any plugin ...  
>  
>         /*  
>  
>         var oPlugin =   editor.GetPluginByID(idd);  /// <-- how can you do this?  
>  
>         oPlugin.doCommand('CollapseAll');           /// <-- or this?  
>  
>         oPlugin.doCommand('ExpandAll');             /// <-- or this?  
>  
>         oAnyPlugin.doCommand('AnyCommandYouWant');  /// <-- or even this?  
>  
>         */  
>  
>  
 It is not possible, unfortunately.
* Author  
Posts

Viewing 4 posts - 1 through 4 (of 4 total)

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
<li><a href="https://fox-helps.techidaily.com/new-in-2024-integrate-srt-into-windowsmacos-operations/"><u>[New] In 2024, Integrate SRT Into Windows/macOS Operations</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/new-mastering-clear-webcam-footage-recording-and-editing-tips-for-2024/"><u>[New] Mastering Clear Webcam Footage Recording & Editing Tips for 2024</u></a></li>
<li><a href="https://screen-recording.techidaily.com/new-unleash-ps2-gaming-on-ios-the-best-emulators-for-2024/"><u>[New] Unleash PS2 Gaming on iOS The Best Emulators for 2024</u></a></li>
<li><a href="https://win-awesome.techidaily.com/effortless-video-extraction-convert-and-save-spiegel-content-as-mp4movavi/"><u>Effortless Video Extraction: Convert and Save Spiegel Content as MP4/MOV/AVI</u></a></li>
<li><a href="https://win-awesome.techidaily.com/free-download-comprehensive-bloomberg-market-insights-and-analysis-on-tech-innovations-political-developments/"><u>Free Download: Comprehensive Bloomberg Market Insights & Analysis on Tech, Innovations, Political Developments</u></a></li>
<li><a href="https://win-awesome.techidaily.com/get-access-now-free-online-course-downloads-from-cybrary/"><u>Get Access Now: Free Online Course Downloads From Cybrary</u></a></li>
<li><a href="https://win-awesome.techidaily.com/get-your-fix-of-channel-ten-shows-with-the-fast-track-video-reader/"><u>Get Your Fix of Channel Ten Shows with the Fast Track Video Reader!</u></a></li>
<li><a href="https://win-awesome.techidaily.com/high-quality-erotic-movie-downloads-avi-and-mp4-for-pcmac-users-unlimited-collection/"><u>High-Quality Erotic Movie Downloads (AVI & MP4) for PC/Mac Users – Unlimited Collection</u></a></li>
<li><a href="https://extra-hints.techidaily.com/highest-rated-10-apps-to-watch-golf-and-soccer-in-the-moment/"><u>Highest Rated 10 Apps to Watch Golf & Soccer in the Moment</u></a></li>
<li><a href="https://win-awesome.techidaily.com/how-to-convert-your-favorite-shows-and-videos-into-mp4-format-for-pcs-and-macs/"><u>How To Convert Your Favorite Shows & Videos Into MP4 Format for PCs and Macs</u></a></li>
<li><a href="https://win-awesome.techidaily.com/how-to-legally-acquire-and-convert-popular-trainmaster-shows-for-offline-viewing-in-mp4-mov-and-avi-files/"><u>How to Legally Acquire and Convert Popular Trainmaster Shows for Offline Viewing in MP4, MOV & AVI Files</u></a></li>
<li><a href="https://smart-video-creator.techidaily.com/new-in-2024-create-stunning-time-lapses-with-the-best-video-editing-software/"><u>New In 2024, Create Stunning Time-Lapses with the Best Video Editing Software</u></a></li>
<li><a href="https://youtube-video-recordings.techidaily.com/playstation-palace-a-million-gaming-moves/"><u>PlayStation Palace A Million Gaming Moves</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/the-complete-guide-to-itel-s23-frp-bypass-everything-you-need-to-know-by-drfone-android/"><u>The Complete Guide to Itel S23 FRP Bypass Everything You Need to Know</u></a></li>
<li><a href="https://sound-issues.techidaily.com/troubleshoot-and-fix-resolving-pc-sound-issues-in-zoom/"><u>Troubleshoot & Fix: Resolving PC Sound Issues in Zoom</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<span id="1982596">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1982596.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1982596">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1982596.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1982596%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1982596/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

