---
title: Frequently Asked Questions
description: FAQ
hide_table_of_contents: true
sidebar_label: Frequently Asked Questions
---

# FAQ

### Onboarding

**How do I add more users to the Antimetal Platform?**  

You can add more users to the Antimetal platform via the Members section, found under settings at the bottom left of the dashboard.  
Settings -> Members -> Enter User Email Address -> Select Permission ->Send Invite  

*Note- Only Admins on the account can make changes to budgets, approve savings, and acknowledge guardrail recommendations*  

<br></br>

**What do I need before my onboarding call?**  

Before your Antimetal onboarding call, we highly recommend:  
- Downloading your historical Cost Explorer data (as far back as you want)  
- Credit card you can use  
- Administrator access to the account you want to onboard to the Antimetal organization  

<br></br>

**How do I download my historical cost explorer data from AWS?**  

For a step-by-step guide on how to download this information from AWS Cost Explorer, please follow the guide [here](/onboarding/csv.md).  

<br></br>

### Savings

**Where do we see how much Antimetal is actually saving us? Is that the Monthly Savings KPI on the top right? These numbers seem to be lower than expected.**  

Monthly savings are the unique savings generated by Antimetal (excludes any savings instruments you purchased or came in with when joining).  

<br></br>

**What's the difference between the savings that are automatically accounted for, and those that are pending approval? Why do they require approval?**  

We automatically approve savings plan recommendations (for Sagemaker and Compute since they are extremely flexible). We expose RI recommendations to you and filter the RI recs for ones that we feel are stable and good choices; however, you know your infrastructure better than us, so we require you to approve any recommendation before making those purchases.  

<br></br>

**How often are SPs(Savings Plans) and RIs (Reserved Instances) information pulled into the Antimetal Platform?**  

SP and RIs information are pulled daily into the platform.  

<br></br>

### Billing

**I am looking to understand the differences between what's on the invoice and what's in AWS billing.**  

The reason here and why Antimetal gives “risk-free savings”, is that you might get savings by consuming savings instruments in another person’s account.  

For example, Company X used a savings plan in Company Y’s account to cover their EC2 spend (since Company X is not using the whole thing). However, AWS doesn’t show the associated savings plan cost on Company X’s account, since Company Y was the one to purchase the instrument, but Antimetal will still display these savings on Company X dashboard.  

Let’s say Company X received $1416.10 in savings. Company X received those savings by using $711.41 of savings instruments in other companies' accounts (i.e Company Y). To be equitable, we pass on any savings instruments cost you consumed to you—it wouldn’t be fair to charge Company Y for savings plan usage used by Company X.  

For more specific questions regarding differences between your companies’ invoices and AWS cost explorer, please contact support@antimetal.com.  

<br></br>

### AWS Questions/Issues

**Why am I getting permission denied when trying to enable the resource cost group in the cost explorer?**  

Enable the following setting from AWS in the company account requested. Please note that this change will be enabled within 48 hours  

<br></br>

**How do I create new cost allocation tags?**  

All tags that you apply to any resource become cost-allocation tags as soon as they are approved. After you create any new tags, Antimetal will approve these tags as cost allocation tags so you can view them in the cost explorer/CUR/etc.  

<br></br>

**What are the implications of leaving my AWS organization?**  

We do not create an “OrganizationAccountAccessRole” in your account when you join our organization, preventing us from getting admin access to any parts of your account. Any administrative changes would need to be explicitly accepted by you via a “handshake”. Read the [<u>**AWS documentation here**</u>](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_manage_accounts_invites.html#:~:text=However%2C%20unlike%20created%20accounts%2C%20the%20OrganizationAccountAccessRole%20IAM%20role%20is%20not%20automatically%20created%20in%20the%20member%20account%20with%20permissions%20for%20the%20management%20account%20to%20assume.).
