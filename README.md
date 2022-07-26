# k8s
<h3>It started working after edited the metrics-server deployment yaml config to include a DNS policy.</h3>
<br> ~$ kubectl apply -f metrics-server-components.yaml</br>
<br> ~$ kubectl edit deployments.apps -n kube-system metrics-server</br>
<br>Add this below dns policy or at the end of the container section above the restart policy.</br>
<br>hostNetwork: true</br>
<img src="./add-line.png">
