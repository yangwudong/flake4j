Flake4J - Flake ID generator for Java
======================================

This is an implementation of the [Flake](https://github.com/boundary/flake) decentralized, k-ordered ID generation algorithm by Boundary.

There is no server implementation yet. To avoid non-unique IDs, it is the programmer's responsibility to  ensure that only one instance of the ID generator is active in a 
single node (if the MAC address based node identification is used). 


Usage
-----

```java
// Create an ID generator that uses the machine's MAC address for node identification
Flake4J f4j = Flake4J.newInstance();

// Use a custom node identifier instead of the MAC address
NodeIdentifier nodeIdentifier = () -> uniqueNodeIdentifier // long value
Flake4J f4j = Flake4J.newInstance(nodeIdentifier);
```
