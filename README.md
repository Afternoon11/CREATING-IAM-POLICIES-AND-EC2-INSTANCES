<picture><source media="(prefers-color-scheme: dark)" srcset="https://nextwork.ai/static/nextwork-logo-paper.svg" /><img src="https://nextwork.ai/static/nextwork-logo-leather.svg" alt="NextWork" width="300" /></picture>

# Cloud Security with AWS IAM

**Project Link:** [View Project](https://nextwork.ai/projects/51a5fd24-7458-58a6-8653-9b90119a0e4a)

**Author:** AFFAN KHAN

---

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to launch an EC2 instance with some IAM Policies  I'm doing this project to learn the service to control who is authenticated (signed in) and authorized (has permissions) in your AWS account.

### Tools and concepts

Services I used were IAM User EC2 instance IAM USER GROUP Key concepts I learnt include instance creation IAM policies .

### Project reflection

This project took me approximately 4 Hours The most challenging part was finding alias in IAM console It was most rewarding to ME.

### ❤️ Thanks for doing this project!

I chose to do this project today because... Something that would make learning with NextWork even better is...

## Tags

### What I did in this step

In this step, I will Launch two Amazon EC2 instances so that we can increase NextWork's computing power! because to Boost our computing power to match increased traffic to the website. Lots of new students want to learn with NextWork over the break!

### Understanding tags

Tags are development and production

### My tag configuration

The tag I’ve used on my EC2 instances is called Env The value I’ve assigned for my instances are Production and Development.

![Tags](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_2e0e5a5d)

## IAM Policies

### What I did in this step

In this step, I will Create an IAM policy that gives access to the development instance. because We don't want them to accidentally shut down the platform or push their changes to the production environment while they're just testing things! .

### Understanding IAM policies

IAM Policies are Identity and Access Management policies. I will use AWS IAM to manage the access level that other users and services have to your resources.

### The policy I set up

For this project, I’ve set up a policy using...

### Policy effect

I’ve created a policy that allows some actions (like starting, stopping, and describing EC2 instances) for instances tagged with "Env = development" while denying the ability to create or delete tags for all instances.

### Understanding Effect, Action, and Resource

The Effect, Action, and Resource attributes of a JSON policy means \
‍Effect

‍This can have two values - either Allow or Deny - to indicate whether the policy allows or denies a certain action. Deny has priority. Looking at the first statement, "Effect": "Allow" means this statement is trying to allow for an action.

‍Action

‍A list of the actions that the policy allows or denies. In this case, "Action": "ec2:\*" means all actions that you could possibly take on EC2 instances are allowed. Woohoo!

‍Resource

‍Which resources does this policy apply to? Specifying "\*" means all resources within the defined scope (see the next point).

## My JSON Policy

![My JSON Policy](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_1c864649)

## Account Alias

### What I did in this step

In this step, I will give our intern access to the development instance. because the intern can't wait to start

### Understanding account aliases

An account alias is a friendly name for your AWS account that you can use instead of your account ID (which is usually a bunch of digits) to sign in to the AWS Management Console.

### Setting up my account alias

Creating an account alias took me half hour Now, my new AWS console sign-in URL is https://nextwork-alias-affankhan

![Account Alias](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_0eb4439b)

## IAM Users and User Groups

### What I did in this step

In this step, I will Create IAM Users and User Groups because Its my choice!

### Understanding user groups

IAM user groups are a collection/folder of IAM users. It allows you to manage permissions for all the users in your group at the same time by attaching policies to the group rather than individual users.

### Attaching policies to user groups

I attached the policy I created to this user group, which means  that will get access to your resources/AWS account, whereas user groups are the collections/folders of users for easier user management..

### Understanding IAM users

IAM users are  the people that will get access to your resources/AWS account, whereas user groups are the collections/folders of users for easier user management.

## Logging in as an IAM User

### Sharing sign-in details

The first way is by url or by sign in details

### Observations from the IAM user dashboard

Once I logged in as my IAM user, I noticed that i was access denied from everything This was because i don't have access

![Logging in as an IAM User](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_6f2ab446)

## Testing IAM Policies

### What I did in this step

In this step, I will... because...

### Testing policy actions

I tested my JSON IAM policy by shutting down the other instance.

### Stopping the production instance

When I tried to stop the production instance i got a big red angry error. This was because i was not authorize for that action.

![Testing IAM Policies](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_0e7a9d6a)

### Stopping the development instance

Next, when I tried to stop the development instance... i got the error  This was because of group policies which take place in .

![Testing IAM Policies](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_1811801c)

## IAM Policy Simulator

To extend my project, I'm going to use policy simulator I'm doing this because i want too

### Understanding the IAM Policy Simulator

The IAM Policy Simulator is... It's useful for...

### How I used the simulator

I set up a simulation for... The results were... I had to adjust...

![IAM Policy Simulator](https://nextwork.ai/appreciative_pink_proud_lynx/uploads/51a5fd24-7458-58a6-8653-9b90119a0e4a_069d8a621)
