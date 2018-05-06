# Twitter Scraper Adapter (Experimental)
[![Chat on Slack](https://img.shields.io/badge/chat-on%20slack-7A5979.svg)](https://openmined.slack.com/messages/team_adapters)

> Scrapes Twitter

## Usage

To run this scraper, run `python3 TwitterScraper.py` in the terminal in whatever directory this has been downloaded to.

## Installation

(NOTE: This is still a highly unstable build, so future versions will likely include a stable binary for whichever OS the user is running)

First, make sure Java is installed

## Current Proposals

THe current proposals for Data types can be found in this Google Doc ([view access](https://docs.google.com/document/d/1TIiIm0aYILd02tfLM57IaLEOs94f1OYa12d5hIw7B_4/edit?usp=sharing)). This unified schema proposal addresses the issue declare that they're loading in data with a consistent schema as some other dataset that's also on Grid

(Additional ideas for Data Sources and Adapters can be found in the [ideas](https://github.com/OpenMined/Adapters/blob/master/ideas.md) document).

## TODO

The output of the Twitter Binary needs to be reformatted to OpenMined's general adapter schema (more details on this discussion [in this proposal](https://docs.google.com/document/d/1TIiIm0aYILd02tfLM57IaLEOs94f1OYa12d5hIw7B_4/edit?usp=sharing))

In it's current form, the general schema takes the following form:

* Profile
	* Names
		* Primary
			* Prefix
			* First
			* Middle
			* Last
			* Suffix
		* Aliases (same format as above)
		* Maiden name (same format as above)
	* Gender (allow for non-binary options)
	* Sex (male, female, or intersex)
	* Sexuality (free-form entry)
	* Birthdate
		* Day
		* Month
		* Year
	* Languages
		* Name
		* Proficiency
* Contact Info
	* Email(s)
	* Phone(s)
	* Online handles (social media and other online accounts)
	* Website
* Relationships
	* Name
	* Relation (i.e. mother, brother, ex-girlfriend, follower, spouse, etc.)
	* Contact information (i.e. email, phone, website, social media, etc.)
* Education
	* Institution
	* Date range
	* Area of study
	* Level of degree
* Employment
	* Organization
	* Date range
	* Location
	* Job title
* Posts
	* Content
	* Timestamp
	* Origin (i.e. Facebook, Twitter, etc.)
	* Metadata (other social information such as images, video, location, etc. that is platform specific)
* Messages
	* Thread
		* Content
		* Timestamp
		* Person(s) involved
* Location
	* Static (general location information)
		* Current city
		* Hometown
		* Birthplace
		* Cities lived in
		* Cities visited
	* Dynamic (populated by geolocation, meant to be on-going, not likely to be manual entry)
* Search History (likely populated solely by an Adapter)
* Health
	* Weight
	* BMI
	* Blood Pressure
	* Etc...
* Photos
* Videos
* Audio


In JSON format, for example, this may take on the following form:

```json

{
	"profile": {
		"names": [
		{
			"primary": {
				"prefix": "",
				"first": "",
				"middle": "",
				"last": "",
				"suffix": ""
			},
			"aliases": {
				"prefix": "",
				"first": "",
				"middle": "",
				"last": "",
				"suffix": ""
			},
			"maiden_name": {
				"prefix": "",
				"first": "",
				"middle": "",
				"last": "",
				"suffix": ""
			}
		}],
		"gender": "",
		"sex": "",
		"sexuality": "",
		"birthdate": {
			"day": "",
			"month": "",
			"year": ""
		},
		"languages: [
		{
			"name": "",
			"proficiency": ""
		}]
	},
	"Contact Info: {
		"Email_s": "",
		"Phone_s": "",
		"Online_handle_s": "",
		"Website": ""
	},
	"Relationships": [
	{
		"name": "",
		"relation": "",
		"contact information": {
			"email": "",
			"phone": "",
			"website": "",
			"social_media": ""
		}
	}],
	"education": {
		"institution": "",
		"date_range": "",
		"area_of_study": "",
		"level_of_degree": ""
	},
	"employment": {
		"organization": "",
		"date_range": "",
		"location": "",
		"job_title": ""
	},
	"posts": [
	{
		"content": "",
		"timestamp": "",
		"origin": "twitter",
		"metadata": {
			"images": "",
			"video": "",
			"location": ""
		}
	}],
	"messages": [
	{
		"thread": {
			"content": "",
			"timestamp": "",
			"person_s_involved": ""
		}
	}],
	"location": {
		"static": {
			"current_city": "",
			"hometown": "",
			"birthplace": "",
			"cities_lived_in": [
			{
				""
			}],
			"cities_visited": [
			{
				""
			}]
		},
		"dynamic": {
			"geolocation": {
				latitude: "".
				longitude: ""
		}
	},
	"search_history": []
	"health": {
		"weight":"",
		"bmi":"",
		"blood_pressure":"",
	},
	"photos": [],
	"videos": [],
	"audio": []
}
```


For ease of execution on Windows, Mac, and Linux, the current python code will also need to be converted to an executable binary ([PyInstaller](http://www.pyinstaller.org/) will likely be used for this.

## Contributions

Contributions and Pull Requests are welcome. See the Issues section for ideas for first commits.

## License

[MIT](LICENSE)
