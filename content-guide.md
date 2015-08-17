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
3. <a href="#mobile-web">Mobile Web</a>
4. <a href="#mobile-apps">Mobile Apps</a>
5. <a href="#api">API</a>
6. <a href="#3d">3D</a>

### Uploads

Once you've successfully [registered](https://littlstar.com/register) for a new account and [logged in](https://littlstar.com/login), you are free to begin [uploading](http://littlstar.com/uploads). The Littlstar platform supports both videos and photos. Our upload form allows you to drag-and-drop or click and select up to 10 videos or photos or any combination of the two simultaneously. Each individual file upload is presented as an individual form allowing you to edit the details for that file while your upload progresses. A title is **required** but the remainder of the information is optional.

#### Categories

Adding your video or photo to one or more categories helps to better organize your content and allows us to present it to other Littlstar users that have indicated their interest in these categories. Each category is available from the left-hand side menu of our web interface and in our [Android][] or [iOS][] mobile apps. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#categories).

#### Hashtags

Hashtags offer more fine-grained and dynamic control over the organization of your video or photo on the Littlstar platform. They foster a community driven discovery engine that grows more and more powerful as content continues to be added and updated. To "[#hashtag](https://en.wikipedia.org/wiki/Hashtag)" your video or photo, simply include as many as you'd like in its description. Our system will handle creating the links to connect all hashtags across the platform. Each hashtag entered into your photo or video description will link to a page where all other videos and photos that share that hashtag are displayed. You can enter hashtags when you first create your photo or video and also when editing it. They can also be independently requested and consumed through our RESTful [API](http://developer.littlstar.com/docs/#hashtags).

#### Visibility

If for whatever reason you are not ready for your content to be publicly consumed, you can mark it as hidden. This will prevent your video or photo from being visible to any other user and removes it from search results. They will only be visible to you when you are [logged in](https://littlstar.com/login). We are in the process of improving this functionality to provide more fine-grained control over when and where your content can be viewed.

#### Downloads

An uploaded video can be marked as "downloadable." When you check "Enable Downloads" a button will be displayed below the video when it is viewed on Littlstar, and an additional version will be included in [API](http://developer.littlstar.com/docs/#videos) responses. These high quality VR optimized versions of your video are intended for local/offline viewing in a VR headset like the [Oculus Rift](https://www.oculus.com/) or [GearVR](http://www.samsung.com/global/microsite/gearvr/index.html).

The following sections will further explain what specifically happens to your videos and photos once they've been successfully uploaded and how they are displayed across different devices.

### Encoding

The consummate staple of our platform lies in how your video or photo is manipulated into the various "versions" that are presented to a user and their device when they view the beauty you've digitally captured across our platform. This is a herculean task. We stand squarely on the precipice of a divide that will change the very nature of how we perceive reality and do not take this responsibility lightly. In an attempt to deliver your vision to as many end users as possible, we must make certain assumptions and take very specific actions to normalize this new experience. The following subsections describe the specifics around what happens to your content once it's been ingested by our platform.

#### Suggestions

As with any digitally captured video or photo, **the higher the original quality the better the final result will be after any manipulation has occurred**. To experience the best results on our platform and to enable proper display across as many devices as possible, we recommend the following original file specifications:

**Original Video Specs**
File Size: Max 5GB
Width: 4096 pixels (4K)
Codec: h.264
Format: mp4
FPS: 60
Bitrate: high as possible

**Original Photo Specs**
File Size: Max 5GB
Format: JPEG, PNG

These are not the **required** specifications, merely the **suggested** format and encoding settings that we've found to produce the highest quality output. The Littlstar platform will make every attempt to properly convert your originally uploaded file into the versions needed for properly optimized delivery.

#### Videos

When you upload a new video to Littlstar we re-encode, or transcode, it into multiple versions that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. We are working on a public HTTP import URL feature which will allow for sizes in excess of this limit. These versions have been designed to work across the maximum number of devices and clients. A 2K **web** and **webm** version will be displayed to visitors on the web. A 1K **mobile** version is displayed on [Android][] and [iOS][] devices. A **VR** version is returned in [API](http://developer.littlstar.com/docs/#videos) responses so it can be displayed in advanced Head Mounted Displays (HMDs) like the GearVR. If downloads are enabled during video creation, or while editing an existing video, a **download** version will be exposed through a button below the video on the web, as well as in API responses, so it can be downloaded and consumed locally in an [Oculus Rift](https://www.oculus.com/) or [GearVR](http://www.samsung.com/global/microsite/gearvr/index.html) style HMD.

##### Posters

Also known as "holdframes," the Littlstar platform will create a "poster image" that is used to display gallery or index pages of videos. These posters are taken from your video during transcoding, and we make every attempt to choose a poster from far enough into the video to ensure a properly representative image is obtained to reflect the content of your video. In the future we will expose the functionality to submit your own posters through our web interface.

##### Banners

A banner is a great way to further promote your video to a wider audience and serves as a kind of advertisement for your video. Banners are **suggested** if you would like your video to be **featured** and **required** if you would like your video to be **sponsored** on our platform. Currently, a banner can only be applied by [specifically requesting](mailto:support@littlstar.com?subject=VIdeo%20Banner%20Request) that one be applied manually by a member of our team. We are working on an automated system that will allow you to apply and replace a banner whenever you wish. When submitting a request for a new banner, please include a JPG image that is at least 1600px wide.

#### Photos

When you upload a new photo to Littlstar we process it into four specific versions (in addition to the originally uploaded photo) that are designed to be consumed across various devices and mediums. **The file size limit for uploads though our web interface is currently 5GB**. We are working on a public HTTP import URL feature which will allow for sizes in excess of this limit. These versions have been designed to work across the maximum number of devices and clients. Each version is used to display your photo in specific sections and areas across our platform. However, the originally uploaded photo is used in our player on that photo's page to ensure every visitor experiences your photo at its maximum resolution and quality.

### Mobile Web

The performance requirements to truly enjoy this type of content means that a native app is almost a requirement. There is a limitation currently in the iPhone iOS operating system that prevents a mobile web page from playing both a video and audio stream simultaneously using WebGL, which is the technology required to play this type of video content. We are continuously investigating solutions to this limitation but a fix seems to be squarely in the hands of Apple for the foreseeable future. If we can find a work-around we will release it as soon as it is ready.

Many of the currently available mobile browsers (Safari, Chrome, Firefox, etc) are steadily adding features to better support the rendering and playback of 360&deg; content. The current limitations are mostly confined to video playback, you should not experience any issues with photos. To date we have experienced the best support from [Chrome](https://www.google.com/chrome/browser/desktop/index.html) on all devices and operating systems.

### Mobile Apps

Littlstar currently has native applications available for both [Android][] and [iOS][] devices. Both of these applications are currently in **beta** release and are under heavy development. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=Mobile%20App%20Feedback) directly.

### API

The [Littlstar API](http://developer.littlstar.com/docs) exposes RESTful endpoints for the programmatic consumption of 360 degree content that has been uploaded to our platform. Version 1 of our API is currently in an **alpha** state, and as such all users should expect rapid changes and frequent breaks of backward compatibility. We are working hard everyday to improve the currently available functionality while adding more interactive features. If you have feedback about any issues you encounter or features/functionality that you would like to see added/improved, please [contact us](mailto:support@littlstar.com?subject=API%20Feedback) directly.

<h3 id="3d">3D</h3>

We are currently working closely with select content producers and early adopters to build 3D support into the platform. If you would like to be part of this process, please [contact us](mailto:support@littlstar.com?subject=3D%20Beta%20Testing) for more information on how to get involved.

[Android]: http://lstar.co/android "Littlstar Android App"
[iOS]: http://lstar.co/ios "Littlstar iOS App"