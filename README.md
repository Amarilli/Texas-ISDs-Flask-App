# Texas Education and Funding: a Visualization 

### Team Members: 
- James Draper
- Kelsey Kraft
- Mariah McLelan
- Amarilli Novel
- Hisako Yamanaka

  
### Project Overview:

Question to answer: How does the funding allocated to education impact the success of students and schools?

This is the second part of our team project focused on [Texas ISDs](https://github.com/mariahmclelan/TexasISDs) where we study the impact of education funding on student success and school performance. 
Our aim is to determine the relationship between Texas state funding for education, SAT scores, and demographics. 
We will use a custom MongoDB database and visual analysis to investigate whether higher funding leads to better outcomes or if there is a point where the impact of funding levels off. 
Additionally, we will analyze demographics and their possible impact.

### Data Sets Source:

[Texas Education Agency](https://tea.texas.gov/)

[Texas Education Agency Public Open Data Site: Current Districts ](https://schoolsdata2-tea-texas.opendata.arcgis.com/)

[Texas Education Agency Public Open Data Site: Currents Schools ](https://schoolsdata2-tea-texas.opendata.arcgis.com/)

[Texas schools geocoding project](https://github.com/utdata/texas-schools)

[The Texas Tribune](https://schools.texastribune.org/states/tx/)

We also used the cleaned dataset we created during the first part of our project: [Score&Finance](https://github.com/mariahmclelan/Project3/blob/main/resources/scores_finances.json) 

### Break Down of Task:

    Mariah: Cleaning, merging, and transform datasets, Flask App Home Page, Maps and visualizations.
    James: Web Scraping.
    Kelsey: MongoDB and Flask App.
    Amarilli: GeoJSON datasets, Flask App Home Page, Maps, Visualizations, README. 
    Hisako: Presentation.

### Ethical data considerations

Part of this project is about web scraping. Before downloading or scraping the data, we reviewed the regulations and documents about the data usage. All the data we used for this project is ethically sourced.

### Development

As part of our project, we aimed to create maps about Education and Funding in Texas. To begin with, we researched to find GeoJSON datasets that could be included along with [our previous dataset](https://github.com/mariahmclelan/Project3/blob/main/resources/scores_finances.json). 

Our first task was to transform the CSV files into JSON format, which we then stored in our MongoDB dataset, named [texasSchoolsDB](https://github.com/mariahmclelan/Project3/blob/main/DB.ipynb). 
We created a separate collection for each dataset, imported it, and stored it in our database. 

Finally, we developed a Flask App with eight routes, which included access to the datasets and two interactive maps. 

![home](https://github.com/mariahmclelan/Project3/blob/main/Images/home.png)

Both cartographic representations exhibit the Texas school districts for the academic year 2022/2023.

The first map comprises a layer control that enables the district boundaries to be activated and deactivated. Furthermore, it comprises financial data obtained from our previous project, in particular:

- The student count for each district,
- The Total operation revenue for each district

The school's ranking distinguishes the markers on the map, while their size reflects the student population.  

The second map is a heat map that illustrates the SAT scores of each district in Texas, and the markers exhibit the demographics of each district. 

Regarding the demographics, we also created radar charts displaying the population of each district.

![radar](https://github.com/mariahmclelan/Project3/blob/main/Images/radar_chart.png)



### Takeaways and conclusions:

- The maps visually confirm the positive correlation between total operating revenue and student count.
  That means the more students a school district has, the bigger the funding received.
  
- The budget doesn't significantly affect SAT scores, as some schools with smaller budgets scored the highest.
  Moreover, smaller schools tend to have higher SAT scores.
  
- There is a substantial decline in academic scores when the school population increases.

- Smaller schools, on average, do better than larger schools.

In conclusion, education funding does not impact students' success. 


After analyzing the data, a pertinent question arises: What is the key to success for smaller schools with higher scores?

As per the American Federation of Teachers Texas, teachers must maintain an average of 20 students per class across the district, although no prescribed limit exists for individual secondary classrooms. The 22:1 ratio only applies to students in Kindergarten through fourth grade.

Further investigation may lead us to hypothesize that the optimal student-to-teacher ratio in smaller schools may be a factor that contributes to their superior academic performance when compared to larger schools with a lower percentage of teachers per student. 

Our web scraping project is ongoing, with thousands of data rows left to analyze and clean. This query may form the basis of our next project

