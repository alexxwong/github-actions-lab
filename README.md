# Tutorial-17: GitHub Action

## Student Info
* **Matric Number:** [298258]
* **Name:** Alex Wong Yung Fei


[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/x7qwpQ24)
## Tutorial-17: GitHub Action



## 🎯 Objective
By the end of this tutorial, students should be able to:
1. Explain the difference between workflow, job, and step
2. Create a simple GitHub Actions workflow
3. Observe how jobs run in parallel, and steps run sequentially
4. Modify the workflow to add a job dependency


## Instructions

### Part A: Repository Setup
1. Create a new GitHub repository
- Name: github-actions-lab
- Public repository
- Add a README file

2. Inside the repository, create this folder:
```
.github/workflows/
```
3. Create a file named:
```
lab-actions.yml
```

### Part B: Create Your First Workflow
Paste the following code into `lab-actions.yml`:
```yml
name: Workflow vs Job vs Step Lab

on: push

jobs:
  job-one:
    runs-on: ubuntu-latest
    steps:
      - name: Step 1 - Print message
        run: echo "This is Step 1 in Job One"

      - name: Step 2 - Print another message
        run: echo "This is Step 2 in Job One"

  job-two:
    runs-on: ubuntu-latest
    steps:
      - name: Step 1 - Print message
        run: echo "This is Step 1 in Job Two"
```
>Commit and push the file.

### Part C: Observe the Execution
1. Go to Actions tab in GitHub
2. Click the running workflow
3. Observe:
   - The workflow name
   - Two jobs running in parallel
   - Steps executing top to bottom inside each job

### Part D: Add Job Dependency
Now modify job-two so it runs after job-one. Update the file:
```yml
job-two:
  needs: job-one
  runs-on: ubuntu-latest
  steps:
    - name: Step 1 - Print message
      run: echo "Job Two runs after Job One"
```
>Commit and push again.

### Part E: Compare Results
You should now observe:
- job-one runs first
- job-two waits until job-one finishes


## Submission
Screenshot of:
1. Workflow page
2. Job execution view

## Results
[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/x7qwpQ24)
## Tutorial-17: GitHub Action

## Student Info:
1. Matric Number:
2. Name:


## 🎯 Objective
By the end of this tutorial, students should be able to:
1. Explain the difference between workflow, job, and step
2. Create a simple GitHub Actions workflow
3. Observe how jobs run in parallel, and steps run sequentially
4. Modify the workflow to add a job dependency


## Instructions

### Part A: Repository Setup
1. Create a new GitHub repository
- Name: github-actions-lab
- Public repository
- Add a README file

2. Inside the repository, create this folder:
```
.github/workflows/
```
3. Create a file named:
```
lab-actions.yml
```

### Part B: Create Your First Workflow
Paste the following code into `lab-actions.yml`:
```yml
name: Workflow vs Job vs Step Lab

on: push

jobs:
  job-one:
    runs-on: ubuntu-latest
    steps:
      - name: Step 1 - Print message
        run: echo "This is Step 1 in Job One"

      - name: Step 2 - Print another message
        run: echo "This is Step 2 in Job One"

  job-two:
    runs-on: ubuntu-latest
    steps:
      - name: Step 1 - Print message
        run: echo "This is Step 1 in Job Two"
```
>Commit and push the file.

### Part C: Observe the Execution
1. Go to Actions tab in GitHub
2. Click the running workflow
3. Observe:
   - The workflow name
   - Two jobs running in parallel
   - Steps executing top to bottom inside each job

### Part D: Add Job Dependency
Now modify job-two so it runs after job-one. Update the file:
```yml
job-two:
  needs: job-one
  runs-on: ubuntu-latest
  steps:
    - name: Step 1 - Print message
      run: echo "Job Two runs after Job One"
```
>Commit and push again.

### Part E: Compare Results
You should now observe:
- job-one runs first
- job-two waits until job-one finishes


## Submission
Screenshot of:
1. Workflow page
2. Job execution view

## Results

![alt text](<Screenshot 2026-01-08 012439.png>) 








