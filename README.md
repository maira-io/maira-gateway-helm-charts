# Maira-gateway helm chart

This helm chart installs maira-gateway on any k8s cluster

You can specify values in value.yaml

If you do not want to connect to maira cloud, skip the maira section, otherwise provide:
```
maira:
  sitemanager: sitemanager.demo.maira.io:443 
  site: <unique site name>
  tenant: <your maira tenant name, usually your domain name, e.g. google.com >
  namespace: default
  auth_client_id: <your client id provided by maira>
  auth_client_secret: <your client secret provided by maira>
```

For laptop based deployment, provide:
```
maira:
  sitemanager: localhost:3000
  site: <unique site name>
  tenant: <your maira tenant name, usually your domain name, e.g. google.com >
  namespace: default
```


To configure each service, follow instructions from our [integration page](https://docs.maira.io/integrations/).

Once configured, you can run the following command:
```
$ helm install -f values.yaml <site-name> .
```


