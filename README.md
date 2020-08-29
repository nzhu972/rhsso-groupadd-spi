# Red Hat SSO Group Add SPI

This RHSSO (Keycloak) SPI will automatically grant group membership on registration. 


## Installing the SPI
 
To install the SPI, first build the jar using Maven:
`mvn clean install`

Step 1: Deploy the jar to Keycloak server

Step 2: After it is deployed, enable it by going to your realm in the RHSSO admin dashboard by clicking `Events -> Config` adding `group-assignment-event-listener` 
in the `Event Listeners` box

Step 3: In the RHSSO admin console, create a role and a group. The group name must match the key-value pair in the properties file in this project located in src/main/resource. The group name will be used for auto-assigning when the email domain is matched.

Step 4: Perform user registration through the app. When email address entered match the email domain defined in the properties file, then group will be auto-assigned. Navigate to RHSSO to confirm.


