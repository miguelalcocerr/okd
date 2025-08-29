# okd
implementación de cluster Okd 

URL iso RHCOS .415:
https://mirror.openshift.com/pub/openshift-v4/x86_64/dependencies/rhcos/4.15/4.15.23/rhcos-4.15.23-x86_64-live.x86_64.iso 

-Bastion
Se crean los directorios:
#mkdir -p /okd_415/install_okd415
#./openshift-install create ignition-configs --dir=/okd_415/install_okd415/
#./openshift-install create install-config --dir=/okd_415/install_okd415


[root@bastion okd_415]# oc get nodes -o wide
NAME                                STATUS   ROLES                  AGE     VERSION           INTERNAL-IP      EXTERNAL-IP   OS-IMAGE                        KERNEL-VERSION          CONTAINER-RUNTIME
master1.clusterokd.alcocerrojo.pe   Ready    control-plane,master   3d22h   v1.28.7+6e2789b   192.168.18.222   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2
master2.clusterokd.alcocerrojo.pe   Ready    control-plane,master   3d22h   v1.28.7+6e2789b   192.168.18.223   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2
master3.clusterokd.alcocerrojo.pe   Ready    control-plane,master   3d21h   v1.28.7+6e2789b   192.168.18.224   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2
worker1.clusterokd.alcocerrojo.pe   Ready    worker                 3d21h   v1.28.7+6e2789b   192.168.18.225   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2
worker2.clusterokd.alcocerrojo.pe   Ready    worker                 3d21h   v1.28.7+6e2789b   192.168.18.226   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2
worker3.clusterokd.alcocerrojo.pe   Ready    worker                 3d21h   v1.28.7+6e2789b   192.168.18.227   <none>        Fedora CoreOS 39.20240210.3.0   6.7.4-200.fc39.x86_64   cri-o://1.28.2

BALANCEADOR:
<img width="2508" height="958" alt="image" src="https://github.com/user-attachments/assets/626b8501-da10-461f-84e7-da52774651f2" />
