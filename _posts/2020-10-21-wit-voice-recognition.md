---
title: Wit Voice Parsing Issues
layout: post
published: false
---
# Wit and Maps
Last week, I noticed it seemed that wit.ai was not decteding map squares (ie A4, B6, etc). Therefore I started by seeing if it could be trained to recognize them. After two hours, I've had one success (with A8). Another hour later, I've had only two more successes, both on H8. As I continued to try and train it to recognise this system, I seemed to be slowly building success. However after a total of six hours I decided it is a huge pain to try and get that working though correcting, and have emailed them about it.

# Next Step
While waiting on a response, I decided to spend some time thinking if there are other possible was to move in rts games beside the A4-style grid. My thoughts have two main possiblities.
1. A coordinate-grid system (ie (0, 0)). While a good idea, I don't believe this is used in any rts games, and thus may be weird or unnatural to use.
2. A landmark-based system (ie forest on the right), may be good, but likely hard to implement or slow to use.

Therefore I began testing if wit.ai could handle these two possibilities.
