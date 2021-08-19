# GSoC'21 @CASTOR FINAL REPORT

## General Information 📝
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

## Abstract 💻 
Project depclean is a tool to automatically remove dependencies that are included in the dependency tree of java
projects but are not used in the code. It detects and removes all the unused dependencies declared in the pom.xml file
of the project or imported from its parent pom.xml. This tool can only be used in maven-based java project only.
For more information [visit here](https://github.com/castor-software/depclean#readme)

## Goals 🎯
- Previously depclean was confined only to maven-based java project, but due to increasing popularity of Gradle, 
  the project requires a feature so that depclean could be used on gradle-based java projects too. So, my main goal
  for the project was to implement a depclean-gradle plugin so that the tool depclean could analyze gradle projects.
- Secondly, the existing depclean maven plugin was failing on the multi-module maven project i.e. the plugin was not
  providing the correct output when there are dependent modules inside a multi-module maven project. So my second goal
  was to fix this bug.
- My third and the last goal was to implement some new tests for the depclean-core and depclean maven plugin.

## Results 💰
Now the project depclean has a gradle plugin just like maven one, which can analyze and debloat out the unused 
dependencies from a gradle-based java project too. It also has all the optional parameter which was present in depclean
gradle maven-plugin. Also, I fixed the multi-module bug too i.e. now depclean-maven plugin will provide the correct
(desired) results whenever it will encounter the dependent modules inside a multi-module project. In the end, I added
some new tests for the depclean core and all of my code that I have written during GSoC with proper documentation.
Proud to say that, I have successfully achieved all of my goals that I offered to complete during the GSoC period. :tada:

## Contributions at a glance :gift: 
In short, upto now I contributed about (3804++  703--) line of code to project depclean out of which before GSoC my
contributed code was of about (453++  109--) lines. It means during the GSoC period I provide a total of (3351++  594--)
lines of code to my project.:thumbsup: 
<p align="center">
<img src = "https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/Images/all-contribution.jpg" alt="Github contribution-snap"/>
</p>

Here is the list of PRs that I created during GSoC but if anyone wants to see only my all commits then he/she may  visit
[here](https://github.com/castor-software/depclean/commits?author=ABHAY0O7)

| PULL REQUESTS                                               | COMMITS                                              | DESCRIPTION                            | STATUS  |
| ----------------------------------------------------------- |----------------------------------------------------- | -------------------------------------- | ------------------------------------------------------------------------------------|
| [#94](https://github.com/castor-software/depclean/pull/94)  | -[1deb166](1deb166d00a49c24a7bfdb1b9f088af372d941d6) <br> -[e9b0bf0](e9b0bf0ae562123bd0ccc4d4e839ef4671caab7e) <br> -[5874777](58747774d1bd20daac6d51a8623fa511867a7f27) <br> -[431e8b2](431e8b2b9b173d2eee8860d4a398099956056f59) <br> -[44f90ea](44f90ea50326a80cd307abbc5b87046d6bd46615) | Started implementation of DepClean Gradle Plugin and implemented some default analyzer to analyze a given gradle project. | Merged :ballot_box_with_check:  |
| [#95](https://github.com/castor-software/depclean/pull/95)  | -[4c00060](4c00060c7c603b9f6e069986f743f3bb19972d54) <br> -[d8931c9](d8931c9284427dd0f76192d39d7fd7afa4c04804) | Added abstract model of the Gradle Plugin development. | Merged :ballot_box_with_check:  |
| [#96](https://github.com/castor-software/depclean/pull/96)  | -[aba5a70](aba5a700aeaac8972244a7e6ea177f223af0ec2f) | Implemented Gradle Action for depclean gradle plugin. | Merged :ballot_box_with_check:  |
| [#97](https://github.com/castor-software/depclean/pull/97)  | -[39033d0](39033d06f172c1f95ec968882278c3a0143bcfb7) <br> -[9bd338b](9bd338b82ae899909a4dbf05c61f6a0b1f454af2) <br> -[6d5824f](6d5824f663e9da1af7eec5d6fc72d5a4be65ffa4) <br> -[0797b3a](0797b3a080b783ba3a88353f354fa630d1da51ce) <br> -[bea014d](bea014d61b7d911380c3136ca28edc65fd0e74ae) <br> -[bb9fa91](bb9fa912ecb6197e0fe32e7c0a19e2832cc7a847) <br> -[7df7c3f](7df7c3f2acd18190f8942350014f920f993e3265) <br> -[c9b5fc6](c9b5fc6bd1e7832f234ce07b94a0fdb9e417f822) | Added some new optional parameters to the plugin to provide flexibility in its usage. | Merged :ballot_box_with_check:  |
| [#98](https://github.com/castor-software/depclean/pull/98)  | -[49e19e3](49e19e3a93904f8c5c6fed1c4c92a81731bae5c9) <br> -[02df4c2](02df4c22b52af629db3d9558f12f0bd4f88fb5d0) <br> -[25d2844](25d28442baca1fb120e3392bfb9b6840a5923599) <br> -[e94255c](e94255c196864c4a9f524f152ade6980b7f8d54d) <br> -[ba0534c](ba0534c9c4f845ada6cc147b9f8c609573868dcf) <br> -[a6f8f9b](a6f8f9bf5974bff28d5efec157045994feae3667) <br> -[a2609a7](a2609a7ea01ed2532c4d80c8c3984d0be6822294) | Implemented some functional test for the plugin to avoid unnecessary failures or crashes and to ensure that plugin is providing a desired output. | Merged :ballot_box_with_check:  |
| [#99](https://github.com/castor-software/depclean/pull/99)  | -[02df4c2](02df4c22b52af629db3d9558f12f0bd4f88fb5d0) <br> -[0f19229](0f19229363ab39e46444e37ef028b4000559d5f0) <br> -[9d374e9](9d374e9cbc3001a3aade80123e49da8362aeb302) | Added gradle build to github actions to check for any build failures on new PRs. | Merged :ballot_box_with_check:  |
| [#100](https://github.com/castor-software/depclean/pull/100)| -[f5ebc81](f5ebc813097cb22692a36785931d89e52191b609) | Implemented json and csv optional parameters for the output report of depclean analysis. | Merged :purple_square:   |
| [#101](https://github.com/castor-software/depclean/pull/101)| -[2a5c170](2a5c1708b9c85f02aaaecb54b7fdbe2683ceae63) | Added support for the correct analysis of dependent modules of a multi-module project. |   Open :green_square:   |
| [#102](https://github.com/castor-software/depclean/pull/102)| -[3dddd8b](3dddd8ba69dfa0e9ce7ed71fafb1e92f129d4a7b) <br> -[dc2b529](dc2b5294175a40c970c5ce9e5b6755a3e29a587e) | Added a unit test for the core of depclean, more precisely it will test the working of asm. | Merged :ballot_box_with_check:  | 
| [#103](https://github.com/castor-software/depclean/pull/103)| -[3ee9e4d](3ee9e4d06e2381f61b6f02ccf2a55b7c0729d9e8) <br> -[a1ff918](a1ff91873b7f57f984896238a2f09944806aba9c) | Added a unit test to ensure the correct working of core-graph which is used as a node in the project. | Merged :ballot_box_with_check:  |
| [#104](https://github.com/castor-software/depclean/pull/103)| -[9005f8b](9005f8bc797bcc076b9de5f16e612ac98be9cd54) <br> -[60e6a71](60e6a717d6fec62c604ca315a72ef590896b96c4) | Added a unit test for core-class analyzer, it will ensure that after analyzing a non-null class, the analyzer must return the desired output | Merged :ballot_box_with_check:  |

### List of closed PRs during GSoC
- [#89](https://github.com/castor-software/depclean/pull/89) - This PR was made to show the demo of depclean gradle plugin implementation.
- [#93](https://github.com/castor-software/depclean/pull/93) - This PR contains the complete implementation of depclean gradle plugin, but was closed due to messy git history, unnecessary commits and lack of commit information.

### List of issues on which I majorly worked during GSoC
- [#67 - Depclean Gradle plugin](https://github.com/castor-software/depclean/issues/67)
- [#68 - Multi-Module support](https://github.com/castor-software/depclean/issues/68)
- [#91 - Porting Maven tests to Gradle tests](https://github.com/castor-software/depclean/issues/91)


## Contributions in detail (For those who wants to know more) :gift: :gift: 


<p align="center">
  <img src="https://github.com/ABHAY0O7/GSoC-21-CASTOR/blob/main/Images/creation.jpg" alt="Summer-creation"/><br>
  During this summer I thought that I am one of the character of this famous cartoon who is working on some cool\
  things with my friends. I will never forget this period of my life.:wink:<br> 
</p>
