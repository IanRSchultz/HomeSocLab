# File Integrity Management

## Windows

To establish file integrity management, the first thing we need are some files which we want to manage. I created a PersonalData folder with an "important" text document inside of it. To enable FIM on the files, we need to add them to the ossec.conf file under the File Integrity Management Section. FIM normally only checks files periodically, but we can label the files as realtime to enable realtime management of them.

![Screenshot of the windows ossec.conf file showing that the PersonalData folder has been added as a realtime directory.](/images/part2/windowsossec.png)

After adding the files to the ossec file and restarting the wazuh agent on the machine, I then tested the FIM by modifying and deleting the text file it was monitoring. In the wazah server, the FIM tool was able to capture both events and displays information about them, such as what event occurred, when it occurred, and which files it effected.

![Screenshow of Wazuh FIM showing the modification and deletion events of the managed files on the windows machine.](/images/part2/windowsFIM.png)

## Linux

Establishing FIM on a linux machine is similar to that of the windows machine. First, I create the directory that I want to monitor and fill it with some data. I then add it to the Linux ossec folder and make sure to label it as realtime management.

![Screenshot of the linux ossec.cong file showing the PersonalData directory being added and marked as realtime.](/images/part2/linuxossec.png)

I then restart the linux Wazuh agent and begin modifying the data on the machine the same way I did on the windows one. The events show up the same on Wazuh, showing various details about each of the events.

![Screenshow of Wazuh FIM showing the modification and deletion events of the managed files on the linux machine.](/images/part2/linuxFIM.png)
