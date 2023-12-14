[Link to Notebook](https://github.com/benharosh/berkeley-ml-1/blob/main/assignment_5_1_starter/prompt.ipynb)

### Will a Customer Accept the Coupon?

**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Overview**

The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.

**Data**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’.  There are five different types of coupons -- less expensive restaurants (under \\$20), coffee houses, carry out & take away, bar, and more expensive restaurants (\\$20 - \\$50). 

**Deliverables**

Your final product should be a brief report that highlights the differences between customers who did and did not accept the coupons.  To explore the data you will utilize your knowledge of plotting, statistical summaries, and visualization using Python. You will publish your findings in a public facing github repository as your first portfolio piece.

### Data Description
Keep in mind that these values mentioned below are average values.

The attributes of this data set include:
1. User attributes
    -  Gender: male, female
    -  Age: below 21, 21 to 25, 26 to 30, etc.
    -  Marital Status: single, married partner, unmarried partner, or widowed
    -  Number of children: 0, 1, or more than 1
    -  Education: high school, bachelors degree, associates degree, or graduate degree
    -  Occupation: architecture & engineering, business & financial, etc.
    -  Annual income: less than \\$12500, \\$12500 - \\$24999, \\$25000 - \\$37499, etc.
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater
    than 8
    -  Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or
    greater than 8
    -  Number of times that he/she eats at a restaurant with average expense less than \\$20 per
    person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    -  Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    

2. Contextual attributes
    - Driving destination: home, work, or no urgent destination
    - Location of user, coupon and destination: we provide a map to show the geographical
    location of the user, destination, and the venue, and we mark the distance between each
    two places with time of driving. The user can see whether the venue is in the same
    direction as the destination.
    - Weather: sunny, rainy, or snowy
    - Temperature: 30F, 55F, or 80F
    - Time: 10AM, 2PM, or 6PM
    - Passenger: alone, partner, kid(s), or friend(s)


3. Coupon attributes
    - time before it expires: 2 hours or one day
    
### Summary and Action Items for Bar Coupons

Drivers who were frequent bar-goers (more than 3 times a month) were more likely (`76.8%`) to accept `Bar` coupons, while drivers who were less frequent bar-goers showed a higher `Bar` coupons rejection rate (`63%`). Drivers who were bar-goers more than once a month had higher `Bar` coupons acceptance rate (`68.7%`), but it was slighltly less compared to the acceptance rate (`76.8%`) of the more frequent bar-goers. Given that, it should be considered to offer more `Bar` coupons to drivers who went more frequently to bars.

For drivers who went to bars more than once a month, it seems that addind a split to driver age groups (older and younger than 25) wasn't a strong indicator of the acceptance rate. Adding an age filter (drivers older than 25) to drivers who went to bars more than once a month, produced a similar `Bar` coupons acceptance rate (`69.5%`), compared to drivers who just went to bars once a month's acceptance rate (`68.7%`).

Rejection rate for drivers who went to bars less than once a month, was higher (`66.5%`) compared to the aggregated rejection rate of (`58.8%`). Given that, it should be considered to offer less `Bar` coupons to this group of drivers. 

Drivers who were bar-goers (more than once a month) and were younger than 30 years, presented a good indicarion for `Bar` coupons acceptance (`72.1%`), than drivers who just went to a bar more than once a month (`68.7%`). We should consider offering more `Bar` coupons to younger drivers that are bar-goers, since this group is more likely to produce higher acceptance rates.

Drivers who were frequent cheap restaurants goers (more than 4 times a month), and had income of less than $50K, had similar acceptance rate to the aggregate acceptance rate of `Bar` coupons. These categories when combined together are not a good indication of acceptance rate for `Bar` coupons.

    
### Summary and Action Items for Coffee House Coupons

Drivers were just slighly more likely (`52%`) to accept `Coffee House` coupons on warmer weather (`80F°`), compared to colder weather and to the overall aggregated `Coffee House` acceptance rate (`49.9%`). Drivers were more likely to reject the coupons on colder days at higher rates (`54.4%` and `55.6%`), compared to the aggregated `Coffee House` rejection rate (`50.1%`). We should consider offering less `Coffee House` coupons on colder days, amd offer more on warmer days.

Drivers who were frequent coffee houses goers (4 or more times a month), showed higher acceptance rate of (`67.5%`), compared to drivers who were less frequent coffee houses goers, and showed acceptance rate of just (`36.2%`). We should consider offering less `Coffee House` coupons to less frequent coffee houses goers, who had 72% `Coffee House` coupons share, in order to lower the `Coffee House` coupons rejection rate, given they presented (`63.8%`) rejection rate (more than the aggregated rate). Alongside with that, we should consider offering more coupons to more frequent coffee houses goers, that had a share of only 22% of total `Coffee House` coupons, and preasented a higher acceptance rate.

Drivers who are 15 minutes or less from their destination, that had 40.365% share of `Coffee House` coupons, presented higher acceptance rate (`59.1%`) compared to drivers who were more than 15 minutes from the destination. We should consider offering more `Coffee House` coupons to drivers are closer to the `Coffee House` coupon location, and less to drivers who are located further than 15 minutes drive from the coupon location, and showed higher rejection rates.

Younger drivers (less than 21 old), showed higher coupon acceptance rate (`69.6%`), but had only (`3.8%`) overall share. We might want to consider to increase their share by offering more coupons and see if in bigger volumes they still keep the high acceptance rate.

Drivers over 50 years old rejected coupuns at a higher rate (`57.9%`), compared to all other age groups and also with comparison to the aggregated `Coffee House` rejection rate of (`50.1%`). We should consider offering less `Coffee House` coupons to this group of drivers.

Drivers offered coupons with longer expiration period (1 day), accepted them at higher rate (`58.3%`), compared to the acceptance rate (`43.1%`) of coupons that were offered with shorter expiration period (2 hours). We should consider offering more coupons with longer expiration period (1 day) or, altenatively, extend the 2 hours expiration period window for the short term expiration coupons, and see if they get higher acceptance rate.

Drivers who were frequent cheap restaurants goers (more than 8 times) and had lower income (less than $25K), had higher acceptance rate (`70.8%`), compared to coupons that were offered to others (`49.5%`). This combination had only (`~2%`) `Coffee House` overall share, so it's hard to make strong assumptions based on the smaller smaple size, but maybe it worth to try and check if increasing this group's `Coffee House` coupons share - will lead to a higher acceptance rate.

[Link to Notebook](https://github.com/benharosh/berkeley-ml-1/blob/main/assignment_5_1_starter/prompt.ipynb)