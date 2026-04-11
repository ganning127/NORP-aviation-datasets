<h1 align="center">ADS-C Text File</h1>

# 1. Message Structure

## 1.1 Flight Information Header

- **Registration**: Registration number of the aircraft.
- **ICAO ID**: Unique identifier assigned to the aircraft by the International Civil Aviation Organization.
- **ATSU Address**: Air Traffic Service Unit Address, which typically includes the area the plane is flying over.
- **Channel Frequency**: The frequency channel being used.

## 1.2 ADS-C Message with FANS Headers and Checksum

Within this message, there are various tags representing different types of data:

### Tag 03 (Acknowledgement)

- Contract Number: A number related to the contract.

---

### Tag 04 (Negative Acknowledgement)

- Contract Request Number
- Reason

---

### Tag 05 (Noncompliance Notification)

- Contract Number

---

### Tag 06 (Cancel Emergency Mode)

- Emergency Mode Cancelled

---

### Tag 07 (Basic Report)

- Latitude: Latitude of the aircraft.
- Longitude: Longitude of the aircraft.
- Altitude: Current altitude of the aircraft in feet.
- Timestamp: The time the data was logged.
- Position accuracy: Accuracy of the positional data.
- NAV redundancy: Navigation system status.
- TCAS: Traffic Collision Avoidance System status.

---

### Tag 09 (Emergency Basic report)

Same data structure as Tag 07, but relates to a significant emergency event.

---

### Tag 10 (Lateral Deviation Change Event)

Same data structure as Tag 07, but relates to a significant lateral deviation change event.

---

### Tag 12 (Flight ID)

- Flight ID: Unique identifier for the flight.

---

### Tag 13 (Predicted Route)

- Next waypoint:
  - Latitude, Longitude, Altitude, and ETA (Estimated Time of Arrival) for the next waypoint.
- Next+1 waypoint:
  - Latitude, Longitude, Altitude for the waypoint after the next one.

---

### Tag 14 (Earth Reference Data)

- True track: The actual path that the aircraft has been following.
- Ground speed: The speed of the aircraft relative to the ground.
- Vertical speed: Speed at which the aircraft is ascending or descending.

---

### Tag 16 (Meteorological Data)

- Wind speed: Current wind speed.
- True wind direction: The actual direction from which the wind is blowing.
- Temperature: Current outside temperature in Celsius.

---

### Tag 18 (Vertical Rate Change Event)

Same data structure as Tag 07, but relates to a significant vertical rate change event.

---

### Tag 19 (Altitude Range Event)

Same data structure as Tag 07, but relates to a significant altitude range event.

---

### Tag 20 (Waypoint Change Event)

Same data structure as Tag 07, but relates to a significant waypoint change event.

---

### Tag 22 (Intermediate Projected Intent Group)

- Distance: Distance to the target location from the current position.
- True track: Direction or bearing of the path relative to the geographical North (True North).
- Altitude: Altitude of the point.
- ETA: Estimated Time of Arrival

---

### Tag 23 (Fixed Projected Intent Group)

- Lat: Latitude of the point.
- Lon: Longitude of the point.
- Alt: Altitude of the point.
- ETA: Estimated Time of Arrival.

---

**CRC**: Cyclic Redundancy Check. A code to ensure data integrity during transmission.

---
# 2. Data analysis
## 2.1 Messages

**First message of ADSC**: 2023-07-07 15:07:18:1688742438

**Last message of ADSC**: 2023-10-20 09:10:50:1697793050

- **Total Messages**: 227126
- **Decoded messages**: 227126
- **Messages with position**: 196951 (86.71%)

---

## 2.2 Tag Counts and Percentages

- **Tag 07 Basic report**: Count: 146537, Percentage: 64.518%
- **Tag 13 Predicted Route**: Count: 145311, Percentage: 63.978%
- **Tag 14 Earth Reference data**: Count: 74189, Percentage: 32.664%
- **Tag 16 Meteorological data**: Count: 60758, Percentage: 26.751%
- **Tag 03 Acknowledgement**: Count: 50441, Percentage: 22.208%
- **Tag 14 Air Reference Data**: Count: 47818, Percentage: 21.054%
- **Tag 12 Flight ID**: Count: 47448, Percentage: 20.891%
- **Tag 20 Waypoint Change Event**: Count: 44124, Percentage: 19.427%
- **Tag 19 Altitude Range Event**: Count: 6272, Percentage: 2.761%
- **Tag 23 Fixed Projected Intent Group**: Count: 1839, Percentage: 0.810%
- **Tag 04 Negative Acknowledgement**: Count: 1265, Percentage: 0.557%
- **Tag 22 Intermediate Projected Intent Group**: Count: 945, Percentage: 0.416%
- **Tag 05 Noncompliance Notification**: Count: 388, Percentage: 0.171%
- **Tag 18 Vertical Rate Change Event**: Count: 99, Percentage: 0.044%
- **Tag 10 Lateral Deviation Change Event**: Count: 80, Percentage: 0.035%
- **Tag 09 Emergency Basic report**: Count: 16, Percentage: 0.007%
- **Tag 17 Airframe Identification Group**: Count: 10, Percentage: 0.004%
- **Tag 06 Cancel Emergency Mode**: Count: 2, Percentage: 0.001%

---

## 2.3 Aircrafts and ATSU addresses

**2999 unique aircraft registrations in the file**.

**Aircraft with the most messages**: F-HHUG  No of messages: 2216

**72 unique ATSU Addresses in the file**.

**ATSU Adress with most messages**: PIKCPYA - Shanwick (55102 messages)
