# KR

Kr is a tool for Kubernetes developers to quickly collect and summarize container error log entries produced by individual pods in a Kubernetes cluster.
These log entries are individually (pod-by-pod) accessible through kubectl. Kr collects, filters and summarizes the error log entries.
It's main use case is during development phase, but it also comes handy in production for being able to quickly identify the root cause for problems.
More sophisticated log processing, monitoring and alerting tools exist for more in-depth analysis.

"kr" is based on the work made by Abhishek Tamrakar for "Krawl". 
"Krawl" relies heavily on the functionalities of "kubectl".
Kr makes use of the functions developed in Krawl and kubectl and adds extra functionality on top of them.

## How to use kr?
1. Place the program to /usr/local/bin/kr and make sure you have execution rights.
2. Invoke the program by typing "kr" at command line.
3. Program collects and displays all container error log entries found for the
EKS cluster which you are currently connected to.
4. Program runs until stopped with control characters "ctrl+c"
5. If no error entries are found the program simply displays the current date.

## User-definable variables
#### location of the kubeconfig file
KUBE_LOC=~/.kube/config
#### time window for which logs are processed
TAIL_SINCE="5m"

## Dependencies (among other dependencies)
kubectl, egrep, awk
