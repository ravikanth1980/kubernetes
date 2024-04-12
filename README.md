Kubectl commands

    1  ls
    2  clear
    3  curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/kubectl
    4  chmod +x ./kubectl
    5  sudo mv ./kubectl /usr/local/bin/kubectl
    6  kubectl version
    7  export PATH=$PATH:/usr/local/bin
    8  ls -l /usr/local/bin/kubectl
    9  kubectl version
   10  curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.21.2/2021-07-05/bin/linux/amd64/aws-iam-authenticator
   11  chmod +x ./aws-iam-authenticator
   12  sudo mv ./aws-iam-authenticator /usr/local/bin/aws-iam-authenticator
   13  aws-iam-authenticator version
   14  aws eks --region us-east-1 update-kubeconfig --name Mycluster
   15  aws configure
   16  aws eks --region us-east-1 update-kubeconfig --name Mycluster
   17  clear
   18  kubectl get nodes
