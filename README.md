
# Welcome to the Carpentry Setup repository. 

This documentation outlines how to create a repository for a Carpentry workshop.

This documentation is long because we detailed some operation extensively. The whole operation is actually rather short and easy (its will take a few hours -2?- to get it all setup and looking good).

## Setting up the carpentry repository and website

This repository is meant to store information on how to create Carpentry GitHub repositories for Carpentry workshop. 
With this information you should be able to : 
- create a new carpentry repository
- update its content to match your workshop (location, date and so on)
- generate automatically the workshop web pages

Official documentation can be found here : 
- https://github.com/carpentries/workshop-template
- https://software-carpentry.org/blog/2014/10/a-new-template-for-workshop-websites.html


For more information about the infrastructure, the whole setup relies on GitHub Pages.
You can consult the official documentation for more information on this mechanism. 

The Software Carpentry organization provides a template repository for all its workshops. The repository itself is a GitHub repository, and with of GitHub Pages, it contains the template and instruction on how to automatically build a website.
The overall approach is the following: 
- copy the template into a new repository (with the right name)
- adjust the content of the repository
- commit your changes to GitHub and watch how the website is updated!

This documentation is split in two parts. The first part is focus on building a carpentry repository following the official guidelines. This is important to do once in a while as the official carpentry repository changes over time. The second part is the quick-and-dirty approach, using a previously created carpentry workshop, closer to what you want, but may be out of data. The second approach is faster if you are confident in what you are doing! Use with care, dear instructor.

-----------------------------

### Step 1: Copy an existing repository 

Let us first find the carpentry repository and copy ("import") its duplicate in the appropriate location.

#### Pick your reference repository

The official documentation suggest copying the following repository to get started : https://github.com/carpentries/workshop-template
This repository is both the template of the website, as well as the documentation of the template and how to adjust it. 

#### Do the import (copy)

Once you have chosen the most suitable repository, `import` it. **Don't fork** it.
NOTE: you can't rename forked repositories, and strong naming conventions apply for carpentries workshop page names.

To [import a repository](https://github.com/new/import), find the "Import repository" button, located on the top right of the github page, inside the drop down menu "+".
Click on the "+", and select "import repository". 

In the Import page, set the name of the source at the top ([full URL of the repository is fine](https://github.com/carpentries/workshop-template)). 
In the bottom field (the destination) select the user that will manage the repository - pick the ["4TUResearchData-Carpentries" organization](https://github.com/4TUResearchData-Carpentries) (so that the repository gets created along side of the others). 

*Set the name of the copy. Follow the carpentry naming convention: DD-MM-YYYY-location*

Click on "Import" at the bottom of the page and wait! This may take a while (5 to 10 minutes). You may get a confirmation email once the operation is completed. 

#### Quick test 

At this point, you should already be able to access the workshop website. It is generated by GitHub, and your source (template or previous repository) should be working. You can try to access to site right away. 

If the URL of your repository is https://www.github.com/4TUResearchData-Carpentries/REPOSITORY-NAME 
then the associated GitHub Page should be https://4TUResearchData-Carpentries.github.io/REPOSITORY-NAME

### Step 2: Adjust the content of the site

Now that we have a working site, we need to change its content. 

There are few files that *must* be updated. 

| Website section/item        | File to edit           | Remarks  |
| ------------- |:-------------:| -----:|
| Title/workshop type                          | _config.yml                | workshop type must match what is set in index.md    |
| practical information (location, date, etc.) | index.md                   | variable definitions at top of file |
| Schedule/agenda                              | _includes/sc/schedule.html |    |
| Syllabus |  _includes/sc/syllabus.html       |     |
| Setup (software installation) | index.md      |     |
| Logos | _includes/navbar.html                 |     |


#### index.md

This file contains the main practical information about the workshop: location, date, program, link to ticket/registration, instructors,... 
There are instruction inside the file on what can and should be changed. 

All you really need to change is located at the top of the file. 

TIP: it is easy to make a mistake (forget a comma, or a quote). When you are editing the page, if you want to test it, try the Preview mode. If the table is not presented neatly (you see text rather than a table), there is something wrong in your page!

Note: for the EventBrite ID, the expected identifier is the numbers at the end of the URL of the dedicated eventbrite event page for the carpentry. If you URL is eventbrite.com/MY-Event-Some-Description-XXXXXXXX , the XXXXXXX are the ID you want.

#### _config.yml

In this file, all you need to update is (located at the top of the page) the workshop type and the workshop title. 

Note: The workshop type must match what you've put in the index.md file. Otherwise you will get an error message on the web page. 

#### _includes/sc/schedule.html

This file contains the agenda for the workshop.

#### _includes/sc/syllabus.html

The syllabus section contains the references to the course material.
Depending on the lessons you teach, you can comment or uncomment parts in order to only show the relevant information on the website. 

#### _include/navbar.html

In this file, you will find the HTML code that describes the content of the top banner of the website. 
You may want to add or changes the images that are displayed there (usually logos of participating institutions). 

To remove an icon, remove the complete HTML block. For instance, this is a complete block for an icon (TU Delft logo here).

    <a href="https://www.tudelft.nl">
      <img src="https://www.xibis.nl/wp-content/uploads/2016/10/tudelft1-300x117.png" alt="xibis.nl/wp-content/uploads/2016/10 /tudelft1-300x117.png" height="50px;" style="margin: 0px 10px" />
    </a>
    
The block starts with `<a href=...>`, and ends with `</a>`. 

To add an icon, copy paste the code above, change the link you want associated with the icon by changing the value after "href", and change is icon by replacing the "src=" value with the URL to the image you want to be displayed. To be proper, update the "alt" URL as well, maybe with an alternate version of the icon/image or the same.

### Step 3: Check everything! 

You can now access your website and check if the content matches your expectation!


## The quick and dirty way. 

This approach is basically the same as above, but instead of starting from the official template, we suggest starting from a previously existing SWC repository. This is a bit dangerous, as we may drift from the official version of the repository, but it can save significant customization effort. 

### Step 1: copy a repository

If you want to minimize the customization effort afterwards, you can pick a workshop website from the "4TU.Center for research data" organization as your reference repository during the import. You should pick a repository containing a workshop which content is close (or identical) to what you intend to do during your workshop. 

Example: the Software Carpentry workshop organized on the 25th of Sept. 2019 covers the Git, Shell and Python lesson. The repository and its website were created by copying the repository of the Software Carpentry organized in Delft in July. The July repository was picked because it covers exactly the same lessons as the one organized in September.

### Step 2: adjust the content of the site
If you picked your reference repository wisely, this step is going to be shorter than the previous one. 
The index.md and \_config.yml files should already be set to the right type of workshops ("swc", "dc", ...).

If you chose a repository covering the same lessons as the one you are planning for your workshop, you can skip the "syllabus" and "schedule" customization. Small gains, but gains nonethless!


