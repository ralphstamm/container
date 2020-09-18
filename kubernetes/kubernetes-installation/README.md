# Kubernetes Installation

The following packages should already be installed on the full version of Photon OS, but you might have to install them on the minimal version of Photon OS. If the `tdnf` command returns "Nothing to do," the package is already installed.

* Install Kubernetes on all hosts--both `photon-master` and `photon-node`.

```text
tdnf install kubernetes
```

* Open the tcp port 8080 \(api service\) on the photon-master in the firewall

```text
iptables -A INPUT -p tcp --dport 8080 -j ACCEPT
```

* Open the tcp port 10250 \(api service\) on the photon-node in the firewall

```text
iptables -A INPUT -p tcp --dport 10250 -j ACCEPT
```

* Edit /etc/kubernetes/config, which will be the same on all the hosts \(master and node\), so that it contains the following lines:

```text
# logging to stderr routes it to the systemd journal
KUBE_LOGTOSTDERR="--logtostderr=true"

# journal message level, 0 is debug
KUBE_LOG_LEVEL="--v=0"

# Should this cluster be allowed to run privileged docker containers
KUBE_ALLOW_PRIV="--allow_privileged=false"

# Comma separated list of nodes in the etcd cluster
KUBE_MASTER="--master=http://photon-master:8080"

```

