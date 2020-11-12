# LeagueOfLegendsWinPrediction


# **Download the dataset here!**
https://www.kaggle.com/bobbyscience/league-of-legends-diamond-ranked-games-10-min

# **Introduction to the problem**

<h1 align=center><strong>League of legends | LOL</strong></h1>


---

<p align='center'><a  href='https://nbviewer.jupyter.org/github/M-Borsuk/LeagueOfLegendsWinPrediction/blob/ada3faa432dcdc13f41cf8e469008ddaac2c374e/LolWinPrediction.ipynb' > View the notebook here for better readability </a></p>

<br>
<br>
<br>
<figure align=center>
  <img src='https://theme.zdassets.com/theme_assets/43400/87a1ef48e43b8cf114017e3ad51b801951b20fcf.jpg' style='width:100%'>
 </figure>
<br>
<br>


---


<p align='center'> As we can read from <a href='https://en.wikipedia.org/wiki/League_of_Legends'> Wikipedia</a> , <strong> League of legends </strong> is a multiplayer online battle arena video game developed and published by Riot Games for Microsoft Windows and macOS; Developed around 2009.</p>
<br>
<p align='center'>
In every single game of league of legends, two teams usually consisting of five players are dropped into the battleground called Summoners Rift. Each of them choose the role of a champion, characters with unique abilities, generally varying around a type of class. The general aim of each of the team is to destroy the base of the other team, which is called The Nexus. <a href='https://en.wikipedia.org/wiki/League_of_Legends' > [1] </a>
</p>
<br>
<p align='center'>
Your team needs to clear at least one lane to get to the enemy Nexus. Blocking your path are defense structures called turrets and inhibitors. Each lane has three turrets and one inhibitor, and each Nexus is guarded by two turrets. <a href='https://na.leagueoflegends.com/en-us/how-to-play/' > [2] </a>
</p>
<p align='center'>
Based on particular player's performance and skill in the games he plays, he is assigned a rank, so he can play with and against players with similar range of skills. The ranks range from iron rank (the lowest) to the challenger rank<a href='https://www.riftherald.com/lol-gameplay/2018/10/5/17940718/new-ranked-league-visuals-2019' > [3] </a>
</p>


---


<br>
<figure align=center>
  <img src='https://nexus.leagueoflegends.com/wp-content/uploads/2019/12/02_Summoner_s_Rift_hi182k3q611izhk9dbql.jpg' style='width:100%'>
  <figcaption align='center'> <a href='https://nexus.leagueoflegends.com/en-au/2019/12/unleashing-the-elements/' >Picture 1. Layout of the Summoner's Rift map.  </a> </figcaption>
 </figure>
 <br>
 <br>
 <figure align=center>
  <img src='https://mobalytics.gg/wp-content/uploads/2018/03/LoL-140-Roster.png' style='width:100%'>
  <figcaption align='center'> <a href='https://mobalytics.gg/blog/how-to-build-your-champion-pool-in-league-of-legends/' >Picture 2. Some of the champions available to play in the game  </a> </figcaption>
 </figure>
 <br>
 <br>
<figure align=center>
  <img src='https://cdn.vox-cdn.com/thumbor/qUg88S58b-ZqDeTMmLXDCrf2Ixc=/1400x788/filters:format(jpeg)/cdn.vox-cdn.com/uploads/chorus_asset/file/13220385/DormHQIUwAA38_9.jpg' style='width:100%'>
  <figcaption align='center'> <a href='https://www.riftherald.com/lol-gameplay/2018/10/5/17940718/new-ranked-league-visuals-2019' >Picture 3. Possible ranks of play available in the game </a> </figcaption>
 </figure>
 <br>
 <br>

---


<p align='center'>
<strong>In this project, we will try to predict whether a team (ranked as diamond players) will win the game based on the statistics of each team in the first 10 minutes of the game. We will also try to conduct an explonatory data analysis to understand how to win more games!
</p>
<br>



---

## **Final thoughts of the EDA proccess | How to win more games?**

So what can we actually take way from this exploration proccess in terms of winning more games by our early game decisions? Here is some main points that stood out to me throughout this EDA:

1. Definitely try to get one of the epic monsters in the early game. As we can see from the summary of the odds ratio between the association of winning the game and slaying at least one elite monster and winning without slaying at least one elite monster. The analysis shows that the chance of the team winning, given they slayed at least one elite monster is 2.4 times higher than the chance of the team winning, given they did not slay at least one elite monster. The best scenario would be to get dragon and herald, but it's not possible in most games. In such case, it turns out that we should prioritize dragons over heralds. Although, the data shows that killing at least one monster might follow the binomial distribution with only 28% of success. The odds ratio of both of these variables (Dragon vs Herald slayed) shows that a team killing a dragon in the first 10 minutes of the game has approximately 2.5 times the chance of winning compared to the team that did not slay the dragon. In contrast, the odds ratio of Heralds variable shows that a team killing a herald in the first 10 minutes of the game has approximately 1.6 times the chance of winning compared to the team that did not slay the herald. That might imply on prioritizing the dragon as the elite monster to kill in the early game. Slaying either of the elite monsters in the first 10 minutes of the game is not likely, but if you manage to do it You will benefit from it in terms of winning the game.

2. Towers.. Data shows that a team who is able to destroy at least one tower in the first 10 minutes of the game wins 70% of the time. Although I am not as confident on this statement as our variable was highly imbalanced, as shown in the contigency table earlier. We can also interpret the odds ratio between the association of winning the game and destroying at least one turret and winning without destroying at least one turret. The analysis shows that the chance of the team winning, given they destroyed at least one tower is 3.2 times higher than the chance of the team winning, given they did not destroy at least one tower.

3.First bloods.. This one is quite interesting. What we could have saw is that getting the first kill of the game contributes to winning the game 60% of the time. It's almost the same percentage as slaying the herald in the early game. The odds ratio metric shows that a chance of team winning, given they got a first kill in the game is 2.3 times higher than a chance of team winning, given they did not get a first kill in the game.

4. Wards.. Neither the amount of wards placed nor destroyed showed some pattern with relation to winning at the end of the game. That surprised me a bit since vision control is always so highly accented to someone who is learning the game. What might be the cause of this phenomenon is the type of data we have. This dataset consists of games played in the diamond elo. This means that players that played in these games are in the 2% best players of the whole server. That does not mean that these players don't care about vision around the map. To me this means that everyone in these games knows the importance of wards, which basically lowers their effect on the outcome of the game.

5. Amount of minions killed per minute.. It definitely matters, since it influences the amount of gold you get. Although the data shows, that kills influence the victory more than the Amount of minions killed per minute, you don't always get the chance to kill the enemy team in the early game. Always remember to keep your CS high to win more games.




---

# **Summary**

---




*   Accuracy of the best model (AdaBoostClassifier) : <strong> 74 % </strong>
*   Precision score of the model : <strong> 73 % </strong>
*   Recall score of the model: <strong> 73 % </strong>
*   AUC score of the model: <strong> 0.73 </strong>





---

# **What's next?**

---

<p align=center>
Overall, I think that I was able to achieve pretty good results through building and tuning the model. Although, I do think that there are a some aspects that could have yielded a better result at the end of the day. <br>


---


Some of these techniques are:


*   Deleting some of the possible outliers; Although I played around with deleting all/some of them it yielded same or worse results.
*   Gathering more data; especially when it comes to the data of victories.
*   Further parameter tuning in terms of the modelling section.



---


# **Thanks for reading!**
