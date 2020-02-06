# UI-Strings

This repository contains the source and translated strings for Arrival Advisor. 

It is integrated with our Weblate application found here: https://translate.peacegeeks.org/ 

This repository is used as a submodule for https://github.com/pg-irc/pathways-frontend 

### Source Strings 

The English source strings are found in the `*.pot` files. The msgid's in the `*.pot` files are used to indicate which strings each locale needs to translate on Weblate. 

### Generating a .pot file from a .csv using csv2po
1. Download the .csv file with the source strings. csv2po makes three assumptions with the layout of the .csv file:
* Column 1 of the .csv file will contain information of where this string is located
* Column 2 of the .csv file contains the source string
* Column 3 of the .csv file contains the target string

2. In terminal run: 
`csv2po *.csv *.pot`

### Git Workflow

There are two branches that are used in in this repository: `translate` and `master`. When committing and pushing changes from Weblate, the changes are automatically merged into the `translate` branch. 
Along with this, a PR is opened into the `master` branch. We are able to test changes made on Weblate using the `translate` prior to merging into `master`.

### Project Structure

We have four components in our UI-Strings project on Weblate. 

* Questionnaire - questionnaire strings in the app.  
* Explore - Explore section strings of Arrival Advisor 
* JSX_Strings - JSX Strings IE: strings found on the About page. 
* release_notes - strings for use on both the Google and Apple Stores. 
* app_screenshots - strings Google Play and Apple Store screen shots
* marketing - strings for marketing - IE posters and brochers

### Roles

There are two roles, not including admin: 

* Translator
    * Translate Strings
    * Add and Accept Suggestions
    * Use Machine Learning Services 
    * Comment on Strings
* Reviewer

    * can do everything above as well as:
    * Review strings
    * Push changes to the Github repository designated in the component settings

### Notifications

Users in either role need to sign up for component and translation notifications - these can be adjusted by clicking on the top right corner and clicking on Settings 

Component notifications are triggered when there is a merge failure and a new language request.

Translation notifications are triggered when there are new strings to translate, there are new comments/suggestions on their specified language.  

### Fuzzy Entries

When there is a situation where a user must take action on a particular string or set of strings on Weblate, a fuzzy entry will be attached to it. 
It often looks like this in the .po file:
```
#, fuzzy
```
It is often the case that you will see this when the same source string is found in different components of a Weblate project, but translated differently in the same locale. 
For more information please read [gettext's documentation](https://www.gnu.org/savannah-checkouts/gnu/gettext/manual/gettext.html#Fuzzy-Entries).

### Version

Currently using Weblate 3.8.1

### For More Informatin

See the Weblate's documentation [here](https://docs.weblate.org/en/weblate-3.8/)

