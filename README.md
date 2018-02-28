# Boilertemplate - Purpose of this repository
This is an initial very basic GTM template for web
to get you started with a naming convention & way of working.

[download it here](https://github.com/Parafix/google-tag-manager/blob/master/GTM-Boilertemplate-web.json)

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

## GTM Boilertemplate Web contains:
1) Page view tracking
- Tag: Track - Page View - All
- uses Trigger: Page View - All Pages
- contains Variables: Google Analytics Settings

2) Event tracking: All links
- Tag: Track - Event - Links - All
- uses Trigger: Page View - All Pages
- contains Variables: Google Analytics Settings
- Extra: non-interaction hit = true (to disable bounce rate impact)

3) Standard transaction tracking
- Tag: Track - Transaction - All
- uses Trigger: DOM ready - Transaction OK - All 
(DOM ready to make sure all e-commerce related vars are loaded before hit is sent to Google Analytics. You still need to integrate the dataLayer on the "transaction thank-you" page: [see the code onder "Standard E-commerce"](https://support.google.com/tagmanager/answer/6107169?hl=en)) 
- contains Variables: Google Analytics Settings
- Don't: mix enhanced ecommerce with standard ecommerce. Integrate the one or the other. Not both. You're data will be messed up.

4) Event tracking: Clicks on e-mail links
- Tag: Track - Event - Mailto - All
- uses Trigger: Links - Click - Mailto - All
- contains Variables: Google Analytics Settings
- Extra: non-interaction hit = true (to disable bounce rate impact)

## Google Analytics Settings
- contains Variables: Constant - UA Code (Google analytics profile code of the profile to track)
