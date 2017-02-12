---
layout: essay
type: essay
title: Release Notes (Alloy)
date: 2017-01-15
labels:
  - Software Engineering
  - Learning
  - Frameworks
  - UI
  - Semantic UI
  - Meteor
  - MongoDB
  - Semantic UI
---

A continuation of my group project Alloy from ICS 314.  My group and I created Alloy during the Fall semester of 2016 with the hopes of making a website that can initiate and strengthen collaboration for projects that needed team members, a way to get a person's project exposure.  At the moment Alloy is bound to the University of Hawaii: Manoa student/faculty bodies.

<h3>Current features of Alloy are the following:</h3>
<ul>
	<li>Login information is the username and password associated with a persons UH Manoa login</li>
	<li>Users are able to create projects, which are public to other users to view</li>
	<li>A search function is available for projects and users, which searches based on skills wanted for projects or skills users currently entered into their personal user information</li>
	<li>Users can view individual project profile pages from the search results page</li>
	<li>From project profile pages a user can request to join a project if they are not a member or if they are a project admin, they can send invitations to other users</li>
	<li>When a request to join is sent to one of their projects a notification is sent to the other of the project</li>
	<li>When a user sends an invitation to join a project to another user a notification is sent to the recipient of the invitation</li>
	<li>User's hompeage includes a feed of notifications showing request or invitations</li>
	<li>User's homepage includes a feed of suggested projects which are related to skills a user has entered into their user information, this is possible through a skill-graph function in Alloy which relates certain skills that are added to an individual project, the more times two skills are added to the same project the stronger the relation between the two will become</li>
</ul>

<h3>January 15: Features/Enhancements</h3>
Last semester many of the user feedback were in regards to the Search function/capabilities of Alloy.  A few of the search function remarks I hope to correct in this initial milestone are the following:  users shouldn't have to press "clear" to see new search results with a new query;  clean up the search pages .html and .js files of unnecessary code; and having the Search pages only available to users who are logged in.
<ul>
	<li>Reactivity:  The clear button on both the user search and project search pages have been removed.  With the addition of the dep(dependancy) variable in the js files for both searches all search results are now cleared whenever new search tags are queried.  The dep variable is given a value when a query is made and if that dep variable is changed in any way all search results are cleared and a whatever changes that are made to the dep variable are displayed.</li>
	<li>Clean-up:  I went through all the .html and .js files regarding the search function and search results pages to clean up unnecessary lines of code.  I removed many lines of commented out code that printed to the console for testing purposes while I was first creating the search tool.</li>
	<li>Privacy:  The solution to this issue was easily solved.  I knew that the other pages on Alloy already worked where a user had to be logged in to see any of the web page so I merely read through their code and took what I needed.  The solution had been to wrap all the code within the template tag with a "spacebars" if currentUser statement.  Now anyone who wants to see and use the search functions of Alloy must have a login and be logged in to view or use the search capability.</li>
</ul>

<ul>
	<b>(PLANNED) February 1: Features/Enhancements</b>
	<li>One issue from the user feedback last semester regarding the Search function had been to have the search users and projects on one page instead of buttons that changed the page regarding which query you are searching.  I plan to consolidate all Search related files into a single .html and .js file.  At the moment there are multiple .html and .js files that make up the Search function.  I would like to cut that down a lot and clean up the overall organization of this capability.  I still plan to keep all the reactivity that the search users or projects currently have.  I can see multiple issues popping up when I start working on the consolidation.  For example, I will need to create a new UI for the single page search feature.</li>
</ul>

<h3>February 1: Features/Enhancements</h3>
The major goal I had planned for this enhancement was in regards to fixing/updating the search page.  Prior to this milestone the Alloy search page was comprised of three seperate pages.  Originally the main Search page's UI consisted of two buttons, one button for project searches and another for user searches.  Alloy users would click either button and then they would be redirected to a new page dependant on which button they chose.  The user and project searches each had their own web pages which had a search bar and each page populated their own query results on the same page reactively.  I found having multiple pages for the search a waste and so did the test users at the end of ICS 314.
<ul>
	<li>Consolidation:  I created a new Search page that consolidated the multiple pages that comprised the old one.  There is just one single page for both Project and User searches.  Test users expressed in feedback about the design with links to multiple search pages not very appealing.</li>
	<li>Reactivity:  Keep the reactivity between searching for projects or users.  There are two forms, one for searching projects and the other for searching users.  Reactivity while searching either projects or users is still available.</li>
	<li>Clean-up:  Clean up old html and js files from the old search pages.</li>
	<li>Admin:  Created a base site admin page.  Currently all users, whether they are site admins or not is able to view the page if they type /admin at the end of the URL in the address bar.  Also there is a admin link in the header which is only viewable if a user is a site admin.</li>
</ul>

<h3>February 15: Features/Enhancements</h3>
During this milestone period I focused on giving more functionality to the admin page.  I ultimately want admins to be able to edit users, projects and skills.  So far I was able to give admins the capability to view all the skills that users have entered via user profiles or project profiles and the ability to add skills into the 'Skills' collections themselves.
<ul>
	<li>Fixed bug:  Formerly when updating a projects 'wanted skills' attribute newly entered skills are not added to the skill graph collection.  Skills are now added correctly to the skills graph collection when a skill that is not in the collection has been entered</li>
	<li>Admins can now see the total number of projects, users and skills the website currently has</li>
	<li>Edit skills UI (for admins) created</li>
	<li>In the 'Edit Skills' page admins can see a list of all the skills</li>
	<li>In the 'Edit Skills' page admins can enter a new skill</li>
</ul>
