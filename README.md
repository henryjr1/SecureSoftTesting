# Project 9

Time spent: **10** hours spent in total

> Objective: Set up a honeypot VM and catalog attacks

## Report
1. Which Honeypot(s) you deployed
    - I deployed the Dionaea over HTTP honeypot.

2. Any issues you encountered
    - I two main issues while attempting this weeks assignment. The first was that my vm instances were not set to accept http or https traffic, which required an intensive amount of trouble shooting to figure out. After that I was able to connect to the vm instance using the external IP address listed and countinue the lab. The second was exporting the session.json file using the command ```gcloud compute scp mhn-admin:~/session.json ./session.json```. I kept receiving an error that the file did not exsist, but I was able to solve this by removing the "~" at the beginning so the comman was ```gcloud compute scp mhn-admin:/session.json ./session.json```. 

3. A summary of the data collected: number of attacks, number of malware samples, etc.
    - There were a total of 2981 attacks 
    - [JSON File](https://github.com/henryjr1/SecureSoftTesting/blob/Week-9/session.json)

4. Any unresolved questions raised by the data collected
    - None


