# NetafimTimerAPP

The code is available in this github link , zipped for convenience.
.NET full project and the published dll  are also inside  
The used DB is Redis cloud - the connection details are part of the code so no need to do anything 
Once extracted and running the application is opening swagger in the browser which allows testing the end points
2 endpoints are included:
- Set Timer
- -  Get time status 
HIgh Level Solution
The application provides the ability to set timer details by hours minutes and seconds and to provide webhook.
Second end point is available to query the timer remaining time.
Background service is running and polling the expired timers
On timer completion , http post request will be sent to the provided webhook
If the notification was successful , the expired timer will be deleted from the redis DB
In case of failure to issue the http post , the status of the timer will be Failed to allow retries in the future
Didn't get to adding the automated test to the project 
