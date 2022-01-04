---
layout: post
title:  "Terraform Rocks!"
date:   2022-01-03 12:41:27 -0400
categories: jekyll update
---

# OMG, where has Terraform been all my life
First of all, apologies for all my posts having exclamation marks.  I'll get those under control... some day!


I've been delving into Terraform for the last few months and I've got to say I love it.  Now i understand why everybody raves about Infrastructure as Code (IAC).  It makes building and destroying servers a blast.  In case you don't know, Terraform allows you to build cloud infrastructure via simple to read code.  From there you can use the same code to build identical prod/staging environments.  That way when you test, you can guarantee that your changes will work in production as the code essentially builds out the same environment.

# Things I learned from Terraform
* Try to have the following terraform files from the get go:
    * **main.tf** - This file contains your main infrastructure code.
    * **variables.tf** - This file contains your variable definitions.  Such as a variable for an AWS instance called *instance_type*
    * **terraform.tfvars** - This file contains all the custom values for your variables. One example: *instance _type = t2.micro*
    * **outputs.tf** - This file contains all the values that you want to spit out on the CLI.  One example would be the public IP of your eC2 instance so you can connect to it.
* Don't forget to destroy your test infrastructure when not in use, that's like leaving the lights on in empty rooms. No Bueno!
* If you are using a version control system (VCS) like git, don't forget to include a **.gitignore** in your Terraform directory so you don't accidentally copy secrets to repo's that may be public.  Last thing you want is leaked info or an AWS bill for several thousand dollars.
* Visual Studio Code is awesome for editing your Terraform code, it offers a free Terraform extension that allows it to auto-expand Terraform syntax as you are typing your code.

I'm going to continue digging into Terraform to learn modules and workspaces.  Those look to be promising.  If you get a chance, dig in your self into Terraform.  Start with youtube.  Excellent surces are Freedcodecamp and Nana Terraform.  Remember to keep learning.