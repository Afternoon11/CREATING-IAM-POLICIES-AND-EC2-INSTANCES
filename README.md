# AWS IAM Policies and EC2 Access-Control Lab

A hands-on learning project exploring how AWS Identity and Access Management (IAM) controls access to Amazon EC2 resources.

## Objective

Understand how IAM users, groups, policies, and EC2 resource tags can be used to separate access to development and production resources.

## Services and Concepts

- **AWS IAM:** Identity and access management.
- **IAM users and groups:** Identities and collections of identities.
- **IAM policies:** JSON documents defining allowed and denied actions.
- **Amazon EC2:** Virtual compute instances.
- **Resource tags:** Key-value labels used to organize resources and, where supported, help scope permissions.

## Lab Overview

1. Launched or reviewed EC2 instances representing development and production environments.
2. Explored resource tags such as `Env=Development` and `Env=Production`.
3. Created and reviewed IAM policies intended to restrict access to the relevant environment.
4. Explored IAM users and groups to manage permissions.
5. Tested access with a lab identity and reviewed the IAM Policy Simulator.

## Understanding an IAM Policy

- **Effect:** `Allow` or `Deny`.
- **Action:** API operations covered by a statement.
- **Resource:** Resources to which the statement applies.
- **Condition:** Optional rules that further restrict a statement.

An explicit `Deny` takes precedence over an `Allow`. Policies should grant only the actions and resources required.

## Security Lessons

- Follow the principle of least privilege.
- Avoid broad permissions such as `ec2:*` unless justified.
- Scope policies to intended resources and supported condition keys.
- Do not treat resource tags alone as a security boundary.
- Enable MFA and protect root credentials.
- Prefer IAM roles and temporary credentials where appropriate.
- Never commit access keys, passwords, or sensitive account details.

## What I Learned

This lab introduced how IAM policy statements work, how groups can simplify permission management, and why access must be tested against the exact action, resource, and conditions.

## Further Improvements

- Add a sanitized copy of the final policy JSON.
- Include a test matrix of actions, resources, expected results, and observed results.
- Document the condition keys used and validate them against current AWS documentation.

---
A learning lab only. Validate policies in a test account before using them in production.
