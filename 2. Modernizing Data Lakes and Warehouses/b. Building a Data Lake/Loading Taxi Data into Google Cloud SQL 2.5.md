Get your IP address
`export ADDRESS=$(wget -qO - http://ipecho.net/plain)/32`

Whitelist the Cloud Shell instance for management access to your SQL instance:
`gcloud sql instances patch taxi --authorized-networks $ADDRESS`

Get Cloud SQL IP

```
MYSQLIP=$(gcloud sql instances describe \
taxi --format="value(ipAddresses.ipAddress)")
```
