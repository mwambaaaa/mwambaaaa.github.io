---
layout: single
title: "How I Locked Myself Out of AWS (and What I Learned About Root Accounts)"
date: 2025-10-01
categories: [AWS]
tags: [root-user, IAM, MFA, beginner, lesson-learned]
author: Happy
description: "A personal story about losing access to my AWS root account, and why you should create IAM users from day one."
---

When I first opened my AWS account, I had no idea what IAM was. I signed in with my root email and thought that was normal. Then I made the mistake that locked me out for months: I lost access to my MFA device.

Without my authenticator, I couldn’t log in at all. I tried recovery codes, email verifications, even creating a new account, but nothing worked smoothly. That period taught me one thing: depending on the root account is risky.

A few months later, I attended an Africa HackOn meeting, trying to connect with other security professionals. I mentioned my situation and asked, *what happens if you lose your MFA device?* One person looked at me and said, “Oh girl, you messed up big time.” Then they explained IAM.

---

## What is IAM?
IAM stands for **Identity and Access Management**. It’s AWS’s way of creating separate users and permissions so you don’t use the root account for daily work.  

With IAM you can:  
- Create users with their own usernames, passwords and MFA.  
- Assign permissions through groups and policies (like Admins, Developers, Auditors).  
- Control exactly who can do what, instead of giving everyone root-level power.  

---

## Why it matters
The root account is like the master key to your entire AWS house. If you lose it or it gets compromised, there’s no backup door. IAM lets you share access, apply least privilege, and protect yourself from lockouts like mine.

---

## Lesson I learned
- **Root account = emergency only.** Use it for billing, support, or rare account-wide settings.  
- **IAM users = daily life.** Give yourself an admin IAM user with MFA and use that login every day.  
- **Backup your MFA.** Store recovery codes or use a hardware key you can keep safe.  

---

Losing months of AWS practice was painful, but it gave me a story and a first lesson worth sharing. If you’re just starting with AWS: create an IAM user today. Don’t wait for a mistake to teach you.
