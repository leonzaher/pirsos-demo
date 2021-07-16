`kubectl config view --raw --minify --flatten -o jsonpath='{.clusters[].cluster.certificate-authority-data}' > cabundle.txt`
-> Paste into values.yaml

Setup other values in values.yaml

`helm install pirsos pirsos/pirsos -n pirsos -f 1_values.yaml`

`kubectl get deployment -n pirsos pirsos`

`kubectl apply -f 2_ingress-pirsos.yaml`

`kubectl apply -f 3_tester.yaml`

https://tester.pirsos.xyz