<center><font size=5 color=#008b8b>Content</font></center> 
[toc]

<div STYLE="page-break-after: always;"></div>
## 1.Brief Description

From this section, you will have an overview of almost everything involved in this SRS document, including a brief description of the system, the purpose of this document and some other miscellaneous things.

### 1.1 Purpose
At present, most club platforms are managed manually , which cannot achieve the purpose of real-time update of personnel data and active promotion of club activities. Therefore,it is great to shift the focus on integrating community information with big data and software development technology. By constructing a community management system, it is convenient for different users to participate in it well.

As we have illustrated in the previous project proposal ,**the Club Communication Platform** mainly aims to build an online student club management system with the purpose of simplifying club management process and achieving real-time club data updating,which promises different kind of target users can take part in club activities or club management with convenience.

Aiming to provide the readers with a detailed description of the functionalities of **JIYU(Meet what you will meet)**, this document will mainly cover the essential use case modelling and snapshots of the system's user interface. Also, the intended features and technical dependencies will be included.

### 1.2 Project Scope
The **JIYU(Meet what you will meet)** is a web-based club management system, whose goal is to simplify the community management process and provide an online club social platform. The users can access the system by PC or mobile device through a Website.

Specially, potential scenarios of this system mainly include searching clubs, browsing activities information and club information, joining clubs, dropping out of a club , and so on. Both club members and non-club members can browse the information and join in the activities ,make comments through the system after they register and log in. In addition, the club members can use the system to organize activities, making the organization easier. As for club union supervisor, they have the authority to manage the online forum and highlight the activities ,which simplifies their work.

![cc3DdP.png](https://z3.ax1x.com/2021/04/14/cc3DdP.png)

Besides, this online system also has the listed features: 
- running in a networked environment.
- handling the user authentication for security.
- owning a centralized database and so on.

### 1.3 Glossary of Terms
|Terms|Definition|
|---|---|
|**JIYU**| The name of our system, which means that you will meet the friends after using our system to join the world of different activities.|
|**Club**|A club is usually composed of a group of people in the university who have common hobbies and goals. It is also usually an important part of university life.|
|**Activity**|The online or offline activity held by the university club, whose main body is users or community members.|
|**TOWS**| A diagram to analyze the main internal strengths, weaknesses and external opportunities and threats closely related to the research object with the idea of systematic analysis, and draw a series of corresponding conclusions. |
|**Online Forum**|A website part, which refers to discussions among different people around the same topic|
|**Authority**|the different operations that each actor can perform when using this system.|
|**Column**|A collection of the same type of topic posts in the forum|
|**Publicize Activities**|the club union supervisor can post the activities reported by the associations to the homepage, so that more people can pay attention to the activities|
|**Report**|Some complaints made by users about the inappropriate columns or comments (E.G.: insulting people or spreading terrifying information) on the forum. The supervisor will check whether it's  a proper report.|
|**Club Statics**|Data on the development of the club, usually including changes in the number of clubs over time, participation in activities, etc.|
|**Resume**|In our system,it refers to an account's basic information when registered,including email,cellphone number,student ID and some other minor information.|
|**Modify Permission**|The system modifies the user's authority and changes the scope of the user's function.|

### 1.4 Target Readers and Suggestions
This SRS document is intended for those taking part in this system. Readers who just want to have a general impression of this product may pay more attention to PART 1(Introduction). Besides, for more detailed information of the system such like features, functions or dependencies, PART 2(Overall Description) is recommended.

As for use case modelling, they are described specifically in PART 3(Specific Requirement), where you can also take a glimpse of the interface of the system. Finally, PART 4(Other  Supplementary specification) includes some additional information about the system.
<div STYLE="page-break-after: always;"></div>
## 2.Introduction

### 2.1 Product Perspective
This system is a web application, including web side and server. The server runs the database to process requests from users. The data requested by different roles to server is different, and more detailed information will be introduced in the use case section.

![cc3BZt.png](https://z3.ax1x.com/2021/04/14/cc3BZt.png)

### 2.2 Product Features
- The system is a web application, so only under the circumstance of Internet can users get access to it.
- The system has strict access control. Users can only access the data within their authority after they have been authenticated and can only operate within their authority.
- The system is user-friendly with simple but beautiful UI.
- The system provides a sequence of operations for users to make clubs management and communication more easily.

### 2.3 Actors
There are 4 types of users interact with the system: **Visitor**, **User** , **Club Member** ,**Club Leader** and **Club Union Supervisor**. As part of system, each of them plays an irreplaceable role.

The **Visitor** can browse information provided by the system, including forum comments, club information and activities information.

The **User** , including club members and non-club members. They can participate in activities, search and join a club, create a club.

The **Club Member** can make comments on forum, quit the club as well as apply for leadership.

The **Club Leader** is the one who can review the club members, modify the information of club, resign from club and dismiss the club.

The **Club Union Supervisor** handles most of reviewing work, such as reviewing club leader, reviewing club information and so on. Besides, they have the authority to manage the online forum. 

### 2.4 Assumptions and Dependencies
The following are assumptions and dependencies of this system:
- School will supply the information of users or directly use unified authentication to approach the system, making the system easier to approach.
- The activities depends on the organizers to organize and review.
- If the users cannot join in an activity because of the capacity or other reason, the system will send a message to make users acknowledged.
<div STYLE="page-break-after: always;"></div>
## 3.Specific Requirement

### 3.1 Agile development and requirement analysis
- **Persona**
The purpose of developing JIYU (Meet what you will meet) exchange platform is to provide convenience for the university club management and students' participation in club activities. Therefore, in the stage of exploring system functions, this document summarizes virous users according to different people's personality and characteristics, living environment and values, and draw a user **persona** on this basis.

  ![ccGE3F.png](https://z3.ax1x.com/2021/04/14/ccGE3F.png)

  <center>(The photos and other parts are fictional)</center>

- **Empathy map**
According to different user portraits, we draw an **empathy map** from the perspective of users. Through their thinking, speaking, hearing, doing and feeling in daily life, we can improve our system functions.

	![ccGiNV.png](https://z3.ax1x.com/2021/04/14/ccGiNV.png)

- **User story**
  By summarizing and analyzing different personas and empathy maps, we have learned a lot about the expectations and needs of many virous users for our system, and displayed the user needs through **user stories**.

  ![ccGPA0.png](https://z3.ax1x.com/2021/04/14/ccGPA0.png)

- **User journey map**
According to different users' different requirements for the system, the user stories are classified according to the users, and then each user story is tracked to build the steps of users' interaction with the system when they complete the requirements and the changes of their mentality, and draw the **user journey map** to help us design the system functions.

	![ccGFhT.png](https://z3.ax1x.com/2021/04/14/ccGFhT.png)

- **User story map**
On this basis, we get the most urgent needs of users for the system and the good ideas that can be improved, and then draw the user story map according to the urgency of the task. The **user story map** can help us build the use case model and distribute the team tasks, develop the feasible version in the shortest time according to the agile development idea, and then update the system according to the user needs.

	![ccGA9U.png](https://z3.ax1x.com/2021/04/14/ccGA9U.png)

<div STYLE="page-break-after: always;"></div>

### 3.2 Use Cases Modeling

1. Global View on Use Case

   ![cc33a6.jpg](https://z3.ax1x.com/2021/04/14/cc33a6.jpg)

2. Visitor Login & Register System

   **Use Case Diagram**

   ![cc31Vx.jpg](https://z3.ax1x.com/2021/04/14/cc31Vx.jpg)

   **Detailed Specification for Use Case**

   Use Case: Register
   | Use Case         | Register                                                     |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC01                                                         |
   | Specification    | Visitors register their own account and fill their own basic information; <br>System give authorization according to the type of the account. |
   | Actors           | **Visitor**                                                  |
   | Pre-condition    | Visitors enter the login webpage for the first time and click "sign in". |
   | Basic Path       | 1. Visitors enter the website.<br/>2. Visitors click "sign up".<br/>3. Visitors fill basic information:<br/>    3.1 Visitors fill cellphone number\email\school ID.<br/>    3.2 Visitors set username and password. <br/>4. Visitors click "send verification code" and fill the code from text or email .<br/>5. System operate account identity verify according to school ID.<br/>6. Visitors successfully create an user account. |
   | Alternative Path | 1. Visitors exit the webpage during information filling<br/>    system will show notification:"Information filling incomplete,do you want to exit anyway?"<br/>2. Visitors have problem during creating the account:<br/>    2.1 Visitors input illegal cellphone number\email\school ID<br/>           system will show notification:"Sorry,illegal cellphone number\email\school ID"<br/>    2.2 Visitors don't receive verification code<br/>           system will allow visitors to resend the verification code again after 60s countdown.<br/>    2.3 Visitors input wrong verification code<br/>            system will show notification:"Sorry,wrong verification code,please input again."<br/> |
   | Post-condition   | Visitors get their personal account and authorization.       |

   Use Case: Login

   | Use Case         | Login                                                        |
| ---------------- | ------------------------------------------------------------ |
| ID               | UC02                                                         |
| Specification    | Visitors type account ID and password to login the account.<br>System provides extend services such as retrieving password. |
| Actors           | **Visitor**                                                  |
| Pre-condition    | Visitors have their own authorized account.                  |
| Basic Path       | 1. Visitors enter the website.<br/>2. Visitors click "login".<br/>3. Visitors fill username and password into the webpage blanks.<br/>4. Visitors successfully login. |
| Alternative Path | 1. Visitors input wrong account information:<br/>    1.1 If Visitors input invalid account ID,<br/>           system will reject login,show notification"Sorry,account doesn't exist,please input again".<br/>    1.2 If Visitors input wrong password,<br/>           system will reject login,show notification "Sorry,wrong password,please input again".<br/>    1.3 If Visitors input wrong password for 5 times,<br/>           system will ban visitors from logging in for 3 minutes. <br/>2. Visitors click "forget password?"<br/>           system will handle the request,send a verification code base on the account's cellphone number\email\school ID.<br/>           Visitors can input the verification code and reset the password. |
| Post-condition   | Visitors enter the system, become users and can access users' operations. |


3. Club Change System

   **Use Case Diagram**

   ![cc38IK.jpg](https://z3.ax1x.com/2021/04/14/cc38IK.jpg)

   **Detailed Specification for Use Case**

   Use Case: Establish a New Club

   | Use Case         | Establish a New Club                                         |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC03                                                         |
   | Specification    | Allow all users to establish a new club                      |
   | Actors           | **User**,**Club Union Supervisor**                           |
   | Pre-condition    | None                                                         |
   | Basic Path       | 1. The use case starts when the User request to establish a new club<br>2. User fills in and submit the application form<br>3. The system upload the form and send it to Club Union Supervisor<br>4. Club Union Supervisor review the club alteration<br>    4.1 If the application is approved,the system will grants the authority of Club Leader to User <br>    4.2 If the application is denied, the system will send a message to User. |
   | Alternative Path | 1. User can't search for a certain club<br>   1.1 User can establish a new club in the searching page |
   | Post-condition   | 1. User establishes a new club<br>2. User become Club Leader of the new club |

   Use Case: Modify Club Information

   | Use Case                   | Modify Club Information                                      |
   | -------------------------- | ------------------------------------------------------------ |
   | ID                         | UC04                                                         |
   | Specification              | Allows the Club Leader to modify the specific club information |
   | Actors                     | **Club Leader**,**Club Union Supervisor**                    |
   | Pre-condition              | The operator has to be a Club Leader                         |
   | Basic Path                 | 1. The use case starts when User request to modify the information of a club<br>2. User modify and submit the information form of Club<br>3. System upload the form and  send it to Club Union Supervisor<br>4. Club Union Supervisor review club information<br>    4.1 If application is approved, the system will upload new information to the club homepage<br>    4.2 If the application is denied, the system will send a message to the user |
   | Alternative Flows of Event | 1. User doesn't fill all the information<br>    1.1 User receives a warning message says "The information cannot be empty"<br>    1.2 User input the information<br>2. User logs out of the system<br>3. User click "back" button after modifying<br>    3.1 User receive a warning message says "Please confirm upload information"<br>    3.2 If user click yes, then save information and go back to previous interface<br>    3.3 Otherwise go back to previous interface without uploading information |
   | Post-condition             | None                                                         |

4. Membership Change System

   **Use Case Diagram**

   ![cc3YGD.jpg](https://z3.ax1x.com/2021/04/14/cc3YGD.jpg)

   **Detailed Specification for Use Case**

   Use Case: Resign 
   | Use Case         | Resign                                                       |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC05                                                         |
   | Specification    | Club leader applies to resign ,becoming a normal club member. |
   | Actors           | **User**,**Club Union Supervisor**                           |
   | Pre-condition    | The club leader applies to resign the leadership.            |
   | Basic Path       | 1. The club leader submits the application for resignation. <br>2. Club Union Supervisor reviews the application form. <br>3. After the review is passed, the authority of the leader will be changed in the background. And basic information of the club will be updated at the same time. |
   | Alternative Path | 1. Club Leader withdraw the application<br>   The club leader who have submitted application withdraws his or her application before the review of Club Union     Supervisor;<br>2. Club Union Supervisor fails to pass the review<br>   Club Union Supervisor rejects the application of the leader. |
   | Post-condition   | The club leader becomes an ordinary club member. And basic information of the club will be updated at the same time. |

   Use Case: Apply for Leadership
   | Use Case         | Apply for Leadership                                         |
| ---------------- | ------------------------------------------------------------ |
| ID               | UC06                                                         |
| Specification    | Club member applies to lead the club                         |
| Actors           | **User**,**Club Union Supervisor**                           |
| Pre-condition    | A club member applies to lead the club without a leader.     |
| Basic Path       | 1. The club member submits the application form for the leader of the club;<br>2. Club Union Supervisor reviews the application form. <br>3. After the review is passed, the authority of the member will be changed in the background. And basic information of the club will be updated at the same time. |
| Alternative Path | 1. Club Member withdraw the application<br>   The club member who have submitted application withdraws his or her application before the review of Club Union Supervisor;<br>2. Club Union Supervisor fails to pass the review<br>   Club Union Supervisor rejects the application of the member. |
| Post-condition   | The club member who has submitted the application becomes the club leader and the basic information of the club is updated. |

5. Activity Organization System

   **Use Case Diagram**

   ![cc3JPO.jpg](https://z3.ax1x.com/2021/04/14/cc3JPO.jpg)

   **Detailed Specification for Use Case**

   Use Case: Participate in Activities

   | Use Case         | Participate in Activities                                    |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC07                                                         |
   | Specification    | Users find the activities and complete registration.         |
   | Actors           | **User**                                                     |
   | Pre-condition    | None                                                         |
   | Basic Path       | 1. User selects activity section<br>2. User views the activity information<br>3. User chooses the activities they want to participate in<br>4. User fills in personal information<br>    4.1 User fills in the ID and name<br>    4.2 User fills in the phone numbers<br>5. User submits the activity application<br>6. User receives the message of successful application |
   | Alternative Path | 1. User isn’t logged in to apply for the activity, the system should turn to the login interface.<br/>2. User leaves the page during the process of filling in the information<br>    2.1 User will receive the message on whether submit or save the content<br>    2.2 If User chooses to submit, the application will be submitted automatically<br>    2.3 Otherwise, the application will not be saved and user will leave the page<br>3. If user logs out during the process of filling in the information by accident, the content will remain<br>4. User doesn’t fill in key information<br>    4.1 User will receive the error message<br>    4.2 User will fill in the information again<br>5. User’s ID doesn’t conform to the format<br>    5.1  User will receive the error message<br>    5.2  User will fill in ID again |
   | Post-condition   | The club leaders can receive the application and review it.  |

   Use Case: Play the Role of a Volunteer

   | Use Case         | Play the Role of a Volunteer                                 |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC08                                                         |
   | Specification    | Club members can voluntarily prepare props for the activity or maintain the order of the activity. |
   | Actors           | **Club Member**                                              |
   | Pre-condition    | Users must be a member of the club that organizes the activity. |
   | Basic Path       | 1. Club members select activity section<br/>2. Club members views the activity held by own club<br/>3. Club members choose the activities they want to volunteer <br/>4. Club members fill in personal information<br/>        4.1  Club members fill in the ID and names<br/>        4.2  Club members fill in the phone numbers<br/>5. Club members submit the activity application<br/>6. Club members receive the message of successful application |
   | Alternative Path | 1. Club member doesn’t log in to apply for the activity volunteer, the system should turn to the login interface.<br/>2. User doesn’t belong to the club<br/>    2.1. User will receive the message<br/>    2.2. The system turns to the activity interface<br/>3. If club member logs out during the process of filling in the information by accident, the content will remain<br/>4. Club member leaves the page during the process of filling in the information<br/>     4.1. Club member will receive the message on whether submit or save the content<br/>     4.2. If club member chooses to submit, the application will be submitted automatically<br/>     4.3. Otherwise, the application will not be saved and user will leave the page<br/>5. Club member doesn’t fill in key information<br/>    5.1. Club member will receive the error message<br/>    5.2. Club member will fill in the information again<br/>6. Club member’s ID doesn’t conform to the format<br/>    6.1. Club member will receive the error message<br/>    6.2. Club member will fill in ID again |
   | Post-condition   | The club leaders can receive the application and review it.  |

   Use Case: Organize the Activities

   | Use Case         | Organize the Activities                                      |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC09                                                         |
   | Specification    | Club Leaders can apply for holding club activities           |
   | Actors           | **Club Leader**                                              |
   | Pre-condition    | None                                                         |
   | Basic Path       | 1. Club leader chooses to hold the activity<br/>2. Club leader fills in the activity application<br/>    2.1. Club leader fills in the ID, name and phone number.<br/>    2.2. Club leader describes the activity<br/>    2.3. Club leader applies for the activity budget<br/>3.  Club leader submits the application to the club Union Supervisor<br/>4. Club leader receives the message of successful application |
   | Alternative Path | 1. Club leader doesn’t log in to apply for holding the activity, the system should turn to the login interface.<br/>2. If club leader logs out during the process of filling in the information, the content will remain<br/>3. Club leader leaves the page during the process of filling in the information<br/>    3.1. Club leader will receive the message on whether save the content<br/>    3.2. If club leader chooses to save, the application will be saved automatically<br/>    3.3. Otherwise, the application will not be saved and user will leave the page<br/>4. Club member doesn’t fill in key information<br/>    4.1. Club member will receive the error message<br/>    4.2. Club member will fill in the information again |
   | Post-condition   | The Club Union Supervisor can receive the application and review it. |

   Use Case: Review the Activity application

   | Use Case         | Review the Activity application                              |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC10                                                         |
   | Specification    | Club union supervisor can review the activity application and give comments for it. |
   | Actors           | **Club Union Supervisor**                                    |
   | Pre-condition    | The Club Leaders submit the activity application             |
   | Basic Path       | 1. Club union supervisor receives the activity application<br/>2. Club union supervisor views the activity application<br/>    2.1. Club union supervisor views the activity content<br/>    2.2. Club union supervisor determines budget and check venue<br/>3. Club union supervisor reviews whether this activity passed<br/>    3.1. Club union supervisor explains the reason and gives advice when the application not passed<br/>    3.2. Club union supervisor saves the activity information when the application passed<br/>4. Club leaders receive the result of the application |
   | Alternative Path | 1. If club union supervisor logs out during reviewing the application, the advice and content will remain<br/>2. Club union supervisor doesn’t log in to apply for holding the activity, the system should turn to the login interface. |
   | Post-condition   | The status of the activity application has changed (passed or not). |

   Use Case: Publicize Activities

   | Use Case         | Publicize Activities                                         |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC11                                                         |
   | Specification    | Club union supervisor can publicize the activity             |
   | Actors           | **Club Union Supervisor**                                    |
   | Pre-condition    | The status of the activity application is passed             |
   | Basic Path       | 1. Club union supervisor edit the activity information<br/>    1.1. Club leaders provide the publicity articles<br/>    1.2. Club union supervisor check the content of the article<br/>    1.3. Club union supervisor fill in the activity site and time<br/>2. Club union supervisor publicize the activity in the activity section<br/>    2.1. Club union supervisor send the activity article to the front page according to the importance of the activity<br/>    2.2. Club union supervisor send private messages to club members |
   | Alternative Path | If the article is not passed, club union supervisor should give modification suggestions through private message. |
   | Post-condition   | Users can participate in activities and be a volunteer in it. |

   Use Case: Review Activity Application

   | Use Case         | Review Activity Application                                  |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC12                                                         |
   | Specification    | Club leaders can review users and  club members who signed up for the activity |
   | Actors           | **Club Leader**                                              |
   | Pre-condition    | The status of the activity application is passed             |
   | Basic Path       | 1. Club Leaders view the approved activities<br/>2. Club Leaders view the information about signing up the activity<br/>3. Club Leaders choose users to participate in activities<br/>    3.1. Club leaders give the reason for the users who not pass<br/>    3.2. Club leaders give the message about activities to the users who pass |
   | Alternative Path | 1. Club leader doesn’t log in to apply for reviewing the application, the system should turn to the login interface.<br/>2. If club leader logs out during the process of filling in the information, the content will remain<br/>3. If the number of people participate in the activity has reached the upper limit<br/>    3.1. club leader will receive the message when the users pass the review<br/>    3.2. the pass review will revoke |
   | Post-condition   | The status of the student activity application has changed   |

6. Online Forum System

   **Use Case Diagram**

   ![cc3Qq1.jpg](https://z3.ax1x.com/2021/04/14/cc3Qq1.jpg)

   **Detailed Specification for Use Case**

   Use Case: View Forum Page

   | Use Case         | Review Activity Application                                  |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC13                                                         |
   | Specification    | Visitors(as well as all users) can have a peak on the forum content |
   | Actors           | **Visitor**                                                  |
   | Pre-condition    | Visitors enter the webpage                                   |
   | Basic Path       | 1.Visitors enter the website.<br/>2.Visitors click "online forum"<br/>3.system show forum column and topics on the website page<br/>4.Visitors can have a view on the website and each column topic.<br/> |
   | Alternative Path | 1.Visitors exit the system.<br/>2.Visitors(non-login) try to create a column for discussion or leave comments on the webpage<br>    system reject the operation,show notification"Sorry,you have to login to join discussion on the forum" |
   | Post-condition   | None                                                         |

   Use Case: Create Columns

   | Use Case         | Create Columns                                               |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC14                                                         |
   | Specification    | Users create column to publish information;<br/>Club union supervisor delete illegal content;system check users' authority and ban illegal users' operations. |
   | Actors           | **User,Club Union Supervisor**                               |
   | Pre-condition    | Users successfully login and has authority to create column on the forum |
   | Basic Path       | 1.include(check authority)<br/>2.Users click "create column".<br/>3.Administrator check the users' authority.<br/>4.Users gain authorization.<br/>5.Users type column content in the talk box.<br/>6.Users click "publish column"<br/>7.Users successfully publish a column.<br/> |
   | Alternative Path | 1.Users exit the system.<br/>2.Users doesn't get authorization<br/>    2.1 When system find illegal record in users' forum history,system will ban users operation.<br/>3.Users exit the forum or logout while editing the column content in step 5<br/>     show notification:"You are still editing your column,do you really want to exit?"<br/>4.Club Union Supervisor detect the content of users' column<br/>    4.1 if users' column cause bad social influence and is reported by other users<br/>         -club union supervisor delete illegal content.<br/>         -when caused severe social influence,Club union supervisor update illegal record to<br>          the system,then the system will ban  users' operation of using the forum. |
   | Post-condition   | None.                                                        |

   Use Case: Leave Comments

   | Use Case         | Leave Comments                                               |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC15                                                         |
   | Specification    | Users leave comments base on their own opinion;<br/>Club union supervisor delete illegal content;system check users' authority and ban illegal users' operations. |
   | Actors           | **User,Club Union Supervisor**                               |
   | Pre-condition    | Users successfully login and has authority to leave comments on the forum. |
   | Basic Path       | 1.include(check authority)<br/>2.Users click "leave your comment".<br/>3.Administrator check the users' authority.<br/>4.Users gain authorization.<br/>5.Users type comment  in the talk box.<br/>6.Users click "publish comment"<br/>7.Users successfully leave a comment.<br/> |
   | Alternative Path | 1.Users exit the system.<br/>2.Users doesn't get authorization<br/>    2.1 When system find illegal record in users' forum history,system will ban users operation.<br/>3.Users exit the forum or logout while editing the comment content in step 5<br/>    show notification:"You are still editing your comment,do you really want to exit?"<br/>4.Club union supervisor detect the content of users' column<br/>    4.1 if users' comment cause bad social influence and is reported by other users<br/>          -club union supervisor delete illegal content.<br/>          -when caused severe social influence,Club union supervisor update illegal record to the system,<br>          -then the system will ban users' operation of using the forum. |
   | Post-condition   | None.                                                        |

   Use Case: Report Inappropriate Comments or Columns

   | Use Case         | Report Inappropriate Comments or Columns                     |
   | ---------------- | ------------------------------------------------------------ |
   | ID               | UC16                                                         |
   | Specification    | User decide the comments or columns that may cause bad social influence,report them with proper report reasons<br/>Club union supervisor handle the report request from users,reject the report or delete illegal content and record the sender's account. |
   | Actors           | **User,Club Union Supervisor**                               |
   | Pre-condition    | Users successfully login.                                    |
   | Basic Path       | 1.include(check reports)<br/>2.Users see inappropriate comments or columns.<br/>3.Users click "report" button.<br/>4.Users input report reasons<br/>5.Users send report request to club union supervisor.<br/>6.Club Union supervisor check report content and react to the report.<br/>    6.1 if club union supervisor confirm the report,delete the illegal content,and send the illegal account to Administrator<br/>    6.2 otherwise,reject the report,the content of the column or column remains.<br/>7.Club union supervisor send results to the users who report the content. |
   | Alternative Path | 1.Users exit the system.<br/>2.Users log out or return while editing the report reason.<br/>    show notification:"You are still editing your report reason,do you really want to exit?" |
   | Post-condition   | Users successfully report,and get report results from the club union supervisor. |

<div STYLE="page-break-after: always;"></div>
### 3.3 Activity Diagrams

- **Resign**
The club leader submits the application for resignation in the system and Club Union Supervisor reviews the application. After the application is approved, the system will modify the leader's authority to ordinary membership. The club information will be modified too. Leaders who have submitted applications can also withdraw their applications before Club Union Supervisor reviews them.

	![cc3nxJ.jpg](https://z3.ax1x.com/2021/04/14/cc3nxJ.jpg)

- **Apply for leadership**
The club member submits the application for leadership in the system and Club Union Supervisor reviews the application. After the application is approved, the system will modify the member's authority to leadership. The club information will be modified too. Members who have submitted applications can also withdraw their applications before Club Union Supervisor reviews them.

	![cc1j58.jpg](https://z3.ax1x.com/2021/04/14/cc1j58.jpg)

- **Establish a new club**
The user submits the application for establishing a new club in the system and Club Union Supervisor reviews the application. After the application is approved, the system will build a new club and modify the applicant's authority to the leader of the club. Users who have submitted applications can also withdraw their applications before Club Union Supervisor reviews them.

	![cc3Prn.jpg](https://z3.ax1x.com/2021/04/14/cc3Prn.jpg)

- **Alter Club Information**
The leader submits an application to modify the community information in the system and Club Union Supervisor reviews the application. After the application is approved, the system will modify the club information. Leaders who have submitted applications can also withdraw their applications before Club Union Supervisor reviews them.

	![cc1XUf.jpg](https://z3.ax1x.com/2021/04/14/cc1XUf.jpg)

- **Login in**
According to the user registration information, the system identifies the identity of visitors,  and provides visitors with the required page.

	![cc3E5T.jpg](https://z3.ax1x.com/2021/04/14/cc3E5T.jpg)

- **Register**
The visitor fills in the registration information, and the system sends a verification code after verifying the information. After receiving the verification code, the visitors filling the form and the system checks whether the code is entirely correct. If so, the system saves the information and activates the visitor's authority.

	![cc3m24.jpg](https://z3.ax1x.com/2021/04/14/cc3m24.jpg)

- **Organize Activities**
Club Leaders apply for activities based on the actual situation. First, log in to the activities page of the club exchange platform to fill in the application form, and then submit the application to the club management department. Club Union Supervisor will review the application after accepting the application. If the activity application is rejected, the corresponding reasons and comments will be given. If the activity review is passed, club union supervisor will collect an activity push from the head of the club, and then publish the activity information in the promotion section after review. The user can apply to participate in the activity by browsing the activity information. The members of the activity carrying out club can also choose to be the activity volunteer to help carry out the activity. Club Leaders will review the application according to the actual situation. If the application is rejected, the corresponding reason will be given. If they agree, it will be released to contact and wait for the activity to proceed smoothly.

	![cc3ZPU.jpg](https://z3.ax1x.com/2021/04/14/cc3ZPU.jpg)

<div STYLE="page-break-after: always;"></div>
## 4.Supplementary Specification

### 4.1 Objectives
The purpose of this document is to define requirements of the Club Communication System. This Supplementary Specification lists the requirements that are not readily captured in the use cases of the use case model. The Supplementary Specifications and the use-case model together capture a complete set of requirements on the system.

### 4.2 Performance
- The system must be able to process at least 100 requests concurrently
- The system must respond to each request within one second
- The system must support more than 50,000 ordinary users and 100,000 tourists at the same time

### 4.3 Reliability
Not considering network failing, the system must fail for no more than 2 hours per year, and the goal is 1 hour per year. It also notes that there should be less than 100 bugs per 10K lines of code during integration and testing.

Specially, the system must be 100% operational in 99.9% of the calendar year during some special time in a year(like Community Culture Festival).

### 4.4 Security
- The security of the system includes authentication, access control, data integrity and data privacy. 
- The system has a centralized database and will not allow inventory data or other important data to be stored outside of its servers. Also, this system assumes that only the user or whoever he/she allows will have access to his/her user interface.
- Users must be authenticated with a user name and password. 
- Sensitive information should be stored in the database with strong encryption algorithm, and transmission information should be encrypted to protect privacy.

### 4.5 Maintainability
- In case of system error, operation and maintenance personnel can diagnose and solve the problem within 1 hour.
- The system should be easy to expand, and the code should be conducive to the realization of new functions.
- The system should back up data regularly.
- The system should be able to go back to the previous version within 2 hours.

### 4.6 Comprehensibility
The text and buttons in the GUI should be friendly for teachers and students.

### 4.7 Design constraints
The system shall provide Web pages that can run on multiple platforms.

<div STYLE="page-break-after: always;"></div>
## 5.Mock-up UI

The user interfaces of the JIYU(Meet what you will meet) communication system and application shall be friendly to users. The user interface design shows as follow:

### 5.1 Login In

Visitors (Users who have not logged in to the system) can log in on this interface.

![cc3AaV.jpg](https://z3.ax1x.com/2021/04/14/cc3AaV.jpg)

### 5.2 Club Exploration

Users can view a variety of clubs in the current interface, and choose the clubs they are interested in to join.

![cc3pvj.jpg](https://z3.ax1x.com/2021/04/14/cc3pvj.jpg)

### 5.3 Club Forum

Users can participate in discussions with other users in the current section.

![cc3ibq.jpg](https://z3.ax1x.com/2021/04/14/cc3ibq.jpg)

### 5.4 Club Statistics

The Club Leaders can view the relevant data of the community on this interface, so as to provide help for the future development of the community.

![cc1xPS.jpg](https://z3.ax1x.com/2021/04/14/cc1xPS.jpg)

### 5.5 Club Information Modification

The Club Leaders can modify the relevant information of the community in the current interface.

![cc3CKs.jpg](https://z3.ax1x.com/2021/04/14/cc3CKs.jpg)

### 5.6 Member Arrangement

The Club Leaders can conveniently view and manage the members of the community in the current interface.

![cc3eGF.jpg](https://z3.ax1x.com/2021/04/14/cc3eGF.jpg)

### 5.7 Activity Arrangement

The Club Leaders can view the ongoing or past activities of the club on the current interface.

![cc1z8g.jpg](https://z3.ax1x.com/2021/04/14/cc1z8g.jpg)

### 5.8 Activity Apply

The Club Leaders can apply for a new activity on the current interface, which will be reviewed by the Club Union Supervisor.

![cc3S2Q.jpg](https://z3.ax1x.com/2021/04/14/cc3S2Q.jpg)

<div STYLE="page-break-after: always;"></div>
## 6.TOWS Strategic Matrix

Through OTWS strategic matrix analysis, we can further master the advantages and disadvantages of the system, combined with the opportunities and threats of the external market and the system analysis idea to formulate corresponding strategies for the next stage of system improvement and realization, avoid risks and develop advantages.

![ccGVc4.png](https://z3.ax1x.com/2021/04/14/ccGVc4.png)

## 7.References

[1] Tan Yunjie. (2012). Elephant: Thinking in UML. Beijing: China Water Conservancy and Hydropower Press.

This book consists of four parts. The first part introduces the basic concepts of object-oriented analysis and basic modeling knowledge; the second part organizes and summarizes the basic concepts of UML; the third part explains how to use UML to implement a project through an example; the fourth part discusses common problems in the application And to be discussed in depth.

[2] Radosław Klimek and Piotr Szwed. Formal Analysis Of Use Case Diagrams[J]. Computer Science, 2010, 11

The paper refers to the formal analysis of the use case diagrams. A formal model of use cases is proposed and its construction for typical relationships between use cases is described. The use case diagrams construction of the document refers to this article.

[3] Evans, Andy, etal. "The UML as a Formal Modeling Notation." 19.7(2014):336- 348. 

This article gives a precise definition and statement of UML, which uses formal specification techniques to explain in depth the semantics of UML symbols and diagrams, and describes the road map of this method. Refer to this paper for the semantics of symbols and diagrams in the document.

## 8.Contributions

This system analysis project has been discussed for four times. In the process of completing this task, all team members actively participate in the discussion and strive to complete their own tasks. Team members cooperate harmoniously, communicate and solve problems in time. The division of labor within the group was average and clear, as follows:

$i$. **Brief Introduction**:
The brief introduction is written by Ningyu Xiang.

$ii$. **Introduction**:
The introduction is written by Ningyu Xiang and Kaixin Chen.

$iii$. **Agile Analysis**:
The analysis about agility is carried out by Liyou Wang and Zhongyue Chen, and finally summarized by Liyou Wang. 

$iv$. **Use Case Diagram**:
All members in group participate in designing and drawing use case diagram, and the use case diagram  is finally summarized by Kaixin Chen.

$v$. **Use Case Specification**:
All members in group participate in completing the use case specification.

$vi$. **Activity Diagram**:
All members in group participate in designing and drawing activity diagram, and the activity diagram is finally summarized by Zhongyue Chen.

$vii$. **Glossary of Terms**:
All members in group participate in completing the glossary of terms.

$viii$. **Mock-up UI**:
The user interface is designed and drawn by Mingjie Wang.

$ix$. **Document**:
The document is integrated and beautified by Ningyu Xiang.


|Student Number|Name|Score Weight|
|---|---|---|
|1851055|Mingjie Wang|100%|
|1954098|Ningyu Xiang|100%|
|1951724|Kaixin Chen|100%|
|1851049| Zhongyue Chen |100%|
|1851231| Liyou Wang    |100%|
