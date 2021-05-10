# PreRequisiteWebsite
## Objective:
### To have an interactive website where people would be able to know what courses they can take.
## How does this work? 
#### Generally speaking, this website implements a topological sort in order to make sure that prerequisites are being met. So what the sort does is that it takes multiple arrays that represents lines that connects two nodes, or courses in this case, and depending which is the preceding and succeeding within the inner array will determine which is the prerequisite. This way, once the sort is done, the output is a list that contains a list of courses in the order that you should take them because that order will not have any issues regarding prerequisites. In this specific implementation, the array is represented as [PreRequisite, NextCourse], and this can be seen in the JSON file that contains all of the sorted major courses. So if we know that CISC 1115 is a prerequisite to CISC 3115 then within the JSON file in the relevant spot it would contain ["CISC 1115", "CISC 3115"] to indicate a relationship. The user has a table where they can input their courses and that removes those courses from the list, which leaves the courses that they have left to take and in the order that they should take them.
## How to add a new major or minor to the website? 
#### Although the process might seem very difficult, it is not. It can be approached by almost anybody and the only time-consumning aspect is organizing the information. The provided tutorial is going to be adding the Biology Major for Brooklyn College. And this information is being sourced from the Brooklyn College Biology department and contains only the department requirements.
Link to Info: http://www.brooklyn.cuny.edu/web/academics/schools/naturalsciences/undergraduate/biology/majors_details.php?major=017&div=U&dept_code=09&dept_id=75&mode=data

#### What information should be gathered? 
The table within the website requires five things, however four things are required by the person adding the major :  
- Course ID, meaning the course department and the associated ID number.
- Full Course Name. 
- Number of Credits
- Minimun Grade so that they can move on.(Note: not the grade a student should strive for, rather the grade that the department deems as minimum for the course to count.

Once that is complete it is important to categorize the information. So to do this make a list of the courses that you are going to input and then graph them out. I recommend drawing out the graph, so that when inputting the courses into the JSON file, it will heavily expediate the process. Here is my example how I drew out the Biology Major.

![Alt text](guideAsset/BioMap.png?raw=true "Title")

The first that I would do is to get done with the tedious stuff first, so I would configure the JSON file that is provided in the repository to accomodate the courses in the HTML file. Although it may seem initimidating, you should not worry, it is simple. It should follow the syntax exactly as shown: 
