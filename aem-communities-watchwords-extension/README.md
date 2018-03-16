aem-communities-watchwords-extension
====================================

This extension provides a sample implementation of com.adobe.cq.social.ugcbase.moderation.AutoModerationProcess to implement a new ProfanityFilter
The sample works on the basis of sentiment score but essentially the resource of ugc created will be available through this interface and this resource can be processed to provide custom moderation

Building the sample
===================

* Change directory to the root of the repository aem-communities-watchwords-extension
* Run *mvn clean install*
* A successful build should create a bundle artifact in *bundles/aem-communities-watchwords-extension* and a package artifact(with bundle embedded) in *content/target*

Installing the sample
=====================

* Use the package manager at http://[server]/crx/packmgr/index.jsp and upload the zip file found at *content/target*
* Install the package
* Add Watchwords path in AEM Communities Sentiment Process at http://[server]/system/console/configMgr by default the negative and positive paths are located at /libs/settings/community/watchwords/default.
![Screenshot](AEM_Communities_Sentiment_Process.JPG)
* Configure the AutoModeration component at http://[server]/system/console/configMgr - Search for AEM Communities Auto Moderation(>=6.4) or automoderation(<6.4)
* Add ProfanityFilter in the list of Automoderaion Sequences
![Screenshot](screenshot.png)

 


