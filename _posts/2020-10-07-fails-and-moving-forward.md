---
published: false
title: Away From UnityWebRequests
layout: post
---

When talking with a friend, the thought that endian type is causing my proble came up, however when I tested that fix it still did not work (~30min). Next I decided to try a Unity Store Asset I happened across (which was not easy to find) called [Voice Recorder](https://assetstore.unity.com/packages/tools/audio/voice-recorder-21884), but after 1hr this didn't solve my problem, and my friend managed to find an ancient (6 year old) wit.ai in Unity repository available [here](https://github.com/dariopasquali/Wit.ai-Unity). After about two hours, I was using this repository as a basis for my [wit.ai](https://wit.ai) successfully, as seen below.
![Image](https://i.imgur.com/RiOg9na.png)
However, sometimes the response would be null, which I began to look into. After an hour I seemed to fix the issue by using https instead of http.
