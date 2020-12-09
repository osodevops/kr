### KR

Kr is a tool for Kubernetes developers. It can be used to quickly collect and summarize
all container error log entries generated in a Kubernetes cluster. These log entries would otherwise
be individually accessible through kubectl (pod-by-pod).

"kr" is based on the work made by Abhishek Tamrakar for "Krawl". 
"Krawl" relies heavily on the functionalities of "kubectl".
Kr makes use of some of the functions developed in Krawl and adds extra functionality on top of them.

### How to use kr?
1. Place the program to /usr/local/bin/kr and make sure you have execution rights.
2. Invoke the program by typing "kr" at command line.
3. Program collects and displays all container error log entries found for the
EKS cluster which you are currently connected to.
4. Program runs until it is stopped with "Ctrl+c"
5. If no error entries are found the program simply displays the current date.

### User-definable variables
# location of the kubeconfig file
KUBE_LOC=~/.kube/config
# time window for which logs are processed
TAIL_SINCE="5m"

### Dependencies (among other dependencies)
kubectl, egrep, awk
