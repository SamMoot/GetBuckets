# GetBuckets - Analyzing NBA Myths

Data: 
> **shots** : used python to extracted from sports_radar (unknown reliability)
Get nba schedule for the Warrior’s last for games: ‘2021-11-30’, ‘2021-12-03’, ‘2021-12-04’, ‘2021-12-06’
Provided game_id in the playperplay database .
information about every shot attempted in all the games played in those 4 dates.

> **allnbagames** : used python to extract from the rapidapi website . (unknown reliability)
It has information about every nba game played between seasonyear 2017 to 2020 inclusive.
“https://api-nba-v1.p.rapidapi.com/games/seasonYear/

> **stephcurry_df** : from https://data.world/datatouille/stephen-curry-stats (unknown reliability)
Has Steph Cury’s box score information for eevery game between 2009 - 2017
“http://api.sportradar.us/nba/trial/v7/en/games/{}/pbp.json


Html too large to render: [Click here! ](https://htmlpreview.github.io/?raw.githubusercontent.com/SamMoot/GetBuckets/main/NBA%20Myths/NBA_Analytics.html)


# 1. Hot Hand ? 
<img width="864" alt="image" src="https://user-images.githubusercontent.com/85631312/222629750-2e212fde-cd18-42ca-af36-b035edba14a6.png">

> **Findings** This shows where in the arc steph curry can make shots. 1.Does this imply that Stephen Curry can only make shots at the top arc and not ? 2. Jimmy Butler makes a lot of his shots by the rim -so x and y are highly coorelated.

<img width="798" alt="image" src="https://user-images.githubusercontent.com/85631312/222629902-f8ae6bb1-27c2-4c1f-82f0-1dcb784cfac0.png">



<img width="813" alt="image" src="https://user-images.githubusercontent.com/85631312/222629959-42eb85ec-39b3-4eb2-b86c-4567c29fded0.png">
> **Findings** Steph Curry generates the most points, followed by Andrew Wiggins and Jordan Poole. He has a lower average points made per attempt than other players, but this may be due to a multitude of reasons. - having more challenging looks (guarded shots) - providing good assists to this teammates - shooting farther

<img width="698" alt="image" src="https://user-images.githubusercontent.com/85631312/222631188-617a4dcd-aa20-4031-8663-2bd0a1d4c2b1.png">

> **Findings** Conclusions: Durant and Jokic has a shorter wait time until their next made shot compare to Curry. However Curry takes more three points. This would mean that every successful shot of Durants and Jokic amounts to 2 points while Curry’s made shots can contribute 2 - 3 points.

It looks like Jokic has a short wait time until his next successful shot given that he has made a shot. However, this was based on 1 game for Jokic, explaining the white spaces between the blue bars. So, the hot hand myth is inconclusive given the lack of data.

Stephen Curry averages 5.25 threes per game while Kevin Durant only averages 2 threes per game.



# 2. Home Court Advantage? 
<img width="787" alt="image" src="https://user-images.githubusercontent.com/85631312/222630016-dd5518f1-ea3c-4d0b-b8e6-2e81bce088fa.png">
<img width="798" alt="image" src="https://user-images.githubusercontent.com/85631312/222630057-3e0d4758-2aab-46d8-bfdd-5022483373d6.png">
> **Findings** On average, NBA teams has a 58% chance of winning at Home Game, giving them a slight advantage over their opponents.
This is only one perspective. There may be many confounding variables e.g. good teams will win at home and away - masking the advantage or home court advantage if there is one. So we cannot make a conclusive statement.

## 2.1 Does location matter? Higher elevation cities?
<img width="658" alt="image" src="https://user-images.githubusercontent.com/85631312/222630099-11891cde-0527-4a00-95e9-77a88f7dd614.png">
> To eliminate others factors that may be affecting the impact of player’s performance in different locations. Denver is the primarly focus. The objective is to calculate the difference between chance of winning for every team not at Devener vs at Denver.
> Even though teams are less likely to win at Denver, 30.46% is within 1 standard derivation of 40.9% (+/- 14.5%). This means we cannot make any conclusions with high confidence.
* League's likelihood of winning at Denver is 30.46%
* League's likelihood of winning at Away Game is 40.9%
* SD is 14.5%


<img width="772" alt="image" src="https://user-images.githubusercontent.com/85631312/222630211-793717ce-5126-4968-964b-b69129c2d0c1.png">


Examine Warror Performance at Home vs Away Games
<img width="797" alt="image" src="https://user-images.githubusercontent.com/85631312/222630230-5a184cd9-0a01-4f2b-a90e-c830f9569411.png">
> **Findings** Warrior’s scoring abilities doesn’t seem to be affected by away games significantly. Only a 4 points difference between at home vs away.

# 3 Do High-Level Players Take Regular Season Games Seriously?
<img width="847" alt="image" src="https://user-images.githubusercontent.com/85631312/222630374-5008041a-951d-46d6-af7d-4495c31ef612.png">
conclusion: The spread of Steph Curry’s shooting percentage is relatively similar between Regular Season Games and Playoff Games. However, there are more variance in the Regular Season Games.

> Regular seasson shooting pecentage: 0.117206780167678 . 
  Post reson shooting percentage:  0.105224210827332 . 
 
<img width="482" alt="image" src="https://user-images.githubusercontent.com/85631312/222631888-77f24441-9467-48a9-a102-02179cae8b32.png">

> Conclusion: The p-value = 0.08 from the Welch Two Sample t-test. There’s no significant shooting difference between regular season games and playoff games for Steph Curry.

