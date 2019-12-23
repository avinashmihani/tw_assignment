# Kubernetes: Change YAML config for different environments prod/dev

1. Default state should have 3 instances of the application available at any given point of time in production environment but for other environments the value is 1.

```
There is a foundation set of yaml, alters depending on the environment.

```

2. If the average CPU utilisation is more than 80% for 5 minutes, then add 1 more instance to the existing number.

```
myapp-hpa.yaml takes care of scale up by 1 until cpu utilization is > 80%

```

3. [Optional]

4. APIs exposed by the application to be accessible to the public using the domain name <env>.api.com over port 80 but the application instances (i.e the executable or the war file) listen on port 8080 only.

```
Deployment, service anc ingress.yaml takes care of the port and the domain name

```


