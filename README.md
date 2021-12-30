# Medical Appointment Noshow Dataset Investigation

## Overview
Patient no-show continues to contribute to the rising healthcare cost, leading to negative impacts on the day-to-day operations of the healthcare system, restricting healthcare delivery efficacy, besides limiting quality healthcare access for all patients.

This report analyses a [dataset](https://www.kaggle.com/joniarroba/noshowappointments) of more than 110k Brazilian patients from late April to early June 2016. Data shows that in 20% of scheduled appointments, the patient didn't show up. Our goal is trying to answer the questions:
- what are the factors leading to no_shows?
- Is it the system or personal attributes to blame?

The report distinguishes between two groups of factors that might have significance: those related to the system, and personal attributes of the patients themselves.

## Dataset
The oringinal dataset can be found [here](https://www.kaggle.com/joniarroba/noshowappointments). The dataset contains 110.527 medical appointments with 14 associated variables (characteristics):
1. **PatientId:** Identification of a patient
2. **AppointmentID:** Identification of each appointment
3. **Gender:** Male or Female . Female is the greater proportion, woman takes way more care of they health in comparison to man.
4. **ScheduledDay:** The day of the actuall appointment, when they have to visit the doctor.
5. **AppointmentDay:** The day someone called or registered the appointment, this is before appointment of course.
6. **Age:** How old is the patient.
7. **Neighbourhood:** Where the appointment takes place.
8. **Scholarship:** True of False . Observation, this is a broad topic, consider reading this [article](https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia)
9. **Hipertension:** True or False
10. **Diabetes:** True or False
11. **Alcoholism:** True or False
12. **Handcap:** True or False
13. **SMS_received:** 1 or more messages sent to the patient.
14. **No-show:** True or False.

## Conclusions
### Results
This report examined a dataset of Brazilian patients, trying to figure out what are the factors that correlates with missing appointments.

It found that the most important factor was whether the patient got his appointment at the same day of booking. This factor was negatively correlated with no_show cases, meaning that there were less no_shows when the patient was scheduled on the same day.

Regarding the system, the report found that sending SMS notifications didn't help. In fact, it was weakly positively correlated with no_show cases. Implying that those who received an SMS were slightly more likely to miss. Receiving benefits from Bolsa Família didn't seem to correlate with no_show cases.

Personal attributes didn't seem to correlate with no_shows. Except that patients who missed their appointments were younger in general of those who didn't. It is also noted that having multiple illnesses seems to correlate with less no_shows.

### Limitations
Most columns in the dataset are binary variables (categorical variables that take only two values), including the dependent variable noshow. This limits the statistical methods that can be used to analyze the data.

Some results were counter-intuitive, The analysis found that there is a slight higher chance of no_show for those who received an SMS. The nature of the data prevents further investigation.

It's important to note that this analysis focus is on the correlation between the variables. This is not enough to assume there is a causal relation between them. Further studies using inferential statistics is required for that. Also, most correlations were weak due to the categorical nature of the variables.
