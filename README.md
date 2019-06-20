
# Welcome to the Carpentry Setup repository. 

This repository is meant to store information on how to create Carpentry GitHub repositories for Carpentry workshop. 
With this information you should be able to : 
- create a new carpentry repository
- update its content to match your workshop (location, date and so on)
- generate automatically the workshop web pages

This version of the documentation is targeted to make the best out of the workshop repositories we already created in the past. 
You can always rely on the official carpentry documentation.

Official documentation can be found here : 
- https://github.com/carpentries/workshop-template
- https://software-carpentry.org/blog/2014/10/a-new-template-for-workshop-websites.html

However, the official documentation covers a number of use cases that, at TU Delft, we are unlikely to encounter. 
(For instance, we do not really host our own website, and "building" the website locally was -so far- only done for bug fixing). 

For more information about the infrastructure, the whole setup relies on GitHub Pages.
You can consult the official documentation for more information on this mechanism. 

-----------------------------

## Step 1: Copy an existing repository 

All workshop websites are very similar in content, therefore the easiest way of setting up a new repository is to start from an existing one and then modify the copy. 

### Pick your reference repository

The official documentation suggest copying the following repository to get started : https://github.com/carpentries/workshop-template
This repository is both the template of the website, as well as the documentation of the template and how to adjust it. 

If you want to minimize the customization effort afterwards, you can pick a workshop website from the "4TU.Center for research data" organization. You should pick a repository containing a workshop which content is close (or identical) to what you intend to do during your workshop. 

Example: the Software Carpentry workshop organized on the 25th of Sept. 2019 covers the Git, Shell and Python lesson. The repository and its website were created by copying the repository of the Software Carpentry organized in Delft in July. The July repository was picked because it covers exactly the same lessons as the one organized in September.


### Do the copy

Once you have chosen the most suitable repository, import it. Don't fork it.

To import a repository do what you must.

NOTE: you can't rename forked repositories, and we have a strong naming convention for workshop names.
