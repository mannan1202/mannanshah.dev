---
title: 'Setup ssh to connect to remote server and github repo access'
description: 'simple process to setup ssh'
pubDate: 2023-01-07
---

It's just a simple thing to do, alas I spend hours getting this right cause of not getting basics right. So here it goes a simple set of instructions to set up ssh access to your remote server and setup access to github repository for code deployment.

### Step 1

First, visit this link and check if you already have ssh key generated, if not follow the instruction for the same to generate ssh keys. <a target="_blank" href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys" class="text-indigo-500 dark:text-yellow-500 font-semibold tracking-wider">Checking for existing SSH keys
</a>

### Step 2

Copy the contents of any .pub file based on the instruction followed from above link.

### Step 3

Login to your remote server using following command and enter your password.

```
ssh <USER>:<YOUR_IP_ADDRESS>
```

### Step 4

Check if .ssh folder is present in your remote server, if not using this command to create a directory

```
mkdir .ssh
```

Post that create a file called <em>authorized_keys</em>. Once done, enter the following command to open the file

```
nano ~/.ssh/authorized_keys
```

Copy the contents of the .pub file and save it. Once you are done, exit from the remote server and try to connect through ssh without using password by using this command again.

```
ssh <USER>:<YOUR_IP_ADDRESS>
```

### Step 5

This step is to connect to github repository for code deployment to remote server, first generate ssh key using Step 1 in your remote server, copy .pub file contents generated. Than go to this link and follow instruction <a target="_blank" href="https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account" class="text-indigo-500 dark:text-yellow-500 font-semibold tracking-wider">Adding a new SSH key to your GitHub account</a>

I hope it help save lot of hours of yours.

Thanks for your time to read, appericiate it.
