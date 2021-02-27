# KR

Kr is a tool for Kubernetes developers to quickly collect and summarize container error log entries produced by individual pods in a Kubernetes cluster.
These log entries are individually (pod-by-pod) accessible through kubectl. Kr collects, filters and summarizes the error log entries.
It's main use case is during development phase, but it also comes handy in production for being able to quickly identify the root cause for problems.
More sophisticated log processing, monitoring and alerting tools exist for more in-depth analysis.

"kr" is based on the work made by Abhishek Tamrakar for "Krawl". 
"Krawl" relies heavily on the functionalities of "kubectl".
Kr makes use of the functions developed in Krawl and kubectl and adds extra functionality on top of them.


![](kr.gif)

## How to use kr?
1. Clone the repo

`$ git clone https://github.com/osodevops/kr.git`

2. Change execution rights

`$ chmod 0744 kr`

2. Move the program to a folder location which is in the user's path.

`$ sudo mv kr /usr/local/bin/`

3. Invoke the program by typing "kr" at command line.

`$ kr`

- Program collects and displays all container error log entries found from the
EKS cluster which you are currently connected to (specified in the kubeconfig-file)

- Program runs until stopped with control characters "ctrl+c"

- If no error entries are found the program simply displays the current date

## User-definable variables
#### Location of the kubeconfig file
KUBE_LOC=~/.kube/config
#### The length of the time window for the log scan
TAIL_SINCE="5m"

## Main dependencies
- kubectl
- egrep
- awk
