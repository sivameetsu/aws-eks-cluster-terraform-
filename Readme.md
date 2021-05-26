aws eks terraform 

    1. create the ec2 instance key
    2. aws access key
    3. aws secret key
    

Resource provisiong command

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
