# Student Data Dictionary (Exam Version)

## Target Variable

| Column | Description |
|------|------------|
| no_show_next_visit | Indicator of whether the patient missed their next scheduled appointment (1 = No-show, 0 = Attended) |

---

## Patient Information

| Column | Description |
|------|------------|
| patient_id | Unique identifier for each patient |
| age | Patient age in years |
| postal_region | Geographic region of the patient based on postal code |
| insurance_type | Type of insurance coverage |
| chronic_condition_count | Number of known chronic conditions |
| patient_tenure_band | Grouped category of how long the patient has been in the system |
| attendance_stability_index | Score representing consistency of past attendance |
| engagement_band | Categorized level of patient engagement |

---

## Appointment & Scheduling

| Column | Description |
|------|------------|
| appointment_id | Unique identifier for the appointment |
| scheduled_date | Date when the appointment was booked |
| appointment_date | Date of the scheduled appointment |
| lead_time_days | Days between scheduling and appointment |
| weekday | Day of the week for the appointment |
| month | Month of the appointment |
| week_of_year | Week number in the year |
| season_code | Seasonal grouping (e.g., winter, summer) |
| time_slot | Time window of the appointment (e.g., morning, afternoon) |
| appointment_type | Type of appointment (e.g., consultation, follow-up) |
| is_first_visit_with_provider | Whether this is the first visit with the assigned provider |

---

## Clinic & Provider Context

| Column | Description |
|------|------------|
| clinic_id | Identifier of the clinic |
| provider_id | Identifier of the healthcare provider |
| clinic_utilization_bin | Categorized clinic capacity utilization level |
| provider_load_group | Grouped measure of provider workload |
| schedule_pressure_score | Composite score indicating scheduling intensity |
| utilization_pattern_score | Pattern-based score of clinic usage |
| care_continuity_score | Score representing continuity of care |

---

## Patient Interaction & Engagement

| Column | Description |
|------|------------|
| sms_sent_count_30d | Number of SMS reminders sent in last 30 days |
| call_attempts_7d | Number of phone call attempts in last 7 days |
| email_open_rate_est | Estimated email engagement rate |
| portal_login_count_30d | Number of patient portal logins in last 30 days |
| last_contact_gap_days | Days since last contact with patient |
| reminder_channel_code | Primary reminder channel used |
| contact_efficiency_score | Score indicating effectiveness of communication |

---

## Historical Behavior

| Column | Description |
|------|------------|
| prior_total_appointments | Total number of past appointments |
| prior_no_show_count | Number of past missed appointments |
| historical_no_show_rate | Ratio of missed appointments historically |
| reschedule_count_90d | Number of rescheduled appointments in last 90 days |
| prior_cancellation_count | Number of prior cancellations |
| return_propensity_index | Likelihood of returning for care |

---

## Accessibility & Logistics

| Column | Description |
|------|------------|
| distance_to_clinic_km | Distance from patient to clinic |
| transport_support_flag | Whether transportation assistance is available |
| estimated_wait_days | Estimated wait time before appointment |

---

## External / Environmental Factors

| Column | Description |
|------|------------|
| rain_mm | Rainfall level on appointment day |
| temperature_band | Temperature category |
| public_holiday_nearby | Whether a holiday is near appointment date |
| local_event_flag | Indicator of nearby events that may affect attendance |
| traffic_risk_band | Estimated traffic conditions |

---

##  Notes on Data Usage

- Some variables are derived or aggregated from historical records.
- Not all variables may be available at prediction time.
- Some features may reflect operational processes rather than patient behavior.
- You are expected to evaluate feature reliability and potential risks.

