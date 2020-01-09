# End-to-End F5 DNS wide-ip provisioning.
# Author: mariel.donila@gmail.com


#### Introduction: 
The biggest problem we have had over the years with F5 devices are 
1. Inconsistency of our naming convention.
2. Easy to follow how the service was provisioned.
3. What the service is for?
4. Where does the F5 service fits into the businesses big picture?
5. There is no need for a VIP. This reduces the "troubleshooting" by different departments for now ;)

#### How did Ansible help you?
We have two main use cases (for now):
1. Fully Qualified Domain Names (FQDN) for "stateless" services like RestAPI, SOAP/XML and etc.
2. Fully Qualified Domain Names (FQDN) for "stateful" services like a HTTP GUI, Java GUI and etc.

For now, we use "three" concepts of "load balancing" which I will explain later.
1. Balanced across all sites.
2. KPR site only.
3. HAM site only.

*Balanced Across Sites* - There are instances that the total number of nodes are uneven or even with an "even" total number of nodes. So ratio, must be calculated. For example, KPR has 5 nodes then HAM has 1 nodes.

*KPR or HAM site only* - More traffic in one site at a time. 
