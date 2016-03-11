---
layout: page
title: Content Guide
permalink: /content-guide/
---

The Littlstar platform has been designed from the ground up to fully support both 360&deg; videos and photos. Our ongoing goal is to provide access to the content you upload to as many different devices as possible. As mass consumer adoption of 360&deg; content is still in its infancy, we are forced to make some tough choices when it comes to when and where your content will be displayed. We will continually strive to expand the reach of your content across our network as new technologies and capabilities become more widely available. This guide will cover some basic background information regarding the best practices around uploading and viewing your content.

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
4. <a href="#mobile-web">Mobile Web</a>
5. <a href="#mobile-apps">Mobile Apps</a>
6. <a href="#api">API</a>
7. <a href="#3d">3D</a>

### Uploads

Once you've successfully [registered](https://littlstar.com/register) for a new account and [logged in](https://littlstar.com/login), you are free to begin [uploading](http://littlstar.com/uploads). The Littlstar platform supports both videos and photos. Our upload form allows you to drag-and-drop or click and select up to 10 videos or photos or any combination of the two simultaneously. Each individual file upload is presented as an individual form allowing you to edit the details for that file while your upload progresses. A title is **required** but the remainder of the information is optional. The Littlstar uploader currently supports the mpg, mp4, m4v, avi, ogg, mov, webm, flv, jpg, and png file types.

#### Categories

Adding your video or photo to one or more categories helps to better organize your content and allows us to present it to other Littlstar users that have indicated their interest in these categories. Each category is available from the left-hand side menu of our web interface and in our [Android][] or [iOS][] mobile apps. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#categories).

#### Hashtags

Hashtags offer more fine-grained and dynamic control over the organization of your video or photo on the Littlstar platform. They foster a community driven discovery engine that grows more and more powerful as content continues to be added and updated. To "[#hashtag](https://en.wikipedia.org/wiki/Hashtag)" your video or photo, simply include as many as you'd like in its description. Our system will handle creating the links to connect all hashtags across the platform. Each hashtag entered into your photo or video description will link to a page where all other videos and photos that share that hashtag are displayed. You can enter hashtags when you first create your photo or video and also when editing it. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#hashtags).

#### Visibility

If for whatever reason you are not ready for your content to be publicly consumed, you can mark it as hidden. This will prevent your video or photo from being visible to any other user and removes it from search results. They will only be visible to you when you are [logged in](https://littlstar.com/login). We are in the process of improving this functionality to provide more fine-grained control over when and where your content can be viewed.

#### Downloads

An uploaded video can be marked as "downloadable." When you check "Enable Downloads" a button will be displayed below the video when it is viewed on Littlstar, and an additional version will be included in [API](http://developer.littlstar.com/docs/#videos) responses. These high quality VR optimized versions of your video are intended for local/offline viewing in a VR headset like the [Oculus Rift](https://www.oculus.com/), [OSVR](http://www.osvr.org/), or [GearVR](http://www.samsung.com/global/microsite/gearvr/index.html).

The following sections will further explain what specifically happens to your videos and photos once they've been successfully uploaded and how they are displayed across different devices.

### Encoding

The consummate staple of our platform lies in how your video or photo is manipulated into the various "versions" that are presented to a user and their device when they view the beauty you've digitally captured across our platform. This is a herculean task. We stand squarely on the precipice of a divide that will change the very nature of how we perceive reality and do not take this responsibility lightly. In an attempt to deliver your vision to as many end users as possible, we must make certain assumptions and take very specific actions to normalize this new experience. The following subsections describe the specifics around what happens to your content once it's been ingested by our platform.

#### Suggestions

As with any digitally captured video or photo, **the higher the original quality the better the final result will be after any manipulation has occurred**. To experience the best results on our platform and to enable proper display across as many devices as possible, we recommend the following original file specifications:

**Original Video Specs**<br />
File Size: Max 5GB<br />
Width: 4096 pixels (4K)<br />
Codec: h.264<br />
Format: mp4<br />
FPS: 60<br />
Bitrate: high as possible<br />

**Original Photo Specs**<br />
File Size: Max 5GB<br />
Format: JPEG, PNG<br />

These are not the **required** specifications, merely the **suggested** format and encoding settings that we've found to produce the highest quality output. The Littlstar platform will make every attempt to properly convert your originally uploaded file into the versions needed for properly optimized delivery.

#### Videos

When you upload a new video to Littlstar we re-encode, or transcode, it into multiple versions that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. These versions have been designed to work across the maximum number of devices and clients. A 2K **web** and **webm** version will be displayed to visitors on the web. A 1K **mobile** version is displayed on [Android][] and [iOS][] devices. A **VR** version is returned in [API](http://developer.littlstar.com/docs/#videos) responses so it can be displayed in advanced Head Mounted Displays (HMDs) like the GearVR. If downloads are enabled during video creation, or while editing an existing video, a **download** version will be exposed through a button below the video on the web, as well as in API responses, so it can be downloaded and consumed locally in an [Oculus Rift](https://www.oculus.com/), [OSVR](http://www.osvr.org/), or [GearVR](http://www.samsung.com/global/microsite/gearvr/index.html) style HMD.

##### Posters

Also known as "holdframes," the Littlstar platform will create a "poster image" that is used to display gallery or index pages of videos. These posters are taken from your video during transcoding, and we make every attempt to choose a poster from far enough into the video to ensure a properly representative image is obtained to reflect the content of your video. In the future we will expose the functionality to submit your own posters through our web interface.

##### Banners

Banners are an important component of the Littlstar interface, and expression of your content's identity. A banner is a great way to properly brand and promote your video on our platform. Banners are **suggested** if you would like your video to be **featured** and **required** if you would like your video to be **sponsored**. Littlstar banner sizes are 1920x1080px and must be submitted as a .jpg or .png under 1MB to be approved. Please [email](mailto:content@littlstar.com?subject=VIdeo%20Banner%20Request) us your banner and be sure to reference your account username and include a link to your video; one of our team members will notify you when the banner has been approved and applied. Please download our [banner guideline](http://media.littlstar.com/littlstar-banner-guideline.pdf) and formatted PSD [template](http://media.littlstar.com/littlstar-banner-template.psd) to help create the best banner for your video.

*Please note: We are working on an automated system that will allow you to apply and replace a banner whenever you wish.*

#### Photos

When you upload a new photo to Littlstar we process it into four specific versions (in addition to the originally uploaded photo) that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. These versions have been designed to work across the maximum number of devices and clients. Each version is used to display your photo in specific sections and areas across our platform. However, the originally uploaded photo is used in our player on that photo's page to ensure every visitor experiences your photo at its maximum resolution and quality.

### Embedding

Videos and photos uploaded to Littlstar can be embedded in other web pages similarly to YouTube or Vimeo videos. Under the player on single video and photo pages there is a gray button that displays the iframe embed code for that specific piece of content. Simply copy and paste this code into your own web page and the same player you see on Littlstar will be displayed on your site. Our iframe embed feature is capable of identifying a logged in user so when your content is being viewed in an iframe on another site and the viewer is logged into littlstar.com they are able to interact with the content as if they were viewing it on our platform. This means they can star your video or photo right in the embedding page. We will continue to add more and more interactivity to this feature in the future. Please see the [Mobile Web](#mobile-web) section of this guide for information regarding support for rendering of your content on mobile devices.

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

### Mobile Web

The performance requirements to truly enjoy this type of content means that a native app is almost a requirement. Many of the currently available mobile browsers (Safari, Chrome, Firefox, etc) are steadily adding features to better support the rendering and playback of 360&deg; content. The current limitations are mostly confined to video playback. To date we have experienced the best support from [Chrome](https://www.google.com/chrome/browser/desktop/index.html) on all devices and operating systems.

The Littlstar player will attempt to display a video or photo wherever it successfully can. When this is not possible it will "deep link" visitors into the appropriate content in our mobile apps. As browsers and devices adopt the appropriate technologies we will continually update our support where applicable.

### Mobile Apps

Littlstar currently has native applications available for both [Android][] and [iOS][] devices. Both of these applications are currently in **beta** release and are under heavy development. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=Mobile%20App%20Feedback) directly.

### API

The [Littlstar API](http://developer.littlstar.com/docs) exposes RESTful endpoints for the programmatic consumption of 360&deg; content that has been uploaded to our platform. Version 1 of our API is currently in an **alpha** state, and as such all users should expect rapid changes and frequent breaks of backward compatibility. We are working hard everyday to improve the currently available functionality while adding more interactive features. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=API%20Feedback) directly.

<h3 id="3d">3D</h3>

We are currently working closely with select content producers and early adopters to build 3D support into the platform. If you would like to be part of this process, please [contact us](mailto:support@littlstar.com?subject=3D%20Beta%20Testing) for more information on how to get involved.

[Android]: http://lstar.co/android "Littlstar Android App"
[iOS]: http://lstar.co/ios "Littlstar iOS App"