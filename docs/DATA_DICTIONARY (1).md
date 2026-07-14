# Data Dictionary

The cleaned dataset contains 53 columns. Times are local airport times. Scheduled and actual times use the `HHMM` format.

| Column | Type | Description |
|---|---|---|
| `year` | Integer | Flight year. |
| `quarter` | Integer | Calendar quarter from 1 to 4. |
| `month` | Integer | Month from 1 to 12. |
| `dayof_month` | Integer | Day of the month. |
| `day_of_week` | Integer | Day of week: 1 = Monday and 7 = Sunday. |
| `flight_date` | Date | Flight date. |
| `reporting_airline` | Text | Reporting airline code. |
| `tail_number` | Text | Aircraft tail number. |
| `flight_number_reporting_airline` | Integer | Flight number used by the reporting airline. |
| `origin_airport_i_d` | Integer | BTS identifier of the origin airport. |
| `origin` | Text | Three-letter origin airport code. |
| `origin_city_name` | Text | Origin city name. |
| `origin_state_name` | Text | Origin state name. |
| `dest_airport_i_d` | Integer | BTS identifier of the destination airport. |
| `dest` | Text | Three-letter destination airport code. |
| `dest_city_name` | Text | Destination city name. |
| `dest_state_name` | Text | Destination state name. |
| `c_r_s_dep_time` | Integer | Scheduled departure time in `HHMM` format. |
| `dep_time` | Integer | Actual departure time in `HHMM` format. |
| `dep_delay` | Decimal | Departure delay in minutes. Negative values mean an early departure. |
| `dep_delay_minutes` | Decimal | Non-negative departure delay in minutes. |
| `dep_del15` | Integer | 1 if departure delay was at least 15 minutes, otherwise 0. |
| `dep_time_blk` | Text | Scheduled departure time block. |
| `taxi_out` | Decimal | Minutes between gate departure and take-off. |
| `wheels_off` | Integer | Take-off time in `HHMM` format. |
| `wheels_on` | Integer | Landing time in `HHMM` format. |
| `taxi_in` | Decimal | Minutes between landing and gate arrival. |
| `c_r_s_arr_time` | Integer | Scheduled arrival time in `HHMM` format. |
| `arr_time` | Integer | Actual arrival time in `HHMM` format. |
| `arr_delay` | Decimal | Arrival delay in minutes. Negative values mean an early arrival. |
| `arr_delay_minutes` | Decimal | Non-negative arrival delay in minutes. |
| `arr_del15` | Integer | 1 if arrival delay was at least 15 minutes, otherwise 0. |
| `arr_time_blk` | Text | Scheduled arrival time block. |
| `cancelled` | Integer | 1 if the flight was cancelled, otherwise 0. |
| `cancellation_code` | Text | Cancellation code: A = carrier, B = weather, C = National Air System, D = security. |
| `diverted` | Integer | 1 if the flight was diverted, otherwise 0. |
| `c_r_s_elapsed_time` | Decimal | Scheduled gate-to-gate time in minutes. |
| `actual_elapsed_time` | Decimal | Actual gate-to-gate time in minutes. |
| `air_time` | Decimal | Time spent in the air in minutes. |
| `distance` | Decimal | Flight distance in miles. |
| `carrier_delay` | Decimal | Delay minutes attributed to the airline or carrier. |
| `weather_delay` | Decimal | Delay minutes attributed to significant weather conditions. |
| `n_a_s_delay` | Decimal | Delay minutes attributed to the National Air System. |
| `security_delay` | Decimal | Delay minutes attributed to security. |
| `late_aircraft_delay` | Decimal | Delay minutes caused by the aircraft arriving late from a previous flight. |
| `airline_name` | Text | Full airline name added during cleaning. |
| `cancellation_reason` | Text | Full cancellation reason added from the cancellation code. |
| `route` | Text | Origin and destination combination, for example `JFK - LAX`. |
| `departure_hour` | Integer | Hour extracted from the scheduled departure time. |
| `time_of_day` | Text | Scheduled period: Morning, Afternoon, Evening or Night. |
| `flight_status` | Text | Final status: On Time, Delayed, Cancelled or Diverted. |
| `on_time` | Integer | 1 for a completed flight arriving less than 15 minutes late, otherwise 0. |
| `delayed` | Integer | 1 for a completed flight arriving at least 15 minutes late, otherwise 0. |

## Notes

- Missing delay-cause values were replaced with zero.
- Cancelled and diverted flights are not counted as on-time flights.
- The last eight columns were created during data cleaning.
