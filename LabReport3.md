# Lab Report 3

I have chosen the `grep` command for this task.

Option #1 `grep -r`: This option performs a recursive search. It searches for the pattern in all files under the specified directory recursively.

```
grep -r "hello"
```
This command searches for all occurences of the word Hotdog in the directory "dir1"
Output:
```
./travel_guides/berlitz1/WhereToItaly.txt:        (or Ca’ Grande), while gondoliers claim Othello’s Desdemona lived in
./travel_guides/berlitz1/WhereToHongKong.txt:        the local people smile “hello” and, if you’re lucky, point you to a
```

```
grep -r "Volcano"
```
This command searches for all occurences of the word Hotdog in the directory "dir1"
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
grep -w "museum"
```
This command searches for all occurences of the word Hotdog in the directory "dir1"
Output:
```

```

```
grep -w ""
```
This command searches for all occurences of the word Hotdog in the directory "dir1"
Output:
```

```




Option #3 `grep -i`: This option performs a case-insensitive search. It ignores case distinctions when searching for the pattern in the input text.
```
grep -i "pericles" travel_guides/berlitz2/*
```
This command searches for 
Output:
```
travel_guides/berlitz2/Athens-History.txt:The moving power behind this unrivaled time of greatness, which has come to be known as the Golden Age, was Pericles. This liberal-inclined aristocrat was, in effect, the supreme ruler of Athens and its empire for 30 years until his death in 429 b.c.
```

```
grep -i "nusa" travel_guides/berlitz2/*
```

```
travel_guides/berlitz2/Bali-History.txt:In the decades following, the economy stabilized as growing oil revenues fueled expansion. The Chinese community, backbone of the nation’s economy, carefully rebuilt its commercial interests, this time much less visibly. Tourism to Bali was seen as a money-spinner: the 1970s saw a rapid increase in the numbers of foreign visitors. During the 1980s, the authorities decided to develop a more up-market tourism on Bali. Nusa Dua was designated to become a huge tourist enclave where only large, luxury hotels would be built.
```

Option #4 `grep -v`: This option inverts the match. It displays only the lines that do not match the pattern.
```
grep -v
```
This command searches for
Output:
```

```
