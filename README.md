[Link to Notebook](https://nbviewer.org/github/benharosh/berkeley-ml-1/blob/main/assignment_5_1_starter/prompt.ipynb)

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

Drivers who were frequent bar-goers (more than 3 times a month) were more likely (`76.8%`) to accept `Bar` coupons, while drivers who were less frequent bar-goers showed a higher `Bar` coupons rejection rate (`63%`).

Drivers who were bar-goers more than once a month still had higher `Bar` coupons acceptance rate (`68.7%`), but it was slighltly less compared to the acceptance rate (`76.8%`) of the more frequent bar-goers.

Consider offering more `Bar` to drivers who went more frequently to bars, since coupons were accepted at a higher rate with more frequent visits to bars on a monthly base. 

For drivers who went to bars more than once a month, it seems who the split of age of the driver (to older and younger than 25) was not an indicaitive factor of the acceptance rate by itself. Looking at drivers older than 25 who went to bars once a month, produced a similar acceptance rate (`69.5%`) of `Bar` coupons, compared to drivers who just went to bars once a month (`68.7%`).

Consider offering less `Bar` coupons to drivers who went to bars less than once a month or were older than 25, since the rejection rate of this group was at higher rate (`66.5%`), compared to the aggregated rejection rate of (`58.8%`)

Drivers who went to bars more than once a month and were younger than 30 years, were more likely (`72.1%`) to accept `Bar` coupon, than drivers who just went to a bar once a month (`68.7%`). When looking at the age histograms we can confirm who drivers above 30 are less likely to accept `Bar` coupons, compared to those below 30. We should consider offering more `Bar` coupons to younger drivers, since it will more likely produce higher acceptance rates.

The sample size of drivers who are widowed (21) and work in farming/fishing/forestry (9) was so little compared to the number of `Bar` coupon drivers (2017), who when trying to exclude them from comparisons, there was no affect on the acceptance rate. Also, because of the small sample size it'll be very hard to draw conclusions on these particular groups.

Drivers who went more frequent (> 4 a month) to cheap restaurants and had income of less than $50K, had similar acceptance rate to the aggregate acceptance rate of `Bar` coupons. These categories when combined together are not a good indication of acceptance rate for `Bar`.

    
### Summary and Action Items for Coffee House Coupons

Drivers were just slighly more likely (`52%`) to accept `Coffee House` coupons on warmer weather (`80F°`), compared to colder weather and to the overall aggregated `Coffee House` acceptance rate (`49.9%`). Drivers were more likely to reject the coupons on colder days at higher rates (`55.6%`, `54.4%`), compared to the aggregated `Coffee House` rejection rate (`50.1%`)

Consider offering more coupons to drivers who went to `Coffee House` 4 or more times a month (had a 22% `Coffee House` coupons share), since they showed higher acceptance rate of (`67.5%`), compared to drivers who went less than 4 times a month to coffee houses, and showed acceptance rate of just (`36.2%`)

Consider offering less coupons to drivers who went to `Coffee House` less than 4 times a month (had 72% `Coffee House` coupons share), since they showed higher rejection rate of (`63.8%`), compared to drivers who went 4 or more times in a month to coffee houses, that had only (`32.5%`) rejection rate, and compared to the aggregated `Coffee House` rejection rate (`50.1%`)

Consider offering more coupons to drivers who are 15 minutes or less from their destination, which their share is currently 40.365%, since the acceptance rate (`59.1%`) was higher compared to drivers who were more than 15 minutes from the destination

Consider offering less coupons to drivers who are 15 minutes and had rejection rate of (`54.7%`, `65.5%`) for (more than 15 mins, more than 25 mins), respectively - which was higher than the aggregated (`50.1%`) rejection rate 

Consider offering more coupons to younger drivers (less than 21 old), who showed higher coupon acceptance rate (`69.6%`), but had only (`3.8%`) ocerall share.

Consider offering less coupuns to older drivers, over 50 years old, who rejected coupuns at a higher rate (`57.9%`), compared to all other age groups and also with comparison to the aggregated `Coffee House` rejection rate (`50.1%`)

Consider offering more coupons with longer expiration period (1 day), that were accepted by drivers at a higher rate (`58.3%`), compared to the acceptance rate (`43.1%`) of coupons that were offered with shorter expiration period (2 hours). Altenatively, we can try and extend the 2 hours expiration period window for the short term expiration, and see if we get higher acceptance rate by doing so.

Consider offering more coupons to drivers who drivers who went more than 8 times a month at cheap restaurants and had lower income (less than $25K), since they had had higher acceptance rate (`70.8%`), compared to coupons that were offered to others (`49.5%`). This combination had only (`~2%`) share, and it's worth checking if increasing its share will ead to a higher acceptance rate.

[Link to Notebook](https://nbviewer.org/github/benharosh/berkeley-ml-1/blob/main/assignment_5_1_starter/prompt.ipynb)
