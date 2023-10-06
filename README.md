# SeaquestPPO

**Project Description:**

In this project, a reinforcement learning agent was made to play the game Breakout using Stable Baselines3 library for the atari game Seaquest.

**Game Description:**

You control a sub able to move in all directions and fire torpedoes. The goal is to retrieve as many divers as you can, while dodging and blasting enemy subs and killer sharks; points will be awarded accordingly. The game begins with one sub and three waiting on the horizon. Each time you increase your score by 10,000 points, an extra sub will be delivered to yourbase. You can only have six reserve subs on the screen at one time. Your sub will explode if it collides with anything except your own divers. The sub has a limited amount of oxygen that decreases at a constant rate during the game. When the oxygen tank is almost empty, you need to surface and if you don’t do it in time, your sub will blow up and you’ll lose one diver. Each time you’re forced to surface, with less than six divers, you lose one diver as well.


**Actions:**

Breakout has the action space of Discrete(18) i.e 0,1,...,17.

*0-NOOP*

*1-FIRE*

*2-UP*

*3-RIGHT*

*4-lEFT*

*5-DOWN*

*6-UPRIGHT*

*7-UPLEFT*

*8-DOWNRIGHT*

*9-DOWNLEFT*

*10-UPFIRE*

*11-RIGHTFIRE*

*12-lEFTFIRE*

*13-DOWNFIRE*

*14-UPRIGHTFIRE*

*15-UPLEFTFIRE*

*16-DOWNRIGHTFIRE*

*17-DOWNLEFTFIRE*


**Observation:**

The observation is a numpy array of the game screen.

**Rewards:**

Score points are your only reward.

Blasting enemy sub and killer shark is worth 20 points. Every time you surface with six divers, the value of enemy subs and killer sharks increases by 10, up to a maximum of 90 points each.

Rescued divers start at 50 points each. Then, their point value increases by 50, every time you surface, up to a maximum of 1000 points each.

You’ll be further rewarded with bonus points for all the oxygen you have remaining the moment you surface. The more oxygen you have left, the more bonus points you’re given.


