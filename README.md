# Jenkins Installation Guide

This guide provides step-by-step instructions to install Jenkins on your machine.

## Prerequisites

- Java Development Kit (JDK) installed (Jenkins requires Java 8 or 11)
- Administrative privileges on the system

## Installation on Ubuntu

### Step 1: Install Java

Jenkins requires Java to run. First, update your package index:

```sh
sudo apt update

Then install OpenJDK:

sudo apt install openjdk-11-jdk -y

Verify the Java installation:

java -version

Add Jenkins repository key:

curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

 Add Jenkins repository:

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

Update package list again:

sudo apt update

Install Jenkins:

sudo apt install jenkins -y

Start and enable Jenkins service:

sudo systemctl start jenkins
sudo systemctl enable jenkins


