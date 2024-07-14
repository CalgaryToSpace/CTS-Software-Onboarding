# CalgaryToSpace Software Onboarding Guide
CTS-SAT-1-era software team onboarding guide

## Getting Started
### Downloads
Please install the following software:

1. [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
2. [Git Bash](https://git-scm.com/downloads) (for Windows only)
3. [GitHub Desktop](https://desktop.github.com/)
4. [Visual Studio Code](https://code.visualstudio.com/) (optional, recommended)

### Hardware
You require at least the following hardware:

- `STM32L4R5ZI` Nucleo-144 dev kit
- Micro-USB Cable
  - Must support data transfer. Please bring one from home if you can.

### Software
The following software is required:
- [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
- [VSCode](https://code.visualstudio.com/download)
- A serial terminal if you don't already have one.  Several options are available:
  - [SerialTest](https://github.com/wh201906/SerialTest)
  - [RealTerm](https://sourceforge.net/projects/realterm/)
  - [Teraterm](https://teratermproject.github.io/index-en.html)
  - [Termite](https://www.compuphase.com/software_termite.htm)

### Tutorials
Please complete the following tutorials:

#### STM32 Programming
1. [STM32 Blinky LED Tutorial - Video](https://www.youtube.com/watch?v=hyZS2p1tW-g&list=PLEBQazB0HUyRYuzfi4clXsKUSgorErmBv)
  * The GPIO pin number for the builtin LD2 LED is PB7, LD1 is Pin PC7, and LD3 is Pin PB14.
2. [STM32 - I2C & UART Guide - Video](https://youtu.be/isOekyygpR8?si=WwGrYZXlniSiYubi)
  * **Task 1:** Use LPUART1 (Pins PG7 and PG8) to communicate via the ST-Link USB connection.
  * **Task 2, if assigned:** Practice using UART by getting a USB-to-Serial converter, and connecting it to the pins on the dev kit.
    * Write firmware that sends UART messages out on the dev kit's TX pin, and is received by a serial terminal through the UART converter's RX pin.
    * Stretch goal: Write firmware that received UART messages on the dev kit's RX pin, and then echos them back to the USB-to-Serial converter.
  * No I2C practice right now
3. (If assigned) [STM32 - FreeRTOS Guide - Video](https://www.digikey.ca/en/maker/projects/getting-started-with-stm32-introduction-to-freertos/ad275395687e4d85935351e16ec575b1)
  * After you get the tutorial working, modify the threads so that each thread blinks a different LED at a different rate.
    * For example, make LD2 blink every 3 seconds, and LD1 blink every 1.3 seconds.

#### Git Version Control
Please complete Item 1. Item 2 is a helpful read, which is essentially a review of Item 1, with more practice.

1. [Git, GitHub, and GitHub Desktop - Video](https://www.youtube.com/watch?v=8Dd7KRpKeaE)
  * Please follow along with the video for practice.
2. [Git and GitHub Desktop - Reading](https://www.codecademy.com/article/what-is-git-and-github-desktop) (optional)
  * In your test repo, try Branching.
3. [Git CLI - Presentation](https://docs.google.com/presentation/d/1wr_xPIai-Gg8E0KEQzC6v0hETkPaw800/edit#slide=id.p1) (optional)

## Version Control (Git) Process

#### Commit Message Format:
- Short Title (under 50 characters)
- Concise Description
- Testing used to verify the change

Example:
```
Improve empty string error handling in hex parser

The function parse_hex_string() would return a garbage value when given an empty string.
Changed the function to now output a zero value and return an integer error code.

Added an empty string case to the unit test.
```

### Using GitHub Desktop (Recommended)
Download and Install GitHub Desktop (link above)
1) Log in to your GitHub account
2) Select your repository (or clone it from Git)

#### Committing a Change 
If you have made changes, GitHub Desktop willl look something like this:
![changes pic](https://github.com/calgarytospace/OBC_software/blob/Onboarding/Example%20Stuff%20for%20Onboarding/pictures/changes.png?raw=true)

1) Select the boxes which associate with the files whose changes you would like to push forwared onto the repository.
2) Write a description of your commit. Generally speaking, it should be short and concise.
3) Press the commit button on the bottom left. This is prompted a change but pushed the change onto the repository (the change is pushed to your local repository)
4) Now, push the `push origin` button on the top right.

If you have any questions about this, or if you find yourself in a tricky or confusing situation with git, please **ask a lead**.
Just trying things can often make things worse.

#### Reviewing a Pull Request:
1) Look over the code and also the commit message. Ensure changes are not out of the scope of the commit message
2) Leave comments for any questions or things you think need changing
3) If you think it's good to submit, comment "Approved"
4) If you think it's not good to submit, comment "Revise"


### Using Git Command Line (Not Recommended)
For CalgaryToSpace, if you are not an expert in the github command line, **using GitHub Desktop is strongly recommended.**

GitHub Desktop's easy-to-use GUI allows for easier review and inclusion of files for commits. Identifying which files should be comitted in a change is important, as STM32CubeIDE sometimes changes/regenerates files that you do not intend to change.

<details>
<summary>Click to expand</summary>

#### Committing a Change and Submitting a Pull Request
1) Update your local repo with `git pull origin main` 
2) Create a working branch with `git checkout -b MyNewBranch`
3) Make your changes on your branch and stage them with `git add .` to stage all changes. 
4) Commit your changes locally with `git commit -m "description of your commit"`
5) Make as many commits as needed to implement the change/feature 
6) Upload the changes (including your new branch) to GitHub with `git push origin MyNewBranch`
7) Go to the main repo on GitHub where you should now see your new branch
8) Click on your branch name
9) Click on "Pull Request" button
10) Click on "Send Pull Request" to development/main 
11) Have Pull Request reviewed by 3 people
12) Pull request is good to submit after 3 Approvals

#### Submitting a Pull Request
1) Open a PR using GitHub online.

#### Modifying an Existing Pull Request
1) Make changes and stage them with `git add .` 
2) Then use `git commit –-amend --no-edit` to modify the previous commit without changing the commit message
3) Upload the changes (including your new branch) to GitHub with `git push origin MyNewBranch`
4) Update the pull request with the new changes

</details>
