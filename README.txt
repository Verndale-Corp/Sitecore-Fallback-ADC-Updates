Verndale ADC searchContrib Updates for Sitecore Language Fallback

Purpose
Enhance the Advanced Database Crawler to take language fallback into account when generating indexes.

Compatibility
This is for use with the latest version of the ADC project on Github
https://github.com/sitecorian/SitecoreSearchContrib
And it assumes you are using the latest version of the Partial Language Fallback Module
http://marketplace.sitecore.net/en/Modules/Language_Fallback.aspx

How to build code and deploy the solution
1. When using the fallback module, make sure to compile the source code to get the dll, do not use the one within the package.

2. Download the AdvancedDatabaseCrawler.cs and CrawlerHelper.cs from this repository

3. In the SitecoreSearchContrib project
Overwrite the AdvancedDatabaseCrawler.cs
Add the file CrawlerHelper.cs to a Utilities folder
Add reference to the Sitecore.SharedSource.PartialLanguageFallback.dll that you compiled

Testing
1. There should be more than one language in your site 
2. Add a version to an item for each language
3. Add content to the fallback language and no content to the language falling back
4. Publish to both languages
5. Perform Index search on the language falling back, the item should come up as a result

Review the blog series about Partial Language Fallback on Sitecore, link TBD
