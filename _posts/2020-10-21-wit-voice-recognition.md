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

# Coordinate-grid System
I spent an hour and a half trying different possible coordinate grid values, and it was correct 61/66 times. Difficulties included (1, 1), (2, 2), (-5, 5), (1, -1), (-4, -4). However this difficulty only occured the first time I said these values, as the second try (after training and correcting) was correct.

# Landmark-based System
This one seems reliable from the hour of tests, however it could be hard to implement and actual system that would use it.
