# Lab Report 5

I have picked Lab report 3 as my favorite and have chosen to go back and explore a different command and command-line options for that command.

I have chosen the `find` command for this task.

Option 1: `-type` This option is used to search for files based on their type.
[Source](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

Example 1:
```find travel_guides -type d```
This command searches for all directories inside the travel_guides directory.

Output:
```
travel_guides
travel_guides/berlitz1
travel_guides/berlitz2
```

Example 2:
```find travel_guides -type f```
This command searches for all files in the travel_guides directory.

Output:
```
travel_guides/berlitz1/HandRLasVegas.txt
travel_guides/berlitz1/HistoryJapan.txt
travel_guides/berlitz1/IntroMalaysia.txt
travel_guides/berlitz1/HandRIstanbul.txt
travel_guides/berlitz1/HistoryJamaica.txt
travel_guides/berlitz1/HandRJamaica.txt
travel_guides/berlitz1/HandRHongKong.txt
```
and some more...


Option 2: `-exec` This option allows you to execute a command on each file that matches your search criteria. 
[Source](https://www.linuxtoday.com/developer/35-practical-examples-of-linux-find-command-3/)

Example 1: Count the number of lines in each .txt file in the travel_guides folder, you can use this command:

```find travel_guides -name "*.txt" -type f -exec wc -l {} \;```

This outputs the following:
```
     251 travel_guides/berlitz1/HistoryJamaica.txt
     379 travel_guides/berlitz1/HandRJamaica.txt
     29 travel_guides/berlitz1/HandRHongKong.txt
     264 travel_guides/berlitz1/HistoryEgypt.txt
     139 travel_guides/berlitz1/IntroEdinburgh.txt
     244 travel_guides/berlitz1/HistoryIsrael.txt
     119 travel_guides/berlitz1/IntroDublin.txt
     792 travel_guides/berlitz1/HistoryIndia.txt
     161 travel_guides/berlitz1/IntroFrance.txt
```
Example 2: Find all the files with the extension ".txt" and search for the string "puppetry" within them:

```find travel_guides  -type f -name "*.txt" -exec grep "puppetry" {} \;```

Output:
```
To see snatches of China’s traditional performing arts in a setting appropriate for an imperial banquet, try one of Beijing’s special teahouses. At these intimate dinner theaters, decorated in Qing Dynasty fashion (carved wood trim, paper lanterns, and red columns), customers can enjoy local snacks or full Chinese meals at their tables while viewing a variety of acts on stage, including opera highlights, acrobatics, magic shows, ethnic dancing, puppetry, storytelling, and comedy.
```

Option 3: `-size`: This option allows you to find files that match a certain size criterion. 
[Source](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)

Example 1: Find all files in travel_guides that are larger than 1 kB
```find travel_guides  -size +1k```

The output will look like this:
```
travel_guides/berlitz1/HistoryHawaii.txt
travel_guides/berlitz1/WhatToFrance.txt
travel_guides/berlitz1/WhereToEgypt.txt
travel_guides/berlitz1/WhereToEdinburgh.txt
travel_guides/berlitz1/WhatToIsrael.txt
travel_guides/berlitz1/HandRLosAngeles.txt
travel_guides/berlitz1/HistoryMadeira.txt
travel_guides/berlitz1/IntroJerusalem.txt
```

Example 2: find all files in travel_guides that are smaller than 1 MB and print their sizes in human-readable format. You can use this command:

```find travel_guides -size -1M -printf "%p %s\n"```
This will output something like this:

```
travel_guides/berlitz1/WhereToEdinburgh.txt
travel_guides/berlitz1/WhatToIsrael.txt
travel_guides/berlitz1/HandRLosAngeles.txt
travel_guides/berlitz1/HistoryMadeira.txt
travel_guides/berlitz1/IntroJerusalem.txt
```

Option 4: Find all files in a directory modified within a specific time period. 
[Source](https://www.tecmint.com/35-practical-examples-of-linux-find-command/)

Example 1: find all the files which are modified less than 100 days ago.
```find travel_guides -mtime -100```

Output: 
```
travel_guides/berlitz1/IntroJamaica.txt
travel_guides/berlitz1/IntroGreek.txt
travel_guides/berlitz1/HandRIsrael.txt
travel_guides/berlitz1/WhatToEdinburgh.txt
travel_guides/berlitz1/WhereToMadeira.txt
travel_guides/berlitz1/WhatToGreek.txt
travel_guides/berlitz1/HandRLakeDistrict.txt
travel_guides/berlitz1/WhereToIbiza.txt
travel_guides/berlitz1/WhereToHawaii.txt
travel_guides/berlitz1/HandRMadrid.txt
travel_guides/berlitz1/HistoryMalaysia.txt
travel_guides/berlitz1/IntroItaly.txt
```

Example 2: find all the files which are modified more than 10 days ago.
```find travel_guides -mtime +10```

Output: 
```
travel_guides/berlitz1/IntroEdinburgh.txt
travel_guides/berlitz1/HistoryIsrael.txt
travel_guides/berlitz1/IntroDublin.txt
travel_guides/berlitz1/HistoryIndia.txt
travel_guides/berlitz1/IntroFrance.txt
travel_guides/berlitz1/IntroMadeira.txt
travel_guides/berlitz1/WhatToLakeDistrict.txt
travel_guides/berlitz1/IntroIbiza.txt
travel_guides/berlitz1/HistoryItaly.txt
travel_guides/berlitz1/WhereToGreek.txt
```
