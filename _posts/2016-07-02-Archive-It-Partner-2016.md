---
layout: slide
title: Archive-It Partner Meeting 2016 - Automating the QA Work Flow
excerpt: "A presentation at the 2016 Archive-It Partner Meeting, focusing on automating the QA workflow to minimize costs by utilizing student employees"
theme: simple
transition: convex
tags: [presentation]
category: presentation
---
<section data-markdown>

### Automating the Web Archiving QA Process
#### August 02, 2014 | Atlanta, GA

[Todd Stoffer - NCSU Libraries](mailto:tdstoffe@ncsu.edu)

[@toddstoffer](www.twitter.com/toddstoffer) | [tdstoffe@ncsu.edu](mailto:tdstoffe@ncsu.edu) | [go.ncsu.edu/atlanta16](https://go.ncsu.edu/atlanta16)

</section>

<section data-markdown>

## QA Automation Goals
>Speed Up This Process:

>Test Crawl > Adjust Scope > Production Crawl

</section>

<section data-markdown>
## QA Automation Goals
>While Also Doing This:

>*   Better Utilize Student Employees
>*   Document QA results for an asynchronous work environment
>*   Limit additional costs (developer time)
</section>

<section data-markdown>
## Current Web Archiving Workflow
![web archiving workflow](/images/partner-meeting/web-archiving-process.png)
</section>

<section data-markdown>
### Initial QA Workflow
![web archiving workflow](/images/partner-meeting/qa-step-1.png)
</section>

<section data-markdown>
### Task Grouping
![web archiving workflow](/images/partner-meeting/qa-step-2.png)
</section>

<section data-markdown>
### Optimized QA Workflow
![web archiving workflow](/images/partner-meeting/qa-step-3.png)
</section>

<section data-markdown>
## Tools We Use

* Google Forms
* Google Sheets
* Google App Scripts
* Trello
* SnagIT (Screenshots)
</section>

<section data-markdown>

## How it Works

![web archiving workflow](/images/partner-meeting/system-steps.png)

</section>
<section data-markdown>

## Google Forms

### [QA Automation Demo Form](httpss://docs.google.com/a/ncsu.edu/forms/d/e/1FAIpQLSfvHD8-_36y8B1C0grjay5MJWGs5rvpLqyDfLMCucyXOJWq9Q/viewform)

</section>
<section data-markdown>

## Google Sheets

### ![Google Sheets Responses](/images/sheets.png)

</section>
<section data-markdown>

## Google App Scripts
* JavaScript Platform
* In the Cloud - Always On
* Can trigger 'On Form Submit'

</section>

<section data-markdown>
## Sample Script

     'function formSubmitReply(e) {
     var sheet = SpreadsheetApp.getActiveSheet();
     var row =  SpreadsheetApp.getActiveSheet().getLastRow();

     var sendToEmail = "YOURTRELLOBOARDEMAIL@boards.trello.com, YOUREMAIL@EXAMPLE.COM";
     var issueNumber = row;

     //Overview information to be included in every ticket
     var seed = e.values[2];
     var wayback = "httpss://wayback.archive-it.org/7087/*/"+ e.values[2];


     //Display error information, to be included in tickets where display error == yes
     var displayError = e.values[3];
     var displayErrorSource = e.values[4];
     var displayErrorType = e.values[5];
     var displayErrorDetails = e.values[6];
     var displayErrorImage = e.values[7];

     //Ready to Be Included in Hunt Library Collection?
     var QAstatus = e.values[8];
     var otherErrorDetails = e.values[9];

     //Messages to Include in Every Ticket Body
     var crawlDetails = "Seed: " + seed +"\n" + "Wayback Link: " + wayback;

     //Specific Error Details

     //Add Message for Display Issues
     var displayIssues;
     if (displayError == "Yes") {
     displayIssues = "Display Issues: " + displayError + "\n" + "Display Error Source (Wayback, Proxy, Live): " + displayErrorSource + "\n" + "Display Error Type: " + displayErrorType + "\n" + "Display Error Details: " + displayErrorDetails + "\n" + "Screenshot: " + displayErrorImage;
     }
     else { displayIssues = "Display Issues: No Display Issues";
     }

     //Add Message for Ready for Inclusion
     var readyToInclude;

     if (QAstatus == "No") {
     readyToInclude = "Is this site ready to be included in Hunt Library Impact Collection? " + QAstatus + "\n" + "Reason: " + otherErrorDetails;
     }
     else {readyToInclude = "This seed passed QA and can be included in the Hunt Library Impact Collection";
     }


     //Email Message Construction
     var subject = "Ticket Number: " + issueNumber + " " + QAstatus;

     var emailBody =  crawlDetails + "\n\n" + displayIssues + "\n\n" + readyToInclude;

     //Send Email Only If Errors Present

     MailApp.sendEmail(sendToEmail, subject, emailBody)

     }​'
</section>
<section>
<section data-markdown>
## Trello Board
![Trello Example](/images/trello-board.png)
</section>
<section data-markdown>
## Trello Card
![Trello Example](/images/trello.png)
</section>
</section>

<section data-markdown>
## Other Tools to Consider

* Zapier
* IFTTT
* Excel / Macros

</section>

<section data-markdown>


## Results

* Hunt Library Impact collection
     * 244 Initial Seeds
     * Averaged 50 Seed per Day QA Rate
     * Fills in Time Gaps of Current GA
     * Reduced Go-Live Time by Months

</section>

<section data-markdown>


## Results Part 2

* NC State Websites Collection
     * Reformatted to focus on seed scoping
     * Addresses hosts with large queued document numbers
     * Able to spread QA work throughout staff
</section>

<section data-markdown>

## What's Next?

* Update script management
     - Move out to standalone scripts
     - Add version control (GitHub)
* Add additional functionality
     - Focus on quantitative measures
* Develop and publish tutorial

</section>
<section data-markdown>

## Takeaways

* Automation doesn't have to be complicated or expensive
* It's fine to automate even small portions of the process
* One tool does fit everyone, find ways to better utilize the tools you have available

</section>

<section data-markdown>

## Questions?
[Todd Stoffer - NCSU Libraries](mailto:tdstoffe@ncsu.edu)

[@toddstoffer](www.twitter.com/toddstoffer) | [tdstoffe@ncsu.edu](mailto:tdstoffe@ncsu.edu) | [go.ncsu.edu/atlanta16](https://go.ncsu.edu/atlanta16)
*********
### Demo Google Forms
[go.ncsu.edu/qa-demo](httpss://go.ncsu.edu/qa-demo)

</section>
