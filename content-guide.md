---
layout: page
title: Content Guide
permalink: /content-guide/
---

The Littlstar platform has been designed from the ground up to fully support both 360&deg; videos and photos. Our ongoing goal is to provide access to the content you upload on as many different devices as possible. As mass consumer adoption of 360&deg; content is still in its infancy, we are forced to make some tough choices when it comes to when and where your content will be displayed. We will continually strive to expand the reach of your content across our network as new technologies and capabilities become more widely available. This guide will cover some basic background information regarding the best practices around uploading and viewing your content.

1. <a href="#uploads">Uploads</a>
- <a href="#categories">Categories</a>
- <a href="#hashtags">Hashtags</a>
- <a href="#visibility">Visibility</a>
- <a href="#downloads">Downloads</a>
2. <a href="#encoding">Encoding</a>
- <a href="#suggestions">Suggestions</a>
- <a href="#videos">Videos</a>
  - <a href="#posters">Posters</a>
  - <a href="#banners">Banners</a>
- <a href="#photos">Photos</a>
3. <a href="#embedding">Embedding</a>
- <a href="#sharing">Sharing</a>
- <a href="#customization">Customization</a>
4. <a href="#sponsored-vs-featured">Sponsored vs Featured</a>
5. <a href="#head-mounted-displays">Head Mounted Displays</a>
- <a href="#side-loading">Side Loading</a>
6. <a href="#mobile-apps">Mobile Apps</a>
7. <a href="#mobile-web">Mobile Web</a>
8. <a href="#api">API</a>
9. <a href="#3d">3D</a>

### Uploads

Once you've successfully [registered](https://littlstar.com/register) for a new account and [logged in](https://littlstar.com/login), you are free to begin [uploading](https://littlstar.com/uploads). The Littlstar platform supports both videos and photos. Our upload form allows you to drag-and-drop or click and select up to 10 videos or photos or any combination of the two simultaneously. Each individual file upload is presented as an individual form allowing you to edit the details for that file while your upload progresses. A title is **required** but the remainder of the information is optional. The Littlstar uploader currently supports the mpg, mp4, m4v, avi, ogg, mov, webm, flv, jpg, and png file types.

#### Categories

Adding your video or photo to one or more categories helps to better organize your content and allows us to present it to other Littlstar users that have indicated their interest in these categories. Each category is available from the left-hand side menu of our web interface and in our [Android][] or [iOS][] mobile apps. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#categories).

#### Hashtags

Hashtags offer more fine-grained and dynamic control over the organization of your video or photo on the Littlstar platform. They foster a community driven discovery engine that grows more and more powerful as content continues to be added and updated. To "[#hashtag](https://en.wikipedia.org/wiki/Hashtag)" your video or photo, simply include as many as you'd like in its description. Our system will handle creating the links to connect all hashtags across the platform. Each hashtag entered into your photo or video description will link to a page where all other videos and photos that share that hashtag are displayed. You can enter hashtags when you first create your photo or video and also when editing it. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#hashtags).

#### Visibility

If for whatever reason you are not ready for your content to be publicly consumed, you can mark it as hidden. This will prevent your video or photo from being visible to any other user and removes it from search results. They will only be visible to you when you are [logged in](https://littlstar.com/login). We are in the process of improving this functionality to provide more fine-grained control over when and where your content can be viewed.

#### Downloads

An uploaded video can be marked as "downloadable." When you check "Enable Downloads" a button will be displayed below the video when it is viewed on Littlstar, and an additional version will be included in [API](http://developer.littlstar.com/docs/#videos) responses. These high quality VR optimized versions of your video are intended for local/offline viewing in a VR headset like the [Oculus Rift](https://www.oculus.com/) or [GearVR][].

The following sections will further explain what specifically happens to your videos and photos once they've been successfully uploaded and how they are displayed across different devices.

### Encoding

The consummate staple of our platform lies in how your video or photo is manipulated into the various "versions" that are presented to a user and their device when they view the beauty you've digitally captured across our platform. This is a herculean task. We stand squarely on the precipice of a divide that will change the very nature of how we perceive reality and do not take this responsibility lightly. In an attempt to deliver your vision to as many end users as possible, we must make certain assumptions and take very specific actions to normalize this new experience. The following subsections describe the specifics around what happens to your content once it's been ingested by our platform.

#### Suggestions

As with any digitally captured video or photo, **the higher the original quality the better the final result will be after any manipulation has occurred**. To experience the best results on our platform and to enable proper display across as many devices as possible, we recommend the following original file specifications:

**Original Video Specs**<br />
File Size: Max 5GB<br />
Container: mp4<br />
Codec: h.264<br />
Resolution: 4096 pixels (4K)<br />
FPS: 60<br />
Level: 5.2<br />
Profile: High<br />
Bitrate: 40 Mbit<br />
B-Frames: 0<br />
Refs: 1<br />

**Original Photo Specs**<br />
File Size: Max 5GB<br />
Resolution: Recommended 8,000-10,000 pixels (8-10K), Max 16,000 pixels (16K)<br />
Format: JPEG, PNG<br />

These are not the **required** specifications, merely the **suggested** format and encoding settings that we've found to produce the highest quality output. The Littlstar platform will make every attempt to properly convert your originally uploaded file into the versions needed for properly optimized delivery.

#### Videos

When you upload a new video to Littlstar we re-encode, or transcode, it into multiple versions that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. These versions have been designed to work across the maximum number of devices and clients. A 1K or 2K **web** version will be displayed to visitors on the web. A 1K **mobile** version is displayed on [Android][] and [iOS][] devices. A **VR** version is returned in [API](http://developer.littlstar.com/docs/#videos) responses so it can be displayed in advanced [Head Mounted Displays](#head-mounted-displays) (HMDs) like the [Oculus Rift](https://www.oculus.com/) or [GearVR][]. If downloads are enabled during video creation, or while editing an existing video, a **download** version will be exposed through a button below the video on the web, as well as in API responses, so it can be downloaded and consumed locally in an [Oculus Rift](https://www.oculus.com/) or [GearVR][] style HMD.

##### Posters

Also known as "holdframes," the Littlstar platform will create a "poster image" that is used to display gallery or index pages of videos. These posters are taken from your video during transcoding, and we make every attempt to choose a poster from far enough into the video to ensure a properly representative image is obtained to reflect the content of your video. In the future we will expose the functionality to choose from multiple poster options or submit your own posters through our web interface.

##### Banners

Banners are an important component of the Littlstar interface, and expression of your content's identity. A banner is a great way to properly brand and promote your video on our platform. Banners are **suggested** if you would like your video to be [featured](#sponsored-vs-featured) and **required** if you would like your video to be [sponsored](#sponsored-vs-featured). Littlstar banner sizes are 1920x1080px and must be submitted as a .jpg or .png under 1MB to be approved. Please [email](mailto:content@littlstar.com?subject=Video%20Banner%20Request) us your banner and be sure to reference your account username and include a link to your video; one of our team members will notify you when the banner has been approved and applied. Please download our [banner guideline](http://media.littlstar.com/littlstar-banner-guideline.pdf) and formatted PSD [template](http://media.littlstar.com/littlstar-banner-template.psd) to help create the best banner for your video.

*Please note: We are working on an automated system that will allow you to apply and replace a banner whenever you wish.*

#### Photos

When you upload a new photo to Littlstar we process it into four specific versions (in addition to the originally uploaded photo) that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. These versions have been designed to work across the maximum number of devices and clients. Each version is used to display your photo in specific sections and areas across our platform.

### Embedding

Videos and photos uploaded to Littlstar can be embedded in other web pages similarly to YouTube or Vimeo videos. Under the player on single video and photo pages there is a gray "Embed" button that displays the iframe embed code for that specific piece of content. Simply copy and paste this code into your own web page and the same player you see on Littlstar will be displayed on your site. Our iframe embed feature is capable of identifying a logged in user so when your content is being viewed in an iframe on another site and the viewer is logged into littlstar.com they are able to interact with the content as if they were viewing it on our platform. This means they can star your video or photo right in the embedding page. We will continue to add more and more interactivity to this feature in the future. Please see the [Mobile Web](#mobile-web) section of this guide for information regarding support for rendering of your content on mobile devices.

#### Sharing

Embedded videos and photos can be shared out to social media by visitors to your site. The Littlstar embed player allows sharing to Facebook, Twitter, Google+ and direct email. The sharing menu is available from the top of the player and displays a short link for easy copy-paste sharing as well as the list of available social networks.

#### Customization

##### Query Parameters

The embed player will accept four query parameter overrides that can be used to customize the experience on a per embed basis. Each of the query parameters are outlined below showing their default value along with a short description of what they do.

1. `autoplay=false` - Enable or disable automatic playback when the embed player is rendered.
2. `loop=false` - Enable or disable automatic looping of a video when it is complete.
3. `time=0` - Start time of the video in seconds.
4. `fov=NUMBER` - Defines the initial Field of View for the content. By default the Littlstar player will mathematically determine an optimal FOV based on the content's dimensions. Minimum value is 0 and maximum value is 150.

Here is an example of an embedded video showing how each of the above parameters can be overridden:

`<iframe src='//embed.littlstar.com/videos/405?autoplay=true&loop=true&time=30&fov=100' width='640px' height='360px' class='lsplayer-frame' frameborder='0' allowfullscreen></iframe>`

We have also assembled some example code showing how our embed player should be wrapped with the optimal HTML/CSS structure to ensure the player remains contained inside its parent element while maintaining proper aspect ratio:

https://gist.github.com/jwerle/ba9ee6212fdcd6a3fd94

##### Javascript SDK

In addition to the URL specific query parameter overrides outlined above, we offer a Javascript SDK that can be included on your site that offers advanced configuration and control options for one or more iframes. This SDK exposes each iframe element on the page individually through an emitted Javascript event so you can customize each piece of content dynamically - while your page is loading. For more in-depth documentation and examples please see the [official documentation](http://developer.littlstar.com/lsplayer-iframe-sdk/doc/).

### Sponsored vs Featured

Sponsored and featured videos are prominently displayed by our platform on the web, in our mobile apps, and in our advanced VR Head Mounted Displays (HMDs) like the [Oculus Rift](https://www.oculus.com/) or [GearVR][]. Sponsored and featured videos are curated by our Content Team and are selected based on the content in the piece as well as the professional quality of the video and its banner.

Sponsored videos are showcased in the large hero section at the top of our [homepage](https://littlstar.com), as well as within any [categories](https://littlstar.com/categories) to which that video has been added. In our mobile apps sponsored videos appear before all other videos in the Home tab as well as in the top horizontal slider of the Discover tab.

Featured videos are presented in horizontal sliders on our homepage and any categories to which that video has been added. In our mobile apps featured videos appear after all sponsored videos in the Home tab.

To have one of your videos considered for sponsored or featured status, you must submit your request and [banner](#banners) creative to our Content Team for approval. Please [email](mailto:content@littlstar.com?subject=Video%20Sponsor%20Feature%20Request) us and be sure to reference your account username and include a link to your video; one of our team members will contact you after your request has been reviewed.

### Head Mounted Displays

Head Mounted Displays (or HMDs) are advanced VR headsets like the [Oculus Rift](https://www.oculus.com/) or [GearVR][]. Littlstar was the first 360&deg; content distribution network to offer a GearVR app and we continue to lead the way in experiencing this new medium in advanced VR headsets. All VR approved videos are curated and individually chosen by our Content Team and are selected based on the content in the piece as well as the professional quality of the video. If you would like your content included in our VR Cinema app please [email](mailto:content@littlstar.com?subject=VR%20Cinema%20Request) us and be sure to reference your account username and include a link to your video; one of our team members will contact you after your request has been reviewed.

#### Side Loading

The GearVR from Samsung has always offered the ability to view local videos through a feature called side loading. This involves copying a piece of content into a specific folder on the device's (Galaxy S6, S7, S7 Edge, and Note 5) internal storage. The Littlstar [GearVR][] VR Cinema app also supports this side loading functionality. This feature is intended for content creators to better test their content within the context of our app and VR UI. It is not intended to accurately represent the experience that a Littlstar end user will experience as our transcode settings may differ from those of your test content. Here are the step by step instructions to get your test content onto your device and properly displayed in the Littlstar GearVR VR Cinema app:

1. Update to the latest version of our app from inside the Oculus app on your device.

2. Connect your device to your computer using a USB cable and create a folder in the root directory of your phone. The folder should be named "Littlstar" (capitalization does not matter). This folder must live alongside other folders like Pictures, Documents, DCIM, Android, etc.

3. Any video copied into the folder will appear in the "Library" section of the left panel in our app's UI; the same location as any videos that you've downloaded while in the app.

4. We have tried to maintain file naming conventions already established by Oculus/Samsung. Therefore, you must append to the video's filename a specific set of letters to instruct our app as to the appropriate rendering system:

* For over/under (top/bottom) stereoscopic: filename_OU.mp4 or filename_TB.mp4

* For side-by-side stereoscopic: filename_SBS.mp4 or filename_LR.mp4 or filename_RL.mp4

Capitalization does not matter here either. They are only capitalized above to emphasize the available options. After following the above steps you should be able to insert your phone into your GearVR headset and launch our app, then navigate to the Library section in the left panel and select the video you'd like to watch.

### Mobile Apps

Littlstar currently has native applications available for both [Android][] and [iOS][] devices. Both of these applications are currently in **beta** release and are under heavy development. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=Mobile%20App%20Feedback) directly.

### Mobile Web

The performance requirements to truly enjoy this type of content means that a native app is almost a requirement. Many of the currently available mobile browsers (Safari, Chrome, Firefox, etc) are steadily adding features to better support the rendering and playback of 360&deg; content. The current limitations are mostly confined to video playback. To date we have experienced the best support from [Chrome](https://www.google.com/chrome/browser/desktop/index.html) on all devices and operating systems.

The Littlstar player will attempt to display a video or photo wherever it successfully can. When this is not possible it will "deep link" visitors into the appropriate content in our mobile apps. As browsers and devices adopt the appropriate technologies we will continually update our support where applicable.

### API

The [Littlstar API](http://developer.littlstar.com/docs) exposes RESTful endpoints for the programmatic consumption of 360&deg; content that has been uploaded to our platform. Version 1 of our API was officially deprecated on 4/13/2016, and will reach End of Life on 1/1/2017. We are hard at work creating the next generation of our RESTful API to provide more robust functionality as well as more security and control over access to your content. Please see [here](http://developer.littlstar.com/announcements/2016/04/13/littlstar-v1-api-deprecation.html) for more information. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=API%20Feedback) directly.

<h3 id="3d">3D</h3>

We are currently working closely with select content producers and early adopters to build 3D support into the platform. If you would like to be part of this process, please [contact us](mailto:content@littlstar.com?subject=3D%20Beta%20Testing) for more information on how to get involved.

[Android]: http://lstar.co/android "Littlstar Android App"
[iOS]: http://lstar.co/ios "Littlstar iOS App"
[GearVR]: http://lstar.co/gearvr "Littlstar GearVR App"
