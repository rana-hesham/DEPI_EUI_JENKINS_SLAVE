# DEPI_EUI_JENKINS_SLAVE
# Build an image on a slave node and push it to docker hub using Jenkins
references: https://docs.redhat.com/en/documentation/red_hat_update_infrastructure/4/html/installing_red_hat_update_infrastructure/assembly_generating-a-cryptographic-key-pair_installing-red-hat-update-infrastructure#proc_generating-an-ecdsa-key-pair_assembly_generating-a-cryptographic-key-pair

https://docs.docker.com/engine/install/linux-postinstall/

Install java and docker on the slave

note: be sure to install ssh on the two machines

Generate a ssh key on the master node then copy the public key to the slave

ssh-keygen -t ecdsa -b 384

ssh-copy-id jenkins@Slave

Add the private key in the slave node credentials on jenkins

![image](https://github.com/user-attachments/assets/ac9ce732-7483-4bdf-98f9-35d108b5cc86)



![image](https://github.com/user-attachments/assets/a8448ddb-d13f-4a53-903a-f6a40f224534)

![image](https://github.com/user-attachments/assets/40f3d327-b7b0-49c0-bed0-60a2ef2aa23d)
