# Recommender_System_E_Commerce
The aim of this project is to create a recommender system based on the concept of item-based collabrorative filitering. The system should recommend products based on the recently bought items and items that are in the basket. In the process of creating the recommender system, the aim is to also understand customer behavior while using the system and understanding what brands are successful and why? 

The Data 

The data is provided by a E-Corp. The data looks like the following. 









Exploratory Data Analysis 

There are 801,575 unique order numbers which have taken place, from which 2107537 products (at the l3 level) have been sold (including duplicates). There are 33 categories (l1) which contain 6203 unique products (at the l3 level).

Below is the list of l1 categories. 

['Power Tools', 'Safety', 'Hardware', 'Electronics, Appliances, and Batteries','Motors', 'Pneumatics', 'Hand Tools',
,'Security', 'HVAC and Refrigeration','Cleaning','Electrical', 'Pumps', 'Hydraulics', 'Welding', 'Lighting', 'Plumbing', 'Material Handling', 'Outdoor Equipment','Paint, Equipment and Supplies','Raw Materials', 'Lubrication', 'Fasteners','Fleet and Vehicle Maintenance','Adhesives, Sealants and Tape', 'Abrasives', 'Power Transmission', 'Machining','Furniture, Hospitality and Food Service','Test Instruments','Office Supplies','Lab Supplies','Reference and Learning Supplies',
 'UNCATEGORIZED']
 
 
 Basket Size:
 
 The average basket size is about 2.6 products, while the median is 1 product per basket. To add, (when sorted) 82% of the baskets have a size of three or under. Which indicate that individuals tend to use the platform only to buy a few products at a time. It seems as if people go use the platform to quickly get something, they don't tend to use it for big shopping purposes. SHOW BOXPLOT 
 
 
 
 Keeping this in mind, the recommender system would play in important role because it can be a method to make the customer buy more products (instead of 1 at a time), which would help the company get more profits. 
 
 
 Below is the distribution of the the categories (l1) and the number of products that have been bought using the platform. 
 
 
 
As we can see, the distribution follows an L shape, what that indicates is that the system is mainly popular for the first 3/4 categories and then the system gets very few interactions/buys with the categories towards the end of the spectrum. The data suggests that people using E-Corp to mainly get products from the category of safety, material handling, hvac and refigeration. 



The following is a chart showing the most successful brands, because it shows the number of products they have sold. As we can see brand number 1793 is doing remarkably greater than the rest. Another thing to bear in mind is that this is also following the l shape. It seems as if customers are coming to the website to mainly buy products from the top 3 companies which means that new companies that enter the E-corp webiste would find it difficult to sell products because of the dominance in the market by the brands already. Will come back to this graph to understand why these brand are successful. 


Below are the most common products that are bought using the platform. 


The data above also supports a L-shaped format. To add, looking at the most successful products, it seems as if customers use e-corp to buy products which are mainly related to electrical parts and safety equipment. From this it is possible to infer that most of the customers would either be workers from a factory and or companies that are in the motor/electrical industry. 




The next step is to figure out in which high level category (l1) do the companies dominate in. I have used 2 standard deviations as the baseline because that is when statistically an event is considered an outlier. (The whole list is available in the notebook; I have listed a few here just for simplicity and readibility purposes). 

For example in the category of 'Electronics, Appliances, and Batteries' and 'Motors', brands 1231 and 1068 (are the only ones that) dominate the market as they sell the majority of the products in that category from the compeition. There are 45 companies in the field of Motors and there are 110 companies in the field of Electronics, Appliances, and Batteries. 


In the category of Office Supplies and Welding there are multiple brands which dominate each category(/industry). 

Wielding: brands which dominate the market are '1793', '2762', '4678', '4692', '4764', '4765'; there are a total of 115 brands in the market in the E-corp website. 

Office Supplies: brands which dominate the market are '1793', '34', '3404', '3788'; there are a total of 219 brands in the market in the E-corp website. 

It is not entirely clear on what makes brand matter based on this topics; however based on research and inference from the data it seems as if the products which are 



