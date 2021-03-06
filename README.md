# MPTCP aware load balancing application on ONOS

##项目介绍
  MPTCP是传统TCP协议的一个扩展，可以将一条TCP流分解为多条子流。对与类似于数据中心这样的场景，网络中有众多的冗余链路，利用MPTCP多子流的特性，可以通过将子流分布在这些冗余链路上传输的方式，增加链路利用率，提供传输吞吐量。对于MPTCP利用的重点于如何充分利用网络中的冗余链路，将子流平摊到这些链路上去。  
  MPTCP-aware APP旨在分析TCP握手阶段的数据包，识别MPTCP流，根据控制器掌握的全局拓扑为MPTCP的主流和多自流进行全局最优选路，充分利用网络中的冗余链路来分摊传输流量，达到网络负载均衡的效果。
