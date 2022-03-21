(Northbound interface - connects to applications, Southbound interface - connects to switches, East and West bound interface - across the control layer)

# Attacks

## 11

Attacks listed-
Controlplane specific attacks - against control and application layer

Controlchannel specific attacks - against openflow
(OpenFlow is a communications protocol that gives access to the forwarding plane of a network switch or router over the network. OpenFlow enables network controllers to determine the path of network packets across a network of switches.)

Dataplane specific attacks - on network devices

Various types of DDoS attacks -- >
Application Layer DDoS attacks
(attack applications, or attack the northbound API)

Control Layer DDoS attacks
(attacking the controller, the northbound API, the southbound API, the westbound API, or the eastbound API. many conflicting flow rules from different applications may cause DDoS attacks on the control plane.)

Infrastructure Layer DDoS attacks
(attack switches or attack the southbound API. if only header information is transmitted to the controller, the packet itself must be stored in node memory until the flow table entry is 
returned. In this case, it would be easy for an attacker to execute a DoS attack on the node by setting up a number of new and unknown flows. As the memory element of the node can be a bottleneck due to high cost, an attacker could potentially overload the switch memory (e.g. targeting to exhaust TCAMs). The generated fake flow requests can produce many useless flow rules that need to be held by the data plane, thus making it difficult for the data plane to store flow rules for normal network flows.)

Packet flooding
(An attacker generates a number of distinct network flows, numerous Packet-In messages are 
sent to the controller, and the resources of the controlplane will be consumed Those a bunch set of Packet-In messages could make a controller be under an unpredictable state.)

Control message manipulation
(Through manipulating control messages, an attacker performs Switch Table Flooding, Switch Identification Spoofing, and Malformed Control Messageattacks. The attack sequences is an attacker manipulates control messages and controller parses sent control messages and worked unexpectedly)


## ref

Attacks in control layer -
DDoS attack
( The attacker creates a series of illegal accesses to impose excessive load on the controller, which causes the system resources unavailable to legitimate users)

Hijacked/Rogue controller
(The attacker can use the admin station to hijack the controller, thus causing the user’s legitimate request to be rejected. In some severe cases, the attacker can use physical or logical method to destroy the controller and modify the network.)

Poor controller deployment
(Single controller instead of keeping backup controllers)

Attacks in data layer -
Authorized authentication
(Lacks effective authentication mechanisms that can lead to acceptance of false data packets and rejection of correct data packets.)

Legality and consistency of flow rules
( During the generation process, multiple applications cause conflicts or override flow rules. During the release process, transmission delay or malicious tampering causes the flow rules inconsistent between the controller and switches. During the update process, updating causes the synchronization of flow rules between different switches. In SDN network, failure of network nodes, traffic load transfer, or network maintenance may cause the flow rules to be updated)

DDoS attacks
(the attacker creates a series of illegal accesses, and the flow table space is squeezed by invalid traffic rules . A lot of flow table resources will be consumed, and normal flow rules do not have enough space to process. DoS/DDoS attacks can degrade network performance.)

Side channel attacks
(By using side channel attacks, an attacker can infer network-related state information (such as flow table information) by testing the execution time of the specific type of data packet. Therefore, the flow table may cause data leakage problems. Although side channel attacks do not directly affect the availability, confidentiality or integrity of data, they can trigger further attack)


## 25

DDoS Attacks
Controller Compromise
Thrid-Party Add-ons
Attacks on control level communication and data transfer
Listening attacks


# Solutions

Preventing DDos Attacks
------------------------

## 5

ensemble model technique, classifiers


## 6

entropy technique followed by ML


## 3

DDoS attack mitigation using DNN


14 another entropy based approach (redundant)


## 21

Various other mitigation techniques


ML based techniques
-------------------

## 28

Attack pattern prediction using ML techniques


## 24

Evaluation of ML techniques for SDN security


Firewall
--------

## 22

Using firewall for SDN security



Blockchain
----------

## 10

Using blockchain for security