# Google-Cloud-Case-Study

A case sudy proposal that suggests a company shift it's on premise VMs to Google Cloud.

## Execution Strategy
Currently we have four SaaS solutions to be hosted on GCP. We will be using different services for each solution:  
• Application Server - The server can be deployed on Google Kubernetes Engine where the containerized software can be hosted in containers using GKE.    
• Wowza Streaming Engine - Streaming will need a dedicated Compute Engine Virtual Machine.  
• Video Transcoder - Transcoder API can be used to transcode video files to be sent to the streaming engine. This will also need its own Compute Engine Virtual Machine.   
• Microsoft SQL Server - The database will be stored in Cloud SQL.  

So instead of 4 VMs, we only need 2 Virtual Machines to be running for Wowza Streaming and Transcoder jobs while the Application Server can be run on Kubernetes Engine (as containers) which will be helpful in automated load balancing. The database can be stored in SQL Server.
