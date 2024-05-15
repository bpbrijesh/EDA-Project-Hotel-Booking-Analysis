
![pexels-bohlemedia-2288281](https://github.com/bpbrijesh/EDA-Project-Hotel-Booking-Analysis/assets/166358322/f2912ebf-d9f0-451e-9a7c-06899d8a582f)

# EDA-Project-Hotel-Booking-Analysis

# Objective
The main objective is that to perform EDA on the given dataset and draw useful conclusions about general trends in hotel bookings and how factors governing hotel bookings interact with each other and which is the best time for booking .

# Dataset

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
- is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
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

# Data preparing and cleaning
1. check is there any null value or missing values
 a. In this dataset we get 112593 null value in 'company' column so we have replaced the null values with 0.
 b. In the 'agent' column we have also get 16340 so we have replaced it with 0.
 c. In country we can not set the country values as 0 becuase it contains country codes representing different countries. So instead of replacing it with zero we have     replaced it with the mode value in country column. Mode is nothing but just the most repeating value. 
 d. Children Column has the count of children then we replaced missing values with mean values.
2. Dropping some coloumn which does not make any sense Several rows in the dataset contains values that does not make any sense like having no adults, children and babies so we directly deleted it by using drop.
3. Change the data type Check the types of datatypes and converting it into int64.

# Exploratory data analysis

1) Hotels type ratio
2) Month wise arrival in the year
3) Hotel wise booking cancellation
4) Hotel wise Average Daily Rate
5) Country wise hotel bookings
6) Night Stay Duration
7) Market Segment Wise hotel bookings
8) Repeated Guests
9)  Pair Plot
10) Hostogram and Boxplot


# conclusion
(1) The pie chart reveals that 66% of the hotels in the dataset are city hotels and the other 34% are resort hotels.

(2)the months of November to March are off-peak periods for hoteliers. Between June and the end of August, attendance is at its peak, it is the high season.

(3)the booking for city hotel is higher than resort yearwise.

(4) Most of the guests came from european countries, with most of guests coming from Portugal.

(5) the most number of guests are 48483 which is from Portugal.

(6)more than 30000 booking were cancelled in city hotel followed by more than 10000 in resort hotel.

(7) most of the transient customers had cancelled the booking.

(8)Most of the market_segment used Online TA and Offline TA/TO

(9)Repeated guests are very few which is only 3.1 %. In order to retained the guests , hotels/resort management should take feedback from the guests in order to imporve their services.

(10)most preferred meal type by the guests is BB.

(11)most of the busiest months are July and August

(12)City hotel has maximum booking from the month April to September but after that there is fall down in booking Now for the Resort hotel March-May,June-August and November-January is busiest month

