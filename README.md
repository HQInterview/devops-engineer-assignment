# DevOps Engineer assignment

This document contains description and requirements for assignment for DevOps Engineer position.

## Requirements

### Problem
In production environment, our system is connecting to 2 MySQL database instances.
We would like to clone these 2 databases into test environment every night. Therefore, test databases are in-sync and developers can test around in test environment without effecting production data.

### Question
1. Please find the solution how to make test databases get cloned every night.
2. Please also setup OpenVPN Server, to allow developers to access it. It should route the traffic through this VPN only when client made a connection to the test databases.
3. Beside OpenVPN, please also make sure that only the applications in following server can made a connection to this new databases. Connection that are not come from following ip addresses should be failed to established.
- 1st Server: x.x.x.x
- 2nd Server: y.y.y.y

### Preparation
1. We will give you an access to google cloud platform, in google cloud console, you will find alice-produciton-db and brandy-production-db in CloudSQL.
2. You will have privileges to create compute engine that you may needed for this pilot project.
3. You will have privileges to set networking and firewall rules to make sure that our system are protected by high security.

### Note
1. Please first describe the intention of your solution and how it works in words.
2. Please also take security in consideration, the database should not be accessed by world, only client that connect to OpenVPN and IP addresses in 3).
3. The script should continuously run every night. Applications and developers should always can access to test databases everyday, anytime.
4. If there are scripts in this pilot project, please also put into github public repo. Cleanliness and naming convention also scores.
