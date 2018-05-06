# Possible data sources / adapters

Ranked by approximate priority/feasibility.

## 1. Twitter

**feasibility**: [manual download](https://twitter.com/settings/account) possible. An experimental Twitter-scraper is also available in this repository.

**data format**: `JSON` (one file per month) directly from website. UTF-8 text from scraper.

**content**: personal tweets/retweets, no responses, like-count, retweet-counts from Website. Raw text available from socket stream for Twitter Scraper.

## 2. Facebook

**feasibility**: manual download possible

**data format**: `HTML` (easily parsable structure)

**content**: more details can be found on [Facebook's "Accessing Your Facebook Data" page](https://www.facebook.com/help/405183566203254)

## 3. LinkedIn

**feasibility**: [manual download](https://www.linkedin.com/psettings/member-data) possible

**data format**: `CSV` multiple files for each content type in .zip

**content**: profile info, skills, connections, education, positions, projects, messages, recommendations

## 4. Google Fit

**feasibility**: [manual download](https://takeout.google.com/settings/takeout) possible

**data format**: individual tracks as `txc` (`xml`) and daily aggregates as `csv`, one file per track/day

**content**: GPS tracks, timestamps

> Start time,End time,Calories (kcal),Distance (m),Low latitude (deg),Low longitude (deg),High latitude (deg),High longitude (deg),Average speed (m/s),Max speed (m/s),Min speed (m/s),Step count,Average weight (kg),Max weight (kg),Min weight (kg),Inactive duration (ms),Walking duration (ms)

## 5. Google Search

**feasibility**: [manual download](https://takeout.google.com/settings/takeout) possible

**data format**: `JSON` every 3 months

**content**: timestamp, search query

## 6. Google Location History

**feasibility**: [manual download](https://takeout.google.com/settings/takeout) possible

**data format**: one giant `JSON`

(One OpenMined Community member claims to have gotten 2,033,770 data points for ~6.5 years of usage.)

**content**: timestamps, GPS positions+accuracy, activity (in vehicle, walking..)

## 7. Runtastic

**feasibility**: Can download directly from account on [website](https://help.runtastic.com/hc/en-us/articles/204773791-Download-Activities)

**data format**: GPX, TCX or KML as default options. CSV files are also possible.

**content**: timestamps, GPS positions+accuracy, activity

## 8. Apple Health

**feasibility**: Extremely difficult without an App. It is likely that this is intentional. Apple has to work through international regulatory and/or data protection limitations governing use of health information. This is happening alongside Medical authorities worldwide who must figure out how to make efficient and interoperable Electronic Health Records. There are multiple standards for health data, and few of them are good.

**data format**: [XML format](https://www.reddit.com/r/AppleWatch/comments/36rjiy/can_you_guys_help_me_visualize_my_exported_health/)

**content**: There is a lot of content. Some includes precise numerical data, while some is far less structured. Some examples include the following:

> Organ Donor Status, Activity (steps taken, Walking/Running/Swimming/Cycling/Wheelchair Distance, flights climbed, active energy, cycling distance, exercise minutes, Resting energy, Stand Hours, Swimming strokes, VO2 max, workouts), Mindfulness records (number of mindful minutes), Nutrition (carbohydrates, dietary energy, dietary sugar, protein, sodium, dietary cholesterol, fiber, potassium, saturated fat, total fat, water, biotin, caffeine intake, calcium, chloride, chromium, copper, folate, iodine, iron, magnesium, manganese, molybdenum, monounsatruated fat, niacin, panthothenic acid, phosphorus, polyunsaturated fat, rioflavin, selenium, thiamin, Vitamin A, Vitamin B12, Vitamin B6, Vitamin C, Vitamin D, Vitamin E, Vitamin K, zinc), Sleep records (timing and analysis of sleep), Body measurements (height, weight, BMI, Body fat %, lean body mass, weight circumference), health records from doctors' offices and hospitals (records from Hospital records APIs like Partners Healthcare, Valley medical Group, NYU Lagone Health, Geisinger Health System, AtlantiCare, Jefferson Health, Penn MedicineMedStar Health, LifeBridge Health, Johns Hopkins Medicine, WVU Medicine, Southwest General, Duke Health, UNC Health CareMission Health, Vanderbilt University Medical Center, Methodist Le Bonheur Healthcare Baycare, and hundreds of others), Heart data (Blood pressure, Elevated Heart Rate Notifications, heart rate, heart rate variability Resting Heart Rate, Walking Heart Rate Average), reproductive health (basal body temperature, sexual activity instances, cervical mucus quality, menstruation, ovulation test results, spotting), test results (blood alcohol content, blood glucose, electrodermal activity, 1 second forced expiratory volume, forced vital capacity, inhaler usage, insulin delivery, number of times fallen, oxygen saturation, peak expiratory flow rate, peripheral perfusion index, UV index).

As you can imagine, there is a great incentive to maintain user privacy when processing all of this, and even then there is a MASSIVE variety of data to process.
