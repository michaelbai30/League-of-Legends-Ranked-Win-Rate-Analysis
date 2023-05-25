# League of Legends Ranked Match Data Analysis 
# Author: Michael Bai

This repository contains a notebook that analyzes data from approximately 10,000 Diamond+ (high elo) matches of League of Legends, a popular online battle arena (MOBA). The game is played between a "blue team" and a "red team" whose goals are to destroy the opposing team's base and ultimately, their "Nexus". The analysis focuses on the first 10 minutes of each match (the early game) and examines various factors to determine their correlation with the win rate.

Note: Because the data covers only the first ten minutes of the game (a typical game of League of Legends can range from around 15 - 60 mins in length with the average being around 30 - 45 mins), some variables are underrepresented because the game has not gone on for long enough yet. For instance, teams typically do not slay elite monsters, dragons, or heralds, nor take down towers within the first 10 mins of the game, despite these being important factors in determining victory.

## Columns / Variables

Note that variables are mirrored between blue and red teams.
Because we have a balanced dataset (as proven in the notebook), we can use either for analysis.
Data for both teams are provided for the goal of creating a binary classifier.

- `gameId`: Unique identifier for each game
- `blueWins`: Binary value (0 or 1) indicating whether the blue team won the match
- `blueWardsPlaced`: Number of wards placed by the blue team
- `blueWardsDestroyed`: Number of wards destroyed by the blue team
- `blueFirstBlood`: Binary value (0 or 1) indicating whether the blue team secured the first blood
- `blueKills`: Number of kills by the blue team
- `blueDeaths`: Number of deaths suffered by the blue team
- `blueAssists`: Number of assists by the blue team
- `blueEliteMonsters`: Number of elite monsters killed by the blue team
- `blueDragons`: Number of dragons killed by the blue team
- `blueHeralds`: Number of heralds killed by the blue team
- `blueTowersDestroyed`: Number of towers destroyed by the blue team
- `blueTotalGold`: Total gold acquired by the blue team
- `blueAvgLevel`: Average level of the blue team
- `blueTotalExperience`: Total experience gained by the blue team
- `blueTotalMinionsKilled`: Total minions killed by the blue team
- `blueTotalJungleMinionsKilled`: Total jungle minions killed by the blue team
- `blueGoldDiff`: Gold difference between the blue and red teams
- `blueExperienceDiff`: Experience difference between the blue and red teams
- `blueCSPerMin`: Average CS (minions killed) per minute for the blue team
- `blueGoldPerMin`: Average gold earned per minute for the blue team
- `redWardsPlaced`: Number of wards placed by the red team
- `redWardsDestroyed`: Number of wards destroyed by the red team
- `redFirstBlood`: Binary value (0 or 1) indicating whether the red team secured the first blood
- `redKills`: Number of kills by the red team
- `redDeaths`: Number of deaths suffered by the red team
- `redAssists`: Number of assists by the red team
- `redEliteMonsters`: Number of elite monsters killed by the red team
- `redDragons`: Number of dragons killed by the red team
- `redHeralds`: Number of heralds killed by the red team
- `redTowersDestroyed`: Number of towers destroyed by the red team
- `redTotalGold`: Total gold acquired by the red team
- `redAvgLevel`: Average level of the red team
- `redTotalExperience`: Total experience gained by the red team
- `redTotalMinionsKilled`: Total minions killed by the red team
- `redTotalJungleMinionsKilled`: Total jungle minions killed by the red team
- `redGoldDiff`: Gold difference between the red and blue teams
- `redExperienceDiff`: Experience difference between the red and blue teams
- `redCSPerMin`: Average CS (minions killed) per minute for the red team
- `redGoldPerMin`: Average gold earned per minute for the red team

## Analysis Goals

In this notebook, we aim to analyze the correlation between the following factors and whether or not a match is won or lost:

- First blood: Examining whether securing the first kill of the match increases the chances of winning the match. First blood grants bonus gold and is a good indicator of early momentum / strong start for a team.
- Number of team kills: Analyzing the impact of the number of kills by a team on the outcome of a match.
- Gold difference: Investigating how the difference in gold between the teams affects the outcome.
- Vision score: Exploring the relationship between vision score (wards placed and destroyed) and the probability of winning.

By conducting this analysis, we hope to gain insights into the importance of these factors in high elo matches and their influence on the overall game outcome.

In addition, feature analysis is done on each variable in order to analyze the most important EARLY GAME factors that contribute to a team's win.

Future Work: Create a binary classifier model that can accurately predict the outcome of a match given data from the blue and red team.

Please refer to the Notebook in this repository for a detailed analysis, including code, visualizations, and conclusions.
