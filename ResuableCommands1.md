 1  uname -a
    2  sudo apt-get update
    3  sudo apt-get install -y     apt-transport-https     ca-certificates     curl     gnupg2     software-properties-common
    4  curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -
    5  sudo add-apt-repository     "deb [arch=amd64] https://download.docker.com/linux/debian \
    6      $(lsb_release -cs) \
    7      stable"
    8  sudo apt-get update
    9  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   10  getent
   11  getent group
   12  sudo usermod -aG docker bitnami
   13  docker run hello-world
   14  sudo docker run hello-world
   15  exit
   16  docker run hello-world
   17  history
   18  docker ingo
   19  docker info
   20  echo $USER
   21  groups $USER
   22  getent passwd
   23  group jenkins
   24  $ sudo usermod -aG docker jenkins
   25  sudo usermod -aG docker jenkins
   26  groups jenkins
   27  sudo -u jenkins docker info
   28  chmod 777 /var/run/docker.sock
   29  sudo chmod 777 /var/run/docker.sock
   30  python3 -m pip install semgrep
   31  ls
   32  cat bitnami_credentials 
   33  kubectl create deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns
   34  kubectl create deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns -v=6
   35  kubectl delet  deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns -v=6
   36  kubectl delete  deployment express-js-app --image=docker.io/333743/express-js-app:latest -n dev-ns -v=6
   37  kubectl delete  deployment express-js-app -n dev-ns -v=6
   38  sudo kubectl delete  deployment express-js-app -n dev-ns -v=6
   39  cd ..
   40  cd ~
   41  ls
   42  ls -la
   43  cd .kube
   44  cat config 
   45  cd ..
   46  history