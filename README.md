# Phishing-Awareness-Simulation

## Overview:

Phishing attacks remain one of the most common and effective social engineering techniques used by cybercriminals. Attackers often send deceptive emails designed to trick users into clicking malicious links or revealing sensitive information such as usernames, passwords, or financial details.

This project demonstrates a phishing awareness simulation conducted using the open-source phishing framework GoPhish. The purpose of this simulation was to understand how phishing campaigns are designed, deployed, and monitored in a controlled environment.

The exercise was performed in a virtual lab environment using Kali Linux and virtual machines to simulate both the attacker infrastructure and the target user system. This type of simulation helps organizations evaluate employee awareness and improve defenses against phishing attacks.

## Objectives:
The primary objectives of this project were:
• Understand how phishing attacks are structured and delivered
• Deploy and configure the GoPhish phishing simulation framework
• Create realistic phishing email templates
• Design a phishing landing page to simulate credential harvesting
• Launch a phishing campaign targeting test users
• Monitor and analyze user interaction metrics

Through this exercise, practical experience was gained in conducting phishing awareness simulations similar to those used by security teams in real organizations.

## Tools and Technologies Used:
The phishing simulation environment consisted of the following tools and technologies:

Kali Linux:
Used as the primary system to host the GoPhish phishing server.

GoPhish:
An open-source phishing simulation framework used to create phishing campaigns, manage email templates, host landing pages, and track user behavior.

VirtualBox:
Used to create and manage virtual machines for the lab environment.

Windows Virtual Machine:
Used as a simulated employee workstation to receive phishing emails and interact with the phishing link.

SMTP Email Service:
Used to send phishing emails from the GoPhish server to the test email account.

## Lab Architecture:
The phishing simulation was conducted inside a controlled virtual environment.
The Kali Linux machine hosted the GoPhish server, while a Windows virtual machine simulated a target user system.

## Lab Structure:

Kali Linux (GoPhish Server)
│
│ Phishing Email Campaign
│
Windows VM (User Workstation)

The Windows virtual machine received the phishing email and interacted with the phishing landing page hosted on the Kali Linux machine.

## Installing and Running GoPhish:
The GoPhish framework was downloaded and extracted on the Kali Linux system.
After extraction, the phishing server was started using the following command:
./gophish
Once started, GoPhish launches two services:

Admin Dashboard
https://127.0.0.1:3333

Phishing Server
http://0.0.0.0:80

The administrative dashboard is used to configure email templates, landing pages, campaigns, and analytics.

## SMTP Configuration:
To send phishing emails, SMTP settings were configured inside the GoPhish dashboard.

## The following parameters were configured:
SMTP From
Email address used as the sender of phishing emails.
Host
SMTP server used for sending emails.
Username
Email account used for SMTP authentication.
Password
Application password used for authentication with the email server.
After configuring the SMTP profile, a test email was sent to verify that the configuration was working properly.

## Creating the Phishing Email Template:
A phishing email template was created inside the GoPhish dashboard to simulate a legitimate security notification.

## Example subject line:
Security Alert – Please Verify Your Account
The email contained a link that redirected users to a phishing landing page. GoPhish automatically generated unique tracking links for each recipient.

## Example link:
http://192.168.100.30/?rid=XXXXX
These links allow GoPhish to track user interaction with the phishing campaign.

## Creating the Phishing Landing Page:
A phishing landing page was created to simulate a login portal where users would enter their credentials.
The landing page was configured with the following options:
- Capture Submitted Data

This option allows GoPhish to record any credentials entered by the user.

## Redirect URL
After submitting credentials, the user is redirected to a legitimate website.
This configuration allows the simulation to mimic a realistic phishing attack while capturing interaction data.

## Creating Target Users:
A target group was created in GoPhish to define the recipients of the phishing email.
For testing purposes, a controlled test email account was added as the recipient. This ensures the phishing campaign can be safely tested without targeting real users.

## Launching the Phishing Campaign:
A phishing campaign was created by combining the following components:
- Email Template
- Landing Page
- Target Group
- SMTP Profile

The campaign URL was configured as:
- http://192.168.100.30
- Once the campaign was launched, GoPhish generated unique phishing links containing recipient identifiers   used for tracking.

## Testing the Phishing Simulation:
- The phishing email was opened on the Windows virtual machine.
- The simulated user performed the following actions:
- Opened the phishing email
- Clicked the phishing link
- Entered login credentials on the landing page

These actions were automatically recorded by the GoPhish dashboard.

## Monitoring Campaign Results:
GoPhish provides detailed analytics to monitor phishing campaign performance.

The following metrics were recorded during the simulation:
- Email Delivered
- Email Opened
- Link Clicked
- Credentials Submitted

These metrics help organizations measure employee susceptibility to phishing attacks and identify areas where additional security awareness training may be required.

## Results and Observations:
The phishing simulation successfully demonstrated how attackers can exploit user trust through deceptive emails and fake login pages. Even simple phishing messages can lead users to click malicious links or disclose sensitive information if proper security awareness training is not implemented. Organizations can use phishing simulations to educate employees, identify weaknesses, and strengthen their human security defenses.

## Conclusion:
Phishing remains one of the most common initial attack vectors used in cyber incidents. Conducting phishing simulations is an effective way for organizations to evaluate employee awareness and improve security training programs. Through this project, practical experience was gained in deploying a phishing simulation using GoPhish, creating phishing email templates, hosting landing pages, and analyzing user interaction data. This hands-on exercise highlights the importance of security awareness training in protecting organizations against social engineering attacks.

## Ethical Disclaimer:
This phishing simulation was conducted strictly in a controlled lab environment for educational purposes. No real users or organizations were targeted during this exercise.
