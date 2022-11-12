# Week 5 Lab Report
Welcome to my Week 5 lab report! Here I will showcase 3 different command-line options for the `grep` command: `-c`, `-n`, and `-L`.  
<br />
<br />

## 1) The "-c" option (aka count)
General description: used to count the number of lines that match the string in the given file(s).

Example #1:\
**The command and output:**

```
$ grep -c abuse ./technical/government/Media/Abuse_penalties.txt
5 
```

**Explanation & potential usage:**\
The `-c` option is used here to count the number of lines "abuse" appears in a single file. Useful if you want to see if the given word exists in a file, such as when you want to ensure your changes were saved.

<br/>

Example #2\
**The command and output:**

```
$ grep -c environment ./technical/government/Env_Prot_Agen/*.txt
./technical/government/Env_Prot_Agen/1-3_meth_901.txt:1
./technical/government/Env_Prot_Agen/atx1-6.txt:2
./technical/government/Env_Prot_Agen/bill.txt:16
./technical/government/Env_Prot_Agen/ctf1-6.txt:2
./technical/government/Env_Prot_Agen/ctf7-10.txt:0
./technical/government/Env_Prot_Agen/ctm4-10.txt:1
./technical/government/Env_Prot_Agen/final.txt:26
./technical/government/Env_Prot_Agen/jeffordslieberm.txt:4
./technical/government/Env_Prot_Agen/multi102902.txt:12
./technical/government/Env_Prot_Agen/nov1.txt:30
./technical/government/Env_Prot_Agen/ro_clear_skies_book.txt:11
./technical/government/Env_Prot_Agen/section-by-section_summary.txt:1
./technical/government/Env_Prot_Agen/tech_adden.txt:29
./technical/government/Env_Prot_Agen/tech_sectiong.txt:4
```

**Explanation & potential usage:**\
The `-c` option is used here to count the number of lines that match "environment" in all files in the given directory. Useful when you want to see the number of times a given method is called between all files in a project.

<br/>

Example #3\
**The command and output:**

```
$ grep -c abuse ./technical/government/Alcohol_Problems/DraftRecom-PDF.txt ./technical/government/Media/Abuse_penalties.txt
./technical/government/Alcohol_Problems/DraftRecom-PDF.txt:3
./technical/government/Media/Abuse_penalties.txt:5
```

**Explanation & potential usage:**\
The `-c` option is used here to compare the number of lines that match "abuse" between these two different files, rather than a singular file or an entire directory. One use of this specific configuration may be if you wanted to see how many times a given preposition was used between two different chapters in order to improve your writing.

<br/>
<br/>

---
## 2) The "-n" option (aka line-number)
General description: used to prefix each line of matching output with its line number.

Example #1\
**The command and output:**

```
$ grep -n abuse ./technical/government/Media/Abuse_penalties.txt
25:would get for cruelty and abuse toward an animal.
30:orders? That it's OK to abuse women in Schuylkill County, because
46:finding legal representation and facing their abuser - not to
58:potential for further incidents of abuse to occur during these
73:other civil matters related to abuse, including custody and
```

**Explanation & potential usage:**\
The `-n` option is used here in order to get the lines where the word "abuse" appears in. Useful when programming, as it can allow you to check how a given method is called in the file.

<br/>

Example #2\
**The command and output:**

```
$ grep -n pricing ./technical/government/Env_Prot_Agen/*.txt
./technical/government/Env_Prot_Agen/jeffordslieberm.txt:332:marginal rather than the regulated, cost-of-service pricing now
./technical/government/Env_Prot_Agen/jeffordslieberm.txt:439:than the regulated, cost-of-service pricing now used throughout
./technical/government/Env_Prot_Agen/multi102902.txt:2816:In some cases, the available crane or the crane pricing may limit
./technical/government/Env_Prot_Agen/tech_sectiong.txt:219:pricing of power generation and, (2) are likely to price retail
./technical/government/Env_Prot_Agen/tech_sectiong.txt:227:likely to use cost-of-service pricing principles.
./technical/government/Env_Prot_Agen/tech_sectiong.txt:244:occur) that allowance allocations will not alter pricing of
using -n on a directory
```

**Explanation & potential usage:**\
The `-n` option is used here on a directory in order to get the matching lines in all files present. Useful when programming, as you can check which file in a project do and don't calls a specific method.

<br/>


Example #3\
**The command and output:**

```
$ grep -n abuse ./technical/government/Media/Abuse_penalties.txt ./technical/government/
Env_prot_Agen/bill.txt
./technical/government/Media/Abuse_penalties.txt:25:would get for cruelty and abuse toward an animal.
./technical/government/Media/Abuse_penalties.txt:30:orders? That it's OK to abuse women in Schuylkill County, because
./technical/government/Media/Abuse_penalties.txt:46:finding legal representation and facing their abuser - not to
./technical/government/Media/Abuse_penalties.txt:58:potential for further incidents of abuse to occur during these
./technical/government/Media/Abuse_penalties.txt:73:other civil matters related to abuse, including custody and
```

**Explanation & potential usage:**\
The `-n` option is used here in order to check the lines that match the given keyword between these two files. Useful as a primitive way to check for potential academic integrity violations between two different submissions.

<br/>

## 3) The "-L" option (aka files-without-match)
General description: Used to print the name of each file and its path which DOESN'T contain a matching line. 

Example #1\
**The command and output:**

```
$ grep -L Daniel  ./technical/government/Media/Abuse_penalties.txt
./technical/government/Media/Abuse_penalties.txt
```

**Explanation & potential usage:**\
The `-L` option is used here to check whether or not the given string doesn't exist within the file. Similar to `-c` where you could use it to check whether a file properly saved your changes; however, this also returns the file's name and path, which can be used in different ways with other commands.

<br/>

Example #2\
**The command and output:**

```
$ grep -L lack  ./technical/government/Env_prot_Agen/*.txt
./technical/government/Env_prot_Agen/bill.txt
./technical/government/Env_prot_Agen/final.txt
./technical/government/Env_prot_Agen/jeffordslieberm.txt
./technical/government/Env_prot_Agen/nov1.txt
./technical/government/Env_prot_Agen/ro_clear_skies_book.txt
./technical/government/Env_prot_Agen/section-by-section_summary.txt
./technical/government/Env_prot_Agen/tech_sectiong.txt
```

**Explanation & potential usage:**\
The `-L` option is used on a directory in order return the names of any files and their paths which do not contain the given string. Useful if you want to mantain some form of homogenity between all files in a directory, and you need to see which files don't conform to that standard.

<br/>


Example #3\
**The command and output:**

```
$ grep -L abuse  ./technical/government/Env_prot_Agen/bill.txt ./technical/government/Media/Abuse_penalties.txt
./technical/government/Env_prot_Agen/bill.txt
```

**Explanation & potential usage:**\
The `-L` option is used on two different files in order to see which (if any) don't contain a given keyword. This can be useful if you were asked to submit your own file on an assignment you did with a lab partner in order to ensure you didn't leave the same name on your submission.

<br/>
<br/>

## ~~end of report ~~