# DevOps Engineer assignment

This document contains description and requirements for assignment for DevOps Engineer position.

## Requirements

### Assumption
The given system has 2 running application servers. Those servers are connecting to 2 MySQL database instances (`alice-production-db`, `brandy-production-db`) which are containing really huge data. Developers are asking us to setup test databases that cloned from production db every night. So they can test around them without effecting production data.

### Question
1. Please setup new Admin Server for OpenVPN server. It should route client traffic through the VPN only when client made a connection to the databases.
2. Please create OVPN file for us to test the connection.
3. Please setup the solution that clone production database to test databases every night. Put the running script in Admin Server and also github public repo.
4. Please provide us connection string for accessing test databases. The connection string should remain unchanged, even if the database has new clone.
5. Please make sure that the database could not be connected by world. It should be allow only access from OpenVPN and application servers.

### Preparation
1. We will give you an access to google cloud platform. In google cloud console, you will find alice-production-db and brandy-production-db in CloudSQL. `(User: root, empty password)` along with 2 application servers.
2. You will have privileges to create compute engine that you may needed for this pilot project.
3. You will have privileges to set networking and firewall rules to make sure that our system are protected by high security.

If you have any question or notice some misconfiguration, please don't hesitate to let us know. So we can clarify it.
