# Maira-gateway helm chart

This helm chart installs maira-gateway on any k8s cluster

You can specify values in value.yaml

If you do not want to connect to maira cloud, skip the maira section, otherwise provide:
  sitemanager: sitemanager.demo.maira.io:443 
  site: <unique site name>
  tenant: <your maira tenant name, usually your domain name, e.g. google.com >
  namespace: default
  auth_client_id: <your client id provided by maira>
  auth_client_secret: <your client secret provided by maira>



To configure appdynamics, provide:
  url: <url to connect to appdynamics>
  client_id: <client id from appdynamics>
  client_secret:  <client secret from appdynamics>
  token_url: <token url from appdynamics>

gcp:
  default_project: <gcp project name that you want to use for default project>
