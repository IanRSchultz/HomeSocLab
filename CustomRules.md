#Custom Rules

There are many rules that are included in wazuh that will alert you about all sorts of activity. However, its always a good idea to know how to create and implement custom rules. In this example, with the help of ai, I created a rule to track when a guest user account was enabled on a Windows machine. The guest account is disabled by default, but attackers might want to enable them so they can use them to gain privilage on a machine.

Here is an example of my custom rule in Wazuh:

/images/part3/customrule.png

After creating the rule and addint it to the wazuh server, I then enabled the guest account myself to check that the rule would generate the event.

/images/part3/rulecaught.png