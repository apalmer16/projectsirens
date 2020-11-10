---
title: The End For Project Siren?
layout: published
published: false
---

# Wit.AI and Last Weeks Issues
I tried to more thouroghly test to see why the problems from last week were arrising. First I turned the visibility of my app to private, in case that affects the voice-to-text stage.
- Giving move commands in the format "Move <unit_name> to <location>" or "Send <unit_name> to <location>" is generally transcribed correctly.
- Giving move commands in the format "Move <unit_name1> and <unit_name2> to <location>" or "Send <unit_name1> and <unit_name2> to <location>" are mostly right, but mess up more than with a single unit name.
- Giving move commands in the format "<unit_name(s)> move to <location>" are terrible at being interpreted.

Since all my previous attack commands had been of the form "<unit_name> attack <target>", the issue could be starting with the unit name. However, I am unsure of a different structure for attack commands (Maybe "Attack <target> with <unit_name(s)>"?).

# Web Captioner Research
I also spent some time looking into what Web Captioner uses as suggested by Prof. Austin Yarger. They use Web Speech API for their voice-to-text. However, it isn't like a normal API. It is the type of API that is ONLY usable by browsers (and only certain ones at that), much like setTimeout, setInterval, etc. Therefore I don't believe it is of any use to me, though in theory it could be used in a webgl build (not exactly sure how though).

# Trial and Attack
Attack commands of the form "<unit_name> attack <target>" still are failing. Therefore I decided to test attack commands of the form "Attack <target> with <unit_name(s)>".
While this did work more often, it was still failing more often than the top two types of movement commands.
