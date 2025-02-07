# Red Teaming | Blue Teaming Lab

## Red Team Adversary Emulation with Caldera

### Project Overview
This project aims to simulate real-world cyber attacks using Caldera, an automated adversary emulation platform built on the MITRE ATT&CK™ framework. The goal is to test and improve the organization's defenses by emulating advanced persistent threats (APTs) and other adversary techniques.

### Objectives
Understand Caldera: Familiarize with Caldera's features and capabilities.

Set Up Environment: Prepare the necessary hardware and software.

Create Adversary Profiles: Develop profiles for different types of adversaries.

Execute Emulation: Run adversary emulation scenarios.

Analyze Results: Evaluate the effectiveness of defenses and identify vulnerabilities.

Report Findings: Document the findings and provide actionable recommendations.

### Prerequisites
Hardware: 8GB+ RAM, 2+ CPUs

Software: Linux server (Ubuntu 20.04 recommended), Python 3.6.1+, Pip3, Git

Skills: Familiarity with Linux system administration, TCP/IP, penetration testing concepts, and Windows.

### Setting Up Caldera

1. Clone the Caldera GitHub Repository

git clone https://github.com/mitre/caldera.git

2. Navigate to the Caldera directory and install the python modules/dependencies

pip3 install -r requirements.txt

3. Initialize the Caldera server

python3 server.py --insecure

*Ref 1: Initializing Caldera*
![Initializing Caldera](images/image1.png)

4. Access the Caldera Web interface

e.g; http://server-ip:8888

5. Login to Caldera 

Credentials: red/admin

*Ref 2: Caldera Login*
![Caldera Login](images/image2.png)

### Campaigns

Step 1: Deploy an Agents

*Ref 3: Deploying Agents*
![Deploying Agents](images/image3.png)

![Deploying Agents](images/image4.png)

![Deploying Agents](images/image5.png)

![Deploying Agents](images/image6.png)

![Deploying Agents](images/image7.png)

![Deploying Agents](images/image8.png)

![Deploying Agents](images/image9.png)

Step 2: Abilities

*Ref 4: Abilities*
![Abilities](images/image10.png)

Step 3: Adversaries

*Ref 5: Adversaries*
![Adversaries](images/image11.png)

Step 4: Setting up Operations

*Ref 6: Setting Caldera Operations*
![Setting Caldera Operations](images/image12.png)
![Setting Caldera Operations](images/image13.png)
![Setting Caldera Operations](images/image14.png)
![Setting Caldera Operations](images/image15.png)

Step 5: Exporting the results

*Ref 7: Exporting the results*
![Exporting the results](images/image16.png)


## Covenant C2

### Installation

Prerequisites

1. Windows GIT client

https://git-scm.com/downloads/win

2. DotNet Core 3.1

https://dotnet.microsoft.com/download/dotnet/3.1

Note:

1. Download and Install Git client and DotNet Core 3.1

*Ref 1: Installation*
![Installation](images/image17.png)
![Installation](images/image18.png)
![Installation](images/image19.png)
![Installation](images/image20.png)
![Installation](images/image21.png)

3. Set Defender Exclusions.

*Ref 2: Setting Exclusions*
![Setting Exclusions](images/image22.png)
![Setting Exclusions](images/image23.png)

5. Clone the GitHub Repository

git clone --recurse-submodules https://github.com/cobbr/Covenant

*Ref 3: Cloning the Repository*
![Cloning the Repository](images/image24.png)
![Cloning the Repository](images/image25.png)

4. Start Covenant

dotnet run

*Ref 4: Initializing the Covenant*
![Initializing the Covenant](images/image26.png)

5. Open a web browser and navigate to https://127.0.0.1:7443/

*Ref 5: Caldera Web Interface*
![Caldera Web Interface](images/image27.png)

### Creating a Listener

*Ref 6: Configuring a Listener*
![Configuring a listener](images/image28.png)

### Start a Listener

*Ref 7: Starting a listener*
![Starting a Listener](images/image29.png)


### Set Up a Launcher

*Ref 8: Configuring a launcher*
![Configuring a launcher](images/image30.png)


### Executing the Grunt

*Ref 9: Executing a Grunt*
![Executing a grunt](images/image31.png)
![Executing a grunt](images/image32.png)
![Executing a grunt](images/image33.png)
![Executing a grunt](images/image34.png)
![Executing a grunt](images/image35.png)
![Executing a grunt](images/image36.png)

## Havoc C2

Installation

sudo apt install havoc

Start the havoc C2 server

havoc server --profile ./profiles/havoc.yaotl -v --debug

*Ref 10: Initialize havoc c2 server*
![Initialize havoc c2 server](images/image37.png)

Start havoc C2 client

havoc client

*Ref 11: Start havoc c2 client*
![Start havoc c2 client](images/image38.png)

### Running Havoc C2

1. Create a Listener

*Ref 12: Creating a Listener*
![Creating a Listener](images/image39.png)

3. Generate a payload

*Ref 13: Generating a payload*
![Generating a payload](images/image40.png)

5. Download and Execute a payload

*Ref 14: Execute a payload*
![Execute a payload](images/image41.png)
![Execute a payload](images/image42.png)
![Execute a payload](images/image43.png)
![Execute a payload](images/image44.png)
![Execute a payload](images/image45.png)
![Execute a payload](images/image46.png)
![Execute a payload](images/image47.png)


## Atomic Red Team

Introduction

Installation

1. Open the PowerShell and run as administrator.
2. Execute the following commands:
powershell -exec bypass
Install-Module -Name invoke-atomicredteam,powershell-yaml -Scope CurrentUser
3. Import the Modules
Import-Module "C:\AtomicRedTeam\invoke-atomicredteam\Invoke-AtomicRedTeam.psd1" -Force

## Mitre Att&ck Framework

# Running Atomic Tests

(PowerShell Commands)

1. Invoke-AtomicTest T1016 -ShowDetailsBrief
2. Invoke-AtomicTest T1016 -ShowDetails
3. Invoke-AtomicTest T1016 -CheckPrereqs
4. Invoke-AtomicTest T1016 -GetPrereqs
5. Invoke-AtomicTest T1016
6. Invoke-AtomicTest T1055 -ShowDetailsBrief
7. Invoke-AtomicTest T1055 -ShowDetails
8. Invoke-AtomicTest T1055 -TestNumbers 1
9. Invoke-AtomicTest T1055 -TestNumbers 2
10.Invoke-AtomicTest T1055 -TestNumbers 3
11. Invoke-AtomicTest T1055 -CheckPrereqs
12. Invoke-AtomicTest T1055 -GetPrereqs
13. Invoke-AtomicTest T1016 -Cleanup
14. Invoke-AtomicTest T1055 -Cleanup
