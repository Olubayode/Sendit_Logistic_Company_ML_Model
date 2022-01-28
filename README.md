# Sendit_Logistic_Company_ML_Model

### Sendit is a logistics company with presence all over Sub-Saharan Africa.
Sendit is Logistics in Sub-Saharan Africa which increases the cost of manufactured goods by up to 320%; while in Europe, it only accounts for up to 90% of the manufacturing cost.

This ML solution help Sendit enhance customer communication and improve the reliability of its service; which will ultimately improve customer experience. In addition, the solution will enable Sendit to realise cost savings, and ultimately reduce the cost of doing business, through improved resource management and planning for order scheduling.

Sendit helps men and women behind every type of business to trade easily, deliver more competitively, and build extraordinary businesses.

The data provided is a critical component in helping Sendit to build more efficient, affordable and accessible solutions. Given the details of a Sendit order, I use historic data to predict an accurate time for the arrival of the rider at the destination of a package. 

My main task is to build a model that predicts an accurate delivery time, from picking up a package to arriving at the final destination. An accurate arrival time prediction will help all businesses to improve their logistics and communicate an accurate time to their customers.

### The Data
The dataset provided includes order details and rider metrics based on orders made on the Sendit platform. The challenge is to predict the estimated time of arrival for orders- from pick-up to drop-off.

The training dataset provided here is a subset of over 20,000 orders and only includes direct orders (i.e. Sendit “express” orders) with bikes in Lagos. Furthermore, I also have data about the weather, that corresponds to the time of the order.

### The necessary files are: 
Train.csv - is the dataset that i useed to train my model. 
Test.csv - is the dataset on which I apply my model to. 
Riders.csv - contains unique rider Ids, number of orders, age, rating and number of ratings 
VariableDefinitions.csv - Definitions of variables in the Train, Test and Riders files

#### Variables

Order details

Order No – Unique number identifying the order

User Id – Unique number identifying the customer on a platform

Vehicle Type – bikes, however in practice

Platform Type – Platform used to place the order, there are 4 types

Personal or Business – Customer type

Placement times

Placement - Day of Month i.e 1-31

Placement - Weekday (Monday = 1)

Placement - Time - Time of day the order was placed

Confirmation times

Confirmation - Day of Month i.e 1-31

Confirmation - Weekday (Monday = 1)

Confirmation - Time - time of day the order was confirmed by a rider

Arrival at Pickup times

Arrival at Pickup - Day of Month i.e 1-31

Arrival at Pickup - Weekday (Monday = 1)

Arrival at Pickup - Time - Time of day the rider arrived at the location to pick up the order - as marked by the rider through the Sendit application

Pickup times

Pickup - Day of Month i.e 1-31

Pickup - Weekday (Monday = 1)

Pickup - Time - Time of day the rider picked up the order - as marked by the rider through the Sendy application

Arrival at Destination times (column missing in Test set)

Arrival at Delivery - Day of Month i.e 1-31

Arrival at Delivery - Weekday (Monday = 1)

Arrival at Delivery - Time - Time of day the rider arrived at the destination to deliver the order - as marked by the rider through the Sendit application

Distance covered (KM) - The distance from Pickup to Destination

Temperature -Temperature at the time of order placement in Degrees Celsius (measured every three hours)

Precipitation in Millimeters - Precipitation at the time of order placement (measured every three hours)

Pickup Latitude and Longitude - Latitude and longitude of pick up location

Destination Latitude and Longitude - Latitude and longitude of delivery location

Rider ID – ID of the Rider who accepted the order

Time from Pickup to Arrival - Time in seconds between ‘Pickup’ and ‘Arrival at Destination’ - calculated from the columns for the purpose of facilitating the task

Rider metrics*

Rider ID – Unique number identifying the rider (same as in order details)

No of Orders – Number of Orders the rider has delivered

Age – Number of days since the rider delivered the first order

Average Rating – Average rating of the rider

No of Ratings - Number of ratings the rider has received. Rating an order is optional for the customer.

I used CATBOOST regression algorithm to build a model that accurately predict delivery time and I used my model on the test data set. 
Then I Saved my test prediction result as a csv in the format . Good luck!
