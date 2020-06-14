# Recommender_System_E_Commerce
The aim of this project is to create a recommender system based on the concept of item-based collabrorative filitering. The system should recommend products based on the recently bought items and items that are in the basket. In the process of creating the recommender system, the aim is to also understand customer behavior while using the system and understanding what brands are successful and why? 

The Data 

The data is provided by a E-Corp. The data looks like the following. 









Exploratory Data Analysis 

There are 801,575 unique order numbers, from which 2107537 products (at the l3 level) have been sold (including duplicates). There are 33 categories (l1) which contain 6203 unique products (at the l3 level).

Below is the list of l1 categories. 

['Power Tools', 'Safety', 'Hardware', 'Electronics, Appliances, and Batteries','Motors', 'Pneumatics', 'Hand Tools',
,'Security', 'HVAC and Refrigeration','Cleaning','Electrical', 'Pumps', 'Hydraulics', 'Welding', 'Lighting', 'Plumbing', 'Material Handling', 'Outdoor Equipment','Paint, Equipment and Supplies','Raw Materials', 'Lubrication', 'Fasteners','Fleet and Vehicle Maintenance','Adhesives, Sealants and Tape', 'Abrasives', 'Power Transmission', 'Machining','Furniture, Hospitality and Food Service','Test Instruments','Office Supplies','Lab Supplies','Reference and Learning Supplies',
 'UNCATEGORIZED']
 
 
 Basket Size:
 
 The average basket size is approximately 2.6 products to 2 significant figures, while the median is 1 product per basket. To add, (when sorted) 82% of the baskets have a size of three or under. Which indicate that individuals tend to use the platform only to buy a few products at a time. It seems as if people use the platform to quickly get something, they don't tend to use it for big shopping purposes. SHOW BOXPLOT 
 
 
 
 Keeping this in mind, the recommender system would play an important role because it can be a method to make the customer buy more products (instead of 1 at a time), which would help the company increase profits. 
 
 
 Below is the distribution of the the categories (l1) and the number of products that have been bought using the platform. 
 
 
 
As we can see, the distribution follows a long-tail distribution, what that indicates is that the system is mainly popular for the first 3/4 categories and then the system gets very few interactions/buys with the categories towards the end of the spectrum. The data suggests that people using E-Corp to mainly get products from the category of safety, material handling, hvac and refigeration. 



The following is a chart showing the most successful brands, because it shows the number of products they have sold. As we can see brand number 1793 is doing remarkably greater than the rest. Another thing to bear in mind is that this is also following the l shape. It seems as if customers are coming to the website to mainly buy products from the top 3 companies which means that new companies that enter the E-corp webiste would find it difficult to sell products because of the dominance in the market by the brands already. Will come back to this graph to understand why these brand are successful. 


Below are the most common products that are bought using the platform. 


The data above also supports a L-shaped format. To add, looking at the most successful products, it seems as if customers use e-corp to buy products which are mainly related to electrical parts and safety equipment. From this it is possible to infer that most of the customers would either be workers from a factory and or companies that are in the motor/electrical industry. 




The next step is to figure out in which high level category (l1) do the companies dominate in. I have used 2 standard deviations as the baseline because that is when statistically an event is considered an outlier. (The whole list is available in the notebook; I have listed a few here just for simplicity and readibility purposes). 

For example in the category of 'Electronics, Appliances, and Batteries' and 'Motors', brands 1231 and 1068 (are the only ones that) dominate the market as they sell the majority of the products in that category from the compeition. There are 45 companies in the field of Motors and there are 110 companies in the field of Electronics, Appliances, and Batteries. 


In the category of Office Supplies and Welding there are multiple brands which dominate each category(/industry). 

Wielding: brands which dominate the market are '1793', '2762', '4678', '4692', '4764', '4765'; there are a total of 115 brands in the market in the E-corp website. 

Office Supplies: brands which dominate the market are '1793', '34', '3404', '3788'; there are a total of 219 brands in the market in the E-corp website. 

It is not entirely clear on what makes brand matter based on this topics; however based on research and inference from the data it seems as if when the product is very accesible and maybe cheap (for example office supplies, weilding) and as long as the the purpose is fufilfilled, then the brand doesn't matter (for example pens a form of office supply, it doesn't really matter where it comes from as long as it fulfils the function it is required for. However, brand seems to matter when the performance/quality it is important, for example in the above examples batteries and motors having poor quality ones can affect the performance of the machine/task invovled. Getting bad quality batteries can affect the ability of a machine to work for longer periods of time, or having motors which are not of good quality can make the product require a lot of maintenance work on machines. Obviously there are a lot more factors which influence when brand matters for example branding, price, loyalty etc. The above were just inferences based on the data in hand. 


I have done the same for the actual product at an l3 level; however, the data does not provide an interesting facts. It shows that for 1007 products there is generally one brand that controls the majority of the market; and that there are 5196 products where there are no companies which dominate the market. Some of the top products (which don't have any one or more brands dominating the market place) include lab supplies, Material Handling, Tools and Plubming. This validates some of the inferences made ppreviously as most of the products from these categories, it doesn't matter about the quality that much as long as they can get the job done (brands won't matter when buying such products under most circumstances, even though there are probably well known brands in that market).

Now, I had a look back to understand why the top ten brands were selling the most products. 

Below are the stats:

Brands, Number of Products Sold, Number of Categories (l1), Number of Unique Products Sold
1793, 265879, 33, 1573
1068 108827 21 543
934 82306 4 161
4355 74020 16 161
4692 66984 21 516
258 47990 1 26
123 46445 3 29
9 38774 24 223
1726 35385 3 27
1231 35121 1 6


From the above data, a couple of patterns emerge. Brands which provide products from multiple categories (l1) have a higher chance of being successful in the E-Corp website. It could be that the platforms allows users to see all the other products the company sells and the user doesn't have to put more effort into exploring other brands, it could also go with the fact that products from the same brand could open up discounts when buying multiple products. Out of the top 10 selling brands, 5 brands sell more products which are in more than 15 categories (l1). The top selling brand, 1793, sell products from all categories is one the reasons why they are very successsful. The other 5 brands sell products in less than 5 categories, which imply that they are very specialized in those categories. Two of the brands only have a speciality in 1 category 258 and 1231. What this implies is that other brands are recongiznes because of their speciality as they would produce products which are very high quality in that specific industry, sell cheap products, and/or have very good branding. 


From the data, it seems as if a successful brand in the E-corp market is based on two factors speciality and variety.




#Recommender System

From the analysis it has become clear that the user's when buying products from E-corp don't tend to buy a lot of products at once. So the aim would be to create a recommender system that would recommend products based on what the user has recently put into the basket and the items in the whole basket to entice the user to buy more products (which would in turn increase the profit margins and products sold).

Data Class:

The aim of the data class is to load and prepare the data for the recommender system class to use and provide recommender systems based on the data provided. 

The data currently looks like this 



we want to get it to like this 


Preprocessing: 

I drop duplicates from the data because the aim is to find similarity between products and not worry about the quantity of how many the product were bought in the basket. I drop the columns sku, brand, l1,and l2 because I am not concerned with anything apart from the product; the aim is to be able to figure out products which are similar to the ones bought (not concerned with brands). I remove all the baskets which have a basket size of less than 10 because it would be very difficult to find accurate relations with basket sizes (of 2). This number is slighltly arbitrary; however, it is there with the purposes of making sure that the similarities we create between products are accurate. I expand the column l3 and consolidate the order so that I can convert each order number into a vector form of zeros and ones indicating zero if a product was not bought and 1 if it was. Consolidating the orders help sum up all the vectors with the same order number so they are all located in the same row. 


Recommender System:

The Recommender System class is responsible for creating the similarity matrix between the pairs of items, and recommend products based on recently bought item and the basket. 


Similarity measure: 

There are various types of similarity measurements that can be used to determine how related two products are: for ex there is pearson similarity and cosine. I tested the recommender system using these measurements and they gave bad results and the reason for this is because the two vectors which I place two find the similarities between are filled with zeros and ones, and it is very much possible in the dataset that there are two products which are not bought that frequently and have been bought once together (in the batch of 588 basket) and the measurement would say that these products are very highly related, when that is not necessarily the case. Therefore the measurements which I use are jaccard similarity and frequency; this is because these two metrics are better used when working with vectors with zeros and ones. 






Imrpovements: 


