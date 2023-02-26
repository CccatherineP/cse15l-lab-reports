# Lab Report 4
## Step 1: Log into ieng6
* By using `ssh xpang@ieng6.ucsd.edu` in the command line, which helps us to log into our remote account
  Here, I use 1 `<up>` to get this command line, which is stored in the search history
![step4_login ssh](https://user-images.githubusercontent.com/122485099/221393673-1e4c1ef7-f940-4acc-81e3-890f46e630de.jpg)
## Step 2: Clone your fork of the repository from your Github account
I clone my fork of the repository from my Github account:<br />
by using `git clone git@github.com:CccatherineP/lab7.git/lab7.git`<br />
In this step, I think it's easier for me to just type `git clone` first, and then copy and paste the ssh key from the website, the paste key for mac is `control c`
 ![image](https://user-images.githubusercontent.com/122485099/221402869-523b6c3a-c393-4a07-972e-5e7a37d88872.png)
## Step 3: Run the tests, demonstrating that they fail
![step6](https://user-images.githubusercontent.com/122485099/221397497-c4123ac1-6ddf-4028-906d-03a347659031.jpg)
`Keys pressed: <up><up><up><up><up><enter>, <up><up><up><up><enter>`
In this case, the first line of command was 5 up in the search history, so I used up arrow to access it, the second line of command was 4 up in the search history, so I used up arrow to access it<br />
## Step 4: Edit the code file to fix the failing test
![step7](https://user-images.githubusercontent.com/122485099/221400549-9d814243-1e8e-47ad-91a0-8f9531cd84e2.jpg)
In this step, I fix the failing test by changing the index1 in the last part of the code to index2<br />
## Step 5: Run the tests, demonstrating that they now succeed
![step8](https://user-images.githubusercontent.com/122485099/221400478-f1172fa2-e1b9-41c2-8b32-fe0a841a1c13.jpg)
I used the command `nano ListExamples.java` to edit the java file, here I typed `nano L` first, and then type `tab` which gives me java file that I needed, all I need to 
do after that is to type `.java` at the end. <br />
To run the test again, `Keys pressed: <up><up><up><up><up><up><enter>, <up><up><up><up><up><enter>`
In this case, the first line of command was 6 up in the search history, so I used up arrow to access it, the second line of command was 5 up in the search history, so I used up arrow to access it<br />
## Step 5: Commit and push the resulting change to your Github account 
![Step9](https://user-images.githubusercontent.com/122485099/221402943-3815e050-259a-48fa-8c5e-31f11fb1e00e.jpg)
* First, I typed `git add L` in the command line, then used `<tab>`, which I got the `ListExamples`, then I just add `.java` behind `ListExamples`
* Second, I typed `git commit -m "Updated` to committed the updated Git code locally
* Last, I typed `push origin main` to get everything up-to-date in my github 
## Here are some preparation for step 1 and 2
1. In order to speed up, we can generate ssh key for ieng6, here are the steps: <br />
* In your local terminal, run `ssh-keygen`
* Keep entering `<Enter>` until the program shows some text it calles the “randomart image”.
![step4](https://user-images.githubusercontent.com/122485099/221393312-93595371-6598-4987-b8f0-a3220eaad724.jpg)
* Now, log into your remote course specific account on `ieng6`
* Run `mkdir .ssh` in the terminal
* Logout of your remote account
* Now, we want to copy the public SSH key you created onto your remote account, specifically inside the `.ssh` directory you just created, in a file called `authorized_keys`.
* Scroll up a bit to where you were creating the SSH key, find the line where it says: `Your public key has been saved in: <path to your public SSH key>`, copy the path. Make sure you get the public key file, ending in `.pub`, here, not the private file.
* From your local computer, run `scp <path to your public SSH key> cs15lwi23__@ieng6.ucsd.edu:~/.ssh/authorized_keys`
Enter password when prompted (this will be the last time you have to type it!)<br />
Here is a screen shot of logging into my remote account without password<br />
2. In order to speed up, we can generate SSH Keys for GitHub<br />
* Login to ieng6 as usual 
* Run the command `ssh-keygen`, and again press Enter until the command completes and shows the “randomart image”
Next, we want to add a the public key to your Github account. This is like the step of copying the public key to `authorized_keys` on `ieng6`, but instead we’re copying to Github.
* Display the SSH public key generated above to your clipboard using cat like below; you can copy it by highlighting and right-clicking<br />
`cat <path of your ssh key .pub file>`
* Open your Github account on the browser.
* In the upper right corner, click on your profile photo, then click **Settings**.
* In the “Access” section of the sidebar, click **SSH and GPG keys**.
* Click **New SSH key** or **Add SSH key** under the “SSH keys” section.
* Add a “Title” to your key (ex: Your Name’s ieng6 machine).
* Select the “Key Type” to be an Authentication Key
* Copy your public key from the output of the `cat` command and paste it into the “Key” field
* Click **Add SSH key**
* If prompted, confirm access to your account on Github.
Go back to the `ieng6` terminal and:
* Run the following command to add Github.com as a recognized host (this avoids the scary yes/no prompt about accepting new connections the first time you connect)<br />
`$ ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts` <br />
`>> means “append stdout of the command to file”`
* Check your connection by running the following command:
`$ ssh -T git@github.com` <br />
It will say something like “Hi supercoolstudent1234! You’ve successfully authenticated, but GitHub does not provide shell access.”<br />









