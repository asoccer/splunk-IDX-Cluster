# Splunk Index Clustering Guide

### Before you begin check the following
1. Your Splunk Install versions are fresh from Splunk.com
2. You have opened up the required ports to the Splunk Env
    * 8000 for WebUI (Optional and will be turned off for the indexers)
    * 8089 for Managing the Splunk Instance remotely
    * 9997 for Indexing Port
    * 9987 for Replication Port
    * 1514 if you plan on doing port ingestion. <1024 needs root access
    
    
### Setup your conf files with your IP's 

All conf files will be stored into an app folder called <companyShortName>_Cluster_Configs. Avoid writing settings to /etc/system/local/* for easy management of settings.
Here are the .conf files you'll need 

* server.[conf](http://docs.splunk.com/Documentation/Splunk/latest/Admin/Serverconf) 
* indexes.[conf](http://docs.splunk.com/Documentation/Splunk/latest/Admin/indexesconf) 
* web.[conf](http://docs.splunk.com/Documentation/Splunk/6.6.2/Admin/webconf) (Only if you plan on disabling the Splunk Web UI from the indexers)

