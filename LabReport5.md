# Lab Report 5

I have picked Lab report 3 as my favorite and have chosen to go back and explore a different command and command-line options for that command.

I have chosen the `find` command for this task.


`exec`: This option allows you to execute a command on each file that matches your search criteria. For example, if you want to count the number of lines in each .txt file in ./written_2, you can use this command:

```find ./written_2 -name "*.txt" -type f -exec wc -l {} \;```

This will output something like this:
```
12 ./written_2/file1.txt
8 ./written_2/file2.txt
10 ./written_2/file3.txt
```
Another example of using -exec is to rename all .jpg files in ./written_2 to .png files. You can use this command:

```find ./written_2 -name "*.jpg" -type f -exec mv {} {}.png \;```

This will rename all .jpg files to .png files by appending .png to their names.

I found out about this option from 1.

`-size`: This option allows you to find files that match a certain size criterion. For example, if you want to find all files in ./written_2 that are larger than 1 MB, you can use this command:
```find ./written_2 -size +1M```
This will output something like this:
```
./written_2/big_file1.dat
./written_2/big_file2.dat
```
Another example of using `-size` is to find all files in ./written_2 that are smaller than 100 KB and print their sizes in human-readable format. You can use this command:

```find ./written_2 -size -100k -printf "%p %s\n"```
This will output something like this:
```
./written_2/small_file1.txt 1024
./written_2/small_file2.jpg 51200
./written_2/small_file3.pdf 92160
```



