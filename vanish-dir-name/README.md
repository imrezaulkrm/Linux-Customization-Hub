# Customizing Terminal Directory Name Or Bash Prompt in `.bashrc`

This guide provides step-by-step instructions to customize Terminal Directory Name Or the Bash prompt (PS1) in the `.bashrc` file. The changes will modify the appearance of the command prompt in your terminal.


## Instructions

### Step 1: Navigate to Home Directory


Open your terminal and navigate to the home directory: 
```sh
cd
```
### Step 2: Open `.bashrc` File
Open the `.bashrc` file using a text editor of your choice. In this example, we'll use `vim`:
```sh
sudo vim .bashrc
```
### Step 3: Locate PS1 Prompt Code

Look for the following line in the `.bashrc` file. This line sets the PS1 prompt:
```sh
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]:\[\033[01;34m\]\w\[\033[00m\]\$ '
```
### Step 4: Modify PS1 Prompt

Replace the line with the following code to customize the prompt:
```sh
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u\[\033[00m\]:\[\033[01;34m\]\W\[\033[00m\]\$ '
```
Explanation of changes:

-   Removed `@\h` to display only the username.
-   Changed `\w` to `\W` to display the base directory name only.
### Step 5: Save and Exit

Save the changes (in nano, press `Esc + :`, then `wq!`, and press `Enter`
### Step 6: Apply Changes

Restart your terminal or run the following command to apply the changes:
```sh 
source .bashrc
```
Now, your terminal prompt should reflect the customizations you made.

Feel free to adjust the instructions based on your preferred text editor or any additional information you'd like to include.

You can copy and paste this markdown content into a file named `README.md` in your project repository.
