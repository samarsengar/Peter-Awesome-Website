---
title: Analysing the Tennis Serve Power vs. Consistency Tradeoff
author: Peter Tea
date: '2020-01-01'
categories:
  - Tennis
tags:
  - Grand-Slam
  - Serve
  - Serve speed
  - Tennis
authors:
  - admin
output:
  html_document:
    keep_md: yes
image:
  caption: Photo by pixelcop on Unsplash
  focal_point: Smart
summary: Serving Need for Speed
---


## How do 1st serves differ from 2nd serves?
Tennis serve faults are a common occurrence in any competitive tennis match. Depending on whether a player is on their 1st or their 2nd serve, serving strategy is at the forefront of the player's decision making process in terms of how they want to attack their opponent. For instance, on 1st serve the player is reassured that no matter the outcome they will at least have a second opportunity to serve again without penalty. Hence, the risk-return tradeoff of attacking the opponent with a big and powerful serve is certainly manageable. However, if the player is instead on 2nd serve then they may be more wary of this tradeoff. Powerful serves are more likely to land ``out``, which is why players tend to instead proceed with a less powerful, but more consistent 2nd serve approach.


In this project, we look deep into the service `` power-consistency`` tradeoff through a couple data visualizations. We will focus our attention on familiar names from both the ATP and WTA worlds. From the ATP, we chose to look at ``Rafael Nadal``, ``Roger Federer`` and ``Novak Djokovic``. From the WTA, we chose to look at ``Serena Williams``, ``Simona Halep`` and ``Bianca Andreescu``. After some data cleaning and aggregating steps on match summary data found on Jeff Sackmann's [Github page](https://github.com/JeffSackmann/tennis_atp/blob/master/README.md), we produce the following analysis from Wimbledon and the US Open grand slam tournaments of 2019. 





### ATP Wimbledon Serve Speeds


First as an exploratory step, we analysed the observed distributions of first serve speeds compared to second serve speeds.

![](index_files/figure-html/pressure2-1.png)<!-- -->![](index_files/figure-html/pressure2-2.png)<!-- -->![](index_files/figure-html/pressure2-3.png)<!-- -->


From the 3 graphics above, we see that among the 3 ATP players, the average 1st serve speed is consistently greater than the average 2nd serve speed. In fact, with the exception of Novak Djokovic, the maximum 2nd serve speed is lower than the average 1st serve speed! Djokovic's 2nd serve speed has greater variance when compared to Roger and Rafa. Perhaps this has to do with Djokovic's strategy of being more unpredictable in his 2nd serves? In any case, these 3 graphics indicate that these 3 ATP players tend to switch up their serve approaches given the situation of the match. 



In the women's game, we observe the same pattern when we look at the 2 WTA players who reached the Wimbledon final (Halep def. Williams). 

## WTA Wimbledon Serve Speeds
![](index_files/figure-html/pressure-1.png)<!-- -->![](index_files/figure-html/pressure-2.png)<!-- -->

Throughout the Wimbledon tournament, both Williams and Halep display distinct serve speeds depending on whether they are on their 1st or 2nd serve.



Inspired by these observed these patterns at Wimbledon, we then explore whether they exist in other tournaments where players play on different surfaces (Wimbledon is played on ``grass`` courts). To provide a partial answer to this question, we perform the same analysis using data from the 2019 US Open tournament, which is played on ``hardcourt``. 


## ATP US Open Serve Speeds



![](index_files/figure-html/USOpen_res-1.png)<!-- -->![](index_files/figure-html/USOpen_res-2.png)<!-- -->![](index_files/figure-html/USOpen_res-3.png)<!-- -->

From the 3 graphics above, we see that the 3 ATP players at the US Open all exhibit similar patterns observed during the Wimbledon grand slam tournament.


## WTA US Open Serve Speeds




![](index_files/figure-html/USOpen_res_WTA-1.png)<!-- -->![](index_files/figure-html/USOpen_res_WTA-2.png)<!-- -->


Given that players modify their approaches 


## What are the implications of a 1st serve appraoch vs. a 2nd serve approach?
We calculate the following:
- Δ Serve Speed (KM/H) = Average 2nd serve speed - Average 1st serve speed
- Δ Win percentage = % Points won on 2nd serve - % Points won on 1st serve
- Δ Rally Length = Average rally length on 2nd serve  - Average rally length on 1st serve
- Δ Distance Run = Average distance run on 2nd serve - Average distance run on 1st serve

| Player |Δ Serve Speed (KM/H) | Δ Win percentage  |  Δ Rally Length | Δ Distance Run
|---|---|---|---|---|---|
| Djokovic  |🔻29|🔻19|❇️ 2.0   | ❇️ 6.0  | 
| Nadal  |🔻29|🔻16| ❇️ 1.0  | ❇️ 3.0  | 
| Federer  |🔻29|🔻15 | ❇️ 1.5  | ❇️ 4.0 |
| Williams |🔻24|🔻14 | ❇️ 1.0  |  ❇️ 3.0 |
| Halep |🔻28|🔻10| ▶️ 0.0  | ▶️ 0.0  |


From the above table, we might be able to make some interesting conclusions about serve speeds. When we compare 2nd serves to 1st serves:

- Serve speed decreases
- Win percentage decreases
- Rally length increases
- Distance Run increases


For completeness, we present the same table of numbers for the 2019 US Open tournament.

| Player |Δ Serve Speed (KM/H) | Δ Win percentage  |  Δ Rally Length | Δ Distance Run
|---|---|---|---|---|---|
| Djokovic  |🔻33|🔻13|❇️ 2.0   | ❇️ 5.0|
| Nadal  |🔻34|🔻18| ❇️ 3.0  | ❇️ 9.0  | 
| Federer  |🔻33|🔻22| ❇️ 2.0 | ❇️ 5.0 |
| Williams |🔻30|🔻17| ❇️ 1.0  |  ❇️ 4.0 |
| Andreescu |🔻21|🔻18|  ❇️ 1.0 | ❇️ 3.0|








- Maybe players are more comfortable (i.e. have more trust in) with their groundstroke game to win


