# CBATS
Cloud-Based Algorithmic Trading Strategies for Individual Investors

## Description
Effective investing strategies have historically been exclusive to professional investors and the wealthy, leaving lower and middle-class individuals with limited options for managing their investments. These groups, who could benefit most from advanced strategies, often lack access to the tools and knowledge necessary for optimizing returns while managing risk. The emergence of cloud-based platforms presents an opportunity to democratize algorithmic trading by making sophisticated strategies, such as the barbell approach, available to individual investors. The Cloud-Based Algorithmic Trading Strategies for Individual Investors project aims to develop an accessible solution for both manual and automated trading, allowing users to maximize profits while minimizing drawdown, regardless of their trading frequency or financial expertise. By leveling the playing field, we empower a broader audience to make informed investment decisions and take control of their financial futures. 

This project is under NDA so there are limited details I can share about the product itself, instead I will focus on the technologies I personally used.

[Watch Demo Video](https://youtu.be/e195tgJF-2A)

## AWS: SES vs SNS

Here’s some of the comparisons of AWS Simple Email Service (SES) and Simple Notification Service (SNS) that I found and took into account while testing each of them and deciding what was right for this particular service:

- **Purpose**
  - **SES**: Designed for sending and receiving email messages (e.g., transactional or marketing emails).
  - **SNS**: A flexible messaging service for sending notifications (e.g., to email, SMS, HTTP endpoints, SQS, etc.).

- **Primary Use Case**
  - **SES**: Sending customized, high-volume email (e.g., password resets, newsletters).
  - **SNS**: Distributing messages to multiple subscribers or triggering workflows.

- **Supported Protocols**
  - **SES**: Email (SMTP, API).
  - **SNS**: Email, SMS, HTTP/S, Lambda, SQS, mobile push (APNS, GCM/FCM).

- **Email Features**
  - **SES**: Supports full email features like attachments, rich formatting (HTML), and inbound email handling.
  - **SNS**: Limited to plain text email notifications.

- **Target Audience**
  - **SES**: Developers building email systems or integrating transactional email into apps.
  - **SNS**: Applications needing a fan-out messaging system for event-driven architecture.

- **Inbound Message Support**
  - **SES**: Yes — can receive and process inbound emails.
  - **SNS**: No — outbound notifications only.

- **Message Customization**
  - **SES**: Highly customizable emails with templates or raw MIME.
  - **SNS**: Basic text messages with limited formatting.

- **Cost**
  - **SES**: Charged per message/email and data sent.
  - **SNS**: Charged per request and delivery type (e.g., SMS messages cost more).

- **Integration**
  - **SES**: Email-focused SDK and SMTP integration.
  - **SNS**: Integrated with many AWS services for decoupled messaging and fan-out delivery.
---
After initially working with SNS, I decided for a realistic production grade service that was notifying users via email, SES was much better suited. To use SES I also had to obtain and verify a domain, which was a simple process. 


## Python
- Yahoo Finance API
- Connecting to AWS

## MongoDB
- Data storage
- Processing and formatting

