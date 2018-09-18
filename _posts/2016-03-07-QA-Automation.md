---
layout: slide
title: Code4Arc Lightning Talk - QA Automation
excerpt: "A lightning talk presented at the 2016 Code4Arc pre-conference focused on using consumer software to automate the web archiving quality assurance process."
theme: sky
transition: slide
tags: [presentation]
category: presentation
---
<section data-markdown>

# Web Archiving <span style="color: #a23">Automation</span>

### Creating a workflow for web archiving QA

<small>[Todd Stoffer | NCSU Libraries](mailto:tdstoffe@ncsu.edu) / [@toddstoffer](www.twitter.com/toddstoffer) / [toddstoffer.com](www.toddstoffer.com)</small>

</section>

<section data-markdown>

## Web Archviing QA Automation

#### by <span style="color: #a23">NCSU Libraries</span>

*   Just Starting
*   Looking for Workflow Ideas
*   Utilizing Student Staff
*   Using Automation to Reduce Overhead

</section>

<section data-markdown>

## Automation

*   Reduces Redundancy
*   Increases Speed
*   Provides a 'Paper Trail'

</section>

<section data-markdown>

## Utilizing Consumer Software

*   Google App Scripts
*   Trello
*   IFTTT

</section>

<section data-markdown>

## Google Forms

Make it easy for student staff to make qualitative decisions. They don't need to know how to fix it, just that it is broken.

</section>

<section data-markdown>

## Google App Script

    	function formSubmitReply(e) {
    	var sheet = SpreadsheetApp.getActiveSheet();
    	var row =  SpreadsheetApp.getActiveSheet().getLastRow();

    	var sendToEmail = "[trelloboardemail]@boards.trello.com";
    	var issueNumber = row;

    	//Overview information to be included in every ticket
    	var seed = e.values[3];
    	var wayback = "https://wayback.archive-it.org/5838/*/"+ e.values[3];
    	var crawlId = e.values[5];
    	var crawlDate = e.values[6];

    	//Display error information, to be included in tickets where display error == yes
    	var displayError = e.values[10];
    	var displayErrorSource = e.values[11];
    	var displayErrorType = e.values[12];
    	var displayErrorDetails = e.values[13];
    	var displayErrorImage = e.values[14];

    	//Scope Error information, to be included in tickets where scope error == yes
    	var scopeError = e.values[15];
    	var scopeErrorUrl = e.values[16];

    	//Outstanding error information
    	var otherError = e.values[17];
    	var otherErrorDetails = e.values[18];

    	//Messages to Include in Every Ticket Body
    	var crawlDetails = "Crawl ID: " + crawlId + "\n" + "Date Completed:" + crawlDate + "\n" + "Seed: " + seed +"\n" + "Wayback Link: " + wayback;

    	//Specific Error Details

    	//Add Message for Display Issues
    	var displayIssues;
    	if (displayError == "Yes") {
    	displayIssues = "Display Issues: " + displayError + "\n" + "Display Error Source (Wayback, Proxy, Live): " + displayErrorSource + "\n" + "Display Error Type: " + displayErrorType + "\n" + "Display Error Details: " + displayErrorDetails + "\n" + "Screenshot: " + displayErrorImage;
    	}
    	else { displayIssues = "Display Issues: No Display Issues";
    	}

    	//Add Message for Scope Issues
    	var scopeIssues;

    	if (scopeError == "Yes") {
    	scopeIssues = "Scope Issues: " + scopeError + "\n" + "Sample Scope Error URLs: " + scopeErrorUrl;
    	}
    	else {scopeIssues = "Scope Issues: No Scope Issues";
    	}

    	//Add Message for Other Issues
    	var otherIssues;

    	if (otherError == "Yes") {
    	otherIssues = "Other Issues Present? " + otherError + "\n" + "Other Error Details: " + otherErrorDetails;
    	}
    	else {otherIssues = "Other Issues Present? No";
    	}

    	//Email Message Construction
    	var subject = "Ticket Number: " + issueNumber;

    	var emailBody =  crawlDetails + "\n\n" + displayIssues + "\n\n" + scopeIssues + "\n\n" + otherIssues;

    	//Send Email Only If Errors Present
    	if(displayError == "Yes" || scopeError == "Yes" || otherError == "Yes") {
    	MailApp.sendEmail(sendToEmail, subject, emailBody)
    	}

    	}​

</section>

<section data-markdown>

# The End

</section>
