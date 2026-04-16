# Data Dictionary

## Dataset Overview

  Attribute       Value
  --------------- -----------------------------------
  Dataset Name    2017 Yellow Taxi Trip Data
  Source          NYC Taxi and Limousine Commission
  Total Rows      22,699
  Total Columns   18
  Description     Each row represents a taxi trip

------------------------------------------------------------------------

## Column Details

  --------------------------------------------------------------------------
  Column Name             Description           Values / Notes
  ----------------------- --------------------- ----------------------------
  ID                      Trip identification   Unique ID
                          number                

  VendorID                Provider code         1 = Creative Mobile
                                                Technologies, 2 = VeriFone

  tpep_pickup_datetime    Pickup date and time  Meter start time

  tpep_dropoff_datetime   Dropoff date and time Meter end time

  passenger_count         Number of passengers  Driver entered

  trip_distance           Distance travelled    In miles

  PULocationID            Pickup zone           TLC Zone ID

  DOLocationID            Dropoff zone          TLC Zone ID

  RateCodeID              Rate code             1 = Standard, 2 = JFK, 3 =
                                                Newark, 4 =
                                                Nassau/Westchester, 5 =
                                                Negotiated, 6 = Group ride

  store_and_fwd_flag      Stored before sending Y = Yes, N = No

  payment_type            Payment method        1 = Credit card, 2 = Cash, 3
                                                = No charge, 4 = Dispute, 5
                                                = Unknown, 6 = Voided

  fare_amount             Base fare             Meter calculated

  extra                   Extra charges         Rush hour, overnight charges

  MTA_tax                 MTA tax               Fixed 0.50

  improvement_surcharge   Improvement surcharge Fixed 0.30

  tip_amount              Tip amount            Credit card tips only

  tolls_amount            Toll charges          Total tolls

  total_amount            Total fare            Excludes cash tips
  --------------------------------------------------------------------------

------------------------------------------------------------------------

## Business Context

Automatidata is a data consulting firm that helps organizations convert
raw data into useful business insights.

They are working with the New York City Taxi and Limousine Commission to
build a regression model for predicting taxi fares before the ride.

The data comes from more than 200,000 licensed vehicles and represents
around one million trips per day.

------------------------------------------------------------------------

## Note

This dataset is a sampled version created for learning purposes and may
not fully represent real world taxi behavior.
