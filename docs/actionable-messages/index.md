---
title: What are actionable messages in Office 365? | Microsoft Docs
description: Learn about actionable messages in Outlook email and connectors for Groups and Teams.
author: jasonjoh

ms.topic: article
ms.technology: office-365-connectors
ms.date: 04/26/2017
ms.author: jasonjoh
---

# Actionable messages in Outlook, Office 365 Groups, and Microsoft Teams

Outlook Actionable Messages allow users who are subscribed to Office 365 to complete simple tasks against external services right within Outlook, so users can save time by avoiding the need to switch between applications.

Office 365 provides two solutions to enhance productivity with Outlook Actionable Messages: actionable messages via email, and actionable messages via Office 365 Connectors.

## User Experience

Let's take a look at the end-to-end user experience for both an email-based and a connectors-based actionable message scenario.

### Actionable messages via email: expense approval scenario

A Contoso employee submits an expense report to the internal system. That system sends an Actionable Message to the person who is to approve or reject the expense. The card included in the message contains all the information the approver might need to quickly understand who submitted the expense, the total amount, and more. It also includes **Approve** and **Reject** actions that can be taken right from Outlook:

![An expense report message card rendered in Outlook](images/expense-report-approval.png)

The recipient decides to approve the request, and clicks the **Approve** action: 

![An expense report message card displaying a spinner, indicating it is processing a user action](images/expense-report-progress.png)

Outlook makes a request to the expense report approval system, and the expense report is marked as "approved" in the system. As a result, the card is refreshed to indicate the new status of the expense report:

![The refreshed card rendered in Outlook](images/expense-report-refresh.png)

### Actionable messages via Office 365 Connectors: task management scenario

Adele Vance and her team use Trello as their task management system. Adele has configured the Trello connector in her account, and will receive granular notifications as activity occurs in the Trello boards she is interested in.

Shiva, in Adele's team, creates a new Trello card in the "Hiring" board. He needs the latest job postings to be published. Adele receives an actionable message that tells here all about the new card and the task it represents: who created it, in which list, what the due date is, and more.

![A Trello connector card with actions](images/trello-card-actions.png)

Adele has a few notes she recently took on a piece of paper with important things that should be mentioned in the job postings. She decides to add these as a comment to the Trello card. She clicks the **Add a comment** action, and is presented with a text input field in which she can type her notes:

![The "Add a comment" action UI with a text input](images/trello-card-add-comment.png)

Adele then clicks the **Save** button, and the notes are immediately saved to the Trello card. A confirmation appears at the bottom of the message:

![The ](images/trello-card-infobar.png)

## Action types

Outlook Actionable Messages support two types of actions: calling an external service via HTTP POST, and opening a URI.

### Calling an external service

The [`HttpPOST`](card-reference.md#httppost-action) action type calls an external service. It supports collecting input from the user and including that in the call.

#### Actions without input

There are many scenarios where the user is expected to confirm a pre-defined request. For example, marking a task as complete or approving access requests to documents. In these scenarios a simple click of a button can invoke an action.

#### Actions with input

Actionable messages can be used to support several scenarios with input. Some scenarios require specialized controls to support them. Here's some example of scenarios corresponding to the controls that are available with actionable messages.

- Date input: The date control enables many scenarios where a date input is desired. For example, it can be used for setting due dates for tasks/projects.
- Choosing from a list: The list box control enables scenarios that require users to pick a value from a pre-defined list. For example, setting a stage for a lead in a CRM system, setting the status of an issue in an incident tracking system.
- Text input: The text box control enables scenarios that require the user to enter text, such as commenting on an assigned task.

### Opening a URI

The [`OpenUri`](card-reference.md#openuri-action) action type opens a URI, either in a browser or as a deep link into an app. This is typically used to view the content that was received in the actionable message directly in the service.

## Office 365 Connectors for Groups and Microsoft Teams

Office 365 Connectors are a great way to get useful information and content into your Office 365 Groups or Microsoft Teams. Any user can connect their group or team to services like Trello, Bing News, Twitter, etc., and get notified of activity from that service. From tracking a team's progress in Trello, to following important hashtags in Twitter, Office 365 Connectors make it easier for an Office 365 group or Microsoft Team to stay in sync and get more done. Office 365 Connectors currently have over 50 connectors with dozen or more to be added each month.

Office 365 Connectors for Groups is broadly available in Outlook 2016, Outlook on the web and the Groups mobile app for iOS and Android. It is also available in Microsoft Teams on web, desktop, iOS and Android.

Office 365 Connectors also provide a compelling extensibility solution for developers. Developers can build connectors through incoming webhooks to generate rich connector cards. Additionally, with the new "Connect to Office 365" button, developers can embed the button on their site and enable users to connect to Office 365 groups. Try them today as part of our general availability!

## Accessing Office 365 Connectors from Outlook

Office 365 Connectors for Groups are available to any Office 365 Mail user. They are available by default when you navigate to any Group from Outlook on the web. To access Outlook on the web, simply connect to [https://outlook.office.com/owa](https://outlook.office.com/owa) from your favorite browser.

Once you are in the Office 365 Mail app, navigate to any Group or create a new Group first and then select **Connectors** as shown in the screenshot.

![A screenshot of the menu on a Group in the Office 365 Mail app](images/group-menu.png)

![A screenshot of the Connectors menu on a Group in the Office 365 Mail app](images/group-connectors-menu.png)

Check out our end-user documentation to learn more on how to <a target="_blank" href="https://support.office.com/en-us/article/Connect-apps-to-your-groups-ed0ce547-038f-4902-b9b3-9e518ae6fbab?ui=en-US&rs=en-US&ad=US">connect apps to your groups</a>.

## Accessing Office 365 Connectors from Microsoft Teams

From Microsoft Teams, you can easily add and configure connectors for any channel, either from the channel context menu or in the channel header.

![A screenshot of the channel context menu in Microsoft Teams](images/teams-context-menu.PNG)

## Release Notes 

Currently, you can only configure connectors from Office 365 Outlook and Microsoft Teams on the web, but you can view information posted by Connectors to your Group or Team by multiple clients such as Outlook on the web, Outlook 2016 and the Office365 Groups Mobile app, as well as Microsoft Teams web, desktop, and iOS and Android apps.

## Submit feedback 

There are multiple ways you can send us feedback.

- The in-product **Send Feedback** link (preferred)
- Post questions to [Stack Overflow](https://stackoverflow.com/questions/tagged/Office365Connectors?sort=newest) - Tag your questions with `Office365Connectors`.
- Post feedback and suggestions to <a target="_blank" href="https://officespdev.uservoice.com/forums/224641-general/category/146379-connectors">UserVoice</a>.