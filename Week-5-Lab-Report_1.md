# Week 5 Lab Report
Welcome to my Week 5 lab report! Here I will showcase some different command-line options with some brief explanations for the `less`, `find`, and `grep` commands.
<br />
<br />


## 1) "less" command-line options

Option #1\
**The command and output:**

```
$ less -N ./technical/government/Media/A_Perk_of_Age.txt
      1
      2
      3
      4
      5 A Perk of Age: Free Legal Advice
      6 By Kelly Greene
      7 Free Legal advice is only a phone call away - and the hot lines
      8 that provide it are expanding their services.
      9 It's a little known perk available to anyone 60 or older: 21
     10 states, Washington D.C., and Puerto Rico operate legal-assistance
     11 hot lines for older adults and most take calls from younger
     12 caregivers as well. Volunteers offer advice on legal questions,
     13 provide self-help materials, and make referrals to legal aid
     14 offices and pro bono or reduced-fee private lawyers. Even if you
     15 live in a state without a hot line, local agencies on aging will
     16 provide you with referrals to nearby lawyers. The hot lines and
     17 referral services tackle estate planning, pension, and health
     18 benefits, elder abuse and neglect, guardianship custodial issues
     19 involving grandchildren, consumer protection and other elder-law
     20 issues.
     21 The U.S. administration on Aging coordinates this loosely knit
     22 legal-services network. Anyone who meets the age requirement can
     23 call the hot line, but hands-on legal counsel goes first to people
     24 with the greatest financial or social needs. The federal Agency
     25 recently awarded $2 million in grants to improve elder-law
     26 services, with the largest part being used to bolster 12 hotlines
     27 around the country, some of which are adding Web-based
     28 questionnaires and outreach projects in rural areas and for older
     29 people who don't speak English.
     30 For a list of where the hotlines operate, along with their phone
     31 numbers and hours, go to www.aoa.gov/legal/hotline.html, or call
     32 the federal Eldercare Locator at 800-677-1116. If you live in a
     33 state without a hot line, the locator can point you to local legal 
```

**Explanation & potential usage:**\
The `-N` option displays the line numbers for the given file. This can be useful when programming with others as it allows you to easily specify which lines you are talking about.

<br/>

Option #2\
**The command and output:**

```
$ less -s ./technical/government/Media/A_Perk_of_Age.txt
 
A Perk of Age: Free Legal Advice
By Kelly Greene
Free Legal advice is only a phone call away - and the hot lines
that provide it are expanding their services.
It's a little known perk available to anyone 60 or older: 21
states, Washington D.C., and Puerto Rico operate legal-assistance
hot lines for older adults and most take calls from younger
caregivers as well. Volunteers offer advice on legal questions,
provide self-help materials, and make referrals to legal aid
offices and pro bono or reduced-fee private lawyers. Even if you
live in a state without a hot line, local agencies on aging will
provide you with referrals to nearby lawyers. The hot lines and
referral services tackle estate planning, pension, and health
benefits, elder abuse and neglect, guardianship custodial issues
involving grandchildren, consumer protection and other elder-law
issues.
The U.S. administration on Aging coordinates this loosely knit
legal-services network. Anyone who meets the age requirement can
call the hot line, but hands-on legal counsel goes first to people
with the greatest financial or social needs. The federal Agency
recently awarded $2 million in grants to improve elder-law
services, with the largest part being used to bolster 12 hotlines
around the country, some of which are adding Web-based
questionnaires and outreach projects in rural areas and for older
people who don't speak English.
For a list of where the hotlines operate, along with their phone
numbers and hours, go to www.aoa.gov/legal/hotline.html, or call
the federal Eldercare Locator at 800-677-1116. If you live in a
state without a hot line, the locator can point you to local legal
assistance.
Another source of low-cost help also expanded this year: AARP's
Legal Services Network is now available in 46 states and expects to
```

**Explanation & potential usage:**\
The `-s` option consolidates multiple blank lines into one blank line. This is especially useful if you want to ensure you have as much text content showing on the terminal at once as possible by reducing "useless" formatting.

<br/>

Option #3\
**The command and output:**

```
$ less -X ./technical/government/Media/A_Perk_of_Age.txt




A Perk of Age: Free Legal Advice
By Kelly Greene
Free Legal advice is only a phone call away - and the hot lines
that provide it are expanding their services.
It's a little known perk available to anyone 60 or older: 21
states, Washington D.C., and Puerto Rico operate legal-assistance
hot lines for older adults and most take calls from younger
caregivers as well. Volunteers offer advice on legal questions,
provide self-help materials, and make referrals to legal aid
offices and pro bono or reduced-fee private lawyers. Even if you
live in a state without a hot line, local agencies on aging will
provide you with referrals to nearby lawyers. The hot lines and
referral services tackle estate planning, pension, and health
benefits, elder abuse and neglect, guardianship custodial issues
involving grandchildren, consumer protection and other elder-law
issues.
The U.S. administration on Aging coordinates this loosely knit
legal-services network. Anyone who meets the age requirement can
call the hot line, but hands-on legal counsel goes first to people
with the greatest financial or social needs. The federal Agency
recently awarded $2 million in grants to improve elder-law
services, with the largest part being used to bolster 12 hotlines
around the country, some of which are adding Web-based
questionnaires and outreach projects in rural areas and for older
people who don't speak English.
For a list of where the hotlines operate, along with their phone
numbers and hours, go to www.aoa.gov/legal/hotline.html, or call
the federal Eldercare Locator at 800-677-1116. If you live in a
state without a hot line, the locator can point you to local legal

noahk@NK MINGW64 ~/OneDrive/Documents/GitHub/docsearch (main)
$
```

**Explanation & potential usage:**\
The `-X` option keeps the output of the less command on the terminal even after stopping the command's operations. This may be useful if you wanted to keep the contents of the file handy in the terminal so that you can reference it without having to copy-and-paste it / output it to a separate file.

<br/>
<br/>

---
## 2) "find" command-line options

Option #1\
**The command and output:**

```
$ find technical -type d
technical
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```

**Explanation & potential usage:**\
The `-type` option specifies the type of file or directory to search for -- in this case, `-type d` is used to find all directories and sub-directories in the `technical` folder. This is useful if you want to search for strictly files or directories.

<br/>

Option #2\
**The command and output:**

```
$ find technical/government/Media/A_Perk_of_Age.txt  -printf %h%t
technical/government/MediaSat Oct 29 17:48:00.0529058000 2022
```

**Explanation & potential usage:**\
The `-printf` option is used with a variety of directives (the commands with a "%") in order to output a variety of different information regarding the target file(s); here, `%h` outputs the leading directories of the specified file, while `%t` outputs the date of the file's latest modification. The `-printf` option is an extremely useful way to quickly get anything you would want to know about a given file, and in this case `%h` can be useful for getting the relative path of a file while `%t` can be useful for checking for any potential modifications to a file similar to a commit on Git.

<br/>

---
Option #3\
**The command and output:**

```
$ find ./technical -maxdepth 2 -iname "chapter*"
./technical/911report/chapter-1.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-8.txt
./technical/911report/chapter-9.txt
```

**Explanation & potential usage:**\
The `-maxdepth` specifies the max number of sub-directories to go into when performing the `find` command; in this case, `-maxdepth 2` means that `find` should only go 2 sub-directories deep when performing its operations. This can be useful if you only want information about a certain number of sub-directories in a directory with many sub-directories, without having to specify the directories to search in explicitly. 


## 3) "grep" command-line options

Option #1\
**The command and output:**

```
$ grep -R "Okay"
technical/911report/chapter-1.txt:    Manager, New York Center: Okay. This is New York Center. We're watching the airplane. I also had conversation with American Airlines, and they've told us that they believe that one of their stewardesses was stabbed and that there are people in the cockpit that have control of the aircraft, and that's all the information they have right now.
technical/911report/chapter-1.txt:    Boston Center: . . . as far as the tape, Bobby seemed to think the guy said that "we have planes." Now, I don't know if it was because it was the accent, or if there's more than one, but I'm gonna, I'm gonna reconfirm that for you, and I'll get back to you real quick. Okay? New England Region: Appreciate it.
technical/911report/chapter-1.txt:    New England Region: Okay. Yeah, we gotta get-we gotta alert the military real quick on this.
technical/911report/chapter-1.txt:    At 9:21, NEADS received a report from the FAA: FAA: Military, Boston Center. I just had a report that American 11 is still in the air, and it's on its way towards-heading towards Washington. NEADS: Okay. American 11 is still in the air?
technical/911report/chapter-1.txt:    NEADS: Okay.
technical/911report/chapter-1.txt:    NEADS: Okay. So American 11 isn't the hijack at all then, right? FAA: No, he is a hijack.
technical/911report/chapter-1.txt:    The NEADS technician who took this call from the FAA immediately passed the word to the mission crew commander, who reported to the NEADS battle commander: Mission Crew Commander, NEADS: Okay, uh, American Airlines is still airborne. Eleven, the first guy, he's heading towards Washington. Okay? I think we need to scramble Langley right now. And I'm gonna take the fighters from Otis, try to chase this guy down if I can find him.
...
```

**Explanation & potential usage:**\
The `-R` option looks for all files in the current directory and all sub-directions for files that have lines matching the current string, then outputs the file names along with the lines that contain the matching string. This can be useful if you want to search for all files in all sub-directories while also outputting the specific lines that contain the given string.

<br/>

Option #2\
**The command and output:**

```
$ grep -c "state" ./technical/government/Media/A_Perk_of_Age.txt
5
```

**Explanation & potential usage:**\
The `-c` option outputs the number of lines that contain the given string. Useful if you want to find how many matching lines there are between different files (such as when comparing student PAs...)

<br/>

Option #3\
**The command and output:**

```
$ grep -v state ./technical/government/Media/A_Perk_of_Age.txt




A Perk of Age: Free Legal Advice
By Kelly Greene
Free Legal advice is only a phone call away - and the hot lines
that provide it are expanding their services.
It's a little known perk available to anyone 60 or older: 21
hot lines for older adults and most take calls from younger
caregivers as well. Volunteers offer advice on legal questions,
provide self-help materials, and make referrals to legal aid
offices and pro bono or reduced-fee private lawyers. Even if you
provide you with referrals to nearby lawyers. The hot lines and
benefits, elder abuse and neglect, guardianship custodial issues
involving grandchildren, consumer protection and other elder-law
issues.
The U.S. administration on Aging coordinates this loosely knit
legal-services network. Anyone who meets the age requirement can
call the hot line, but hands-on legal counsel goes first to people
with the greatest financial or social needs. The federal Agency
recently awarded $2 million in grants to improve elder-law
services, with the largest part being used to bolster 12 hotlines
around the country, some of which are adding Web-based
questionnaires and outreach projects in rural areas and for older
people who don't speak English.
For a list of where the hotlines operate, along with their phone
numbers and hours, go to www.aoa.gov/legal/hotline.html, or call
the federal Eldercare Locator at 800-677-1116. If you live in a
assistance.
Another source of low-cost help also expanded this year: AARP's
reach all 50 by the end of March. You have to pay the group's dues
($10 a year) to use the services; after that you get 30 minutes of
legal counseling, either face-to-face or by phone, at no cost.
Lawyers discount their usual rate by 20% after that. Simple wills
cost $75 apiece. You can reach the service at 800-424-3410 or go to
www.aarp.org/LSN to find a lawyer nearby
```

**Explanation & potential usage:**\
The `-v` option excludes all of the lines matching the given string performing the `-grep` command. This may be useful if you want to see how a file would look like without the given matching lines, such as when editing an essay.

<br/>
<br/>

## ~~end of report ~~