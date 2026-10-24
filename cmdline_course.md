---
layout: default
title: Command Line Course
---

---
layout: default
title: Command Line Course
---

# Command-line Course Reflection

During this course, I have been introduced to the concept of coding and working with a text-based interface for the very first time. Below is a week-by-week breakdown of the topics covered, including command examples and reflections.

---

## Week 1: Introduction and Terminology
We learned the basic concepts of the terminal environment, system directories, and shell syntax. 

### Command Example:
```bash
pwd
```
*Explaining the code:* The `pwd` (Print Working Directory) command outputs the absolute path of the current directory you are working in.

### Reflection:
It was slightly overwhelming to navigate without a mouse at first, but understanding the core terminology made it much easier to comprehend how the computer structures its files.

---

## Week 2: Navigation and File Management
This week focused on moving through the file system and manipulating files and folders efficiently.

### Command Example:
```bash
cd project && ls -la
```
*Explaining the code:* This is a combined command. First, `cd project` changes the directory into the "project" folder, and `ls -la` lists all files inside, including hidden ones, in a long list format.

### Reflection:
Learning how to copy (`cp`) and move (`mv`) files via text felt faster than using a traditional desktop window once I got used to the syntax.

---

## Week 3: Text Manipulation and Data Extraction
We practiced working directly inside text files like `life_of_bee.txt` to extract insights and search for patterns.

### Command Example:
```bash
grep -i "bee" life_of_bee.txt | head -n 5
```
*Explaining the code:* This uses `grep` with the `-i` flag to search case-insensitively for the word "bee" inside `life_of_bee.txt`. The output is then piped (`|`) into `head -n 5`, which only displays the first 5 matching lines.

### Reflection:
It was fascinating to see how fast the terminal can scan through a whole text document to extract specific data without opening heavy software.

---

## Week 4: Automation and Makefiles
We learned how to automate repetitive workflows using tools like `make` and structured scripts. Below is a comparison table of the redirection operators we used to save our data.

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
*Explaining the code:* This is a pattern rule in a `Makefile`. The target is `%.freq` (the frequency list file), and its dependency is `%.no_md.txt`. The command executes a shell script `freqlist.sh`, where `$<` represents the dependency file and `$@` represents the target file.

### Reflection:
Writing automated rules saved me a lot of time. It made me realize how powerful scripts are for managing larger scientific datasets.

---

## Week 5: Jekyll and GitHub Pages
The final week was spent learning how to turn our Markdown repositories into live web applications using Jekyll and GitHub Pages.

### Command Example:
```bash
bundle exec jekyll serve
```
*Explaining the code:* This command boots up a local development web server using Ruby Bundler, allowing us to preview the generated HTML website locally at `http://127.0.0.1:4000`.

### Core Takeaways from Week 5:
* **Static Site Generation:** Transforming raw `.md` files into valid HTML.
* **Version Control Integration:** Pushing clean layouts up to Git braches.
* **Theme Customization:** Altering layouts and global SCSS variables.

### Project Overview Illustration:
Below is the visual structure representing our web environment:

![Web Project Preview](thumbnail.png)

### Reflection:
Seeing my local text files turn into a live website via GitHub Pages was highly rewarding. Learning to fix the menu layout taught me a lot about structural HTML files.

 


