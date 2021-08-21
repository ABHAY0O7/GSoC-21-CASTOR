# GSoC'21 @CASTOR FINAL REPORT
<div align="center">
<img src="https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/utils/Images/header-image.png" alt="GSoC-logo" height=250px width=600px>
</div>

## General Information 📝
<b>Organization:</b> [CASTOR](https://www.castor.kth.se/) <br>
<b>Project:</b> [DEPCLEAN](https://github.com/castor-software/depclean) <br>
<b>Tasks:</b> 
1. Implementation of a depclean-gradle-plugin like depclean-maven-plugin.
2. Implement a feature in depclean-maven-plugin to analyze multi-module projects.
3. Implementation of some new tests.

<b>Student:</b> [Abhay Singh](https://github.com/ABHAY0O7) <br>
<b>Mentors:</b> [Thomas Durieux](https://github.com/tdurieux), [César Soto Valero](https://github.com/cesarsotovalero) 
& [Benoit Baudry](https://github.com/bbaudry) <br>
<b>My proposal: </b> [Click here](https://docs.google.com/document/d/1WG1kZ5bHKFLf2PCKPQdWQn2VSGbvdQBJ6eixddJMmNs/edit)

## Abstract :scroll: 
This summer, I was selected for GSoC to work on project DepClean for [CASTOR organization](https://github.com/castor-software).
CASTOR is a research software center at [KTH Royal institiute](https://www.kth.se/en) :classical_building: . It performs lots of cool stuffs like
developing software tools, perform excellent research, train world class Graduates and a lot more. One of the best software tools
which is provided by CASTOR is depclean. It is a tool to automatically remove dependencies that are included in the dependency
tree of java projects but are not used in the code. It detects and removes all the unused dependencies declared in the pom.xml
file of the project or imported from its parent pom.xml. This tool can only be used in maven-based java projects.
For more information [visit here](https://github.com/castor-software/depclean#readme)

## Goals :dart: 
- Previously depclean was confined only to maven-based java projects, but due to the increasing popularity of Gradle, 
  the project requires a feature so that depclean could be used on gradle-based java projects too. So, my main goal
  for the project was to implement a depclean-gradle plugin so that the tool depclean could analyze Gradle projects.
- Secondly, the existing depclean maven plugin was failing on the multi-module maven project i.e. the plugin was not
  providing the correct output when there are dependent modules inside a multi-module maven project. So my second goal
  was to fix this bug.
- My third and last goal was to implement some new tests for the depclean-core and depclean maven plugin.

## Results :rocket:
Now the project depclean has a gradle plugin just like maven one, which can analyze and debloat out the unused 
dependencies from a gradle-based java project too. It also has all the optional parameter which was present in depclean
gradle maven-plugin. Also, I fixed the multi-module bug too i.e. now depclean-maven plugin will provide the correct
(desired) results whenever it will encounter the dependent modules inside a multi-module project. In the end, I added
some new tests for the depclean core and all of my code that I have written during GSoC with proper documentation.
Proud to say that, I have successfully achieved my goals that I planned to do during the GSoC period. :tada:
Here are some results of the tasks that I have completed during GSoC, you can treat them as a working prototype. :wink: 
- [Depclean Gradle plugin](https://github.com/ABHAY0O7/GSoC-21-CASTOR/tree/main/utils/gradle-plugin-result.md)
- [Depclean Maven plugin with multi-module analysis feature](https://github.com/ABHAY0O7/GSoC-21-CASTOR/tree/main/utils/multi-module-result.md)

## Contributions :gift:
Here are some stats of my contributions to project DepClean during GSoC:

- I made a total of 13 PRs during GSoC, out of which 11 got successfully merged and 2 got closed.
- In those 11 successfully merged PRs, I made a total of 35 commits during the program.
- Overall up to now I had contributed with `4367++ 918--` lines of codes to this project out of which `3914++ 809--` 
  lines of code have been written during the program.

<p align="center">
<a href = "https://github.com/castor-software/depclean/graphs/contributors"><img src = "https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/utils/Images/all-contribution.png" alt="Github contribution-snap"/></a>
</p>

Here is the list of PRs (both open & closed) that I created during GSoC but if anyone only wants to see all of my commits then he/she may visit [here](https://github.com/castor-software/depclean/commits?author=ABHAY0O7).

| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;PULL &nbsp;&nbsp;REQUESTS                         | &nbsp;&nbsp;COMMITS                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;DESCRIPTION                                                                                     | &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;STATUS |
|:------------------------------------------------------------------------------------- |:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |:------------------------------------------ |
| [#94](https://github.com/castor-software/depclean/pull/94)                            | <ul> <li> [1deb166](1deb166d00a49c24a7bfdb1b9f088af372d941d6) </li> <li> [e9b0bf0](e9b0bf0ae562123bd0ccc4d4e839ef4671caab7e) </li> <li> [5874777](58747774d1bd20daac6d51a8623fa511867a7f27) </li> <li> [431e8b2](431e8b2b9b173d2eee8860d4a398099956056f59) </li> <li> [44f90ea](44f90ea50326a80cd307abbc5b87046d6bd46615) </li> </ul>                                                                                                                                                                                              | This PR marked the starting of the implementation of DepClean Gradle Plugin. It also covers the analysis part of the plugin which is required to collect all the dependencies from the project itself and then using them to get the used artifact of the project from depclean core.                                                                       | :purple_square:Merged                      |
| [#95](https://github.com/castor-software/depclean/pull/95)                            | <ul> <li> [4c00060](4c00060c7c603b9f6e069986f743f3bb19972d54) </li> <li> [d8931c9](d8931c9284427dd0f76192d39d7fd7afa4c04804) </ul>                                                                                                                                                                                                                                                                                                                                                                                                 | This PR implements the abstract classes or methods which are must to build a gradle plugin like action and tasks classes. </li> </ul>                                                                                                                                                                                                                       | :purple_square:Merged                      |
| [#96](https://github.com/castor-software/depclean/pull/96)                            | <ul> <li> [aba5a70](aba5a700aeaac8972244a7e6ea177f223af0ec2f) </li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                          | In this PR, I implemented complete Gradle Action i.e. the working of the depclean gradle plugin.                                                                                                                                                                                                                                                            | :purple_square:Merged                      |
| [#97](https://github.com/castor-software/depclean/pull/97)                            | <ul> <li> [39033d0](39033d06f172c1f95ec968882278c3a0143bcfb7) </li> <li> [9bd338b](9bd338b82ae899909a4dbf05c61f6a0b1f454af2) </li> <li> [6d5824f](6d5824f663e9da1af7eec5d6fc72d5a4be65ffa4) </li> <li> [0797b3a](0797b3a080b783ba3a88353f354fa630d1da51ce) </li> <li> [bea014d](bea014d61b7d911380c3136ca28edc65fd0e74ae) </li> <li> [bb9fa91](bb9fa912ecb6197e0fe32e7c0a19e2832cc7a847) </li> <li> [7df7c3f](7df7c3f2acd18190f8942350014f920f993e3265) </li> <li> [c9b5fc6](c9b5fc6bd1e7832f234ce07b94a0fdb9e417f822) </li> </ul> | In this PR, I added some new (but based on maven plugin) optional parameters to the plugin to make it highly configurable and to provide flexibility in its usage.                                                                                                                                                                                          | :purple_square:Merged                      |
| [#98](https://github.com/castor-software/depclean/pull/98)                            | <ul> <li> [49e19e3](49e19e3a93904f8c5c6fed1c4c92a81731bae5c9) </li> <li> [02df4c2](02df4c22b52af629db3d9558f12f0bd4f88fb5d0) </li> <li> [25d2844](25d28442baca1fb120e3392bfb9b6840a5923599) </li> <li> [e94255c](e94255c196864c4a9f524f152ade6980b7f8d54d) </li> <li> [ba0534c](ba0534c9c4f845ada6cc147b9f8c609573868dcf) </li> <li> [a6f8f9b](a6f8f9bf5974bff28d5efec157045994feae3667) </li> <li> [a2609a7](a2609a7ea01ed2532c4d80c8c3984d0be6822294) </li> </ul>                                                                | In this PR, I implemented some functional test which are needed for the plugin to avoid unnecessary failures or crashes and to ensure that plugin is providing a desired output.                                                                                                                                                                            | :purple_square:Merged                      |
| [#99](https://github.com/castor-software/depclean/pull/99)                            | <ul> <li> [02df4c2](02df4c22b52af629db3d9558f12f0bd4f88fb5d0) </li> <li> [0f19229](0f19229363ab39e46444e37ef028b4000559d5f0) </li> <li> [9d374e9](9d374e9cbc3001a3aade80123e49da8362aeb302) </li> </ul>                                                                                                                                                                                                                                                                                                                            | In this PR, I added gradle build to depclean workflow (github actions) to check for any build failures on new PRs.                                                                                                                                                                                                                                          | :purple_square:Merged                      |
| [#100](https://github.com/castor-software/depclean/pull/100)                          | <ul> <li> [f5ebc81](f5ebc813097cb22692a36785931d89e52191b609) </li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                          | This PR marked the implementation of json and csv optional parameters for depclean gradle plugin. These parameters help depclean to show its result in the provided format **`(.json or .csv)`**. Also, this PR marked the complete deployment of depclean-gradle plugin. :smiley:                                                                          | :purple_square:Merged                      |
| [#101](https://github.com/castor-software/depclean/pull/101)                          | <ul> <li> [2a5c170](2a5c1708b9c85f02aaaecb54b7fdbe2683ceae63) </li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                          | In this PR, I added support (fixed bug) for the correct analysis of dependent modules of a multi-module project.                                                                                                                                                                                                                                            | :purple_square:Merged                      | 
| [#103](https://github.com/castor-software/depclean/pull/103)                          | <ul> <li> [15ef0cd](15ef0cdce12f20cb66b87b86bb1057e112012241) </li> <li> [77ff120](77ff12018ae5f08c4f59e7fb4a6142cede09bb45) </li> <li> [43f4ecd](43f4ecd3425bdd313508e8194ecb655a571a0bf8) </li> </ul>                                                                                                                                                                                                                                                                                                                            | In this PR, I added a unit test for the core of depclean, more precisely it will test the working of asm.                                                                                                                                                                                                                                                   | :purple_square:Merged                      | 
| [#104](https://github.com/castor-software/depclean/pull/104)                          | <ul> <li> [ada4b1e](ada4b1e09e3e326fd00e327da75678e95bc6994a) </li> <li> [8342536](8342536997a09e2f7e810db05e6c8b09e6b2be8c) </li> </ul>                                                                                                                                                                                                                                                                                                                                                                                           | In this PR, I added a unit test to ensure the correct working of core-graph which is used as a node in the project.                                                                                                                                                                                                                                         | :purple_square:Merged                      |
| [#105](https://github.com/castor-software/depclean/pull/105)                          | <ul> <li> [fc4e0a7](fc4e0a7a8d06621bd5c6595a09a959bdc4a336d6) </li> <li> [0f2a3bc](0f2a3bc5dc753f881f1df899f175511a5a56dbf3) </li> </ul>                                                                                                                                                                                                                                                                                                                                                                                           | In this PR, I added a unit test for core-class analyzer, it will ensure that after analyzing a non-null class, the analyzer must return the desired output                                                                                                                                                                                                  | :purple_square:Merged                      |

### List of my closed PRs during GSoC
- [#89](https://github.com/castor-software/depclean/pull/89) - This PR was made to show the demo of depclean gradle plugin implementation.
- [#93](https://github.com/castor-software/depclean/pull/93) - This PR contains the complete implementation of depclean gradle plugin, but was closed due to messy git history, unnecessary commits and lack of commit information.

### List of issues on which I majorly worked upon during GSoC
- [#67 - Depclean Gradle plugin](https://github.com/castor-software/depclean/issues/67)
- [#68 - Multi-Module support](https://github.com/castor-software/depclean/issues/68)
- [#91 - Porting Maven tests to Gradle tests](https://github.com/castor-software/depclean/issues/91)

## Communication (Chat) :speaking_head: 
In our very first virtual meet, we decided to keep all our technical discussions to be open to all for future 
references. So, all of our formal (technical) discussion took place over GitHub. Here are the required threads links
- [Thread-1](https://github.com/castor-software/depclean/issues/92)
- [Thread-2](https://github.com/castor-software/depclean/issues/91)

## Future plans :timer_clock:
The last three months of my life were unforgettable. This time was very precious to me, and I hope that it was so too
for my community. After GSoC, I would like to continue the same spirit of the contribution that I maintained during GSoC.
I would like to get involved more in the community and will be happy to guide new developers as well. I will also like
to work on some new (if any) or existing projects from my organization. In the end, I will try my best to be more 
and more helpful to the community. :innocent: If anyone wants any kind of help or wants to connect with me, then he/she is just
[two clicks away](https://github.com/ABHAY0O7/ABHAY0O7/blob/main/README.md). 

## Key takeaways :brain: 
There's a lot that I learned from GSoC, I mean what can be better than working on a community product that is used by
around 10k users. This is the list of my key takeaways from this program.
- Got experience of working on a community product.
- Learned lots of new things in Java, and also learned some new concepts in OOPS.
- Learned lots of new things about project management tools like Gradle and Maven and also learned about dependency management.
- Got experienced developing Gradle & Maven plugins.
- Learned about how to work in a team or with a broad community on single or multiple projects.

## Acknowledgement :clap:
On this ending note, I want to thank my mentors [Thomas Durieux](https://github.com/tdurieux), [César Soto Valero](https://github.com/cesarsotovalero) 
& [Benoit Baudry](https://github.com/bbaudry) for constantly supporting me from the very beginning of my contributions.
I am very thankful for their patient behavior whenever I got stuck and their suggestions that helped me in resolving them.
Also, I am thankful to the whole CASTOR family who provided me this wonderful opportunity of working on such an amazing project.

I would also like to thank my family and my friends who constantly supported and helped me throughout the program. 
Special thanks to [Mitul varshney](https://github.com/Mitul16) for helping me out during my tough times of debugging. :heart: 

In the end, I would like to thank Google for organizing such a wonderful program and also kudos to me who successfully
completed this program. :wink: I am ending this report with an image, which precisely describes my feelings of this summer. <br>

<p align="center">
  <img src="https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/utils/Images/creation.jpg" alt="Summer-creation"/><br>
  <h5 align = "center">During this summer I thought that I am one of the character of this famous cartoon who is working on some cool
  things with his friends. I will never forget this period of my life.:wink:<br></h5>
  <h2 align = "center"> Thanks for your precious time. 👋</h2>

