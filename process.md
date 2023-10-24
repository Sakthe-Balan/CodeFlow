# Jenkins Configuration Changes:

## Find and Kill Jenkins Process:

ps aux | grep jenkins
sudo kill <process-id>

## Change Jenkins Configuration:

 Edit the Jenkins config file (typically located at /home/ubuntu/.jenkins/config.xml) and change:
 <useSecurity>true</useSecurity>
 to:
 <useSecurity>false</useSecurity>
 Restart Jenkins to apply the changes.


# Kubernetes and Docker:

## Running Docker Commands Without sudo:

 Note: If you don't use sudo su, you need to run Docker commands with sudo.

## Join Kubernetes Worker Node to Master:

kubeadm join <master-ip>:6443 --token <token> \
    --discovery-token-ca-cert-hash <cert-hash>

## Reset Kubernetes Node:
# Purpose: Reset a Kubernetes node to its initial state.
sudo kubeadm reset


# Notes:

- Please replace placeholders like <process-id>, <useSecurity>, <master-ip>, <token>, <cert-hash> with actual values.
- Be cautious while making changes to Jenkins and Kubernetes configurations. Back up important files before modifying them.
- Always follow best practices and official documentation for Jenkins and Kubernetes to avoid unintended issues.

Remember that these commands and instructions are presented out of context, so it's essential to apply them correctly based on your specific environment and requirements.
