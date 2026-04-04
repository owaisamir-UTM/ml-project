# Student Data Dictionary

This dataset represents appointment-level records for a healthcare operations setting.
The target is `no_show_next_visit` (1 = patient missed the scheduled follow-up appointment, 0 = attended).

Some fields are direct operational variables, while others are derived or composite indicators.
As in many real-world datasets, not every field has identical reliability.

## Column notes
- `patient_id`: patient identifier. Multiple rows may belong to the same patient.
- `scheduled_date`, `appointment_date`: booking and appointment dates.
- `lead_time_days`: days between scheduling and appointment.
- `historical_no_show_rate`: patient's past proportion of missed visits.
- `sms_sent_count_30d`, `call_attempts_7d`, `email_open_rate_est`, `portal_login_count_30d`: communication and engagement related metrics.
- `attendance_stability_index`, `schedule_pressure_score`, `utilization_pattern_score`, `contact_efficiency_score`, `visit_gap_estimate`, `return_propensity_index`, `care_continuity_score`: operational/derived indicators.
- Missing values may reflect ordinary system limitations or real operational differences.

You are expected to decide how to validate, preprocess, model, and justify your decisions.
