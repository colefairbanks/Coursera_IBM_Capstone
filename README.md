# Coursera IBM Data Science Capstone 
IBM Data Science Professional Certificate

### The Problem - Moving to New York City's Upper West Side (UWS)
The golden rule of real estate has always been “location, location, location.”  This is true for both buyers and sellers as well as renters and landlords.  As someone who is moving to New York City within the next 6 months, I wanted to solve my own personal business problem by using the skills acquired from these courses.  Specifically, finding a place to live in the city.  However, this business problem is not unique to me – it could apply to anyone moving to the area.  That being said, from a purely business perspective, I could easily be a broker for a property management company giving professional recommendations to a client moving into the area by using the location data.

Why is solving this problem important?  There are three reasons – all of which revolve around quality of life.  First, living close to or far away from major transit points can affect a renter’s commute time.  In this example, if I do not live near one of IBM’s employee shuttle stops, my commute could run well over an hour, which cuts into free time.  Second, the location has a direct impact on the price of the apartment.  Yes, everything is expensive in Manhattan but here are some worthwhile questions – what is the optimal price to distance from the shuttle stop? Would you sacrifice 10 minutes a day in commute time for an additional $300 per month? Third, having things to do in your neighborhood is important – so what are they? Using foursquare data, hopefully we will be able to find out.

### Description of Data and how it will be used to help solve problem
The data I am using is primarily from Apartments.com.  I will build a web scraping tool that will pull the address and rent price from 125 1-bedroom apartments in the Upper West Side neighborhood. (NYC pretty big and so, I thought this would help limit the scope for this project).  Geopy will be used to find the latitude and longitude of each address, which all will be added to a pandas dataframe.  With that information, I will calculate the distance between each apartment and the shuttle stop, which is located at 86th and Amsterdam.  The two main variables are price and distance from stop.  This information will help me filter down any apartments that are over a half mile away and then look for the best price.

Finally, in addition to price and location, I will use the Foursquare API to find the top 10 most common places near the same shuttle stop to get idea of what people do in the neighborhood.

All of this information together gives me an idea of what to do in the neighborhood and potential places to rent.  Moving just got a little bit easier!

### Conclusion
Overall, the location data generated through geopy and Foursquare's API proved to be very useful in finding an apartment in UWS based on price, distance to the IBM shuttle stop, and common venues in the neighborhood.  In terms of price and the distance to ther shuttle stop, a 1-bedroom apartment located under 0.5 miles from the stop had a range between $2,350 - $4,300 per month, with the median being roughly $2,500.  Future analysis could include a trade-off scenario in which one could ask: is walking 10-15min more each day worth saving $100 - $200 per month?

Regarding venues in the neighborhood, Foursquare's API provided valuable insight into the social makeup of UWS.  From the results gathered, it is now clear that UWS consists of many restaurants (especially italian ones), coffee shops, bars in addition to an AMC movie theatre and a Barnes & Noble book store.  However, one thing that confused me was the fact that Foursquare didn't return any parks, which I know UWS has plenty of.

### Thoughts on Improvement and Scaling Up Project in Future
This project was limited in scope to the Upper West Side neighborhood.  However, there are still 5+ IBM shuttle stops in Manhattan that could be added to the scraped results for analysis.  Additionally, in the realm of machine learning, an interesting avenue to pursue would be a logistical regression to describe whether the price for NYC apartments is going up or down in the midst of the pandemic and more interestingly, predict what the price of apartments will be come next summer.  
