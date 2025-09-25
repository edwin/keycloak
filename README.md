# Custom Keycloak with a Longer SMTP Timeout

All changes happen in this class 
```
services/src/main/java/org/keycloak/email/DefaultEmailSenderProvider.java
```
changing SMTP timeout from `10s` into `30s`, and also configurable thru ENV Variables.

## Env Variables
```
KEYCLOAK_SMTP_TIMEOUT 
KEYCLOAK_SMTP_CONNECTION_TIMEOUT 
KEYCLOAK_SMTP_WRITE_TIMEOUT 
```

## How to Build
```
$ mvn -pl services -am clean install -DskipTests
```