# zabbix-k8s

An example of zabbix-server / zabbix-agent deployment using k8s.

## Usage

clone this project.

```
git clone https://github.com/megmogmog1965/zabbix-k8s.git
cd zabbix-k8s
```

Run zabbix-server.

```
kubectl create -f zabbixserver.yml
```

Run zabbix-agent.

```
kubectl create -f zabbixagent.yml
```

Use web browser to access http://xx.xx.xx.xx .

```
$ kubectl get services
NAME                CLUSTER-IP     EXTERNAL-IP     PORT(S)                                      AGE
mysql               10.0.28.96     <none>          3306/TCP                                     52m
zabbixserver        10.0.83.213    <none>          10051/TCP                                    52m
zabbixweb           10.0.72.125    xx.xx.xx.xx     80:30390/TCP                                 52m
```
