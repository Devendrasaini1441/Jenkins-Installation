# Jenkins Installation Guide

This guide provides step-by-step instructions to install Jenkins on your machine.

## Prerequisites

- Java Development Kit (JDK) installed (Jenkins requires Java 8 or 11)
- Administrative privileges on the system

## Installation on Ubuntu


Jenkins requires Java to run. First, update your package index:

```sh
sudo apt update

sudo apt install openjdk-11-jdk -y

java -version

curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update

sudo apt install jenkins -y

sudo systemctl start jenkins
sudo systemctl enable jenkins


