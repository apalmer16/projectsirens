---
title: Research Begins
layout: post
---

Most voice-to-text API's have a cost associated with using them (Google Cloud Voice-to-text, IBM's Watson, etc). Therefore, the options for a free voice command system is limited to either being one that can smartly use a built-in voice-to-text system based on what OS the game is running on or using the free API called [wit.ai](https://wit.ai) that is now owned by Facebook.

This week I decided to start trying out [wit.ai](https://wit.ai). When using [wit.ai](https://wit.ai), the first thing that must be done is creation of an app. With an app created, I proceded to have the app train for a few different movement commands that would be possible in a real-time strategy game ("Unit 7 go to the enemy base", "Move Unit 7 to the enemy base", and "Captain Mixin, move to A7"). These commands all were linked to the same intent (move), and have two entities (troop_name and move_destination) which [wit.ai](https://wit.ai) is supposed to parse from the utterance.

I proceded to test how well it is doing by running the command `curl -H 'Authorization: Bearer $TOKEN' 'https://api.wit.ai/message?v=20200920&q=Move%20Unit%2037%20to%20A50'`. Running this command, I got a response that indicated [wit.ai](https://wit.ai) had successfully found the intent of 'move' with confidence level of 100%, and it found the troop_name of 'Unit 37' (71.79% certainty) and destination of 'A50' (72.63% certainty).

After noting this information, I opened the [wit.ai](https://wit.ai) dashboard and found the new utterance in there and was able to easily add it to the utterances already present. I proceded to add several more variations using this process to help improve the accuracy.

I proceeded to start sending actual voice commands through by recording the audio in Voice Recorder, converting to mp3, and sending that via a curl request like this: `curl -XPOST 'https://api.wit.ai/speech?v=20200513' -i -L -H "Authorization: Bearer $TOKEN" -H "Content-Type: audio/mpeg3" --data-binary "@Recording.mp3"`. Through this process I brought the number of trained examples to 33.

Next I began work on setting up a way to record audio and send it through to [wit.ai](https://wit.ai), which is still in progress as I have ran into some issues setting it up.

From this I've learned that it needs as much data as possible, which means if this is to be officially used, data from testing phases should be used to improve the reliability of the NLP and voice-to-text system through the method above. It also would be quite valuable to port the app data to similar projects, so a company that produces mainly one type of game could use that data over again to improve the starting quality of their voice command system in their next game.

The next steps I plan on taking are creating some more intents and finishing setting up some C# unity code that interfaces with the API.
