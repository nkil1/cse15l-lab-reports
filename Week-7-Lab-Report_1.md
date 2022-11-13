# Week 7 Lab Report
Welcome to my Week 7 lab report! Here I will showcase the best way I came up with in order to change the main mthod to take a command-line argument, then time the difference between scp-ing a file and simply just editing directly with vim. 
<br />
<br />

## 1) Part 1: Changing the main method

### The full sequence:
 `/ t e c <Enter> n b c % ( a r g s [ 1 ] ) <Esc> : w <Enter>`

<br/>

---
### Sequence with screenshots:

1. File when opened. No keystrokes.
![Initial](./week7images/one.png)

<br/>

2. Searching for keyword. Keystrokes: `/ t e c`
![Second](./week7images/two.png)

<br/>

3. Jumping to matched word. Keystrokes: `<Enter>`
![Third](./week7images/three.png)

<br/>

4. Jumping to next matched word. Keystrokes: `n`
![Fourth](./week7images/four.png)

<br/>

5. Going back a word. Keystrokes: `b`
![Fifth](./week7images/five.png)

<br/>

6. Replacing everything between the parenthesis. Keystrokes: `c %`
![Sixth](./week7images/six.png)

<br/>

7. Appending onto "Handler" so that main takes 2nd command line arg. Keystrokes: `( a r g s [ 1 ] )`
![Seventh](./week7images/seven.png)

<br/>

8. Exiting insert mode. Keystrokes: `<Esc>`
![Eigth](./week7images/eight.png)

<br/>

9. Entering command to save changes. Keystrokes: `: w `
![Ninth](./week7images/nine.png)

<br/>

10. Saving changes. Keystrokes: `<Enter>`
![Tenth](./week7images/ten.png)

<br/>
<br/>

## 2) scp vs vim 