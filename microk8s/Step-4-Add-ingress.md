### Expose Dashboard with Ingress

For this you need below things:
* Ingress resource
* Ingress Controller
* MetalLB Load Balancer
* microK8s comes with both; just run below command.
```
$ microk8s enable metallb
$ microk8s enable ingress
```

* Create an Ingress Resource
```yml
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: dashboard-ingress
spec:
  rules:
  - http:
      paths:
      - path: /dashboard
        pathType: Prefix
        backend:
          service:
            name: kubernetes-dashboard
            port:
              number: 443
```