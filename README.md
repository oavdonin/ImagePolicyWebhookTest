This manifests are built to spin up an extertnal service, which can be used together with K8S ImagePolicyWebhook Admission Controller for CKS exam preparation.

1) Generate x509 key & certicate with OpenSSL 


2) Create secrets before deployment

`$ kubectl create secret generic conf -n imgvalidator --from-file=external-cert.pem --from-file=external-key.pem`

3) Create all the resources

`kubectl apply -f .`