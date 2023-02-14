# Lab Report 3

I have chosen the `grep` command for this task.

Option #1 `grep -r`: This option performs a recursive search. It searches for the pattern in all files under the specified directory recursively.

```
grep -r "hello"
```
This command searches for all occurences of the word "hello" in the directory "written_2"
Output:
```
./travel_guides/berlitz1/WhereToItaly.txt:        (or Ca’ Grande), while gondoliers claim Othello’s Desdemona lived in
./travel_guides/berlitz1/WhereToHongKong.txt:        the local people smile “hello” and, if you’re lucky, point you to a
```

```
grep -r "Volcano"
```
This command searches for all occurences of the word "Volcano" in the directory "written_2"
Output:
```
./travel_guides/berlitz1/IntroFWI.txt:        steep hills and rolling plains. Volcanoes, hummingbirds, mangroves,
./travel_guides/berlitz1/WhereToHawaii.txt:        Volcanoes National Park has active lava flows flowing to
./travel_guides/berlitz1/HandRHawaii.txt:        Chalet Kilauea $$–$$$ P.O. Box 998, Volcano, HI 96785; Tel.
./travel_guides/berlitz1/HandRHawaii.txt:        of bed & breakfast accommodations in the Volcano area. They have
./travel_guides/berlitz1/WhereToFWI.txt:        Vacillating Volcano
./travel_guides/berlitz1/WhereToFWI.txt:        Saint-Pierre and the Volcano
```


Option #2 `grep -w`: This option matches only whole words. It searches for the pattern only when it forms a whole word.
```
grep -w "creative" travel_guides/berlitz2/*
```
This command searches for all occurences of the whole word "creative" in the directory "travel_guides/berlitz2/*".
Output:
```
travel_guides/berlitz2/Algarve-WhatToDo.txt:Art. The lure of the city for creative people has existed for centuries and modern artists follow in the wake of Rembrandt and the Dutch masters.
```

```
grep -w "protest" travel_guides/berlitz2/*
```
This command searches for all occurences of the whole word "protest" in the directory "travel_guides/berlitz2/*"
Output:
```
travel_guides/berlitz2/Algarve-WhereToGo.txt:Sagres’s connections to the sea, and Portugal’s maritime exploits, are strong. Prince Henry the Navigator established his Navigation School here (though some protest that it was farther east, near Lagos).
```


Option #3 `grep -i`: This option performs a case-insensitive search. It ignores case distinctions when searching for the pattern in the input text.
```
grep -i "pericles" travel_guides/berlitz2/*
```
This command searches for "pericles" in upper or lowercase in the directory travel_guides/berlitz2. 
Output:
```
travel_guides/berlitz2/Athens-History.txt:The moving power behind this unrivaled time of greatness, which has come to be known as the Golden Age, was Pericles. This liberal-inclined aristocrat was, in effect, the supreme ruler of Athens and its empire for 30 years until his death in 429 b.c.
```

```
grep -i "nusa" travel_guides/berlitz2/*
```
This command searches for "nusa" in upper or lowercase in the directory travel_guides/berlitz2. 
Output:
```
travel_guides/berlitz2/Bali-History.txt:In the decades following, the economy stabilized as growing oil revenues fueled expansion. The Chinese community, backbone of the nation’s economy, carefully rebuilt its commercial interests, this time much less visibly. Tourism to Bali was seen as a money-spinner: the 1970s saw a rapid increase in the numbers of foreign visitors. During the 1980s, the authorities decided to develop a more up-market tourism on Bali. Nusa Dua was designated to become a huge tourist enclave where only large, luxury hotels would be built.
```

Option #4 `grep -c`: This option counts the number of times the pattern occurs in the input text and displays the count for each file.
```
grep -c "the" travel_guides/berlitz2/Amsterdam-Intro.txt
```
This command counts how many times the word appeared in the text Amsterdam-Intro.txt
Output:
```
13
```

```
grep -c "and" travel_guides/berlitz2/Athens-Intro.txt
```
This command counts how many times the word appeared in the text Athens-Intro.txt
Output:
```
14
```
