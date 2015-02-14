---
layout: post
title: "Littlstar v1.2.0 Release"
date: 2015-02-14
author: Dominic
category: Announcements
---

Today, the Littlstar team is proud to announce the latest release of the [Littlstar](https://littlstar.com) web app and [API](http://developer.littlstar.com/docs) (v1.2.0). Many hours have been spent discussing, pondering, debating and arguing over what wonderful functionality our users should have access to next. We've consulted with content producers, listened to user feedback, and distilled the most important topics into this release. Much has changed while much has stayed the same. We strive to always provide new features and functionality while maintaining a consistent experience. This announcement will highlight some of the most interesting features, with a focus on those that primarily affect our developer community.

First and foremost there are new [terms](http://developer.littlstar.com/terms/) regarding the usage of the Littlstar API. Please read and follow these terms.

### Video Endpoints

* New versions are now being created by our transcoder (vr, download) and these are now included in the video JSON response.
* A new [endpoint](http://developer.littlstar.com/docs/#vr-videos) specifically designed to deliver high quality VR content has been created.
* Videos marked as "hidden" by their creator are now conditionally returned in the [User Videos](http://developer.littlstar.com/docs/#user-videos) response.
* A new [endpoint](http://developer.littlstar.com/docs/#video-search) has been added to search for videos.

### Category Endpoints

* Category [endpoints](http://developer.littlstar.com/docs/#categories) have been improved to provide counts of the content that's been assigned to them.

### Photo Endpoints

Oh wait, did we forget to mention at the start of this announcement that Littlstar now supports photos alongside our existing video support? Sorry about that!! But it's true, registered users are now free to upload both photos and videos. The API has been updated to provide the same or similar [endpoints](http://developer.littlstar.com/docs/#photos) for photos that already exist for videos. We are just getting started with photo support, so please be patient and stay tuned - we have much planned for the future of this functionality.

This is one of the largest releases, in terms of functionality, in Littlstar's short history. As always, for all the latest info please [subscribe](/feed.xml) or [follow us]({{ site.social.twitter.url }}), and if you'd like to reach out to let us know what else you want to see on the platform (or even just to let us know how awesome you think we are) please [contact us](mailto:support@littlstar.com) directly.

Sincerely,

The Littlstar Team
