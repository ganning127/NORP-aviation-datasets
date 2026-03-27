# Aviation Safety Reporting System (ASRS) Dataset

All data was downloaded from https://asrs.arc.nasa.gov/search/database.html.

The only search criteria used is for all data from January to December 2025.

### Report & Time Information
* **`acn`**: Accession Number; the unique identifier for the ASRS report.
* **`date`**: The date (year and month) the incident occurred.
* **`local_time_of_day`**: The general block of time the event happened (e.g., 0601-1200).
* **`synopsis`**: The official, brief ASRS summary of the incident.
* **`full_narrative`**: The combined, detailed first-hand account(s) written by the reporter(s).
* **`asrs_report_number_accession_number_1`**: The secondary ACN if multiple reports were merged into this single event.

### Location & Environment
* **`locale_reference`**: The closest facility, airport, or navigational aid.
* **`state_reference`**: The US state where the incident occurred.
* **`relative_position_distance_nautical_miles`**: Distance in nautical miles from the locale reference.
* **`altitude_agl_single_value`**: Altitude Above Ground Level (AGL) in feet.
* **`altitude_msl_single_value`**: Altitude Mean Sea Level (MSL) in feet.
* **`flight_conditions`**: Visual (VMC) or Instrument (IMC) conditions.
* **`light`**: Lighting conditions (e.g., Daylight, Night).
* **`ceiling`**: Height of the lowest broken or overcast cloud layer in feet.

### Primary Aircraft (Aircraft 1)
* **`atc_advisory`**: Primary Air Traffic Control facility handling the aircraft (e.g., tower, center).
* **`aircraft_operator`**: Type of operation (e.g., Air Carrier, Personal).
* **`make_model_name`**: Make and model of the aircraft.
* **`crew_size`**: Number of flight crew members aboard.
* **`operating_under_far_part`**: Federal Aviation Regulation (FAR) rules the flight operated under (e.g., Part 91, 121).
* **`flight_plan`**: Type of flight plan filed (e.g., VFR, IFR).
* **`mission`**: Purpose of the flight (e.g., Passenger, Training).
* **`flight_phase`**: Phase of flight during the incident (e.g., Cruise, Takeoff).
* **`airspace`**: Class of airspace the aircraft was in (e.g., class b, class g).
* **`aircraft_component`**: Specific physical part/system involved in the issue.
* **`problem`**: Primary nature of the equipment issue (e.g., failed, malfunctioning).

### Secondary Aircraft (Aircraft 2)
* **`atc_advisory_1`**: Primary ATC facility for the second aircraft.
* **`aircraft_operator_1`**: Operator type for the second aircraft.
* **`make_model_name_1`**: Make and model of the second aircraft.
* **`crew_size_1`**: Number of crew members on the second aircraft.
* **`operating_under_far_part_1`**: FAR operating rules for the second aircraft.
* **`flight_phase_1`**: Phase of flight for the second aircraft.
* **`airspace_1`**: Airspace class for the second aircraft.

### Reporter Information (Reporters 1 & 2)
* **`location_in_aircraft`** / **`location_in_aircraft_1`**: Specific location inside the aircraft (e.g., Flight Deck).
* **`reporter_organization`** / **`reporter_organization_1`**: The entity the reporter represents or works for.

### Event Detection & Assessment
* **`detector`**: The person or system that first noticed the problem.
* **`when_detected`**: The phase of flight or operation when the issue was recognized.
* **`primary_problem`**: The root cause of the incident as determined by ASRS.

---

### Anomaly Indicators (Boolean 0/1 Flags)
*Indicates whether a specific type of event or deviation occurred.*

**Equipment & ATC:**
* **`anomaly_aircraft_equipment_problem_critical`**: Severe mechanical or system failure.
* **`anomaly_aircraft_equipment_problem_less_severe`**: Minor mechanical or system issue.
* **`anomaly_atc_issue_all_types`**: Any Air Traffic Control operational issue.

**Conflicts & Airspace:**
* **`anomaly_airspace_violation_all_types`**: Unauthorized entry into airspace.
* **`anomaly_conflict_airborne_conflict`**: Loss of separation in the air.
* **`anomaly_conflict_ground_conflict`**: Loss of separation on the ground.
* **`anomaly_conflict_nmac`**: Near Midair Collision (typically < 500 feet).

**Flight Deviations:**
* **`anomaly_deviation_altitude_crossing_restriction_not_met`**: Missed assigned crossing altitude.
* **`anomaly_deviation_altitude_excursion_from_assigned_altitude`**: Wandered off assigned altitude.
* **`anomaly_deviation_altitude_overshoot`**: Climbed/descended past assigned altitude.
* **`anomaly_deviation_altitude_undershoot`**: Failed to reach assigned altitude.
* **`anomaly_deviation_speed_all_types`**: Deviated from assigned airspeed.
* **`anomaly_deviation_track_heading_all_types`**: Deviated from assigned heading/route.

**Procedural Deviations:**
* **`anomaly_deviation_discrepancy_procedural_clearance`**: Failed to follow ATC clearance.
* **`anomaly_deviation_discrepancy_procedural_far`**: Violated a Federal Aviation Regulation.
* **`anomaly_deviation_discrepancy_procedural_hazardous_material_violation`**: Hazmat rule violation.
* **`anomaly_deviation_discrepancy_procedural_landing_without_clearance`**: Landed without tower approval.
* **`anomaly_deviation_discrepancy_procedural_maintenance`**: Improper maintenance action.
* **`anomaly_deviation_discrepancy_procedural_mel_cdl`**: Flew with unauthorized broken equipment.
* **`anomaly_deviation_discrepancy_procedural_other_unknown`**: Unclassified procedural rule break.
* **`anomaly_deviation_discrepancy_procedural_published_material_policy`**: Ignored chart or company policy.
* **`anomaly_deviation_discrepancy_procedural_security`**: Security protocol breach.
* **`anomaly_deviation_discrepancy_procedural_unauthorized_flight_operations_uas`**: Unauthorized drone operation.
* **`anomaly_deviation_discrepancy_procedural_weight_and_balance`**: Flew outside weight/balance limits.

**Cabin Events:**
* **`anomaly_flight_deck_cabin_aircraft_event_illness_injury`**: In-flight medical emergency.
* **`anomaly_flight_deck_cabin_aircraft_event_other_unknown`**: Unclassified cabin event.
* **`anomaly_flight_deck_cabin_aircraft_event_passenger_electronic_device`**: Issue with passenger electronics.
* **`anomaly_flight_deck_cabin_aircraft_event_passenger_misconduct`**: Unruly passenger.
* **`anomaly_flight_deck_cabin_aircraft_event_smoke_fire_fumes_odor`**: Smoke, fire, or fumes in aircraft.

**Ground Events:**
* **`anomaly_ground_event_encounter_aircraft`**: Proximity/strike with aircraft on ground.
* **`anomaly_ground_event_encounter_fod`**: Foreign Object Debris encounter.
* **`anomaly_ground_event_encounter_fuel_issue`**: Ground fuel spill or misfueling.
* **`anomaly_ground_event_encounter_gear_up_landing`**: Landed without gear deployed.
* **`anomaly_ground_event_encounter_ground_equipment_issue`**: Issue with tugs, loaders, etc.
* **`anomaly_ground_event_encounter_ground_strike_aircraft`**: Tail/wing strike on ground.
* **`anomaly_ground_event_encounter_jet_blast`**: Damage/issue from jet wash.
* **`anomaly_ground_event_encounter_loss_of_aircraft_control`**: Lost directional control on ground.
* **`anomaly_ground_event_encounter_object`**: Struck stationary object on ground.
* **`anomaly_ground_event_encounter_other_unknown`**: Unclassified ground event.
* **`anomaly_ground_event_encounter_person_animal_bird`**: Ground personnel or animal encounter.
* **`anomaly_ground_event_encounter_vehicle`**: Ground vehicle encounter.
* **`anomaly_ground_event_encounter_weather_turbulence`**: Ground weather issue.
* **`anomaly_ground_excursion_ramp`**: Drove off paved ramp.
* **`anomaly_ground_excursion_runway`**: Veered off runway.
* **`anomaly_ground_excursion_taxiway`**: Veered off taxiway.
* **`anomaly_ground_incursion_ramp`**: Unauthorized entry to ramp.
* **`anomaly_ground_incursion_runway`**: Unauthorized entry to runway.
* **`anomaly_ground_incursion_taxiway`**: Unauthorized entry to taxiway.

**In-flight Events:**
* **`anomaly_inflight_event_encounter_aircraft`**: Airborne proximity issue.
* **`anomaly_inflight_event_encounter_bird_animal`**: Airborne bird strike.
* **`anomaly_inflight_event_encounter_cftt_cfit`**: Controlled Flight Toward/Into Terrain.
* **`anomaly_inflight_event_encounter_fly_away_uas`**: Drone lost connection and flew off.
* **`anomaly_inflight_event_encounter_fuel_issue`**: Airborne low fuel/starvation.
* **`anomaly_inflight_event_encounter_laser`**: Laser illumination event.
* **`anomaly_inflight_event_encounter_loss_of_aircraft_control`**: Temporary loss of control (e.g., stall).
* **`anomaly_inflight_event_encounter_object`**: Airborne object strike (e.g., balloon).
* **`anomaly_inflight_event_encounter_other_unknown`**: Unclassified inflight event.
* **`anomaly_inflight_event_encounter_unstabilized_approach`**: Poorly flown landing approach.
* **`anomaly_inflight_event_encounter_vfr_in_imc`**: Flying into clouds without instrument clearance.
* **`anomaly_inflight_event_encounter_wake_vortex_encounter`**: Encountered wake turbulence.
* **`anomaly_inflight_event_encounter_weather_turbulence`**: Severe weather/turbulence encounter.

**Severity / General Types:**
* **`anomaly_critical`**: Highly critical/dangerous event.
* **`anomaly_less_severe`**: Minor event.
* **`anomaly_no_specific_anomaly_occurred_all_types`**: Unclassified incident.
* **`anomaly_no_specific_anomaly_occurred_unwanted_situation`**: Bad situation without rules broken.

---

### Reporter Function Flags (`function_` & `function_1_`)
*Indicates the specific role/job of the reporter(s) at the time of the incident.*
* **`function_[role]`**: Primary reporter's role (e.g., `function_captain`, `function_first_officer`, `function_dispatcher`, `function_student_pilot`, `function_approach` [ATC], `function_passenger`, `function_visual_observer_uas`).
* **`function_1_[role]`**: Secondary reporter's role (matching the categories above).

---

### Human Factors & Communication (`human_factors_` & `communication_breakdown_`)
*Indicates contributing human elements and specific communication failures.*
* **`human_factors_[factor]`**: Primary reporter's human factor (e.g., `confusion`, `distraction`, `fatigue`, `situational_awareness`, `time_pressure`, `workload`).
* **`human_factors_1_[factor]`**: Secondary reporter's human factor.
* **`communication_breakdown_party1_[party]`**: The first party involved in a miscommunication (e.g., `atc`, `flight_crew`).
* **`communication_breakdown_party2_[party]`**: The second party involved in a miscommunication.

---

### Event Results (`result_`)
*Indicates the operational outcome of the incident.*
* **ATC Actions**: `result_air_traffic_control_issued_advisory_alert`, `_issued_new_clearance`, `_provided_assistance`, `_separated_traffic`.
* **Aircraft/UAS State**: `result_aircraft_aircraft_damaged`, `_automated_return_to_home_uas`, `_equipment_problem_dissipated`, `_lost_unrecoverable_uas`, `_lost_link_uas`.
* **Flight Crew Actions**: e.g., `result_flight_crew_diverted`, `_executed_go_around_missed_approach`, `_landed_in_emergency_condition`, `_rejected_takeoff`, `_returned_to_departure_airport`, `_took_evasive_action`.
* **General Outcomes**: e.g., `result_general_evacuated`, `_flight_cancelled_delayed`, `_maintenance_action`, `_physical_injury_incapacitation`, `_police_security_involved`.

---

### Contributing Factors (`contributing_factors_situations_`)
*Broad environmental or systemic elements that contributed to the event.*
* **`contributing_factors_situations_[factor]`**: e.g., `aircraft`, `airport`, `airspace_structure`, `company_policy`, `human_factors`, `procedure`, `weather`, `software_and_automation`.

---

### Weather Elements & Visibility (`weather_elements_visibility_`)
*Specific weather phenomena or exact visibility measurements (in statute miles).*
* **Weather Conditions**: `blowing_dust`, `cavu` (Clear Above Visibility Unlimited), `cirrostratus`, `clear`, `cloudy`, `crosswind`, `cumulus_clouds`, `fog`, `gusty_winds`, `hail`, `haze`, `icing`, `imc`, `low_ceiling`, `overcast`, `rain`, `snow`, `thunderstorm`, `turbulence`, `windshear`.
* **Visibility Distances**: Numeric flags indicating reported visibility distance (e.g., `_0_5` = 0.5 miles, `_10` = 10 miles, `_9999` = unlimited/unrestricted visibility).