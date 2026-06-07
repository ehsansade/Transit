This repository contains self-created task materials for evaluating real-time bus departure prediction accuracy from a passenger perspective.

The files were prepared for a benchmark-style data analysis task. The goal of the task is to compare predicted bus departure times from website screenshots against observed actual departures, then calculate route-level accuracy using two methods: a direct prediction-labeling method and an expected wait-time method.

Files
departure_data.xlsx

Main analysis dataset containing bus departure prediction records and observed actual departure information for one bus stop on a single service day.

The prediction records represent the next three estimated departures shown on the public-facing website at each screenshot timestamp. The predictions are expressed as the number of minutes away from the screenshot timestamp.

This file is used to identify screenshot-based predictions, match them to observed departures, calculate prediction labels, and calculate expected passenger wait time.

bus_assignments.xls

Supporting lookup file containing bus assignment information by route.

This file is used to confirm or fill the correct bus number for each evaluated route/departure record when the bus number is missing or inconsistent in the main dataset.

accuracy_define1.png

Self-created rule image defining how prediction accuracy should be labeled.

The image shows the acceptable prediction-error range by time-to-departure bucket. A prediction should be labeled accurate if it falls within the corresponding acceptable range for its bucket, and inaccurate otherwise.

headway.png

Self-created histogram image showing the headway distribution for the same stop.

This image is used to estimate the average headway needed for the expected wait-time accuracy calculation.
