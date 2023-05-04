Download Link: https://assignmentchef.com/product/solved-csci251-assignment-2
<br>
In a theoretical flat-land universe, everything is in 2 dimensions. People, animals, plants to planets, moons, galaxies and even space itself, is in 2D, In our flat-land space (i.e. ‘flat-space’), there is a powerful organization called 2D-StarFleet (2DSF), whose goals include seeking out new life and civilization via exploration.

While on a routine mission of exploration, the flagship of 2DSF, the Enterprise-2D is trapped in an expanse of space encircled by a massive ring of violent, electrical plasma storm. Data coming in from the sensor array reveals that the only opening in this storm is located at the far end of the enclosed area, from Enterprise-2D’s current location

In addition, the sensor data also revealed that this area is populated by strange, 2D geometrical shapes, with sizes ranging from a small moon, asteroid, to large planets, or even a star! This implies that to travel to the ‘exit’ at the far end of the storm, you need to understand more about the properties of these shapes and attempt to chart a course to navigate to the exit!

As a Science Officer aboard Enterprise-2D, you need to develop a program that has the following capabilities:

a) read in sensor data on the strange 2D shapes (via manual input)

b) compute the area (‘mass’) of these shapes

c) print shapes report (e.g. list of points: on its perimeter, or totally within shape’s area)

d) sort shapes data (sorted by special type and area)

The next section provides information about the requirements for developing this program.

Task Requirements

A) In terms of relative positioning, you may assume a coordinate system with Enterprise-2D at the origin, trying to navigate in a general ‘upper-right’ direction, to get to the exit in the storm. Please refer to Appendix A, which elaborates on this coordinate system and the unit representation of 2D shapes.

IMPORTANT : For this assignment, you should not assume that the 2D shapes in Appendix A are positioned exactly as shown in Appendix A, nor that there are not more shapes. There will, however, only be shapes of the types listed in Appendix B

B) The sensor data coming in from Enterprise-2D’s sensor array provides crucial information about the 2D shapes such as name, special type and location of all vertices (that outlines the perimeter of the shape). Please refer to Appendix B, which provides a more detailed description of the sensor data.

C) To assist you in the initial class design of your program, please refer to Appendix C, which illustrates one possible way of designing your program. It also describes a list of requirements which you need to implement, especially those marked under “compulsory”. The classes highlighted in Appendix C are purely meant to store data about the 2D shapes entered into your program by user.

D) You are required to implement a main driver class called ‘Assn2’, whose methods are called to start the program. When started, it should print a menu providing the following functionalities :

· read in sensor data on the strange 2D shapes (via manual input)

· compute the area (‘mass’) of these shapes

· print shapes report (e.g. list of points on its perimeter, or totally within shapes area)

· sort shapes data (sorted by special type and area)

Appendix D provides more information about implementing this class.

E) Once the program is completed and tested to be working successfully, you are highly encouraged to add on “new features” to the program that you feel are relevant to the problem. Additional marks may be awarded subject to the relevancy and correctness of the new functionalities.

F) You are to use only C++ language to develop your program. There is no restriction on the IDE as long as your source files can be compiled by g++ compiler (that comes packaged in Ubuntu linux) and executed in the Ubuntu terminal shell environment.

Deliverables

1) The deliverables include the following:

a) The actual working C++ program (soft copy), with comments on each file, function or block of code to help the tutor understand its purpose.

2) IMPT: Please follow closely, to the submission instructions in Appendix E, which contains details about what to submit, file naming conventions, when to submit, where to submit, etc.

3) The evaluation will be held during lab session where you are supposed to submit your assignment. Some time will be allocated for you to present / demonstrate your program during the session.

Grading

Student’s deliverable will be graded according to the following criteria:

(i) Program fulfills all the basic requirements stipulated by the assignment

(ii) Successful demonstration of a working program, clarity of presentation and satisfactory answers provided during Q &amp; A session.

(iii) Additional effort (e.g. enhancing the program with relevant features over and above task requirements, impressive, ‘killer’ presentation, etc)

(iv) After the submission of deliverables, students will be required undergo an evaluation process (to determine fulfillment of task requirements.) Further instructions will be given by the Tutor during the subsequent respective labs. Please pay attention as failure to adhere to instructions may result in deduction of marks.APPENDIX A

(Coordinate System w.r.t. Enterprise-2D, and the plasma storm)

Enterprise-2D is trapped in this huge ring of electrical plasma storm. The only opening to exit this storm is located in the far ‘upper-right’ of the coordinate system, for e.g. at Point2D (14, 14) !

APPENDIX B(Description of Sensor Data)

Name

The name of the 2D shape reveals the general type of shape encountered. Currently, the values consist of : “Square”, “Rectangle” and “Cross”.

Special Type

Enterprise-2D’s sensor has detected that some shapes encloses a ‘warp-space’ with the amazing ability to teleport any objects that touches one of its vertex, to any other vertices of the same shape, instantaneously !

This makes it highly desirable, for Enterprise-2D to travel towards this kind of shape, in the hopes of travelling faster, and saving precious fuel at the same time!

There are only 2 values for ‘special type’ : “WS” (Warp-Space) or “NS” (Normal-Space).

Vertices

The vertices is actually a set of (x, y) points, that describes the outline of the 2D shape. The number of points in the set, depends on the name of the shape. The table below summarizes the kind of sensor data your program expects to receive.

NameSpecial TypeNo. of Vertices (i.e. x, y, points)Actual Vertex Data …“Cross”“WS” or “NS”12e.g. (1, 3), (1, 4), … etc.“Square”“WS” or “NS”4

“Rectangle”“WS” or “NS”4

Note :

As mentioned in the Background section, the 1st capability of your program should allow manual input of the above data.

It is not necessary to prompt user for “No. of Vertices” because the name of the shape will already inform your program about how much vertex data to expect.

For example, when your program prompt for name of the shape, if user enters “Cross”, it is safe for your program to assume that user is going to key a set of 12 (x, y) points later!

APPENDIX C

(Implementation Requirements)

Compulsory requirements

#1 The parent class is ‘ShapeTwoD’. Any attributes, constructors and methods specified in the diagram must be implemented, with the exact same name, parameter, type and access!

#2 The sub-classes of ShapeTwoD must be named ‘Cross’, ‘Square‘ and ‘Rectangle‘.

#3 The method ‘toString()‘ in class ShapeTwoD is a virtual function that returns a string containing all the values of the attributes in the shape, excluding the array of vertex data. (However, sub-classes of ShapeTwoD must output the array of vertex data, inclusive of any other attribute’s values it inherited)

#4 The method ‘computeArea()’ in class ShapeTwoD is a virtual function. It must be override by the sub-classes and implemented individually.For example, because each sub-class has different number of vertices and values, sub- class Cross’s computeArea() implementation would use a different algorithm / formula from sub-class Square’s computeArea() implementation!Note : The sensor data will only provide the locations (vertices) of each 2D shape encountered. You will be required to do the necessary research to derive the formula to compute the area for each shape, based on the set of vertex data (i,e. a set of [ x, y ] points) provided!

#5 The method ‘isPointInShape()’ in class ShapeTwoD is a virtual function. It takes in a [ x, y ] location and returns a boolean value indicating whether the location is totally within the shape’s area. It must be over-ridden by the sub-classes and implemented individually. (Pls refer to sample output in Appendix D). #6 The method ‘isPointOnShape()’ in class ShapeTwoD is also a virtual function. It takes in a [ x, y ] location and returns a boolean value indicating whether the location is found on any lines joining the shapes’ vertices! It must be over-ridden by the sub- classes and implemented individually. (Pls refer to sample output in Appendix D).

Other requirements

i) For parent class ‘ShapeTwoD’. You are free to add on any additional methods or attributes deemed necessary for your program to provide its services.

ii) Since user will key in the name of the shape, it is possible for you to declare arrays of fixed sizes in the sub-classes to store the coordinate vertices of the shape!

iii) You are free to implement any other additional classes you feel necessary so as to provide the required capabilities for this program.

APPENDIX D

(Implementation info for : Assn2 driver class)

This class contains the main () method which declares and instantiates all other classes (i.e. Shape2D, Square, … etc) and sets up all the necessary interactions to perform its task.

The figure on the left describes a sample interaction between the main menu and ‘Input sensor data’ sub-menuNote :

All shapes data should be stored in a Shape2D array in the Assn2 driver class. You may assume that no more than 100 shapes will be entered into your program at any one time!

The figure on the right describes a sample interaction between the main menu and ‘Compute area (for all records)’ function.

Note : The example assumes the case where there are only 5 shapes input so far, hence, the message that ‘5 records were updated’!

In this compute area function, you must exhibit polymorphic behavior and dynamic binding by invoking the correct function for each shape stored in the Shape2D array !

The figure on the right describes a sample interaction between the main menu and ‘Print shapes report’ function.Notes : The example assumes the case where there has only been 5 sensor data records input so far.

‘Points on perimeter’ refers to only those points lying on the line drawn between 2 vertices, for each pair of vertices defining the shape’s outline.E.g. (1, 2) lies on a line between vertices (1, 1) and (1, 3) !

You do not need to include those points which describe the vertices of the shape!

‘Points within shape’ refers to those points which are totally within the shape.

You do not need to include :– those points which describe the vertices of the shape!

– those points on the perimeter of the shape!

The figure on the right describes a sample interaction between the main menu and ‘Sort shapes data’ sub-menu.

Note : For ‘sort by special type and area’ option in the sub-menu, shapes with special types ‘WS’ should be displayed first, followed by all shapes with special types ‘NS’.Within each group of shapes (i.e. WS or NS), display the shapes in descending order!

APPENDIX E

Submission Instructions (V. IMPT!!)

1) Deliverables

a) All submissions should be in softcopy, unless otherwise instructed

b) For the actual files to be submitted, you typically need to include the following:

– word document report (e.g. *.doc), save as MS Word 97-2003 format

– the source file(s), (e.g. *.h, *.o, or *.cpp files)

– the executable file, compile into an executable file with *.exe

(e.g. Assn2.exe)

2) How to package

Compress all your assignment files into a single zip file. Please use the following naming format :

&lt;FT/PT_Assn2_

Example : FT_Assn2_1234567_JohnDoeAnderson. zip

– &lt;FT/PT Use “FT” for Full-Time student, “PT” if you are Part-Time student

– Assn2 if you are submitting assignment 2, Assn3 if submitting assignment 3 etc.

–

–

3) Where to submit

Please submit your assignment via Moodle eLearning site.

In the event of UNFORSEEN SITUATIONS :

( E.g. Student’s moodle account not ready, cannot login to moodle, eLearning site down on submission day, unable to upload assignment, etc )

Please email your single zip file to your tutor at :

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="650616060c575551100a12251c040d0a0a4b060a08">[email protected]</a> for FULL TIME students

<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="422131212b707276372d35023b232a2d2d6c212d2f">[email protected]</a> for PART TIME students

In your email subject line, type in the following information :

&lt;FT/PT

Example:

To : tutor’s email (see above)

Subject : FT Assn2 1234567 JohnDoeAnderson

Note 1 : The timestamp shown on tutor’s email Inbox will be used to determine if the assignment is late or not.

Note 2 : After email submission, your mailbox’s sent folder would have a copy (record) of your sent email, please do not delete that copy !! It could be used to prove your timely submission, in case the Tutor did not receive your email!

4) When to submit

a) Depending on the time-table, a demo / evaluation for your assignment may be scheduled during the:

– 3rd – 5th lab session for the semester (i.e. lab 3 – 5), for Full Time (FT) students

– 2nd – 4th lab session for the semester (i.e. lab 2 – 4), for Part Time (PT) students

Please consult your tutor for further details. Some time may be allocated for each student to present / explain your system design during the session.

b) Please refer to the following table on the different submission events and deadlines

AssignmentSubmission Deadline

(latest by 2300 hrs)Assignment Evaluation (Tasks), during …Email Evaluation files by :

PTFT123 / 10 / 201626 / 10 / 2016Lab 2(PT), Lab 3(FT)End of Lab 2(PT), Lab 3(FT)201 / 11 / 201602 / 11 / 2016Lab 3(PT), Lab 4(FT)End of Lab 3(PT), Lab 4(FT)313 / 11 / 201615 / 11 / 2016Lab 4(PT), Lab 5(FT)End of Lab 4(PT), Lab 5(FT)

Note: (PT) = Part Time Students, (FT) = Full Time Students !

c) Example #1, for Full Time (FT) students submitting Assignment 1 …

– Submit your zip file to Tutor by 26 / 10 / 2016, 2330 hrs

– Setup your Assn 1 program for evaluation on the date of : Lab 3

– Finish evaluation tasks, email Assn 1 evaluation files by end of : Lab 3

d) Example #2, for Part Time (PT) students submitting Assignment 3 …

– Submit your zip file to Tutor by 13 / 11 / 2016, 2330 hrs

– Setup your Assn 3 program for evaluation on the date of : Lab 4

– Finish evaluation tasks, email Assn 3 evaluation files by end of : Lab 4

5) Please help by paying attention to the following …

! VERY IMPORTANT !

PLEASE FOLLOW THE GUIDELINES IN ALL ASSIGNMENT APPENDICES !!

PLEASE FOLLOW THE SUBMISSION INSTRUCTIONS FROM 1 TO 4 !!

IF YOU ARE NOT SURE,

PLEASE CHECK WITH YOUR TUTOR DURING LABS / LECTURES !

OR …

PLEASE EMAIL YOUR ENQUIRIES TO YOUR TUTOR !

MARKS WILL BE DEDUCTED IF YOU FAIL TO FOLLOW INSTRUCTIONS !!

Example :

· Your report document or zip file does not follow naming convention

· Your email address does not include your name (i.e. cannot be used to identify sender)

· You have no email subject

· Wrong naming or misleading information given

(e.g. putting “Assn2” in email subject, when you are submitting “Assn1”)

(e.g. naming “Assn1” in your zip file, but inside contains Assn2 files )

· Your submission cannot be downloaded and unzipped

· Your report cannot be opened by Microsoft Word 2003

· Your program cannot be re-compiled and/or executable file cannot run

· You email to the WRONG tutor

6) Re-submission administration

After the deadline, (on case-by-case basis), some students / grp may be granted an opportunity for an un-official resubmission by the tutor. If this is so, please adhere to the following instructions carefully:

Zip up for re-submission files according to the following format :

&lt;FT/PT_Assn2_Resubmit_v1_

Example : FT _ Assn2_Resubmit_v1_1234567_JohnDoeAnderson. zip

– &lt;FT/PT Use “FT” for Full-Time student, “PT” if you are Part-Time student

– Assn2 if you are submitting assignment 2, Assn3 if submitting assignment 3 etc.

– Resubmit_v1 if this is your 1st re-submission

– Resubmit_v2 if this is your 2nd re-submission

–

–

– V. IMPT – To prevent Tutor’s Inbox from blowing up in his face, each student is only allowed to re-submit twice, for each assignment only!

Please email your single zip file to your tutor’s email (refer to section 3) – Where to submit)

In your email subject line, type in the following information :

&lt;FT/PT

Example:

To : tutor’s email (refer to section 3) – Where to submit)

Subject : FT Assn2 Resubmit_v1 1234567 JohnDoeAnderson