# GSoC'21 @CASTOR FINAL REPORT

## General Information
<b>Organization:</b> [CASTOR](https://github.com/castor-software) <br>
<b>Project:</b> [DEPCLEAN](https://github.com/castor-software/depclean) <br>
<b>Tasks:</b> 
1. Implementation of a depclean-gradle-plugin like depclean-maven-plugin.
2. Implement a feature in depclean-maven-plugin to analyze multi-module projects.
3. Implementation of some new tests.

<b>Student:</b> [Abhay Singh](https://github.com/ABHAY0O7) <br>
<b>Mentors:</b> [Thomas Durieux](https://github.com/tdurieux), [César Soto Valero](https://github.com/cesarsotovalero) 
& [Benoit Baudry](https://github.com/bbaudry) <br>
<b>My proposal: </b> [Click here](https://docs.google.com/document/d/1WG1kZ5bHKFLf2PCKPQdWQn2VSGbvdQBJ6eixddJMmNs/edit)

## About project
Project depclean is a tool to automatically remove dependencies that are included in the dependency tree of java
projects but are not used in the code. It detects and removes all the unused dependencies declared in the pom.xml file
of the project or imported from its parent pom.xml. This tool can only be used in maven-based java project only.
For more information [visit here](https://github.com/castor-software/depclean#readme)

## Goals
- Previously depclean was confined only to maven-based java project, but due to increasing popularity of Gradle, 
  the project requires a feature so that depclean could be used on gradle-based java projects too. So, my main goal
  for the project was to implement a depclean-gradle plugin so that the tool depclean could analyze gradle projects.
- Secondly, the existing depclean maven plugin was failing on the multi-module maven project i.e. the plugin was not
  providing the correct output when there are dependent modules inside a multi-module maven project. So my second goal
  was to fix this bug.
- My third and the last goal was to implement some new tests for the depclean-core and depclean maven plugin.


<p align="center">
  <img src="https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/Images/creation.jpg" alt="Summer-creation"/><br>
  During this summer I thought that I am one of the character of this famous cartoon who is working on some cool\
  things with my friends. I will never forget this period of my life.:wink:<br> 
</p>
