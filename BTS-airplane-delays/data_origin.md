# BTS Flight Delays Dataset
**Source:** [Bureau of Transportation Statistics](https://www.transtats.bts.gov/DL_SelectFields.aspx?gnoyr_VQ=FGJ&QO_fu146_anzr=b0-gvzr)

To obtain the data, I downloaded all data for Jan 2025, Feb 2025, ..., Nov 2025 (11 datasets total). At the time of data-gathering, Dec 2025 is not yet available. 

The columns downloaded from the database are listed below:

| Field Name | Description |
| :--- | :--- |
| **FlightDate** | Flight Date (yyyymmdd) |
| **Reporting_Airline** | Unique Carrier Code (Use for analysis across a range of years) |
| **IATA_CODE_Reporting_Airline** | IATA Carrier Code (May not be unique over time; use Unique Carrier Code for analysis) |
| **Tail_Number** | Aircraft Tail Number |
| **Flight_Number_Reporting_Airline** | Flight Number |
| **OriginAirportID** | Unique Origin Airport ID (Persistent across airport code changes) |
| **Origin** | Origin Airport Code |
| **OriginCityName** | Origin Airport City Name |
| **OriginState** | Origin Airport State Code |
| **OriginStateFips** | Origin Airport State Fips |
| **DestAirportID** | Unique Destination Airport ID (Persistent across airport code changes) |
| **Dest** | Destination Airport Code |
| **DestCityName** | Destination Airport City Name |
| **DestState** | Destination Airport State Code |
| **DestStateFips** | Destination Airport State Fips |
| **CRSDepTime** | Scheduled Departure Time (local time: hhmm) |
| **DepTime** | Actual Departure Time (local time: hhmm) |
| **DepDelay** | Difference in minutes between scheduled and actual departure (Early = negative) |
| **TaxiOut** | Taxi Out Time (Minutes) |
| **WheelsOff** | Wheels Off Time (local time: hhmm) |
| **TaxiIn** | Taxi In Time (Minutes) |
| **CRSArrTime** | Scheduled Arrival Time (local time: hhmm) |
| **ArrTime** | Actual Arrival Time (local time: hhmm) |
| **ArrDelay** | Difference in minutes between scheduled and actual arrival (Early = negative) |
| **Cancelled** | Cancelled Flight Indicator (1=Yes) |
| **CancellationCode** | Specifies The Reason For Cancellation |
| **Diverted** | Diverted Flight Indicator (1=Yes) |
| **CRSElapsedTime** | Scheduled Elapsed Time of Flight (Minutes) |
| **ActualElapsedTime** | Actual Elapsed Time of Flight (Minutes) |
| **AirTime** | Flight Time in Air (Minutes) |
| **Flights** | Number of Flights |
| **Distance** | Distance between airports (Miles) |
| **CarrierDelay** | Carrier Delay (Minutes) |
| **WeatherDelay** | Weather Delay (Minutes) |
| **NASDelay** | National Air System Delay (Minutes) |
| **SecurityDelay** | Security Delay (Minutes) |
| **LateAircraftDelay** | Late Aircraft Delay (Minutes) |