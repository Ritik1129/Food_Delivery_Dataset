# Food_Delivery_Dataset

Dataset Description
This dataset contains information related to delivery orders, delivery personnel, and other relevant factors for analyzing delivery logistics. The dataset is structured in a star schema, which consists of one central fact table and several dimension tables. Below is an overview of each component of the dataset:

Fact Table
fact_df: This table represents the core data of the delivery operations, linking the dimensions together with relevant metrics.

Columns:
ID: Unique identifier for each delivery.
Delivery_person_ID: Unique identifier for each delivery person.
Order_Date: Date when the order was placed.
Time_Orderd: Time when the order was placed.
Time_Order_picked: Time when the order was picked up by the delivery person.
Delivery_person_Ratings: Ratings received by the delivery person.
Restaurant_latitude, Restaurant_longitude: GPS coordinates of the restaurant.
Delivery_location_latitude, Delivery_location_longitude: GPS coordinates of the delivery location.

Dimension Tables
Delivery Person Dimension Table - 
delivery_person_dimension_df: This dimension provides information about the delivery personnel.

Columns:
Delivery_person_ID: Unique identifier for each delivery person.
Delivery_person_Age: Age of the delivery person.
Vehicle_condition: Condition of the delivery vehicle as rated by the delivery person or service personnel.

Order Dimension Table -
order_dimension_df: This dimension provides details about individual orders.

Columns:
ID: Unique identifier for each delivery.
Type_of_order: Type of food or item being ordered (e.g., grocery, restaurant, etc.).
Type_of_vehicle: Type of vehicle used for delivery (e.g., bike, car, etc.).
multiple_deliveries: Number of deliveries grouped with this order (if any).

Festival: Indicates if the delivery took place during a festival.
Location Dimension Table -
location_dimension_df: This dimension provides information related to delivery locations and conditions.

Columns:
ID: Unique identifier for each delivery.
City: The city where the delivery took place.
Weatherconditions: Weather conditions at the time of delivery.
Road_traffic_density: Traffic density during the delivery period.
