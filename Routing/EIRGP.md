# EIGRP Overview
- Purpose
- Benefits
  - **Fast Convergence**
  - **Scalability**
  - **Reduced Network Traffic**
  - **Multiple Network Layer Protocols Support**
- History and Evolution
  - **EIGRP v1** (Early Proprietary Version)
  - **EIGRP for IPv4** (Standard Implementation)
  - **EIGRP for IPv6** (Support for IPv6 Networks)

---

# EIGRP Fundamentals
- **Distance Vector Protocol with Link-State Features**
- **Hierarchical Design**
  - **Autonomous System (AS)**
  - **Scalability with Network Hierarchy**
- **Router ID** (Unique Identifier for Each Router)
- **Metric Calculation**
  - **Bandwidth**
  - **Delay**
  - **Load**
  - **Reliability**
  - **MTU**
- **Administrative Distance (AD)**
  - Default AD of **90** for EIGRP
- **EIGRP Neighbor Adjacency**
  - Adjacency vs. Neighboring Relationship
  - **EIGRP Neighbor States**

---

# EIGRP Packet Types
- **Hello Packet**
  - Establishes and Maintains Neighbor Adjacency
  - **Default Hello Interval** (default: **5 seconds** on LAN, **60 seconds** on WAN)
  - **Default Hold Time** (default: **15 seconds** on LAN, **180 seconds** on WAN)
- **Update Packet**
  - Sends routing updates to neighbors
- **Query Packet**
  - Requests specific routing information from neighbors
- **Reply Packet**
  - Responds to a Query Packet
- **Acknowledgment Packet**
  - Acknowledges the receipt of Update Packets

---

# EIGRP Neighbor Discovery
- **EIGRP Neighbor Discovery Process**
  - Discovering and maintaining neighbor relationships
- **Multi-Access Networks (e.g., Ethernet)**
- **Point-to-Point Links**
- **Neighbor Relationship States**
  - Initial, 2-Way, and Fully Established
- **EIGRP Timers**
  - Hello Interval
  - Hold Time

---

# EIGRP Metrics
- **Composite Metric Calculation**
  - **Bandwidth** (in kbps)
  - **Delay** (in microseconds)
  - **Load** (as a percentage)
  - **Reliability** (1-255, where 255 is 100% reliable)
  - **MTU** (Maximum Transmission Unit)
- **Metric Weighting Factors**
  - Default weights: 
    - **K1** (Bandwidth) = **1**
    - **K2** (Load) = **0**
    - **K3** (Delay) = **1**
    - **K4** (Reliability) = **0**
    - **K5** (MTU) = **0**
- **Metric Calculation Formula**
  - `Metric = ((K1 * Bandwidth) + (K2 * Bandwidth) / (256 - Load) + (K3 * Delay))`

---

# EIGRP Topology
- **Topology Table**
  - Maintains routes and associated metrics
- **Neighbor Table**
  - Maintains information about neighboring routers
- **Routing Table**
  - Contains the best routes to reach destinations
- **Dijkstra's Algorithm**
  - Used for calculating the shortest path

---

# EIGRP Features
- **Load Balancing**
  - Equal-Cost Multi-Path (ECMP) Support
  - Supports up to **16 equal-cost paths**
- **Route Summarization**
  - Manual Summarization on Interfaces
  - Automatic Summarization by Default
- **Route Redistribution**
  - Redistributing routes between different routing protocols
- **EIGRP Authentication**
  - Plaintext Authentication
  - MD5 Authentication
- **EIGRP for IPv6**
  - EIGRPv6 for IPv6 Networks
  - Uses similar principles as EIGRP for IPv4

---

# EIGRP Advanced Features
- **EIGRP Stub Routing**
  - Restricts the routes advertised by stub routers
- **EIGRP Traffic Engineering**
  - Provides mechanisms to manage bandwidth usage
- **EIGRP Named Mode**
  - Configuration using named EIGRP instances for better organization
- **Support for Multiple Network Layer Protocols**
  - Including IP, IPX, AppleTalk, etc.

---

# EIGRP Optimization Techniques
- **Reduced Update Frequency**
  - Using triggered updates instead of periodic updates
- **Path Control**
  - Adjusting metrics for preferred routes
- **Route Filtering**
  - Using access lists to control which routes are advertised
- **EIGRP Path Manipulation**
  - Changing route metrics for specific paths

---

# EIGRP Security
- **EIGRP Authentication**
  - Securing routing updates with authentication mechanisms
- **Passive Interfaces**
  - Disable EIGRP on specific interfaces to prevent exposure
- **Preventing Routing Loops**
  - Ensuring loop-free topology using feasible distance and reported distance

---

# EIGRP Design Considerations
- **Scalability**
  - Suitable for large networks with hierarchical design
- **Network Topology**
  - Consideration of multi-access versus point-to-point links
- **Load Balancing Strategies**
  - Configuring for optimal load distribution
- **EIGRP in Data Center Networks**
  - Enhancing connectivity and redundancy in data centers

---

# EIGRP Troubleshooting
- **Common Issues**
  - Neighbor adjacency problems
  - Mismatched EIGRP settings
  - Metric inconsistencies
- **Diagnostic Tools**
  - `show ip eigrp neighbors` Commands
  - `debug eigrp` for real-time troubleshooting
- **Monitoring and Logging**
  - Utilizing Syslog and SNMP for EIGRP
- **Performance Tuning**
  - Adjusting EIGRP timers for optimal performance

---

# EIGRP Miscellaneous
- **EIGRP for Traffic Engineering**
- **EIGRP with BGP**
- **EIGRP in MPLS VPNs**
- **EIGRP for GRE Tunnels**
