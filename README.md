# CalgaryToSpace Software Onboarding Guide
CTS-SAT-1-era software team onboarding guide

## Getting Started
### Downloads
Please install the following software:

1. [STM32CubeIDE - Integrated Development Environment Download](https://www.st.com/en/development-tools/stm32cubeide.html)
2. [Git Bash Download](https://git-scm.com/downloads) (for Windows only)
3. [GitHub Desktop Download](https://desktop.github.com/)
4. [Visual Studio Code](https://code.visualstudio.com/) (optional, recommended)

### Hardware
You require at least the following hardware:

- `STM32L4R5ZI` Nucleo-144 dev kit
- Micro-USB Cable
  - Must support data transfer. Please bring one from home if you can.

### Guides
Please complete the following guides:
1. [GIT Tutorial](https://docs.google.com/presentation/d/1wr_xPIai-Gg8E0KEQzC6v0hETkPaw800/edit#slide=id.p1)
2. [STM32 Blinky LED Tutorial - Video](https://www.youtube.com/watch?v=hyZS2p1tW-g&list=PLEBQazB0HUyRYuzfi4clXsKUSgorErmBv)
3. [STM32 - FreeRTOS Guide - Video](https://www.digikey.ca/en/maker/projects/getting-started-with-stm32-introduction-to-freertos/ad275395687e4d85935351e16ec575b1)
4. [STM32 - I2C & UART Guide - Video](https://youtu.be/isOekyygpR8?si=WwGrYZXlniSiYubi)

## Code Push and Review Process

#### Commit Message Format:
- Short Title
- Concise Description
- Testing used to verify the change

### Using GitHub Desktop (Recommended)
Download and Install GitHub Desktop (link above)
1) Log in to your GitHub account
2) Select your repository (or clone it from Git)

#### Committing a Change 
If you have made changes, GitHub Desktop willl look something like this:
![changes pic](https://github.com/calgarytospace/OBC_software/blob/Onboarding/Example%20Stuff%20for%20Onboarding/pictures/changes.png?raw=true)

1) Select the boxes which associate with the files whose changes you would like to push forwared onto the repository.
2) Write a description of your commit. Generally speaking, it should be short and concise.
It should now look something like this:
![commit pic](https://github.com/calgarytospace/OBC_software/blob/Onboarding/Example%20Stuff%20for%20Onboarding/pictures/commit.png?raw=true)
3) Press the commit button on the bottom left. This is prompted a change but pushed the change onto the repository (the change is pushed to your local repository)
4) Now, push the `push origin` button on the top right.
![push pic](https://github.com/calgarytospace/OBC_software/blob/Onboarding/Example%20Stuff%20for%20Onboarding/pictures/push.png?raw=true)
Nice, you have just pushed a change. Remember that pushes and commits can be reverted, just search up how to do that.

#### Reviewing a Pull Request:
1) Look over the code and also the commit message. Ensure changes are not out of the scope of the commit message
2) Leave comments for any questions or things you think needs changing
3) If you think its good to submit, comment "Approved"
4) If you think its not good to submit, comment "Revise"


### Using Git Command Line (Not Recommended)
For CalgaryToSpace, using GitHub Desktop is strongly recommended.
<details>
<summary>Click to expand</summary>

#### Committing a Change and Submitting a Pull Request
1) Update your local repo with `git pull origin master` 
2) Create a working branch with `git checkout -b MyNewBranch`
3) Make your changes on your branch and stage them with `git add .` to stage all changes. 
4) Commit your changes locally with `git commit -m "description of your commit"`
5) Make as many commit as needed to implement the change/feature 
6) Upload the changes (including your new branch) to GitHub with `git push origin MyNewBranch`
7) Go to the main repo on GitHub where you should now see your new branch
8) Click on your branch name
9) Click on "Pull Request" button to 
10) Click on "Send Pull Request" to development/main 
11) Have Pull request reviewed by 3 people
12) Pull request is good to submit after 3 "Approves"

#### Submitting a Pull Request
1) Open a PR using GitHub online.

#### Modifying an Existing Pull Request
1) Make changes and stage them with `git add .` 
2) Then use `git commit –-amend --no-edit` to modify the previous commit without changing the commit message
3) Upload the changes (including your new branch) to GitHub with `git push origin MyNewBranch`
4) Update the pull request with the new changes

</details>

## GoogleTest Setup Guide: (https://github.com/CalgaryToSpace/OBC_software/blob/Onboarding/GoogleTestSetup.md)
