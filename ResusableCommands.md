sudo snap install microk8s --classic
    3  sudo ufw allow in on cni0 && sudo ufw allow out on cni0
    4  sudo ufw default allow routed
    5  microk8s enable dns
    6  sudo microk8s enable dns
    7  sudo microk8s enable dashboard
    8  sudo microk8s enable storage
    9  sudo microk8s enable ingress
   10  sudo microk8s enable registry
   11  sudo microk8s status
   12  microk8s kubectl get all --all-namespaces
   13  sudo microk8s kubectl get all --all-namespaces
   14  curl 10.152.183.84:443
   15  curl https://10.152.183.84:443
   16  token=$(microk8s kubectl -n kube-system get secret | grep default-token | cut -d " " -f1)
   17  microk8s kubectl -n kube-system describe secret $token
   18  sudo microk8s kubectl port-forward service/kubernetes-dashboard 8085:443
   19  sudo microk8s kubectl port-forward service/kubernetes-dashboard 8085:443 -A
   20  sudo microk8s kubectl cluster-info
   21  curl https://127.0.0.1:10443
   22  ls
   23  ls -la
   24  nano .bashrc
   25  m
   26  source ~/.bashrc
   27  source ~/.bashrcm
   28  m
   29  clar
   30  ms
   31  clear
   32  ms
   33  ms create ns dev-env
   34  mk create ns dev-env
   35  mk create ns sit-env
   36  mk create ns uat-env
   37  mk create ns prod-env
   38  mk create deployment microbot --image=dontrebootme/microbot:v1
   39  mk get all -dev-env
   40  mk get all --dev-env
   41  mk get all ns dev-env
   42  mk get all -n dev-env
   43  mk delete ns dev-env
   44  mk delete ns sit-env
   45  mk delete ns uat-env
   46  mk delete ns prod-env
   47  mk get all 
   48  mk scale deployment microbot  --replicas=2
   49  mk get all 
   50  mk expose deployment microbot --type=NodePort --port=80
   51  mk get all 
   52  curl localhost:80
   53* curl localhost:3214
   54  mk get all --all-namespaces
   55  mk describe service/kubernetes-dashboard
   56  mk describe service/kubernetes-dashboard -n kube-system
   57  mk describe service/kubernetes-dashboard -n kube-system -0 json
   58  mk describe service/kubernetes-dashboard -n kube-system -o json
   59  mk edit service/kubernetes-dashboard -n kube-system
   60  mk get all --all-namespaces
   61  token=$(microk8s kubectl -n kube-system get secret | grep default-token | cut -d " " -f1)
   62  microk8s kubectl -n kube-system describe secret $token
   63  sudo token=$(microk8s kubectl -n kube-system get secret | grep default-token | cut -d " " -f1)
   64  microk8s kubectl -n kube-system describe secret $token
   65  token=$(mk -n kube-system get secret | grep default-token | cut -d " " -f1)
   66  mk -n kube-system describe secret $token
   67  m config
   68  mk get all
   69  mk -v=6
   70  mk get pods -v=6
   71  m config
   72  mk get ns
   73  mk create ns dev-ns
   74  kubectl create deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns
   75  mk create deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns
   76  mk delete deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns
   77  mk delete deployment express-js-app  -n dev-ns
   78  history