---
layout: post
title: "Littlstar v1.2.2 Release"
date: 2015-03-05
author: Dominic
category: Announcements
---

Today, the Littlstar team is proud to announce the latest release of the [Littlstar](https://littlstar.com) web app and [API](http://developer.littlstar.com/docs) (v1.2.2). Many hours have been spent discussing, pondering, debating and arguing over what wonderful functionality our users should have access to next. We've consulted with content producers, listened to user feedback, and distilled the most important topics into this release. Much has changed while much has stayed the same. We strive to always provide new features and functionality while maintaining a consistent experience. This announcement will highlight some of the most interesting features, with a focus on those that primarily affect our developer community.

First and foremost we've created a new [Content Guide](http://developer.littlstar.com/content-guide/) outlining some of the basics around uploading to Littlstar and what happens to your videos and photos once they've been received by our platform. Please check it out and let us know what you think.

### Hashtags

Littlstar now supports the ability to [#hashtag](https://en.wikipedia.org/wiki/Hashtag) a photo or video. Simply include any number of hashtags in your description and our system will handle creating the links to connect all hashtags across the platform. For more information please see the new [Content Guide](http://developer.littlstar.com/content-guide/#hashtags).

### Hashtag Endpoints

* The [All Hashtags](http://developer.littlstar.com/docs/#all-hashtags) endpoint returns a paginated array of all hashtags.
* The [Single Hashtag](http://developer.littlstar.com/docs/#single-hashtag) endpoint returns the details for the requested hashtag.
* The [Hashtag Videos](http://developer.littlstar.com/docs/#hashtag-videos) endpoint returns a paginated array of all videos with the requested hashtag.
* The [Hashtag Photos](http://developer.littlstar.com/docs/#hashtag-photos) endpoint returns a paginated array of all photos with the requested hashtag.

### Video Endpoints

* A new `hashtag_list` array property is now returned in [video responses](http://developer.littlstar.com/docs/#videos) that includes all hashtags currently associated with that video.

### Photo Endpoints

* A new `hashtag_list` array property is now returned in [photo responses](http://developer.littlstar.com/docs/#photos) that includes all hashtags currently associated with that photo.
* The URL to the originally uploaded photo is now included in photo responses.

As always, for all the latest info please [subscribe](/feed.xml) or [follow us]({{ site.social.twitter.url }}), and if you'd like to reach out to let us know what else you want to see on the platform (or even just to let us know how awesome you think we are) please [contact us](mailto:support@littlstar.com) directly.

Sincerely,

The Littlstar Team
