# CSE 15L: Researching Commands

## Intro:

Hello, my name is Brian Ponce and in this lab report I will be researching the git bash command `wc` and four of its important command options (with examples below).

## 1) -l:

This command only displays the number of lines in a file

Example 1:

* Input:

`wc -l technical/911report/chapter-1.txt`

* Output:

`731 technical/911report/chapter-1.txt`

Example 2:

* Input:

`wc -l technical/government/Media/balance_scales_of_justice.txt`

* Output:

`86 technical/government/Media/balance_scales_of_justice.txt`

* The -l command option is useful when we need to quickly determine the number of lines in a file, especially when navigating through multiple files. It allows us to display the line count without having to distinguish between different counts for other parameters.

> Source: asking Chat-GPT to list various -wc command options 

## 2) -L:

This command displays the length of the longest string in the file.

Example 1:

* Input:

`wc -L technical/911report/chapter-1.txt`

* Output:

`1022 technical/911report/chapter-1.txt`

Example 2:

* Input:

`wc -L technical/government/Media/balance_scales_of_justice.txt`

* Output:

`67 technical/government/Media/balance_scales_of_justice.txt`

* The -L command option helps us to quickly find the longest line in a file. The command option is especially a useful tool for optimizing the formatting of a file, especially when checking that a specific line does not exceed a predetermined maximum length.

> Source: asking Chat-GPT to list various -wc command options 

## 3) -c:

This command only displays the number of bytes in the file.

Example 1:

* Input:

`wc -c technical/911report/chapter-1.txt`

* Output:

`118656 technical/911report/chapter-1.txt`

Example 2:

* Input:

`wc -c technical/government/Media/balance_scales_of_justice.txt`

* Output:

`4279 technical/government/Media/balance_scales_of_justice.txt`

* The -c command option is a useful tool to count the number of bytes in a file. This command option is especially helpful when working with storage limitations or sending files over networks.

> Source: asking Chat-GPT to list various -wc command options 

## 4) -w:

This command option only displays the number of words in a file

Example 1:

* Input:

`wc -w technical/911report/chapter-1.txt`

* Output:

`19259 technical/911report/chapter-1.txt`

Example 2:

* Input:

`wc -w  technical/government/Media/balance_scales_of_justice.txt`

* Output:

`710 technical/government/Media/balance_scales_of_justice.txt`

* This -w command option is a tool to only display the number of words in a file. The command option is especially important when we want to get a quick glimpse to the size of a particular file.

> Source: asking Chat-GPT to list various -wc command options 














  
 
   




