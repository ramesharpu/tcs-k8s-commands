|	Sl. No.	|	explaination	|	commands	|
| :---: | --- | --- |
|	1	|	to create a pod	|	kubectl run nginx-demo --image=nginx	|
|	2	|	to create deployment	|	kubectl create deployment depl --image=nginx	|
|	3	|	to create deployment with replicas	|	kubectl create deployment depl --image=nginx --replicas=5	|
|	4	|	to get the pods	|	kubectl get pods	|
|	5	|	to get the pods with more information	|	kubectl get pods -o wide	|
|	6	|	to get the deployement	|	kubectl get deployment	|
|	7	|	to describe the deployment	|	kubectl describe deployment depl	|
|	8	|	to describe the pods	|	kubectl describe pods <pod-name>	|
|	9	|	to see the pods changes	|	kubectl get pods -o wide --watch	|
|	10	|	to explain the resource documentation	|	kubectl explain resource-name <p> eg: <p> * kubectl explain deployment <p> * kubectl explain pod	|
|	11	| selector - equality based	|kubectl get pods --selector color=blue	|
|	12	|		|	kubectl get pods --selector color==blue	|
|	13	|		|	kubectl get pods --selector color==green	|
|	14	|		|	kubectl get pods --selector color!=blue	|
|	15	|		|	kubectl get pods --selector color!=green	|
|	16	| selector - set based		  | kubectl get pods --selector "color in (blue)"	|
|	17	|		|	kubectl get pods --selector "color in (green)"	|
|	18	|		|	kubectl get pods --selector "color not in (green)"	|
|	19	|		|	kubectl get pods --selector "color notin (green)"	|
|	20	|		|	kubectl get pods --selector "color notin (blue)"	|
|	21	|	to delete a resource	|	"kubectl delete <resource-type> <resource-name> eg: kubectl delete deployment depl"	|
|	22	|	to create a resource using the file	|	kubectl apply -f <file-name.yaml>	|
|	23	|	to delete a resource using the file	|	kubectl delete -f <file-name.yaml>	|
| 24 | service | to connect via cluster plane | kubectl expose deployment depl --port=80 --target-port=80 --type=ClusterIP | 
| 25 | | to connect via node machines | kubectl expose deployment depl --port=80 --target-port=80 --type=NodePort | 
| 26 | | to connect via loadbalancer | kubectl expose deployment depl --port=80 --target-port=80 --type=LoadBalancer | 
| 27 | | to connect via external name| kubectl expose deployment depl --port=80 --target-port=80 --type=ExternalName | 
| 28 | |  to expose the created service in minikube | minikube service service-name
