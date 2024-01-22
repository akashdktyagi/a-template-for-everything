### Expose Dashboard with Ingress

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