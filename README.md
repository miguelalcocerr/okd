# okd
implementación de cluster Okd 4.15  

Método de instalación: UPI   
URL Instalador FCOS = https://builds.coreos.fedoraproject.org/prod/streams/stable/builds/39.20240210.3.0/x86_64/fedora-coreos-39.20240210.3.0-live.x86_64.iso  
URL = https://docs.okd.io/4.15/installing/installing_bare_metal/preparing-to-install-on-bare-metal.html     
URL = https://github.com/okd-project/okd/releases/tag/4.15.0-0.okd-2024-03-10-010116  
URL = https://mirror.openshift.com/pub/openshift-v4/dependencies/rhcos/latest  
URL iso RHCOS .415 = https://mirror.openshift.com/pub/openshift-v4/x86_64/dependencies/rhcos/4.15/4.15.23/rhcos-4.15.23-x86_64-live.x86_64.iso   
URL CoreOS = https://mirror.openshift.com/pub/openshift-v4/clients/coreos-installer/latest   
URL descarga iso OKD = https://fedoraproject.org/en/coreos/download?tab=metal_virtualized&stream=stable   
URL descarga iso OKD = https://builds.coreos.fedoraproject.org/browser?stream=stable&arch=x86_64   


Bastión:    
Se crean los directorios:  
#mkdir -p /okd_415/install_okd415  
#./openshift-install create ignition-configs --dir=/okd_415/install_okd415/  
#./openshift-install create install-config --dir=/okd_415/install_okd415  

<img width="793" height="347" alt="image" src="https://github.com/user-attachments/assets/75f23988-0b67-458e-9059-fe254fcbe9e7" />

<img width="469" height="200" alt="image" src="https://github.com/user-attachments/assets/19a2b6e6-d8ce-492d-9544-5077f0aaea60" />


Cluster OKD:
<img width="1406" height="145" alt="image" src="https://github.com/user-attachments/assets/caa1c63c-35b2-4409-b93b-7a6704e816c2" />

URL = https://console-openshift-console.apps.clusterokd.alcocerrojo.pe/dashboards  
<img width="2493" height="961" alt="image" src="https://github.com/user-attachments/assets/ade625eb-6c1e-455b-85ef-31ff173b20ce" />

Revisar Logs del cluster OKD:  
#oc get co | grep -v "True.*False.*False"  
#oc get csr
#oc get csr -o name | xargs oc adm certificate approve  --> Aprobar los certificados  



BALANCEADOR:
Se realizó la instalación del paquete HAProxy
<img width="2508" height="958" alt="image" src="https://github.com/user-attachments/assets/626b8501-da10-461f-84e7-da52774651f2" />

APP web de Clínica de salud para generar citas:

URL = http://clinica-alcocer-web-clinica-alcocer-rojo.apps.clusterokd.alcocerrojo.pe  
Repositorio = https://github.com/miguelalcocerr/appp_web_clinica  
<img width="1582" height="950" alt="image" src="https://github.com/user-attachments/assets/d3d78398-fc14-4f66-847f-0252ced6b17a" />  

<img width="1299" height="574" alt="image" src="https://github.com/user-attachments/assets/fcab0f9c-ca5a-46e2-a70c-7e1903b6bd08" />  

