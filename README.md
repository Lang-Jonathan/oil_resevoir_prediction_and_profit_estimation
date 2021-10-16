# Oil Resevoir Prediction And Profit Estimation
## Project description
In this project the best place for a well for the fictive company OilyGiant mining should be found. Therefore the company provided data of sample drillings of three regions and historic data.


## Content   

The process should contain multiple steps:

1. Building a linear regression model to predict volume for wells in the three regions
2. Selection of top 200 wells for each region
3. Calculation of break even point considering costs and outcome
3. Analysing  the profit and risk potentials for each regions using bootstrapping
4. Making suggestion of best region wit risk of loss below 2.5%


## Outcomes
### Step 1:
The model results for the three regions are:  
| Region  	| RMSE  	| R2 Score 	|  
|---------	|-------	|----------	|  
| Region0 	| 37.58 	| 0.28     	|  
| Region1 	| 00.89 	| 0.99     	|  
| Region2 	| 40.03 	| 0.21     	|  

Based on that the real and predicted outcomes are resulting as the following:

- The real mean volume of top 500 is the highest in region 2 and 0. (Around 180) Whereas the real mean value of region 1 is around 130.
- In contrast to that, the mean prediction of the top 500 spots form the model shows complete different results: 
    - region 1 has the highest average which is around the same level than the real average (130)
    - the mean of predicted means for region 0 and region2 decreased to around 115 and are now lower than region 1 
    - The mean decreased around 70 units for region 0 and 2 (in middle) wherease the mean in region decreased just 0.49 units
    - The RMSE for the top 500 is over 63 for region 0 and over 47 for region 2 and so massively over the RMSE of the models (37-40)

### Step 2:
- Based on the costs and estimated prices, the break even point for 200 wells has been calculated for a production of minimum 111.11 mio. barrels.
- A sample of 500 wells per region of which the 200 most promising would have been developed shows, that region 2 is the most profitable region using the estimations of the model.

### Step 3:
- With bootstrapping with 1000 Samples the average profit and the probability of a loss per region results as:
| Region  	| Estimated Profit in $	| Probability of loss in %	|   
|---------	|---------------------- |-------------------------	|  
| Region0 	| 3.88e6			 	| 6.85						|  
| Region1 	| 4.91e6		     	| 0.36						|  
| Region2 	| 3.62e6		     	| 9.23						|

### Step 4:
Based on the previously carried out steps the new 200 wells should be developed in region 1. This region is choose because it has the highest to expecting profit with a minimal chance of losses compared to region 0 and 2.
