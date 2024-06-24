This project was developed as a proof of concept to demonstrate the value data can bring to marketing campaigns to Volkswagen Group Australia.

Volkswagen were looking to launch their ID.4 and ID.5 electric vehicles to the AUS market, but wanted to take a blanket market approach using 
the ID series as a brand support, despite a very small budget - especially when compared to competitors who were earlier to market and in many
cases had lower priced offerings.

We aimed to use publicly available and owned data to model the propensity of customers in particular geographies in terms of our assumed 
likelihood to purchase an ID. series vehicle. 

![image](https://github.com/cslim95/vw_id_targeting/assets/169668063/634948b8-b8dc-48dc-b94c-9afbb407eeb8)

The data available, at the postcode level, was:
- Past VW owners, from the VW CRM system (this data was deduplicated, anonymised and aggregated before uploading)
- Website visitors who have clicked the CTA "Register Your Interest" (RYI) and completed the form, (again this data was deduplicated,
  anonymised and aggregated before uploading)
- Current EV owners, from the Australian Automobile Association (AAA) and later, from the Electric Vehicle (EV) Council.

![image](https://github.com/cslim95/vw_id_targeting/assets/169668063/c08fea9d-d5e5-42fe-9078-014c75e470c6)

We used python (Jupyter Notebooks) for ETL, including some additional data sources such as creating a mapping between post code and suburb 
(which unfortunately don't correspond 1:1 in the Australian geospatial data structure).

Tableau was used to visualise the data, because it has built in geospatial visualisation tools that render this task trivial. We mapped 
propensity across the different AU metro areas, but also within each metro area, to identify high propensity postcodes that Volkswagen should be
targeting.

Perhaps unsurprisingly, we found that in general the high propensity areas skewed towards wealthier suburbs in the two largest metro areas (Sydney
and Melbourne), as well as the ACT.

We assessed the opportunity of each metro are by computing both the average propensity in the city (normalised against the highest propensity 
average), and also the size of the market in terms of light vehicles on the road:

![image](https://github.com/cslim95/vw_id_targeting/assets/169668063/44e5b87d-3a74-42c7-a3c2-b5ddce83ac37)

A typical intra-city mapping, built in Tableau desktop looked like this: 

![image](https://github.com/cslim95/vw_id_targeting/assets/169668063/9fda3487-3e6d-4d1d-b7c3-1261f21db820)




