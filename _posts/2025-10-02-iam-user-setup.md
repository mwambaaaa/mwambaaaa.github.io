---
layout: post
title: "Create an IAM User, Step by Step (Stop Using the Root Account)"
date: 2025-10-02
author: Happyness Mwamba
description: "A beginner-friendly guide to creating an IAM user, enabling MFA, and setting up your account for safe daily use."
---

After I locked myself out of my AWS root account, the first piece of advice I got was: *don’t use root for daily work*. The fix is to create an **IAM user**. This is your everyday login, protected with MFA, while root stays tucked away for emergencies.

Here’s a step-by-step guide to creating an IAM user and signing in with it.

---

## Step 1: Sign in as root one last time
Use your root email and password to log into AWS. Head to the **IAM** service in the console.  

![AWS Console Home](/assets/images/iam/console-home.png)  
*The AWS Console home page, signed in as root.*

---

## Step 2: Create an Administrators group
- Go to **Groups → Create group**.  
- Name it `Administrators`.  
- Attach the managed policy `AdministratorAccess`.  

![Create Group](/assets/images/iam/create-group.png)  
*Creating the Administrators group and attaching AdministratorAccess.*

---

## Step 3: Create your IAM user
- **Users → Add user**.  
- Username: `happy-admin` (or something meaningful).  
- Select **AWS Management Console access** and set a strong password.  

![Add IAM User](/assets/images/iam/add-user.png)  
*Adding a new IAM user with console access.*

---

## Step 4: Add the user to your group
On the permissions page, add your new user into the `Administrators` group.  

![Add User to Group](/assets/images/iam/add-user-to-group.png)  
*Assigning the user to the Administrators group.*

---

## Step 5: Enable MFA
- Open your IAM user → **Security credentials** → **Manage MFA**.  
- Add a virtual MFA device (like Google Authenticator) or a hardware key.  

![Enable MFA](/assets/images/iam/enable-mfa.png)  
*Enabling MFA for the IAM user.*

---

## Step 6: Create an account alias
- IAM → **Account settings → Create account alias**.  
- Example: `happy-cloud`.  
- Your new login URL will be:  
