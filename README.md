
# Complaints Against the Chicago Police Department

[**Dataset**](http://how.cpdp.works/en/articles/1889786-where-does-the-data-come-from-who-is-doing-this-and-why)

The Citizens Police Data Project has collected more than 56,000 allegations of police misconduct.

The data, covering 2002-2008 and 2011-2015, includes demographic information about the complainant and the officer, as well as the type and location of the incident.

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/17x94gvbIL6oyJDeYV49Q_678nRrCdPH7/view?usp=sharing)

## Overview

Police violence has been a hot topic in the US for decades. We have seen data on the disproportionate level of violence aimed at black people, as well as the effects of overpolicing on communities of color. But what effect does objecting to this violence achieve? Here we have data on allegations aimed at the police, which include everything from violent abuse of authority, to intoxication, to traffic violations. These complaints and the ensuing investigations are important in understanding the cycle of police brutality in the US.

What we want to know about this data is, What is the percentage of allegations that result in findings or discipline? How many allegations are sustained? And which members of the police are more likely get an allegation on their record?

__Is there any significant difference between the population of the police on who will sustain an allegation?__

Towards the end of this workbook, I show what statistics I use, and in what sequence, to test my hypotheses.

By looking closely at this data and drawing statistically sound conclusions, we can speak with more authority on the issue of police brutality in Chicago.

----

## Key Features

Most of the features are converted with PCA for confidentiality. The exceptions are **time** (seconds elapsed between transactions), **amount** (€), and **fraud** (0 or 1). 

![image](https://storage.googleapis.com/earth_data_247/races.png)
![image](https://storage.googleapis.com/earth_data_247/male-female.png)
![image](https://storage.googleapis.com/earth_data_247/breakdown-sustained-uns.png)
![image](https://storage.googleapis.com/earth_data_247/age-unsustained.png)
### Sustained Allegations:

|allegation name|	category|	count|
|---------------|---------------|------------|
|Neglect Of Duty	|Operation/Personnel Violations|	361|
|Miscellaneous	|Operation/Personnel Violations	|216|
|Unknown	|Unknown	|112|
|Inadequate / Failure To Provide Service	|Operation/Personnel Violations|	111|
|Association With Felon	|Conduct Unbecoming (Off-duty)|	99|

### Unsustained Allegations:

|allegation name|	category|	count|
|---------------|---------------|------------|
|Inadequate / Failure To Provide Service	|Operation/Personnel Violations|	3647|
|Search Of Premise Without Warrant	|First Amendment and Illegal Arrest|	2888|
|Unknown	|Unknown|	2879|
|Excessive Force / On Duty - Injury	|Arrest/Lock-up Procedures|	2330|
|Illegal Arrest / False Arrest	|First Amendment and Illegal Arrest|	2258|

- Notes
	* The length between the time of the incident and the end of the investigation has a mean of 241 days.
	* Out of the 20 officers with the highest count of allegations, only 4 are black and one is Asian. The rest are white.
	* The total rate for sustaining an allegation is 8%. This means that 92% of allegations are unsustained and do not result in discipline.
	* Searching without a warrant is often not sustained, even though it is the top complaint.
	* Men in the CPD have a 5.9% chance of sustaining an allegation.
	* Women in the CPD have a 7.9% change of sustaining an allegation.
	* Black members of the police have a 10.3% chance of an allegation being sustained.
	* White members of the police have a 4.8% chance of an allegation being sustained.
	* Hispanic members of the police have a 5.3% chance of an allegation being sustained.

----

## Integrations

* [Pandas](https://pandas.pydata.org/pandas-docs/stable/)
* [Seaborn](https://seaborn.pydata.org/)
* [Matplotlib](https://matplotlib.org/stable/index.html)
* [Plotly GO](https://plotly.github.io/plotly.py-docs/plotly.graph_objects.html#graph-objects)

----

## Conclusions

![image](https://storage.googleapis.com/earth_data_247/hispanic-black.png)

![image](https://storage.googleapis.com/earth_data_247/white-black.png)

![image](https://storage.googleapis.com/earth_data_247/white-hispanic.png)



# Two-group test

We see what null hypothesis can be rejected using a significance level of 0.05.

The t-test shows that the biggest difference is between white and black police members, with a p-value well under 0.05. The p-value is the probability that, given that the null hypothesis  𝐻0  is true, we could have ended up with a statistic at least as extreme as the one we got.

![img](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fwww.biologyforlife.com%2Fuploads%2F2%2F2%2F3%2F9%2F22392738%2F949234_orig.jpg&f=1&nofb=1)

----

## Questions/Comments

Any contributions are more than welcome!

Feel free to leave me a message on Git or email me at mcclure.dean@gmail.com
