Step 4: I typed in `ssh` then copied and pasted `cs15lwi23ahv@ieng6.ucsd.edu` from notion using <Command> <V> and pressed <Enter>. This prompted a password. 
Then I typed in my password and pressed <Enter>. This brought up details of my login. 
<img src= "15L/Screen Shot 2023-02-26 at 10.58.26 PM.png" width="600" height="600">

Step 5: I typed git clone into the terminal then used <Command> <V> to paste the link to the terminal and pressed `<Enter>`.
<img src= "15L/Screen Shot 2023-02-26 at 11.06.19 PM.png">

Step 6: I typed `cd lab7` to change into the directory then pressed `<Enter>`.
I typed in `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *java` and pressed enter to compile.
Then I typed in `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` to run the tests from ListExamplesTests. These tests failed because of an issue in the `ListExamples.java` file
  
<img src= "15L/Screen Shot 2023-02-26 at 11.10.30 PM.png">

  
Step 7: Typed in `nano ListExamples.java` and pressed `<enter>` to open up the file and edit it. 

Keys pressed `<down> <down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down><down> <right><right><right><right><right><right><right><right><right><right><right><right><delete> <2> <control><o><cntrl><o><enter><cntrl><x>` This combination of keys allows me to go down to the incorrect line and change "1" to "2" then save the file. 
  
<img src= "15L/Screen Shot 2023-02-27 at 4.38.39 PM.png">

Step 8: I had to recompile the file and run the tests again. To do this I just went 3 lines up and copied the same commands. 
  Keys pressed: `<Up><Up><Up><enter> <Up><Up><Up><enter>`
<img src= "15L/Screen Shot 2023-02-26 at 11.38.12 PM.png">
  
Step 9: I typed `git add ListExamples.java` then pressed enter to add changes made to the file to the staging area before it can be committed. Then I typed in `git commit -m "Committed to main"` and pressed enter to save these changes. 
Finally, I had to type `git push origin main` to commit the saved changes to the main origin repository. 
<img src= "15L/Screen Shot 2023-02-26 at 11.52.30 PM.png"> 
