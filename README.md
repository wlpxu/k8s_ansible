# выполнить на мастере 
sudo kubeadm init
# результат вставить в ноды 
$ sudo kubeadm join k8scontrol:6443 --token n26y5i.thy19qec7vgo2ml7 \
        --discovery-token-ca-cert-hash sha256:7410e9117dc43ce8e194558f0753f907690058d61872f7ff9a9f09457fa30ccd

# загрузка и установка calico прописывать на мастере
kubectl apply -f https://raw.githubusercontent.com/projectcalico/calico/v3.29.1/manifests/calico.yaml




# для создания kube config
 mkdir -p $HOME/.kube
$ sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
$ sudo chown $(id -u):$(id -g) $HOME/.kube/config
