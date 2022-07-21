---
title: Preparing for Submission
permalink: /assignments/pa2_4_submit
key: assignments-pa2_4_submit
layout: article
nav_key: assignments
sidebar:
  nav: assignments
license: false
aside:
  toc: true
show_edit_on_github: false
show_date: false
---

If you have reached this stage, you have completed 95% of this assignment, <span style="color:#f7007f;"><b>congratulations</b></span>! One final step is some <span style="color:#f77729;"><b>administrative work</b></span> that will help your instructors grade your assignments seamlessly. 

Please read this section very very carefully and watch the given demo with your full attention. 
{:.error}

You are expected to <span style="color:#f77729;"><b>store</b></span> TWO additional files each time a client send a file to the server:
1. Client to save encrypted files to `source/send_files_enc` before sending, with the name: `enc_[filename]`, e.g: `enc_image.ppm` if it is sending `image.ppm` to the server. 
2. Server to save received encrypted file to client to `source/recv_files_enc` before decrypting, with the name `enc_recv_[filename]`, e.g: `enc_recv_image.ppm`. 

You should have the following files now:
<img src="/50005/assets/images/pa2/2.png"  class="center_fifty"/>

The new files are mainly (<span style="color:#f7007f;"><b>names must be exactly these!</b></span>):
1. `server_signed.crt`, and `server_private_key.pem` under `source/auth`
2. `ClientWithSecurityAP/CP1/CP2.py` and `ServerWithSecurityAP/CP1/CP2.py`. 

All other files inside `source/files` directory must remain as per the original files.

You can now run the autograder yourself, assuming your current working directory is at the same level as `source/`. The second argument can be 1 or 2 depending on whether you want to test CP1 or CP2. 
```
python3 autograde.py 1
python3 autograde.py 2
```

You should have the following message if everything goes well (`8` marks for CP1, and `14` marks for CP2). The 8 marks for CP1 will be mapped to 2% of your grade, and the 18 marks for CP2 will also be mapped to 2% of your grade. 

<img src="/50005/assets/images/pa2/3.png"  class="center_fifty"/>

You should then make the final commit of all tracked files so far:
```
git commit -a -m "feat: save to recv_files_enc and send_files_enc before encrypting and before sending" 
```

You can also put your own large files at `/source/files` (>100MB) to <span style="color:#f77729;"><b>test</b></span> internally, but <span style="color:#f77729;"><b>remove</b></span> it before pushing to Github since it doesn't allow you to push any single file >100MB. Please <span style="color:#f77729;"><b>do not use</b></span> `git-lfs`.  
{:.info}

# Demo 
The following gif shows the expected interaction between Server and Client processes.

<img src="https://www.dropbox.com/s/ajjzhzh9zcv1rfo/pa2.gif?raw=1"  class="center_ninety"/>

# Submission
Go to our bot and type `/start`. Follow the instructions there. You're only required to submit the github remote repo link. Ensure that you have invited `natalieagus-sutd` as collaborator. 

<span style="color:#f7007f;"><b>We will clone your repo for grading. Make sure you check that it runs with the given autograder before submitting.</b></span> The bot <span style="color:#f77729;"><b>WILL NOT</b></span> report any marks to you. We will mark your submission after all submissions are collected. 

And it goes without saying that submitting any unrunnable code grants you <span style="color:#f7007f;"><b>0</b></span>. This <span style="color:#f7007f;"><b>includes</b></span> using other modules that's not already been stated in the starter code. Please <span style="color:#f7007f;"><b>do NOT</b></span> import anything else. Our VM will not have any other modules installed to run your script.
{:.error}





