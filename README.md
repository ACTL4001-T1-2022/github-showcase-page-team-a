![](coollogo_com-20588320.png)

On behalf of the Comissioner of Sport for Rarita, Team A has constructed the inaugural Raritan football team! 

This page outlines the statistical methodologies and analysis undertaken to support the team recommendation. 

## Team A Members
- Abhi Khosla
- Finn Hellen-Ford
- Thomas Ding

---


![](coollogo_com-16557518.png)

| Player | Position|
| :---:  | :---:  |
| K. Kazlo?  | FW |
| A. Kyarikunda | FW |
| U. Shoko | FW |
| W. Martinez | FW |
| P. Rabiu | MFFW |
| P. Villa | MFFW |
| Q. Morrison | MF |
| J. Nurhayati | MF |
| X. Leroy | MF |
| S. Barman | MF |
| O. Wanjala | MF |
| F. Chin | MF |
| H. Zare | DF |
| C. Tukamushaba | DF |
| H. Azizi | DF |
| N. Terzi? | DF |
| T. Nouri | DF |
| A. Omar | GK |
| B. Ampofo | GK |

The above 20 players were chosen from three separate logistic GLM models, applied to three groups of players:				
				
- Tournament Forwards – Shooting and Passing metrics for 2021
- Tournament Defenders – Defending and Passing metrics for 2021
- Tournament Goalkeepers – Goalkeeping metrics for 2021

The model was designed to both select and provide weights for each of the metrics depending on their significance in predicting tournament success for each of the three groups of players. Tournament success was defined as placing in the top 3 teams in the 2021 FSA Tournament. 
		 	 	 		
			
Specific metrics were then manually adjusted where deemed necessary, in particular when some variables were assigned negative coefficients.  Then, from the top Raritan candidates ranked by the models, the final team selection was made. 

![](coollogo_com-245443321.png)
		 	 	 		
We’ve developed an estimate of the winning probabilities for each matchup of the 2021 FSA tournament, calculated by merging key team performance metrics: 


| Result | Calculation |
| :---:  | :---:  |
| Win | Sum of Goalkeeper 'W', opponent Goalkeeper 'L', Total xG, opponent Total GA |
| Draw | Sum of Goalkeeper 'D', opponent Goalkeeper 'D', Absolute Difference between Total xG and Total GA, Opponents Absolute Difference between Total xG and Total GA|
| Loss | Sum of Goalkeeper 'L', opponent Goalkeeper 'W', Total GA, opponent Total xG |

So then the probability of a win will be this 'Win' metric divided by the sum of all 3 'Win', 'Draw' and 'Loss' metrics.

From these probabilities, the teams’ expected number of tournament points across a season (home and away) were calculated. (3 for a Win, 1 for a Draw, 0 for a Loss). The expected points table alligns quite well with the 2021 Tournament results, demonstrating the validity of this using this approach for predicting Tournament Results. Many of the teams have a total quite close to each other, so some discrepancy is expected.

| 2021 FSA Tournament Placement | Nations ordered by Expected Tournament Points | Expected Tournament Points |
| :---:  | :---:  | :---:  |
| Sobianitedrucy | Sobianitedrucy| 80.39256|
| People's Land of Maneau | Nganion |77.57156|
| Nganion | People's Land of Maneau |75.75966|
| Mico | Byasier Pujan |74.79793|
| Quewenia | Rarita |74.66649|
| Southern Ristan | Greri Landmoslands |73.42093|
| Galamily | Djipines |71.63178|
| Bernepamar | Giumle Lizeibon |69.43081|
| Giumle Lizeibon | Southern Ristan |69.12867|
| Greri Landmoslands | Manlisgamncent |68.40061|
| Xikong | Mico |64.96052|
| Manlisgamncent | Ngoque Blicri |64.82188|
| Esia | Bernepamar |63.32280|
| Byasier Pujan | Galamily |62.73767|
| Djipines | Leoneku Guidisia |61.85567|
| Leoneku Guidisia | Xikong |60.79721|
| Ledian | Quewenia |58.76166|
| Eastern Sleboube | New Uwi |57.54362|
| New Uwi | Nkasland Cronestan |56.26734|
| Ngoque Blicri | Esia |52.72160|
| Nkasland Cronestan | Eastern Niasland |51.88768|
| Eastern Niasland | Varijitri Isles |47.44720|
| Varijitri Isles | Ledian |46.41649|
|  | Eastern Sleboube |40.63047|


Monte Carlo simulation was then used to simulate the tournament points earned throughout a theoretical season for our recommended Raritan national team, and the highest and lowest placing nations from the 2021 RFA tournament for comparison. Fitting a gamma distribution to these results allows us to compute an estimated probability of achieving a top 10 placement (estimated by achieving greater than 65 tournament points), and a tournament title (estimated by achieving 85 points).

![](RaritaTP.png)

| Probabilities | Top 10 placement | At least one Top 10 placement within 5 years| At least one Tournament title within 10 years |
| :---:  | :---:  | :---:  |:---:  |
| Rarita | 0.763 | 0.999  |0.473  |
| Sobianitedrucy | 0.920  | 0.999 |0.842 |
| Varijitri Isles  | 0.009 | 0.04 | 0.0001  |

# Salary Projection 

Player salaries are projected following three simple rules. They either increase due to age, decrease after an expected peak or are reset to the average of the past years’ team salary. 

An increase of 1.05 has been used to account for inflation, skill development and contract convention.  

A decrease factor of 0.9 has been used to account for players getting worse after reaching their peak. Research has shown salaries for midfielders and forwards are more likely to continually increase. The expected peak for players is at 27 years.
 		
Resets are done after players are expected to retire. As we can not perfectly predict whether the team will draft rookies or buy out existing players, we will use the average of the past years’ team salary as the new salary for this player slot. A 3 year lag has been used to correct current salaries until they are in line with the distribution of tournament player salaries (as the bulk of our team is from the RFL).

<p align="center" width="100%">
<img width="620" alt="graph 1" src="https://github.com/ACTL4001-T1-2022/github-showcase-page-team-a/blob/main/SalaryProjection.png">
</p>

![](EconomicImpactslogo.png)

# World Cup Data 

Data from the world cup was used to model the GDP growth of Rarita since the World Cup was the largest soccer tournament in the world where teams could represent their home countries on the international level.


<img width="620" alt="graph 1" src="https://user-images.githubusercontent.com/103164965/162573688-b18f2bbb-9e0e-4893-8678-a56a342977fe.png">

	

<img width="620" alt="graph 2" src="https://user-images.githubusercontent.com/103164965/162573766-a8557281-a102-4b96-bc84-09d7280ea452.png">


The two graphs above shows the GDP growth of the winning World Cup countries and the runner up countries respectively. 

|*Countries*|*t-2*	|*t-1*	|*t*	|*t+1*	|*t+2*| 
| :---:  | :---:  | :---:  | :---:  | :---:  | :---:  |
|Brazil (1970)	|10%	|10%	|10%	|11%	|12%|
|West Germany (1974)	|4%	|5%	|1%	|-1%	|5%|
|Argentina (1978)	|-2%	|7%	|-5%	|10%	|2%|
|Italy (1982)	|3%	|1%	|0%	|1%	|3%|
|Argentina (1986)	|2%	|-5%	|6%	|3%	|-1%|
|West Germany (1990)	|4%	|4%	|3%	|5%	|2%|
|Brazil(1994)	|1%	|-3%	|6%	|8%	|7%|
|France (1998)	|1%	|2%	|4%	|3%	|4%|
|Brazil (2002)	|4%	|1%	|4%	|1%	|6%|
|Italy (2006)	|1%	|1%	|2%	|1%	|-1%|
|Spain (2010)	|1%	|-4%	|0%	|-1%	|-3%|
|Germany (2014)	|0%	|0%	|2%	|1%	|2%|
|France (2018)	|1%	|2%	|2%	|2%	|-8%|


<img width="547" alt="graph 3" src="https://user-images.githubusercontent.com/103164965/162576740-e1a60b50-9829-479a-821b-9191ae588749.png">


The above table and graph shows the GDP growth trend during a 5-year period for the winning World Cup countries where data two years before and after the world cup win are shown.

From all the data shown, we made the assumptions that the economic impacts of a successful soccer team would have a larger effect on developing countries than developed countries. 

# Economic Impacts on Rarita

|*Year*	|*East Rarita*	|*Central Rarita*	|*West Rarita*	|*Rarita*|
| :---:  | :---:  | :---:  | :---:  | :---:  |
|2012	|2%	|-2%	|3%	|1%|
|2013	|2%	|0%	|3%	|1%|
|2014	|4%	|2%	|2%	|3%|
|2015	|11%	|5%	|6%	|8%|
|2016	|5%	|4%	|3%	|4%|
|2017	|7%	|6%	|6%	|6%|
|2018	|2%	|5%	|3%	|3%|
|2019	|3%	|4%	|7%	|4%|
|2020	|-2%	|-6%	|-4%	|-4%|
|2022E	|2%	|2%	|4%	|3%|
|2023E	|3%	|2%	|4%	|3%|
|2024E	|3%	|3%	|5%	|3%|
|2025E	|4%	|3%	|5%	|4%|
|2026E	|4%	|3%	|5%	|4%|
|2027E	|4%	|3%	|5%	|4%|
|2028E	|4%	|3%	|5%	|4%|
|2029E	|4%	|3%	|5%	|4%|
|2030E	|4%	|4%	|5%	|4%|


<img width="454" alt="graph 4" src="https://user-images.githubusercontent.com/103164965/162578460-9e87a753-1bd8-443a-8d3c-e3d18a730b8e.png">


From the World Cup data and Rarita's economic data, we predict that Rarita's inflation rate will increase linearly at a rate of 0.1% until 2025 and then increase at a rate of 0.2%. This is because we believe there is an economic lag following the success of Rarita's soccer team. Similarly the GDP growth rates have been projected linearly with West Rarita having the highest growth since it is much less developed than the other two provinces.

## Key Assumptions and Limitations

|*Metric*| *Assumption* | *Rationale*|
| :---:  | :---:  | :---:  |
|Rarita GDP Growth Rate| Modelled on the GDP growth rates of countries who participated in the World Cup.| World Cup is the largest soccer tournament where teams get to represent their home country which means that the team’s performance has a direct impact on the home country’s economy.|
|Rarita Inflation Rate|Increase linearly for the first five years at a rate of 0.1% and then increase by 0.2% for the next 5 years.| The performance of Rarita’s soccer team will not have an immediate effect on the economy and the economic impacts will most likely be evident after a few years.|
|Source of Growth|Mostly be affected due to the growth in West Rarita|West Rarita is the more developing part of Rarita’s economy and therefore any economic impact would be most prominent in that province|
|Predictor of Raritan Player Ability|Modelled from Tournament Data. The response variable was whether the player was in the Top 3 scoring teams in of the 2021 FSA|If a model predicts a high likelihood of a Raritan player performing like the top 3 Tournament teams, it makes sense to choose them.|
|Model coefficients|Model coefficients that were negative were changed to 0 or 0.2|Penalising players for large positive attributes didn’t make sense. It makes more sense that these metrics are not an indicator of player performance|
|Success Probabilities|65 Tournament points are required to break top 10, 85 for a Championship|The expected points of the top 10 teams were approximately 65. The top team has an expected 80 points, so 85 is conservative|





