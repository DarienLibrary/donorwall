# Electronic Donor Wall Dev Notes

## Overview

This project is for an electronic donor wall.  We currently have a similar application written in flash that we want to be re-written in javascript. What we want is a javascript application that will run on full-screen in a browser (Safari, Chrome, or Firefox) and be displayed on a large flat panel with a touch screen overlay. We will also need a back-end form that will allow us to upload media (such as a photo, video file, or audio file) and associate it with a specific donor. The deliverable will be the web application front-end as well as the back-end utility.

The application will retrieve donor data in JSON format from an existing web service. We will make that service available to the developer and provide the necessary documentation to access it.

The application itself will let users walk up to the display and scroll through a list of donor names. If we have a photo, audio, or video available for a donor, a small icon will appear next to the name. If the icon appears, a user can press on (click on) that name and see the photo or hear and watch the testimonial. The web service will provide a URL to the photo, MP3, or video file.  **Very** crude examples are provided (see attached images or examples folder in repository).  This should be a visually appealing application that takes full advantage of the Twitter Bootstrap framework.

When the application is idle (no activity for several minutes) it should revert back to an idle mode that gently scrolls through donors' names.

## Working with Darien Library

As we are a public library and we believe that sharing and openness is an inherently good and essential endeavor, this project and any resulting code will be made open source and freely available under GPL v3.  If you wish to work with us, you must agree the following criteria:

* You must agree that any code you write will belong to Darien Library and, in turn, be made open source under GPL3.
* All code will be maintained, versioned, and maintained under the Darien Library organizational Github account
* You must already have a Github account (which will be given push permission to the project repository)
* You must already be very familiar with git and completely comfortable with the git workflow.
* You love libraries.

## Languages to be used

* PHP 5.3+
* Javascript
* HTML/CSS

## Front-end requirements

* Touch-screen interface (assume no keyboard input is available)
* Use Twitter Bootstrap CSS framework

## Back-end specifications

* Simple upload form
  * Ability to search MySQL database by name and select a donor name to associate a file with
  * Once a donor name is selected, an upload form will be presented and a radio button allowing the staff member to select between audio/visual/text.
  * No processing of the uploaded file is needed, it simply needs to be stored on the local filesystem in a definable location.
  * Schema is already established
  * The upload form is completely standalone and will reside on a separate server
* Sample data will be provided but must be treated as confidential.

## User types

* End-user: members of the public who will view and interact with the kiosk
* Admin: Staff member who will upload content occasionally

## Other details

* Integration of other open source packages is fine as long as they are well documented and maintained projects and considered to be the most appropriate tool for the job. (ie, jquery).  However, simpler is generally better in our estimation.
* The only framework we're requiring for this project is Twitter Bootstrap (and by extension, jquery).
* No transactional (business logic) functionality is required
* No security features/encryption required--will be handled by the web server