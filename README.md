# EDA-on-HotelBooking-data-Analysis
A dataset containing 119390 records across 32 features has been given with information regarding bookings of two hotels from July 2015 to August 2017. These two hotels are City Hotel and Resort Hotel. 
# Dataset
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.
- hotel: Name of hotel ( City or Resort)
- is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
- lead_time: time (in days) between booking transaction and actual arrival.
- arrival_date_year: Year of arrival
- arrival_date_month: month of arrival
- arrival_date_week_number: week number of arrival date.
- arrival_date_day_of_month: Day of month of arrival date
- stays_in_weekend_nights: No. of weekend nights spent in a hotel
- stays_in_week_nights: No. of weeknights spent in a hotel
- adults: No. of adults in single booking record.
- children: No. of children in single booking record.
- babies: No. of babies in single booking record. 
- meal: Type of meal chosen 
- country: Country of origin of customers (as mentioned by them)
- market_segment: What segment via booking was made and for what purpose.
- distribution_channel: Via which medium booking was made.
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for 
                     Yes)
- previous_cancellations: No. of previous canceled bookings.
- previous_bookings_not_canceled: No. of previous non-canceled bookings.
- reserved_room_type: Room type reserved by a customer.
- assigned_room_type: Room type assigned to the customer.
- booking_changes: No. of booking changes done by customers
- deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
- agent: Id of agent for booking
- company: Id of the company making a booking
- days_in_waiting_list: No. of days on waiting list.
- customer_type: Type of customer(Transient, Group, etc.)
- adr: Average Daily rate.
- required_car_parking_spaces: No. of car parking asked in booking
- total_of_special_requests: total no. of special request.
- reservation_status: Whether a customer has checked out or canceled,or not showed 
- reservation_status_date: Date of making reservation status.
# Data Cleaning
(1)Removing Duplicate rows
All duplicate rows were dropped.
(2) Handling null values
Null values in columns company and agent were replaced by mean of the company column and mode of the agent column.
Null values in column country were replaced by 'bfill'method.
Null values in column children were replaced by the 0.
(3) Converting columns to appropriate data types
Changed data type of children, company, agent to int type.
(4) Removing outliers
One outlier was found in the adr column. Simply dropped it.
(5) Creating new columns
Created new column total_stay by adding stays_in_weekend_nights+stays_in_week_nights.
Created new column total_people by adding adults+children+babies.

# Exploratory Data Analysis
1. Correlation Analysis
It is used to measure the strength of the linear relationship between two variables and compute their association. Correlation analysis calculates the level of change in one variable due to the change in the other. Correlation analysis of the dataset was carried out using a correlation heatmap with the features.
2. Univariate Analysis
Uni means one and variate means variable, so in univariate analysis, there is only one dependable variable. The objective of univariate analysis is to derive the data, define and summarize it, and analyze the pattern present in it. In a dataset, it explores each variable separately.
3. Bivariate Analysis
Bi means two and variate means variable, so here there are two variables. The analysis is related to cause and the relationship between the two variables. 
# Conclusion
The following conclusions were drawn from analysis:

City hotels are the most preferred hotel type by the guests. We can say City hotel is the busiest hotel.
Most number of bookings are made in July and August.
agent iD no 9 made most number of booking
The length of the stay decreases as ADR increases probably to reduce the cost.
Room Type A is the most preferred room type among guests.
27.5 % bookings were got cancelled out of all the bookings.
Only 3.9 % people were revisited the hotels. Rest 96.1 % were new guests. Thus retention rate is low.
The percentage of 0 changes made in the booking was more than 82 %. Percentage of Single changes made was about 10%.
Most of the customers (91.6%) do not require car parking spaces.
79.1 % bookings were made through TA/TO (travel agents/Tour operators).
BB( Bed & Breakfast) is the most preferred type of meal by the guests.
Maximum number of guests were from Portugal, i.e. more than 25000 guests
Most of the bookings for City hotels and Resort hotel were happened in 2016.
Average ADR for city hotel is high as compared to resort hotels. These City hotels are generating more revenue than the resort hotels.
Booking cancellation rate is high for City hotels which almost 30 %.
Average lead time for resort hotel is high.
Waiting time period for City hotel is high as compared to resort hotels. That means city hotels are much busier than Resort hotels.
Optimal stay in both the type hotel is less than 5 days.
