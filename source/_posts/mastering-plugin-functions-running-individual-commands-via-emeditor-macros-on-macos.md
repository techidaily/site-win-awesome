---
title: "Mastering Plugin Functions: Running Individual Commands via EmEditor Macros on MacOS"
date: 2024-10-07T04:14:22.072Z
updated: 2024-10-14T04:43:03.353Z
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
<li><a href="https://instagram-videos.techidaily.com/new-breathe-life-into-your-reels-adding-drama-with-slow-motion/"><u>[New] Breathe Life Into Your Reels Adding Drama with Slow Motion</u></a></li>
<li><a href="https://youtube-webster.techidaily.com/ed-2024-approved-from-raw-to-refined-expert-techniques-for-youtube-content-creators/"><u>[Updated] 2024 Approved From Raw to Refined Expert Techniques for YouTube Content Creators</u></a></li>
<li><a href="https://win-awesome.techidaily.com/1-enhance-text-editing-with-emeditor-api-wrapper-add-on/"><u>1. Enhance Text Editing with EmEditor API Wrapper Add-On</u></a></li>
<li><a href="https://win-awesome.techidaily.com/advanced-text-editor-explore-the-capabilities-of-emeditor-by-eaglesoft/"><u>Advanced Text Editor: Explore the Capabilities of EmEditor by EagleSoft</u></a></li>
<li><a href="https://tech-revival.techidaily.com/are-you-overestimating-ai-detectors-such-as-zerogpt-understanding-its-flaws-and-shortcom-ings/"><u>Are You Overestimating AI Detectors Such as ZeroGPT? Understanding Its Flaws & Shortcom Ings</u></a></li>
<li><a href="https://tech-haven.techidaily.com/are-you-willing-to-pay-for-premium-knowledge-on-apple-products-industry-leaders-say-monthly-fees-could-reach-up-to-20-insights-from-zdnet/"><u>Are You Willing to Pay for Premium Knowledge on Apple Products? Industry Leaders Say Monthly Fees Could Reach Up to $20 - Insights From ZDNet</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/easy-guide-how-to-bypass-infinix-smart-7-hd-frp-android-10111213-by-drfone-android/"><u>Easy Guide How To Bypass Infinix Smart 7 HD FRP Android 10/11/12/13</u></a></li>
<li><a href="https://win-awesome.techidaily.com/efficient-coding-with-emeditor-a-fast-and-feature-rich-text-editing-solution/"><u>Efficient Coding with EmEditor - A Fast and Feature-Rich Text Editing Solution</u></a></li>
<li><a href="https://win-awesome.techidaily.com/emeditor-text-editor-master-your-coding-sessions-with-the-power-of-code-folding/"><u>EmEditor Text Editor: Master Your Coding Sessions with the Power of Code Folding</u></a></li>
<li><a href="https://win-awesome.techidaily.com/enhance-your-coding-experience-with-emeditors-minimalzen-color-theme-for-text-editors/"><u>Enhance Your Coding Experience with EmEditor's MinimalZen Color Theme for Text Editors</u></a></li>
<li><a href="https://fox-direct.techidaily.com/in-2024-dive-into-apods-an-uncomplicated-download-guide/"><u>In 2024, Dive Into APods An Uncomplicated Download Guide</u></a></li>
<li><a href="https://review-topics.techidaily.com/infinix-smart-8-hd-support-turn-off-screen-lock-by-drfone-android-unlock-android-unlock/"><u>Infinix Smart 8 HD support - Turn Off Screen Lock.</u></a></li>
<li><a href="https://win-awesome.techidaily.com/maintaining-concentration-with-emeditor-solutions-for-post-output-distraction-issues/"><u>Maintaining Concentration with EmEditor - Solutions for Post-Output Distraction Issues</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/premium-voice-capture-apps-on-mac-the-best-five-ranked-for-2024/"><u>Premium Voice Capture Apps on Mac The Best Five Ranked for 2024</u></a></li>
<li><a href="https://win-awesome.techidaily.com/understanding-text-file-encoding-in-emeditor-why-reloading-wont-change-it/"><u>Understanding Text File Encoding in EmEditor - Why Reloading Won't Change It</u></a></li>
<li><a href="https://tech-revival.techidaily.com/iphonedvdand/"><u>プロ並みiPhone動画DVD化：高画質&スムーズ、コンビニ手順解説</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134244/18498" target="_top" id="2134244">
  <img src="//a.impactradius-go.com/display-ad/18498-2134244" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134244/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

