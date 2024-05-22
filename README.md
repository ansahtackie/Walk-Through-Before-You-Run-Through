# Capstone Project  |  HackTheBox Challenge Walkthrough 

## Objective:

Our group project focused on developing a comprehensive walkthrough for the Photon Lockdown challenge on Hack The Box (HTB). This challenge required us to crack a code and locate the hidden flag. Through collaborative efforts, we documented our approach and solutions, providing detailed insights and step-by-steo instruction to help others solve the challenge. 


## Skills Learned:

#### Penetration Testing
- Gaining practical expereince in identifying and exploiting vulnerabilities.
- Learning techniques for cracking codes and uncovering hidden flags.

#### Collaboration and Teamwork
- Working effectively with team members to solve complex problems.
- Sharing knowledge and coordinating efforts to achieve a common goal.

#### Technical Writing
- Documenting the problem-solving process clearly and comprehensively.
- Creating detailed walkthroughs that can be understood and followed by others.

#### Problem-Solving
- Applying critical thinking and analytical skills to overcome challenges.
- Developing systematic approaches to troubleshooting and resolving issues.

#### Research and Analysis
-  Conducting thorough research to understand the challenge requirements.
-  Analyzing different methos and techniques to find the most effective solution.

#### Persistence and Patience
- Demonstrating determination in solving complex challenges.
- Learning to be patient and methodical in the face of difficult tasks.

#### Communication Skills
- Effectively communicating technical details and findings to team members.
- Presenting the final walkthrough in a clear and organized manner.


## Tools Used:

#### Virtual Machines
- Kali Linux virtual machine used for the project.

#### Linux Command Line Tools
- Basic command line tools like "grep", "find", "unzip", "cat", "file", "ls-la", "sudo unsquashfs" and others to solve the task.

#### Hack The Box Site
- We accessed the Hack The Box site for the challenge information and the file.
- Hack The Box (HTB) is an open source cybersecurity training platform that provides a variety of hacking experiences, from labs and challenges to capture-the-flag (CTF) competitions and educational content. The challenged solved was the "Photon Lockdown" challenge. The Photon Lockdown is a challenge that requires users to crack a code by finding a flag.



## Steps Used:

#### Accessing The Challenge from HTB
- Create an account on HTB using your email address and password. If you have an account you can log in with the email and pass word.
- Access HTB site through the Kali Linux machine. Click on the Kali icon at the top left corner to open the search box.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/31150241-0583-4ed9-8d9c-0a5fe5eb6aa4)

- In the search box type "web browser" then click on the browser.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/3cf1a459-d80b-4f53-b9c9-d43b406e7929)


- After opening the web browser, use that to access HTB website. To do that, type "hackthebox" in the web browser's search bar. 
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/935a2fc1-6f2b-4cef-883c-93256a27f85b)

- Click enter to launch onto the HTB website.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/c218fa18-7ce7-45c0-856f-cfe22e79ae83)

- Once on the site, login with your email and password.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/8397613a-1d26-4640-a8e2-497f64efd385)


- Navigate to "challenges" and look for the Photon Lockdown challenge. Look for a icon on for the challenge to download the file.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/6b119854-094e-4a6f-b7bf-3c93e2d43324)


- Click on "Download" to download the file. When you click on "Download" a pop-up winow with the file information will come up.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/822e181f-85be-4bb0-a423-2cb6b97ab26c)


- The downloaded file will be in the downloads folder. 
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/9939a20e-3746-4260-9670-47067805e42f)


- The downloaded folder can be accessed from the Kali machine. On the Kali machine, click on the blue kali icon at the top left corner of the screen to go to the Home page.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/a897bbd9-939c-4108-bce1-f9c3a5df885e)


- Next, click on "Home."
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/bb9de6af-22ec-4714-923e-c914cdfd0af6)

- On the next page, click on "Kali" to access all the home directories.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/6abb560b-9e2b-4b45-9317-470ef75e734d)


- Check/verify the Photon Lockdown zip file is located in the Downloads folder.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/e2d93607-3cba-4ff5-a1bf-9b9344751ae8)


#### Using Linux Commands To Crack The Code

- Once the Photon Lockdown file has been successfully downloaded onto the Kali machine, analysis on the file can begin to crack the code. Use Linux commands to crak the code.
- Open the terminal.
- Use the "ls" and the "ls - la" commands to access the content of the "Downloads" directory. The ls -la command provides a long list of the contents of the "Downloads" folder and also shows all hidden files. It also shows the permissions of all files.
- Verify that the Photon_Lockdown.zip file is in the "Downloads" directory.


![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/7515ea08-2249-46c7-b6ff-da8d621e6910)

- Use the "unzip" command to unzip the Photon_Lockdown.zip file.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/b5227755-d275-4ed8-acac-bcf730211e04)

- The unzipped file contains three directories:
    ONT/hw_ver
    ONT/rootfs
    ONT/fwu_ver

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/ab34586a-7fed-4dfd-bc02-eb7fbf277686)


- Use the file * command to determine the file type and what data is stored inside the following directories: 
    ONT/hw_ver
    ONT/rootfs
    ONT/fwu_ver

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/114d56b1-4a08-4449-b804-a132f4751004)

- After accessing the three directories from the Photon Lockdown file, we started looking for the required flag to solve the challenge. To do this, use appropriate Linuz commands to search through all the files and directories until the correct flag is obtianed.
- Use the "cat" command to print out the content of the three files:
    ONT/hw_ver
    ONT/rootfs
    ONT/fwu_ver

The following shows the content of the ONT/hw_ver and ONT/fwu_ver

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/c24716f5-c6ae-4021-aa29-5a866fadb138)

These two files does not give the required flag. Continue the investigations with the ONT/rootfs file.

- Use the "cat" command to print the content.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/65ebc335-bf6d-4992-a0d2-4bb61c0bb284)

The file is not a human-readable. 

- Use "file *" command to chek the file type for the ONT/rootfs file. The following is the output from the Linux command:

  ┌──(kali㉿kali)-[~/Downloads]
└─$ file * ONT/rootfs
ONT:                 directory
Photon_Lockdown.zip: Zip archive data, at least v1.0 to extract, compression method=store
ONT/rootfs:          Squashfs filesystem, little endian, version 4.0, zlib compressed, 10936182 bytes, 910 inodes, blocksize: 131072 bytes, created: Sun Oct  1 07:02:43 2023

We found that the the ONT/rootfs file is a Squashfs file system. Internet search for this type of file system revealed that the Squashfs file system is a compressed read-only file system designed for Linux. 

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/17caf706-55f7-483b-8951-7a03ef0b0278)

- Use the "sudo unsquashfs" command to unsquash the file system.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/ef904118-6c12-441f-89d0-b1b8c5f2bcf3)


Use the "ls - la" command to print the content of the ONT directory.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/6fb8f600-b64f-44e4-a27c-0f83445f01b9)

- Use the "cd" command to change directory into the squashfs-root directory. Then use the "ls - la" command to list the content of the squashfs-root directory.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/13e8b1e0-16a8-41a8-ad04-65efd757eaea)

From here, we used diffeent linux commands to change directory into specific directories and to print the content of the files to crack the code. The following screenshots show some of the commands used.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/eb36515b-7328-4f1c-baff-70ae3d11ef96)


![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/070885c8-ed91-4e17-bc49-3bfaf32c915f)


![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/8bc37a44-35fe-484d-8624-249d8a2cc595)


![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/806a1d5d-1fd4-4512-9337-c182fc70218d)


![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/b800ebc0-3d0c-4877-9179-69d46b9399e0)


After a series of trial and error approach to search through different files and directories to crack the code and not being successful, we did some research on the most efficient way to search through all the directories and files to obtain the desired flag. Through the research, we realized that we could use the "find" and "grep" commands to achieve a specific outcome. These two commands can provide a list of file names without duplicate that match a specific text string.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/40031cc2-dd27-430a-9d7a-f97217203255)

- After identifying the specific file which contained the flag, we used the "cat" command to print the output of the file hopping to get the required flag. 

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/6f0ff0b7-f2d9-4c91-9ce4-b6abb89bddd9)


We realised that the output from the "cat" command did not produce just the flag we were looking for. To identify the specific flag, used the "cat" command and pipped the output into the "grep" command to search for the string "HTB" because we knew that the required flag contained that stringe. 

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/002cf396-0164-4051-a535-398febf32aaa)


- After finding the flag, we submitted it to the HTB website to check if that was the correct code.

![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/d674e532-a6eb-41d5-87ea-ad3453e6cdb7)


- This solved the challenge.
  
![image](https://github.com/ansahtackie/Walk-Through-Before-You-Run-Through/assets/148600552/62efbd74-41da-4b25-9166-535406a86f51)



  
