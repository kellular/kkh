---
layout: project
title: IBM dashDB
duration: March 2015—July 2016
thumbnail: index-dashdb
---
<div class="o-wrap" markdown="1">
###### This was the first product team I joined at IBM after finishing Designcamp, a three-month on-boarding program for new designers at the company. With this particular project, we were unable to deliver value for the user and the business in the end. I chose to share this project because it was a humbling lesson in understanding business requirements and user needs, while also aligning between disciplines across the team.
~
# IBM dashDB
### dashDB is a cloud data warehouse where companies can bring together all of their data and house it within one location so that they can run queries, extract information, and perform analytics in order to drive business insights.
<hr>
## Overview
### Problem
Loading data was a major pain point in dashDB. Users worried that automated loads were not updating in tables properly. Stressed by their lack of direct visibility into the server, users found it challenging to keep everyone in the organization on the same page as data structures in dashDB evolved.

### Design prompt
How might we help data warehouse architects quickly and confidently load data from multiple sources into dashDB and minimize the need to worry about it?

### Role and team
As a visual and interaction designer, I divided my time between working with developers to make improvements to the current product, as well as creating concepts for the new version.

I worked with a UX designer, two content designers, one researcher, and one front-end developer.
<hr>
## Ecosystem of personas
![dashDB Personas](../../images/dashdb-personas.png)

Our main persona was the data warehouse architect. This person does the initial setup, architects the data system, sets access controls, connects new tools, and updates warehouse with additional sources.

As secondary personas, the data analyst and report developer were the consumers of the data that loads into dashDB. The data analyst runs hypothesis testing and works in the product's SQL editor. The report developer builds reports and dashboards for analysis throughout their company.

### Discovering our users
A persistent blocker for us was that we did not have direct access to people who used dashDB. Much of our connections to people who worked with other cloud data warehouses came from grassroots efforts initiated by myself and our user researcher. Both of us would literally search for people on LinkedIn and reach out for an interview, or tap into our social media networks. This strategy landed us several user interviews, which informed a better understanding of the domain. (secondary research)
<hr>
## Making sense of the product and landscape
I was brand new to the analytics and data warehousing domain. I knew next to nothing about this world. At times, ramping up to speed felt overwhelming, but I was excited and determined to figure this out.

One method that helped tremendously was mapping concepts out and validating them with subject matter experts on our team. These diagrams helped me develop relationships with teammates who were not colocated with me. After they saw how eagerly I wanted to understand the product and how much I valued their knowledge, the door for stronger collaboration was opened. The diagrams below have less to do with the interface output and more to do with the product functionality, domain vocabulary, and flow of data into and out of dashDB.

![dashDB food analogy](../../images/dashdb-food-analogy.png)
###### A grocery store analogy explained to me by an architect on the product. The grocery stores are a representation of the data sources a company can have. The truck transporting the groceries represents the extract, transform, and load process. The refrigerator is the data warehouse, or dashDB in our case. The characters grabbing food from the refrigerator are analysts querying data from the warehouse for analysis.

![dashDB set-up diagram](../../images/dashdb-setup-diagram.png)
###### A basic overview of how a user sets up dashDB. After purchasing a payment plan, the load architect will use a third-party tool to connect data sources to dashDB. Then inside dashDB, the architect sets up table structures and schedules the load jobs.

![dashDB schemas](../../images/dashdb-schemas.png)
###### Schema is a good example of terminology in dashDB that was confusing for both our users and our team. The conceptual relationship between schemas and tables in dashDB was different than how they are traditionally organized in data warehousing.
<hr>
## Assessing the current data load flow
![dashDB As Is Load flow](../../images/dashdb-as-is-load-flow.png)

Our UX designer and I went through the load flow in the current product. At the time, a user could load data from five different sources: desktop, cloud, geospatial datasets, Twitter, or an open-source data set. Since we did not have strong insights into user pain points, our UX designer and I came up with assumptions to explore and validate later:

1. Users had trouble understanding the five load options
2. Users had no clear insight into the status of the load job
3. Users could not load data from multiple sources in one job
4. Users want the option to preview their data before loading it into dashDB
5. Users liked the idea of the progress tracker, but needed clearer copy
6. Users did not receive confirmation from the product that their load job was scheduled
</div>

{% capture background-alt %}

<div class="o-wrap" markdown="1">
## Proposing a new approach
Based on our assumptions, we worked on a new user flow and experience. We presented the following concept to our offering manager and development team.

![dashDB Load Hub and credentials](../../images/dashdb-loadhub-creds.png)
###### Users would land on the Load Hub, where they can start a new load and/or view their current load jobs.

**Assumptions:**
1. Users had trouble understanding the five load options
2. Users had no clear insight into the status of the load job

**Design decisions:**
- Consolidated the five load options into two choices. This was because four of the original options were cloud sources, all with similar steps for loading data into dashDB.
- Provided more transparency into the current load jobs, so we included the source name, the target table, and the status and time remaining.
- Proposed functionality to pause, restart, edit, or delete the job altogether.
- Current interface had accessibility issues with input fields. There was a lack of immediate feedback and confusing copy.

![dashDB source and target](../../images/dashdb-source-target.png)
###### After selecting the data source, users can preview the incoming data and the target table

**Assumptions:**
3. Users could not load data from multiple sources in one job
4. Users want the option to preview their data before loading it into dashDB
5. Users liked the idea of the progress tracker, but needed clearer copy

**Design decisions:**
- Organized data files into a tree structure navigation to help users see the context of which their data is coming from
- Exposed a preview of the data in a table format
- Pitched a shopping cart concept where users could add multiple files to a queue to load in one job

![dashDB schedule and summary](../../images/dashdb-schedule-summary.png)
###### Users would then schedule the load job and receive a confirmation

**Assumptions:**
6. Users did not receive confirmation from the product that their load job was scheduled

**Design decisions:**
- Rewrote form field copy so that it was more direct and friendly
- Broke out scheduling sections into a step-by-step conversational format
- Provided a receipt page to summarize the load job before users returned to the load hub

</div>

{% endcapture %}

{% include background-alt.md %}

<div class="o-wrap" markdown="1">
##
Shifting with the business needs

<hr>
## Reflecting
### We did not understand our user, their workflow, and their needs
It was difficult for us to understand our users true problems with the product. Despite conducting secondary research and making the best decisions we could at the time, not having the opportunity to test these designs made it challenging to validate our assumptions.

**What I learned**
- Users need to be at the core. Product decisions should be driven by data and insights drawn from user research.

### Lack of visibility into the business strategy
Our design team did not have insight into the product strategy until much later when we learned from the product owner that the top focus was performance and security. As a result, we shifted focus to stakeholder interviews with key people across the platform in order to gain a better understanding of how we could best support the team.

**What I learned**
- No product discipline should work in a silo. Initially our design team worked separately from the wider team of offering management and engineering. This contributed to basic user flow inaccuracies and functionality that simply was not feasible.
- Scope is critical. dashDB Load is a massive section of the product. At the start of this project, we wanted to cover all load options but this proved to be too ambitious for the timeline.


### We designed in a vacuum
With a fairly inexperienced design team, there was a lack in knowledge of the importance of communicating with offering management and development so that we could move forward as a team.

**What I learned**
- Never assume you have expertise. We were the newest people to join the dashDB team. Collectively we made the egotistic mistake of pitching new design concepts under the assumption that because we were designers that meant we understood what “good user experience” meant in this product context.
- Designers should understand the technical context. dashDB was built on older technology, which greatly impacted how much of the front-end interface we could influence. There was a huge disconnect between our new design team and our established development team. A lot of our prototypes were grand ideas that were not feasible to build in the production code.
- On-boarding new teammates to the team/product is vital. Learning the domain space requires a balance between a new teammate being proactive and asking questions, while also being supportive and giving time as a teammate familiar with the product and space.
</div>
