# DataMiningForNetworks
The goal of the project is to develop a method to carry out anomaly detection in IP traffic. 

Different types of attacks exist in a network, e.g. port scan, denial of services, botnets. There are two main ways to prevent them. The first one is to try to detect explicitely a virus in the payload of packets. The second one is to detect anomalous patterns of communication.  In few words, the principle of the method is to build a profile of each IP address under the form of a small graph, called graphlet. We then build a model using Support Vector Machine to distinguish normal from malicious end hosts from an annotated trace. The last step will be to try to detect attack in a not annotated trace.

The project is based the concept from *Karagiannis, T., Papagiannaki, K., Taft, N., and Faloutsos, M. (2007, April). Profiling the end host. In International Conference on Passive and Active Network Measurement (PAM) (pp. 186-196). Springer, Berlin, Heidelberg.*


1. Build all the end host graphlets corresponding to a traffic trace with annotated flows.
2. Build the end host models using the random walk kernel, but in two ways. First, do not use the kernel trick to avoid the mapping of the graphlets in the high dimensional space. Second, using the kernel trick. To be more specific, transform the graphlets into the high dimensional space of the random walk kernel (consider only walks of length 4).
