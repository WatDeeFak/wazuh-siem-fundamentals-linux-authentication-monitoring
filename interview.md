# Interview Preparation: Wazuh SIEM Fundamentals Project

## Question 1: Detecting Suspicious Login Activity

**HR Question:**

Imagine you are working for a company, and its Linux server receives multiple failed SSH login attempts. How would your project help the security team identify this activity?

**Suggested Answer:**

In my project, I used Wazuh SIEM to monitor authentication activity on an Ubuntu Linux endpoint. The Wazuh Agent collected security events and sent them to the Wazuh Manager for analysis.

I simulated repeated SSH login failures using a non-existent username. Wazuh detected the repeated activity and generated a brute-force alert with Rule ID 5712 and severity level 10.

In a real-world environment, I would review the source IP address, attempted username, timestamps, and related events to understand the activity. I would then document the findings and escalate the incident according to the company's security procedures.

This project helped me understand how a SIEM can turn individual security events into useful alerts for investigation.

## Question 2: Handling a Security Alert

**HR Question:**

Suppose your monitoring system generates a high-severity alert, but you are not sure whether it is a real attack or legitimate user activity. What would you do?

**Suggested Answer:**

I would not immediately assume that the alert represents a successful attack. First, I would review the alert details, including the source IP address, affected account, timestamp, and detection rule.

Next, I would compare the event with other available logs to understand whether the activity was expected or suspicious. If the evidence suggested a potential security incident, I would document my findings and escalate the case to the appropriate security team.

Through my Wazuh project, I learned that an alert is a signal that requires investigation. Its severity helps prioritize attention, but the final assessment must be based on evidence.

## Question 3: Applying the Project in a Cloud Environment

**HR Question:**

Your project was performed locally using VirtualBox. How could the knowledge you gained be useful in a company that operates its infrastructure in AWS?

**Suggested Answer:**

Although I performed this project in a local virtual environment rather than AWS, the fundamental security concepts are transferable to cloud environments.

For example, a company may operate Linux servers on Amazon EC2. A SIEM can help centralize security events from supported endpoints and identify suspicious authentication activity.

In an AWS environment, I would also consider AWS-native security data sources, such as CloudTrail for recording AWS API activity and GuardDuty for detecting potential threats. These services complement endpoint monitoring because they provide visibility into different types of activity.

