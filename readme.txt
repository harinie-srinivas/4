Step 1: Open Project
1. Open your StudentManagement folder.
2. Right-click and select Open Git Bash Here.
Step 2: Create Registration Branch
git checkout -b student-registration

Open script.js and add:
function registerStudent() {
    let name = prompt("Enter Student Name");
    if(name) alert(name + " registered successfully");
}

Save the file and execute:
git add .
git commit -m "Added student registration feature"

Step 3: Create Student Search Branch
Go back to the main branch:
git checkout main

Create a new branch:
git checkout -b student-search

Add this code to script.js:
function searchStudent() {
    let name = prompt("Enter student name");
    alert("Searching for: " + name);
}

Save and execute:
git add .
git commit -m "Added student search feature"

Step 4: Merge Branches
Go to the main branch:
git checkout main

Merge registration branch:
git merge student-registration

Merge search branch:
git merge student-search

Step 5: Push to GitHub
git push origin main

Step 6: Check Branches
git branch

To check commit history:
git log --oneline
