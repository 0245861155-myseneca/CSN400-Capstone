# This is checkpoint 1 

- **COURSE INFORMATION: CSN400-2234**
- **STUDENT’S NAME: Tyler Kirkwood**
- **STUDENT'S NUMBER: 024861155**
- **GITHUB USER_ID: 024861155-myseneca.ca**
- **TEACHER’S NAME: Atoosa Nasiri**

### Table of Contents
_placeholder for Table of Contents, in hyperlink format to the actual header, follow the example below_
1.  [my repo collaborators screenshot](#my-repo-collaborators-screenshot)
2.  single line code snippet
3.  multi line code snippet "preferably bash script"
4.  sample json objects
5.  sample table
6.  sample hyperlink

### My repo collaborators screenshot
This is a Screenshot of teacher as a collaberator 

<img src="Checkpoint 1 - Collaberation.png"
     alt="Markdown Monster icon"
     style="float: left; margin-right: 10px;" />

### Single line code snippet
This is this is a powershell command that counts the number of files in 
the current Directory of a windows system.
`(Get-ChildItem -Recurse | Measure-Object).Count`

### Multi line code snippet
This is a multi line code snippet that is a caculator in `.bash` scripting 

```bash
#!/bin/bash

# Define the directory to search in and the file extension to search for
dir="/path/to/directory"
ext=".txt"

# Use grep to search for the pattern in all files with the specified extension in the directory and its subdirectories
grep -r "pattern to search for" "$dir" --include "*$ext"

```
### Sample Json object
this `.json` code shows the persons address name and phone numbers
```json
{
  "firstName": "John",
  "lastName": "Doe",
  "age": 30,
  "address": {
    "street": "123 Main St",
    "city": "New York",
    "state": "NY",
    "postal code": "H0H 0H0"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555-1234"
    },
    {
      "type": "work",
      "number": "555-5678"
    }
  ],
  "email": "johndoe@example.com"
}

```

### Sample Table
This is my sample table

| Month    | Savings |
| -------- | ------- |
| January  | $250    |
| February | $80     |
| March    | $420    |
 
### my sample hyperlink
[magic school bus](https://www.google.com "Google's Homepage")

