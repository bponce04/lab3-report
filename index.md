# CSE 15L: Researching Commands

## Intro:

Hello, my name is Brian Ponce and in this lab report I will be researching the git bash command `grep` and four of its interesting (and helpful) command options.

## 1) -r:

This `grep` command line option will recursively search for the given key word in multiple directories (and even sub-directories)

Example 1:

* Input:

`grep -r "Tuesday" technical/911report/chapter-1.txt`

* Output:

`    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.
    On the morning of 9/11, there were only 37 passengers on United 93-33 in addition to the 4 hijackers. This was below the norm for Tuesday mornings during the summer of 2001. But there is no evidence that the hijackers manipulated passenger levels or purchased additional seats to facilitate their operation.`
    
Using `grep -r` will search for the keyword `Tuesday` recursively through directories and subdirectories. In this example, `grep -r` finds all instances of the word inside the file `chapter-1.txt`.

Example 2:

* Input:

`grep -r Tuesday technical/911reports`

* Output:

`technical/911report/chapter-1.txt:    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.
technical/911report/chapter-1.txt:    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.
technical/911report/chapter-1.txt:    On the morning of 9/11, there were only 37 passengers on United 93-33 in addition to the 4 hijackers. This was below the norm for Tuesday mornings during the summer of 2001. But there is no evidence that the hijackers manipulated passenger levels or purchased additional seats to facilitate their operation.
technical/911report/chapter-13.2.txt:                seating capacity of 168, below the 49.22 percent for Flight 175 on Tuesdays in the
technical/911report/chapter-13.2.txt:                Tuesdays in the three-month period prior to September 11 (June 11-September 4,
technical/911report/chapter-13.4.txt:                not asking the Pakistanis to deliver Bin Ladin next Tuesday; the DCI said he was`

In this example, `grep -r` will find all instances of the word `Tuesday` inside `911reports`, in this case various files. 

* The -r command option is useful when we need to quickly find a document (or multiple documents) that contain the keyword that we are looking for.

> Source: giving Chat-GPT the following prompt: "what are four interesting grep command line options for git bash" 

## 2) -v:

This `grep` command line option will return all passages that do not contain the given key word. Note that for this command, you will need to be inside a file in order for the command line option to work.

Example 1:

* Input:

`grep -v Tuesday technical/911report/chapter-1.txt`

* Output:

`    At 8:41, in American's operations center, a colleague told Marquis that the air traffic controllers declared Flight 11 a hijacking and "think he's [American 11] headed toward Kennedy [airport in New York City]. They're moving everybody out of the way. They seem to have him on a primary radar. They seem to think that he is descending."`

In this example, `grep -v` will find for all instances of the keyword `Tuesday` and only return the passages in the file that does not contain it.

Example 2:

* Input:

`grep -v September technical/911reports/chapter-2`

* Output:

`THE FOUNDATION OF THE NEW TERRORISM
            A DECLARATION OF WAR
            In February 1998, the 40-year-old Saudi exile Usama Bin Ladin and a fugitive Egyptian
                physician, Ayman al Zawahiri, arranged from their Afghan headquarters for an Arabic
                newspaper in London to publish what they termed a fatwa issued in the name of a
                "World Islamic Front." A fatwa is normally an interpretation of Islamic law by a
                respected Islamic authority, but neither Bin Ladin, Zawahiri, nor the three others
                who signed this statement were scholars of Islamic law. Claiming that America had
                declared war against God and his messenger, they called for the murder of any
                American, anywhere on earth, as the "individual duty for every Muslim who can do it
                in any country in which it is possible to do it." `
                
In this example, `grep -v` will search for all instances of the keyword `September` inside `chapter-2.txt` and return all passages in the file that does not contain it.

* The -r command option helps us to quickly find all instances of the passages in a file that does not contain the given keyword.

> Source: giving Chat-GPT the following prompt: "what are four interesting grep command line options for git bash" 

## 3) --color:

This `grep` command line option allows us to better see the keyword in given passages

Example 1:

* Input:

`grep --color=always September technical/911reports/chapter-1.txt`

* Output:

`    Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.`

In this example, `grep --color=always` will make it so that when the command does find the keyword, `September`, then it will highlight it in a different color.

Example 2:

* Input:

`grep --color=never September technical/911report/chapter-2.txt`

* Output:

`                most militant opponents. But after September 1996, when first Jalalabad and then`

in this example, `grep --color=never` will make it so that when the command does the find the keyword, `September`, it will not highlight it and will simply return the passage in which the keyword exists.

* The `--color=` command line option is very useful when we not only want to find the keyword inside various passages, but we also want to find it easily.

> Source: giving Chat-GPT the following prompt: "what are other cool command line options for grep" 

## 4) -C <num>:

This `grep` command line option will provide the given number of lines before and after the keyword is found.

Example 1:

* Input:

`grep -C 2 planes technical/911report/chapter-1.txt`

* Output:

`The 19 men were aboard four transcontinental flights.

    They were planning to hijack these planes and turn them into large guided missiles, loaded with up to 11,400 gallons of jet fuel. By 8:00 A.M. on the morning of Tuesday, September 11,2001, they had defeated all the security layers that America's civil aviation security system then had in place to prevent a hijacking. The Hijacking of American 11 American Airlines Flight 11 provided nonstop service from Boston to Los Angeles. On September 11, Captain John Ogonowski and First Officer Thomas McGuinness piloted the Boeing 767. It carried its full capacity of nine flight attendants. Eighty-one passengers boarded the flight with them (including the five terrorists).22 The plane took off at 7:59. Just before 8:14, it had climbed to 26,000 feet, not quite its initial assigned cruising altitude of 29,000 feet. All communications and flight profile data were normal. About this time the "Fasten Seatbelt" sign would usually have been turned off and the flight attendants would have begun preparing for cabin service.`
  
In this example, `grep -C 2` will provide two lines before the keyword is found and 2 lines after it is found.

Example 2:

* Input:

`grep -C 1 Tuesday technical/911report/chapter-1.txt`

* Output:

`Tuesday, September 11, 2001, dawned temperate and nearly cloudless in the eastern United States. Millions of men and women readied themselves for work. Some made their way to the Twin Towers, the signature structures of the World Trade Center complex in New York City. Others went to Arlington, Virginia, to the Pentagon. Across the Potomac River, the United States Congress was back in session. At the other end of Pennsylvania Avenue, people began to line up for a White House tour. In Sarasota, Florida, President George W. Bush went for an early morning run.`
  
In this example, `grep -C 1` will only provide one line of text of before the keyword and one line of text after it is found.

* This `grep -C <num>` command line option is useful when we want to know the context of the passage where the keyword is found.

> Source: giving Chat-GPT the following prompt: "what are other cool command line options for grep" 














  
 
   




