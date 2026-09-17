# firstf.js

## Section 1 — Command Description

My tool is called `firstf.js`.

It is a simple Node.js program that combines the basic behavior of the Linux `grep` and `head` commands.

The program searches a file for a pattern or word, similar to `grep`, and then only displays the first number of matching lines requested by the user, similar to `head`.

### How to Run It

The command format is:

```bash
node firstf.js PATTERN FILENAME NUMBER_OF_LINES

```
### AI Reflection
I used AI to help me understand how Linux commands such as grep and head work and how I could recreate some of their behavior in Node.js. I asked AI how process.argv works, how to read a file with fs, how to check whether a file exists, and how to search through lines for a specific word.

AI was most helpful when I had syntax and logic errors. It helped me fix mistakes with process.argv, fs.existsSync(), and the loop that searches through the file. It also helped me understand the difference between checking only the first few lines of a file and searching the whole file but only printing the first few matches.

I still had to think independently about how I wanted my custom command to behave. I decided that firstf.js should combine grep and head by searching the entire file for a pattern, then stopping after the requested number of matching lines were printed. I also had to test the code myself and make sure the command-line arguments were in the correct order.

AI did not get everything right immediately. At one point, the suggested logic only searched the first N lines of the file instead of finding the first N matching lines. That did not match the behavior I wanted for my combined command. I had to recognize the difference and change the loop so it searched the whole file and counted the matches instead.
