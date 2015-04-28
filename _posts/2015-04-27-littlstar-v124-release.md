---
layout: post
title: "Littlstar v1.2.4 Release"
date: 2015-04-27
author: Dominic
category: Announcements
---

Today, the Littlstar team is proud to announce the latest release of the [Littlstar](https://littlstar.com) web app and [API](http://developer.littlstar.com/docs) (v1.2.4). Many hours have been spent discussing, pondering, debating and arguing over what wonderful functionality our users should have access to next. We've consulted with content producers, listened to user feedback, and distilled the most important topics into this release. Much has changed while much has stayed the same. We strive to always provide new features and functionality while maintaining a consistent experience. This announcement will highlight some of the most interesting features, with a focus on those that primarily affect our developer community.

The main focus of the v1.2.4 release cycle was centered on improving both the look and feel of the upload interface and the infrastructure responsible for re-encoding, or transcoding, videos and photos into the versions necessary to support as many devices as possible. A brand new multi-upload interface has been built and a custom transcoding service has been created to accomplish these goals. This release is only a first step; there are many new features and functionality planned for future releases. We also took this opportunity to normalize some internal processes we use to store and organize content uploaded to Littlstar. This normalization required changes to API responses that are outlined below.

### Photo Endpoints

All API endpoints responsible for returning a photo's details have been altered to reflect a more normalized naming convention as well as to match that of video responses. The paths to each photo size used to be called "posters," they are now properly referred to as "versions." The [API Documentation](http://developer.littlstar.com/docs) has been updated to reflect this change.

#### List of Affected Endpoints

* [All Photos](http://developer.littlstar.com/docs/#all-photos)
* [Featured Photos](http://developer.littlstar.com/docs/#featured-photos)
* [Latest Photos](http://developer.littlstar.com/docs/#latest-photos)
* [VR Photos](http://developer.littlstar.com/docs/#vr-photos)
* [Single Photo](http://developer.littlstar.com/docs/#single-photo)
* [Photo Search](http://developer.littlstar.com/docs/#photo-search)
* [User Photos](http://developer.littlstar.com/docs/#user-photos)
* [Category Photos](http://developer.littlstar.com/docs/#category-photos)
* [Hashtag Photos](http://developer.littlstar.com/docs/#hashtag-photos)

We've also updated our [Content Guide](http://developer.littlstar.com/content-guide/) to reflect the changes to uploading and transcoding. As always, for all the latest info please [subscribe](/feed.xml) or [follow us]({{ site.social.twitter.url }}), and if you'd like to reach out to let us know what else you want to see on the platform (or even just to let us know how awesome you think we are) please [contact us](mailto:support@littlstar.com) directly.

Stay excellent,

The Littlstar Team
