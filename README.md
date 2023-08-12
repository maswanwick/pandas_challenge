# pandas_challenge

### This repo contains the necessary artifacts to satisfy the requirements of this challenge.
| File | Description | 
| - | - |
| `PyCitySchools/Resources/schools_complete.csv` | Dataset representing the school data for the challenge. |
| `PyCitySchools/Resources/students_complete.csv` | Dataset representing the student data for the challenge. |
| `PyCitySchools.ipynb` | Jupyter Notebook file that contains the code to complete the challenge as well as the written analysis. |

# Analysis

This analysis report is also found in the Jypyter Notebook, but is included here as well for convenience.

After reviewing the data, there are a couple of areas I would recommend further analysis to improve test scores across the school district:
* Increase focus in the math curriculum.
* Apply practices used at our charter schools to our district schools.

### Increase focus in the math curriculum

Across the district, the average math score is lower than the average reading score (78.99 vs. 81.88).  This is also true at every high school:

| School | Average Math Score | Average Reading Score |
|-|-|-|
| Bailey High School	| 77.048432	| 81.033963| 
| Cabrera High School	| 83.061895	| 83.975780| 
| Figueroa High School	| 76.711767	| 81.158020| 
| Ford High School	| 77.102592	| 80.746258| 
| Griffin High School	| 83.351499	| 83.816757| 
| Hernandez High School	| 77.289752	| 80.934412| 
| Holden High School	| 83.803279	| 83.814988| 
| Huang High School	| 76.629414	| 81.182722| 
| Johnson High School	| 77.072464	| 80.966394| 
| Pena High School	| 83.839917	| 84.044699| 
| Rodriguez High School	| 76.842711	| 80.744686| 
| Shelton High School	| 83.359455	| 83.725724| 
| Thomas High School	| 83.418349	| 83.848930| 
| Wilson High School	| 83.274201	| 83.989488| 
| Wright High School	| 83.682222	| 83.955000| 

(source: per_school_summary DataFrame)

By directing more focus on math competencies, those scores will go up, which will boost the overall passing rate district wide.

### Apply practices used at our charter schools to our district schools

None of the District type schools had an overall passing rate above 60%, whereas the Charter schools all had a passing rate around 90%.  This is a staggering difference across these school types:

| School | Type | Total Students | % Overall Passing | School Size|
| - | - | - | - | - |
|Bailey High School	|District	|4976	|54.642283	|Large |(2000-5000)|
|Figueroa High School	|District	|2949	|53.204476	|Large |(2000-5000)|
|Ford High School	|District	|2739	|54.289887	|Large |(2000-5000)|
|Hernandez High School	|District	|4635	|53.527508	|Large |(2000-5000)|
|Huang High School	|District	|2917	|53.513884	|Large |(2000-5000)|
|Johnson High School	|District	|4761	|53.539172	|Large |(2000-5000)|
|Rodriguez High School	|District	|3999	|52.988247	|Large |(2000-5000)|
|Cabrera High School	|Charter	|1858	|91.334769	|Medium| (1000-2000)|
|Griffin High School	|Charter	|1468	|90.599455	|Medium |(1000-2000)|
|Holden High School	|Charter	|427	|89.227166	|Small |(<1000)|
|Pena High School	|Charter	|962	|90.540541	|Small |(<1000)|
|Shelton High School	|Charter	|1761	|89.892107	|Medium |(1000-2000)|
|Thomas High School	|Charter	|1635	|90.948012	|Medium |(1000-2000)|
|Wilson High School	|Charter	|2283	|90.582567	|Large |(2000-5000)|
|Wright High School	|Charter	|1800	|90.333333	|Medium |(1000-2000)| 

(source: per_school_summary DataFrame, sorted by School Type)

One might be tempted to correlate school size to the overall passing rate, but there is one charter school (Wilson High School) that is in the "Large" category that is excelling with 90.58% passing rate.  Therefore, we need to look at the curriculum being used in the charter schools and see if we can apply any of those concepts to the district schools.