# AWS EKS TERRAFORM

----------------

    1. create the ec2 instance key
    2. aws access key
    3. aws secret key
    4. backend s3 bucket
    5. iam users 

----------------

# PROCESS FLOWS

----------------

![1](Images/1.png)

![2](Images/2.png)

![3](Images/3.png)

----------------

# RESOURCE PROVISION DEPLOYMENT

----------------

![1](Images/D1.png)

![2](Images/D2.png)

![3](Images/D3.png)

----------------








    terraform init
    terraform apply   -var-file=config.tfvars -auto-approve
    terraform destroy -var-file=config.tfvars -auto-approve


    # aws eks --region eu-central-1 update-kubeconfig --name ts-staging

    aws iam create-access-key --user-name democlt-alb-user
  
    ALB_ACCESS_KEY_ID=XXXX
    ALB_SECRET_ACCESS_KEY=XXXX

    kubectl create secret generic \
      alb-ingress-controller-creds -n kube-system \
      --from-literal=access_key_id=$ALB_ACCESS_KEY_ID \
      --from-literal=secret_access_key=$ALB_SECRET_ACCESS_KEY
