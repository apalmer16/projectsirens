---
title: Away From UnityWebRequests
layout: post
---

When talking with a friend, the thought that endian type is causing my proble came up, however when I tested that fix it still did not work (~30min). Next I decided to try a Unity Store Asset I happened across (which was not easy to find) called [Voice Recorder](https://assetstore.unity.com/packages/tools/audio/voice-recorder-21884), but after 1hr 30min this didn't solve my problem, and my friend managed to find an ancient (6 year old) wit.ai in Unity repository available [here](https://github.com/dariopasquali/Wit.ai-Unity). After about three hours examining and updating the code, I was using this repository as a basis for my [wit.ai](https://wit.ai) successfully, as seen below.

![Image](https://i.imgur.com/RiOg9na.png)

From this working, I determined there were two possibilities for why mine didn't work.
1. UnityWebRequests was messing up the sent info for wav files
2. File.ReadAllBytes method and binaryReader.ReadBytes methods had different results for wav files

Sometimes though the response would be null, which I began to look into. After an hour I seemed to fix the issue by using https instead of http.
Next, since the method the repo used to "parse" the response would add significant overhead for the developer, I began to create a different parser. At first I tried using the built in JSON parser, but it was failing. After a few hours I was able to parse the intent successfully. Now I just need to parse the entities. The parsing took ~6 hours to figure out.
