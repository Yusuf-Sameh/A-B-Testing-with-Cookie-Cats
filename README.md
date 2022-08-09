# A-B-Testing-with-Cookie-Cats

# Project Description

This data is taken from the DataCamp website

Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It's a classic "connect three"
style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level.

As players progress through the game they will encounter gates that force them to wait some time before they can
progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate
in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention.

---- More explanation about the game and the task I will be doing will be found inside the brochure.----

---- You will also find this project on the Kaggle https://www.kaggle.com/youssefspasha/a-b-testing-with-cookie-cats/edit ---

# Data Description

The data we have is from 90,189 players that installed the game while the AB-test was running. The variables are:

userid - a unique number that identifies each player.
version - whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).
sum_gamerounds - the number of game rounds played by the player during the first 14 days after install.
retention_1 - did the player come back and play 1 day after installing?
retention_7 - did the player come back and play 7 days after installing?

When a player installed the game, he or she was randomly assigned to either gate_30 or gate_40. As a sanity check, let's see if there are roughly the same number of players in each AB group.

# Work Description

The main criterion for making a decision about changing the gate was the retention rate of the players. players were divided into two groups,
one of which used the game when the gate was at level 30 and the other was the gate at level 40. There were two parts in this first matter,
which is the retention rate of players after the first day of the game install, and when it was measured, the difference percentages was close,
and to confirm this results,i make bootstraping with replacement of the sample to make the data more accurate, and also after that there was a
small difference in the retention rate of the players in the two groups, however, it will not be important because the two groups did not reach
the level 30 or 40 in first day, it was normal to measure the retention rate of players after a week.

# Conclusion

The bootstrap result tells us that there is strong evidence that 7-day retention is higher when the gate is at level 30 than when it is at level
40. The conclusion is: If we want to keep retention high — both 1-day and 7-day retention — we should not move the gate from level 30 to level 40.

So, why is retention higher when the gate is positioned earlier? One could expect the opposite: The later the obstacle, the longer people are going
to engage with the game. But this is not what the data tells us. The theory of hedonic adaptation can give one explanation for this. In short, hedonic
adaptation is the tendency for people to get less and less enjoyment out of a fun activity over time if that activity is undertaken continuously.
By forcing players to take a break when they reach a gate, their enjoyment of the game is prolonged. But when the gate is moved to level 40, fewer
players make it far enough, and they are more likely to quit the game because they simply got bored of it.
