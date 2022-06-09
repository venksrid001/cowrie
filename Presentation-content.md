Introduction - Thomas

Good evening/good morning/ good afternoon, we are ENGR301 Group 3 and today we will be discussing our project, supercharged cowrie. 
My group members, Selby, Shruti, Deepika, Srid, Lucy and I (Thomas) will be discussing to you about the scope of our project, the what, why and how of the project, the project timeline, sprint planning, proof of concept and a brief conclusion to wrap things up.

So, Scope! Like any project, we must define a scope. Scope is extremely important, it helps us, as a team, plan out potential risks, design constraints, scheduling, budgeting, health, and safety and so on. Scope is also extremely helpful for you! Our client and stakeholder(s), this is because it helps provide clarity on what you expect us to create, this help prevents things such as feature creep, where we just add way too much, or a swing in the opposite direction, failure to meet your design due to a lack of features. One way to define scope is having a clear Minimum Viable Product.

The process of creating a Minimum Viable Product starts with a set of specifications provided by you guys, our client and stakeholder(s). From there, after numerous meetings, we form a Minimum Viable Product based on those specifications. Based off the agreed Minimum Viable Product, we now have a shared scope in what we all want the final outcome to roughly resemble and prevent that feature creep and lack of features I discussed earlier. In the case of our project, our main two specifications for our Minimum Viable Product are implementing the text editor nano and implementing the locate command. 

After defining the scope, of course comes the fun part! The details! After all the devil is in the detail. The next presenter Selby will be delving further in detail of the importance and justifications for each of these specifications, and why they are even needed in the first place.

Importance - Selby (Draft presentation)

Why are these commands important?
The short answer is:
To increase Cowries level of interaction.
The long answer is:
Cowrie is designed around 3 ideas, to detect attackers in a network, Capture malware and malicious files for analysis and to research attacker habits.
To do this successfully a honeypot must be enticing to an attacker and act in an expected manner.
Cowrie is marketed as a medium to high interaction honeypot, however it is still missing a few unix-based commands. For Cowrie to be successful, it needs to have all the programs and tools that attackers expect to see and use.
If a common command has an unexpected result or is missing all together, an attacker may get suspicious about the system they have infiltrated. If the commands work as expected attackers may believe they are on a legitimate system and stick around to try and exploit it further. 
With all this in mind, we chose the Nano text editor and the locate command to increase the level of interaction within Cowrie. Nano is a common text editor that attackers like to use to read and write files within the environment. As Cowrie is missing a basic text editor this can be a big flag for attackers. 
Locate is a common command that can be used to quickly find directories and files within a system. It is faster then the find command and can be useful when looking for a particular file that an attacker knows exists. 
 Both of these functions increase the level of interaction between the honeypot and the attacker. The more interaction an attacker has with Cowrie the more information can be gathered for future research. 
Shruti will go into more technical details of how these will be implemented.



How we'll implement - Shruti

How do we plan on actually doing the project? 
The current implementation of cowrie is in python, therefore we will be continuing the development in python also.
To implement our 2 commands, locate and nano, we will be breaking them down into smaller functions and then we will be splitting up the team into groups of 2 to cover each function. By working programming in pairs we can have one person writing the code and one person testing. 
As stated previously by thomas, our main focus will be implementing nano on cowrie 
This will involve opening up an editor when nano is typed. 
 -This includes opening a blank file or opening an existing file.
The attacker can then type anything into the editor.
We will also be implementing the other usual features you would see in an editor. Such as cut, paste, replace, and find using keyboard shortcuts. This will make the honeypot more realistic and increase deception to the attacker.
Another function we will include in the editor will be saving. When control o is pressed: the attacker can save a new file, save an existing file or rename the file (save as)
And finally, to exit the editor, the attacker will be asked if they want to save their file before exiting and they will be returned back to the terminal when they press control x.
The locate command will be a lot simpler than the editor.  The functions for this command will include a string search that goes through the file system and an output function that will print the file name and the absolute path to the file. 
Each of these functions will be done in fortnightly sprints and which will give us the chance to make small developments on prototypes of functional features and will also allow us to constantly provide updates and present these developments to the you (client) and the rest of the team. Deepika will talk more in detail about our sprint plan.
You will then have an opportunity to clarify and voice any feedback or opinions ypu may have so that changes can be made on prototypes early on to ensure we still meet our deadlines and deliver you the product you requested.


Timeline - Deepika

Hi everyone, I am Deepika. My team mates already explained about the technical part. Now, I am going to talk about delivery part, which is divided into Timeline, Sprint Planning and Task Division.
Super Charge cowrie project is started in Trimester-1and it will be delivered in Trimester-2. Here is the agreed timeline with the client for the delivery in different phases.

Architectural Prototype will be delivered by 31st July 2022, followed by MVP on 19th August 2022 and Final release by 1st October 2022. At the end, final presentation will be presented on 10th Oct 2022.
Now, I am going to walk through the sprint planning with their objectives. We have already completed Sprint 0 and Sprint 1 in this trimester and rest will be focused on next trimer which will start at 11th July 2022. In the next Trimester, we have planned for 5 sprints, from Sprint 2 to Sprint 6. However, each spring size is for 2 weeks, but we have tweaked couple of sprints due to mid term break and final exams.

Sprint 2 is starting on 11th July and ends on 25th July 2022, in this sprint, we will get up and running Cowrie Project and get ready Architecture Prototype for review. In the next sprint, we have delivery for the Architecture Prototype on 31st July and we will start working on the MVP. Spring 4 is bit shorter dule to mid term break by 2 days and we will get deliver MVP by the end of this sprint. After the break in Sprint 5, we will start working on the features for locate command and nano text editor. In the last sprint 6, we will deliver final product.
In the last sprint, we planned for the user stories to be delivered for the whole project. We have created these as issues in the GitLab as shown in the screenshot. Let’s have a closer look at the GitLab issues. We have created 2 Epics – one for nano editor and another one for locate command. We have six teammates in our project, and we have created 3 teams with 2 members in each team. We have labelled few users stories for these teams and agreed on who is going to work on which user story. 

We have final delivery for project on 10th Oct 2022.
 

POC - Sridhar

From the perspective of an attacker logged into the Cowrie environment he/she will need some CLI text editor to edit their scripts, hence they insert a command named 'nano', along with a filename to open the environment.

Since this file has not been created yet, this will open up a blank canvas, for the user to roam around and add their changes when necessary. Most likely we would like to customize the environment to properly emulate the environment that nano provides.

When the user has completed or finished making their necessary changes to the file, they can press CTRL+X to save their progress in the file. 

In our POC, we also allow users to open previously edited files such as in this case. Where an attacker can access their created script just by simply inserting the same command 'nano' along with the file of their choosing. As we see here the file opened with the original content that the attacker last saved it with. 

Through our POC, we have demonstrated that our text editor, already has saving and opening file capabilities, the next step would be to place this code and have it properly working in the Cowrie environment. This a current indication of our progress thus far, and to summate what we have discussed in this presentation, I will hand it over to Lucy to conclude things. 




Conclusion - Lucy
