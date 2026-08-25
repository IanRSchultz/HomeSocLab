# Dashboard

For the first excercise, I will be generating some suspicious activity on my windows machine. Afterwards, I will set up a dashboard on Wazuh to monitor and display relevant information about the activity.

Here is the activity that generated on the windows machine:
![Screenshot of windows powershell showing me creating a user, adding it to the administrator group, and deleting it](./images/part1/soclab1/png)

The first thing I did after ingesting some information from the connected machines was set up a basic dashboard to display some potentially important information

![Screenshot of Wazuh Dashboard showing the following 3 elements](/images/part1/DashboardDemo.png)

1. The first element is tracking the amount of failed logons for the connected Windows machine, which I tested by failing some logons. The metric is tracked by checking the archive for events with the eventID 4625, which correlates to failed logon attempts.

2. The second element is table showing failed SSH authentication attempts to the connected Ubuntu machine. The table displays additonal information such as the time of the authentication, the source ip address, and the source user.

3. The third element is a graph plotting the changes in user accounts on the windows machine. This includes changes such as the creation, deletion, or changing of groups, permissions, and passwords of accounts.

The Dashboard proves to be a way to combine records from many different areas on the server and display them in an easily digestable way for users.