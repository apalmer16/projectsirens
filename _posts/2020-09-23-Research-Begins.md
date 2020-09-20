---
title: Research Begins
layout: post
published: false
---

Most voice-to-text API's have a cost associated with using them (Google Cloud Voice-to-text, IBM's Watson, etc). Therefore, the options for a free voice command system is limited to either being one that can smartly use a built-in voice-to-text system based on what OS the game is running on or using the free API called [wit.ai](https://wit.ai) that is now owned by Facebook.

This week I decided to start trying out [wit.ai](https://wit.ai). When using [wit.ai](https://wit.ai), the first thing that must be done is creation of an app. With an app created, I proceded to have the app train for a few different movement commands that would be possible in a real-time strategy game ("Unit 7 go to the enemy base", "Move Unit 7 to the enemy base", and "Captain Mixin, move to A7"). These commands all were linked to the same intent (move), and have two entities (troop_name and move_destination) which [wit.ai](https://wit.ai) is supposed to parse from the utterance.
