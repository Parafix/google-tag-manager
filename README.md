# Boilertemplate - Purpose of this repository
This is an initial very basic GTM template for web
to get you started with a naming convention & way of working.

https://github.com/Parafix/google-tag-manager/blob/master/GTM-PKX25W_workspace1.json

# Folder convention
- Tracking: contains all the tags for tracking
- Utility: contains all the triggers and variables to support tracking

# Naming convention
Naming convention should help you read the purpose of the tag, trigger or variable in a blink of eye.
Here's how it's build up:

## Tags
What is it for - What type of tracking is it - What does get tracked - For what part of the site (language/locale)

Not every tag contains all the parts

Examples:

Track - Page View - All 
- tracks all page views of all languages of the site

Track - Page View - EN 
- tracks all page views of the English part of the site

Track - Event - Links - All 
- tracks all the links clicked of all languages of the site

Track - Event - Links - NL 
- tracks all the links clicked of the Dutch part of the site

Track - Transaction - All 
- tracks all transactions of all languages of the site

## Triggers
Event based on the loading order - What does get triggered - For what part of the site (language/locale)

* triggers are activated by types suchs as page view, clicks, loads, etc.

Examples:

All pages 
- triggers all pages (standard GTM trigger)

DOM ready - All 
- triggers on DOM ready for all the languages of the website

DOM ready - EN 
- triggers on DOM ready for the English part of the website

DOM Ready - Transaction OK - All 
- triggers on DOM ready when the transaction is confirmed for all the languages of the website

## Variables
When seeying a extensive list of variables used to support tracking, it's very easy to spot based on its name, what its for

Type - What/Name

Examples:

Google Analytics Settings 

Constant - UA Code 
- Constant var with the UA Code of the Analytics profile

Others can be DLV (dataLayer variable), JSV or JSVAR (Custom Javascript Variable), ...
