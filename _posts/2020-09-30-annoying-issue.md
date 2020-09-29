---
published: false
title: Audio Pains
layout: post
---
Using information found on the web, I created a C# script that was able to send externally created mp3 files to [wit.ai](https://wit.ai) via Unity, which was resulting in the output below.
![Image](https://i.imgur.com/8Yr3FgR.png)
The next step was to make it so that I could send Unity created audio files through this interface as well, with minimal changes. The library I found converts AudioClips to wav format. Inside Unity, it was failing to send the file, however, I could send it through the terminal and get the expected response.
![Image](https://i.imgur.com/O5ldJu1.png)
![Image](https://i.imgur.com/gYkqkMv.png)
This lead to me undoing the saving and just trying to send through a previously created wav file in Unity.
I tried to troubleshoot this issue and was unable to figure out a reason. Therefore I started to investigate converting the audioclip to mp3. Everything I could find for free required the audio clip to already be in wav format, which was untrue  of my created recording. Therefore I turned to converting the saved wav file to mp3 using the CSAudioConverter library. I ran into an error I could not make sense of, and now am waiting on their support to get back to me.
