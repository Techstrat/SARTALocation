# SARTALocation


## Aim to

* Determine the continent and countries where South African ex-pats are staying.
* Map the change in locations over time in monthly intervals.

## Methodology

In this proof of concept the origin of tweets containing specific South African words will be used to determine the location of South African expats.

* Harvest tweets sent containing specific South African slang words.  The slang words was originally sourced from the [Brand South Africa's website](https://www.brandsouthafrica.com/people-culture/culture/south-african-english).  The list is reduced to words uniquely South African in any context.  
The following 17 words are included:
yebo, mzansi, braai, jozi, boet, bottle store, lekker, kwaito, biltong, voetsek, gatvol, spaza, sangoma, bakkie, rooibos, chommie, tsotsi


* Refer to the location field in the twitter record to determine the origin of each tweet.

* Map the continent and country of the origin of the tweets, excluding Africa.

## Test quality of results

* The majority of tweets per word need to come from South Africa else the word is not uniquely South African.

* In addition the resulting countries are similar to surveys conducted by the site [wheredidwego.com](https://www.wheredidwego.com/) listing the following 10 countries as the top destinations:
New Zealand, Australia, UK, Canada, USA, Netherlands, Ireland, Germany, UAE, Qatar

## Roadblock

The location field is a free text field.  Many users do not complete the field which means these tweets would need to be discarded.
Where the location field is completed, the entries varies. Each of these entries needs to be mapped to a valid country and continent.
The expectation is the need to map will decrease as more mapping is added.

After harvesting tweets for 14 days there was still around 300 locations that needed to be mapped each day which made the excercise unsustainable beyond a proof of concept.  If the proof of concept pass, the next step is to connect to the Google Maps API to allow a more efficient determination of the location origin of the a tweet.

## Resulting data

These are the resutls from the 14 day excercise - 12 October to 26 October 2019.  

All the words in scope are used more than 50% of the time by twitters from South Africa validating the words as typical South African.  

The only exception is the word Rooibos.  Although less than 50% of the tweets come from South Africa, Africa is still the largest single source of tweets containing the word Rooibos and Rooibos is still included as a typical South African word.

The Excercise fail the test of likely countries to appear on the list. Refer to the list of countries and continents repesented in the double pie chart.

The two most popular countries listed on the site [wheredidwego.com](https://www.wheredidwego.com/) for South Africans to migrate to are Australia and New Zealand.  Refering to the chart, Australia and New Zealand are dwarfed by the USA and UK in the twitter stats.

It is possible that countries have different cultures when it comes to sending tweets and South African expats in the USA and UK tweet alot more than their cousins in Australia and New Zealand.  The location origin of tweets can not be taken as a single indicator of where South African have settled.

## What next ?

It is interesting to note if Australia and New Zealand is taken out of the equation, the list of most populater countries are very similar.  This should be explored.
In addition if a more accurate and efficient determination of origin with the google maps API is used the result can be measured with more confidence.
