# Hotel-Meal-Predection

## Data:
I got this data from www.kaggle.com . The link for the data is in the program folder.

## Descreption:
The meaning of each colums are

1. hotel Hotel (H1 = Resort Hotel or H2 = City Hotel)

2. is_canceledValue indicating if the booking was canceled (1) or not (0)

3. lead_timeNumber of days that elapsed between the entering date of the booking into the PMS and the arrival date

4. arrival_date_yearYear of arrival date

5. arrival_date_monthMonth of arrival date

6. arrival_date_week_numberWeek number of year for arrival date

7. arrival_date_day_of_monthDay of arrival date

8. stays_in_weekend_nightsNumber of weekend nights (Saturday or Sunday) the guest stayed or booked to stay at the hotel

9. stays_in_week_nightsNumber of week nights (Monday to Friday) the guest stayed or booked to stay at the hotel

10. adultsNumber of adults

11. childrenNumber of children

12. babiesNumber of babies

13. mealType of meal booked. Categories are presented in standard hospitality meal packages: Undefined/SC – no meal package; BB – Bed & Breakfast; HB – Half board (breakfast and one other meal – usually dinner); FB – Full board (breakfast, lunch and dinner)

14. countryCountry of origin. Categories are represented in the ISO 3155–3:2013 format

15. market_segmentMarket segment designation. In categories, the term “TA” means “Travel Agents” and “TO” means “Tour Operators”

16. distribution_channelBooking distribution channel. The term “TA” means “Travel Agents” and “TO” means “Tour Operators”

17. is_repeated_guestValue indicating if the booking name was from a repeated guest (1) or not (0)

18. previous_cancellationsNumber of previous bookings that were cancelled by the customer prior to the current booking

19. previous_bookings_not_canceledNumber of previous bookings not cancelled by the customer prior to the current booking

20. reserved_room_typeCode of room type reserved. Code is presented instead of designation for anonymity reasons.

21. assigned_room_type
Code for the type of room assigned to the booking. Sometimes the assigned room type differs from the reserved room type due to hotel operation reasons (e.g. overbooking) or by customer request. Code is presented instead of designation for anonymity reasons.

22. booking_changesNumber of changes/amendments made to the booking from the moment the booking was entered on the PMS until the moment of check-in or cancellation

23. deposit_typeIndication on if the customer made a deposit to guarantee the booking. This variable can assume three categories: No Deposit – no deposit was made; Non Refund – a deposit was made in the value of the total stay cost; Refundable – a deposit was made with a value under the total cost of stay.

24. agentID of the travel agency that made the booking

25. companyID of the company/entity that made the booking or responsible for paying the booking. ID is presented instead of designation for anonymity reasons

26. days_in_waiting_listNumber of days the booking was in the waiting list before it was confirmed to the customer
customer_type

27. Type of booking, assuming one of four categories:
Contract - when the booking has an allotment or other type of contract associated to it; Group – when the booking is associated to a group; Transient – when the booking is not part of a group or contract, and is not associated to other transient booking; Transient-party – when the booking is transient, but is associated to at least other transient booking

28. adr Average Daily Rate as defined by dividing the sum of all lodging transactions by the total number of staying nights

29. required_car_parking_spacesNumber of car parking spaces required by the customer

30. total_of_special_requestsNumber of special requests made by the customer (e.g. twin bed or high floor)

31. reservation_statusReservation last status, assuming one of three categories: Canceled – booking was canceled by the customer; Check-Out – customer has checked in but already departed; No-Show – customer did not check-in and did inform the hotel of the reason why

32. reservation_status_dateDate at which the last status was set. This variable can be used in conjunction with the ReservationStatus to understand when was the booking canceled or when did the customer checked-out of the hotel

## Columns used for ML:
'is_canceled','lead_time','arrival_date_year','arrival_date_month','arrival_date_week_number','arrival_date_day_of_month',
'stays_in_week_nights','stays_in_weekend_nights','adults','children','babies','agent','adr','total_of_special_requests','required_car_parking_spaces',"meal"

where "meal" is the Target and all the other columns are Feature 

## Algorithm Used and their accuracy:

Since we are going to predict meal that the coustomer will choose. We can use the Classification algorithm for this problem.

I have used 
[K-Nearest Neighbors (KNN)] accuracy_score: 0.799.
[Decision Tree -- entropy] accuracy_score: 0.849.
[Decision Tree -- gini] accuracy_score: 0.834.
[RandomForest] accuracy_score: 0.866.
