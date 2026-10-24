---
layout: default
title: Command Line Course
---

# Command-line Course Reflection

During this course, I have been introduced to the concept of coding and working with a text-based interface for the very first time. Below is a week-by-week summary of the topics we have covered, some examples, and my reflections.

---

## Week 1: Introduction and Terminology

We learned the basic concepts of the terminal environment, system directories, and shell syntax.

### Command Example:

```bash
pwd
```

_Explanation:_ The `pwd` (Print Working Directory) command outputs the absolute path of the current directory you are working in.

### Reflection:

It was slightly overwhelming to navigate so many new concepts and terms at first, but learning about the core terminology made it more manageable. Furthermore, the practical assignments slowly made it easier to follow along with how the computer structures its files.

---

## Week 2: Navigation and File Management

This week focused on moving through the file system and manipulating files and folders efficiently. 

### Command Example:

```bash
cd project && ls -la
```

*Explanation*: This is a combination of commands. First, `cd project` changes the directory into the "project" folder, and `ls -la` lists all files inside, including hidden ones, in a long list format.

### Reflection:

Learning how to copy (`cp`) and move (`mv`) files via text felt faster than using a traditional desktop window once I got used to the syntax. However, it took me some time before I could stop worrying about losing my documents or misplacing them in the process. 

---

## Week 3: Text Manipulation and Data Extraction

We practiced downloading texts from websites such as [Project Gutenberg](https://www.gutenberg.org/) and how to work directly inside a text file like `life_of_bee.txt` to extract information and search for patterns.

### Command Example:

```bash
grep -i "bee" life_of_bee.txt | head -n 5
```

*Explanation*: This uses `grep` with the `-i` flag to search case-insensitively for the word "bee" inside `life_of_bee.txt`. Then the output is piped (`|`) into `head -n 5`, which only displays the first 5 matching lines.

### Reflection:

Once the task was made clear, it was fascinating to see how fast the terminal can scan through a whole text document to extract specific data. With that being said, it still felt a bit clumsy navigating big text files and only being able to search and edit through commands as opposed to just clicking. 

---

## Week 4: Scripting, Configuration Files and Installing Programs  

We learned how to write and borrow scripts. We learned the importance of an automated repetitive workflow and using tools like `make`. Below is a comparison table of the redirection operators we used to save our data.

### Redirection Operators:

| Operator | Action | Description |
| :--- | :--- | :--- |
| `>` | Overwrite | Redirects output and replaces the target file content. |
| `>>` | Append | Redirects output and adds it to the end of the file. |
| `\|` | Pipe | Passes the output of one command as input to another. |

### Code Example (Makefile Rule):

```make
%.freq: %.no_md.txt
	bin/freqlist.sh < @
```

_Explanation:_ This is a pattern rule in a `Makefile`. The target is `%.freq` (the frequency list file), and its dependency is `%.no_md.txt`. The command executes a shell script `freqlist.sh`, where `$<` represents the dependency file and `$@` represents the target file.

### Reflection:

Writing automated rules can be a real time saver... if it works! It made me realize how many elements one must take into consideration to keep it running smoothly and how powerful scripts can be for managing larger datasets. Furthermore, it is nice to know that you don't have to start from scratch when writing a script, as there are plenty of shared scripts that can be used. 

---

## Week 5: Using ssh, scp and Version Control

This week we were introduced to resources such as GitHub and how to keep several versions of your working projects without having to worry about losing the given changes. 

### Command Example:

```bash
scp life_of_bee.txt fridagrant@server.helsinki.fi:~/
``` 

*Explanation*: `life_of_bee.txt` is the file on your current computer. `fridagrant@server.helsinki.fi` is the username and server address. `:~/` tells the server to save the file in your remote home directory.

### Reflection:

I had a lot of challenges with the remote server, as there seemed to be overall technical difficulties. However, I managed to navigate through the jungle after a few extra attempts.  

---

## Week 6: Jekyll and GitHub Pages

The final week was spent learning how to turn Markdown repositories into live web applications using Jekyll and GitHub Pages. 

### Command Example:

```bash
bundle exec jekyll serve
```

_Explanation:_ This command boots up a local development web server using Ruby Bundler, allowing you to preview the HTML website locally at `http://127.0.0.1:4000`.

### Core Takeaways from Week 6:

- **Static Site Generation:** Transforming raw `.md` files into valid HTML.
- **Version Control Integration:** Pushing layouts up to Git branches.
- **Theme Customization:** Altering layouts and global SCSS variables.

### Project Overview Illustration:

![Web Project Preview](https://fridagrant2008-glitch.github.io/thumbnail.png)

### Reflection:

It was very inspiring to see different people's work on GitHub and nice to learn that there exists a whole online community that is truly passionate about sharing perspectives and ideas when it comes to coding. With that being said, GitHub is a user-specific platform and it didn't always feel intuitive to navigate the site. Seeing my local text files turn into a live website via GitHub Pages was highly rewarding. Learning to fix the menu layout taught me a lot about structural HTML files.


