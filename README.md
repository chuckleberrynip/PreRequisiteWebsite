## Objective:
### To have an interactive website where people would be able to know what courses they can take.
## How does this work? 
#### Generally speaking, this website implements a topological sort in order to make sure that prerequisites are being met. So what the sort does is that it takes multiple arrays that represents lines that connects two nodes, or courses in this case, and depending which is the preceding and succeeding within the inner array will determine which is the prerequisite. This way, once the sort is done, the output contains a list of courses in an order that you should take them because that order will not have any conflicts regarding prerequisites. In this specific implementation, the array is represented as [PreRequisite, NextCourse], and this can be seen in the JSON file that contains all of the sorted major/minor courses. So as an example, if we know that CISC 1115 is a prerequisite to CISC 3115 then within the JSON file in the relevant spot it would contain ["CISC 1115", "CISC 3115"] to indicate a relationship. The user has a table where they can input their courses and that removes those courses from the list, which leaves the courses that they have left to take and in the order that they should take them.

## How to add a new major or minor to the website? 
#### Although the process might seem very difficult, it is not. It can be approached by almost anybody and the only time-consumning aspect is organizing the information. The provided tutorial is going to be adding the Biology Major for Brooklyn College. And this information is being sourced from the Brooklyn College Biology department and contains only the department requirements.
Link to Info: http://www.brooklyn.cuny.edu/web/academics/schools/naturalsciences/undergraduate/biology/majors_details.php?major=017&div=U&dept_code=09&dept_id=75&mode=data

#### What information should be gathered? 
The table within the website requires five things, however four things are required:
- Course Name
- Full Course Name 
- Number of Credits
- Minimun Grade so that they can move on.(Note: not the grade a student should strive for, rather the grade that the department deems as minimum for the course to count.
#### Working with the JSON file: 
Once the course information gathering is complete it is important to categorize the information. So to do this, make a list of the courses that you are going to input and then graph them out. I recommend drawing out the graph, so that when inputting the courses into the JSON file, it will heavily expediate the process. Here is my example how I drew out the Biology Major:

![Alt text](guideAsset/BioMap.png?raw=true "BioMap")

The first that I would do is to get done with the tedious stuff first, so I would configure the JSON file that is provided in the repository to accomodate the courses in the HTML file. Although it may seem initimidating, you should not worry, it is simple. It should follow the syntax exactly as shown: 

![Alt text](guideAsset/correctedBioJSON.png?raw=true "JSON")

Notice how each array is just representing the line that connects the courses in the diagram. There are other majors/minors that are within the JSON file, so please check those out if you want more examples as to how to make the array and please be consistent with the naming conventions where the courses are uppercase, and camel casing is being used for the name of the major/minor, and for majors its just the name of the department , i.e psychology, and for minors it should be the name of the department and then minor added to the end, i.e psychologyMinor. Once that is done please upload it to github so that the HTML file can access it. Now, that the hard part is done, the rest is just using the course template that is provided and adding the courses. Working with the HTML in this specific case is kind of like working with an excel file in that it is simple data input. So please go to the Majors folder, or Minors, folder and open the courseTemplate.html.

#### Working with the HTML file:
Go to the respective folder that you want, meaning either Major or Minor, and open the course template HTML file. This file is a blank file that is meant to ease the process of adding new majors. The first thing that I would recommend is to comment in the Major/Minor in the top for memory's sake. Once you do that, there is an area that contains a comment for you to input the name of the department and what type of courses you are going to input. After doing  that, scroll down to the "TABLE AREA", where you will find something like this: 


![Alt text](guideAsset/tableArea.png?raw=true "tableArea")

Please input the information their respctive places and then it should look something like this: 

![Alt text](guideAsset/inputTable.png?raw=true "inputArea")

#### Please make sure that the values in "name" and "id" correspond to the name that you inputted into "Courses" and is found exactly in the same manner in the JSON file.

Once that is done, please scroll down to where the comment

"//lines = courses.majorName "

is as this the part of the file that interacts with the JSON file. All you have to do is input the desired major name as it is found in the JSON file, meaning the case of the letters count. The line of code in the template is left blank and it looks like : 

  lines = courses. 

Your job is to input the major name after the dot and end with a semi-colon, this is how it looks: 

![Alt text](guideAsset/toposortlink.png?raw=true "Jquery")

After that, we finish by adding the link to the main homepage. This means adding a link that points to the location of the major file. Be wary, there is a section for majors and another section for minorsn here they are respectively:

![Alt text](guideAsset/menuindexbefore.png?raw=true "Majors")

![Alt text](guideAsset/MinorSection.png?raw=true "Minors")

Adding the link means following a certain syntax, and this is using a relative path to point to the file that we want to add. If you have any trouble, just copy the any one of the previous majors and replace the other major with the major that you want.

Example:

![Alt text](guideAsset/menuindexafter.png?raw=true "AddedBio")

Finally, we are done and all we do is upload to the github. The first time of doing this might take the longest, but it is much quicker the second time around. Excluding the time that it took me to write this document, it took me abotu 30-40 minutes to add a new major.

Here is the GitHub pages [links](https://chuckleberrynip.github.io/PreRequisiteWebsite/) to view your achievement.
I hope that this was as beneficial for you as it was me.



