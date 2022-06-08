Introduction - Thomas
- Introduce group members
- Introduce what the project is (why do we need supercharged cowrie? What benefits does it provide etc)
- Introduce what will be discussed in the presentation
- Minimum Viable Product discussion (mentioning but not in depth about why we choose the commands)






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





POC - Sridhar

- From the perspective of an attacker, I start with the attacker logged into Cowrie
- I then introduce the ability of the attacker to summon a text editing environment - by simply typing in Nano
- This will open up a blank text environment as no file has been opened with it
- I then will show the attacker putting in the command 'nano' but this time along with a filename
- This will open up the text environment with the necessary content of the file the user chooses
- Our POC is just simply demonstrating the ability to open a text editing environment within Cowrie.




Conclusion - Lucy
