###  Modeling the Adaptability of Network Protocols

####  Abstract 

The adaptability of network protocol( TANP ), which means whether the protocol can be deployed to the network and the extent of  application after a period of evolution. Many protocols developed slowly or failed, although they met the requirements of design technically. We propose a new model of TANP  which has two models to solve the problem, the self-evolution model(SEM) and the user dynamic selection evolution model(UDSEM). SEM determines whether the new network protocol can survive in evolution by simulating the evolution process of the protocol in the protocol stack. UDSEM counts the new user's penetration by simulating the transfer process of new protocol users in logical network. Then calculate the communication efficiency of new protocol evolves to the final state through the adaption of new protocol model to measure the adaptability of new network protocol, formulate the adaptability evaluation model based on the communication efficiency. We also present some main factors affect TANP and methods to improve the adaptability by analyzing the impact of factors on TANP.  After theoretic model simulation analysis, we draw some conclusions,the protocols at the waist of the hourglass appear to have less survival, while the lower and higher layers tend to live longer and easier. If we improve the utility of the protocol, the external utility of the protocol and the efficiency of the converters appropriately can play important roles in improving the ANP. The network protocol adaptability evolution model we proposed can be applied to assess the ANP. 

**[key Words]** Adaptation, Network Protocol,   

#### 0. Introduction

The Internet community has specified a large number of protocols to date, although they were developed, these protocols have achieved varying degrees of success. Two major dimensions on which a protocol can be evaluated are scale and purpose. Purpose can be explained whether the protocol could meet the design goals, which belongs to technical areas. Scale relates to the protocols were deployed at last, whether the numbers of users expected. Lots of protocols were not deployed  extensively. For example, IPv6 caused great concern since 1996, its deployment and usage is not optimistic at the moment compared to IPv4.  Most research on IPv6 is focused on technical research, such as, IP address allocation, dual stack coexistence, new network protocol and so on, which makes it dose not get enough attention about how to deploy and operate. That's why IPv6 develops so slowly although we made lots of progress.  This shows the research and develop about protocol is not just a technical problem, but the benefits, deployment expense, switch costs are important factors whether the protocol can be accepted by users after the protocol is applied to the network. It is the degree of users's acceptance of the protocol called "adaptability" after the protocol is applied to the network for a period. So not only the features and performance should be focused but the adaptability when we develop the protocol. Research on TANP, enabling developers to focus on technology to improve performance while designing the protocol , follow the protocol-related technology that focus on how to improve the adaptability of the protocol, increase the degree of users's acceptance. That makes different for lowering the costs and reducing the blindness of protocol development.  The emerging of various theories and methods lay a foundation for TANP which makes  TANP a very popular research at home and abroad. However,  the research of TANP is never easy, because the developers were not take economic, environment factors into consideration even based on false assumptions. Besides, common agreement has not been reached about evaluate the adaptability home and abroad, that's the problem to be solved. 

#### 1. Situation Analysis

The methods focused on TANP research  has two categories which is  intuitive methods of measurement and  modeling analysis. Traditional studies suggest that there are five factors can affect the deployment of a new protocol, they are relative advantage, compatibility, complexity, workability, observability. They study the effects of  economic factors, external network properties on the deployment of protocol and evaluate the adaptability of IPv6 from economic perspective by visiting equipment manufacturers, application providers, ISP and users\[10\]. Colitti L et al evaluate the adaptability of IPv6 as a user. When users post HTTP requests, they can choose post the data to the sever by IPv4 only or by dual-stack. They apply this method to Google then count and analyze the post data over past year,  the result shows a small-scale IPv6 deployment\[11\]. Zhus' opinion is that reasons affecting TANP is complex, and it is impossible to draw a conclusion by simple simulation or performance measurement. They visited 19 experts and had a discussion about the problem of HIP protocol was not widely used and its deployed policy from June 2011, 16 to September 1, finally analyze the reason why HIP protocol was not widely deployed.  On the one hand, intuitive measurement can analyze TANP in some degree and the data is not convincing,  on the other hand, the evaluation of TANP based on measurement should execute after the protocol applied to the network and the evaluation always fall behind in develop moment, so the evaluation cannot provide theoretical guidance at the beginning of develop the protocol\[7\].

To further characterize the evolution of the protocol in the network, scholars began apply modeling to analyze TANP, the adaptability model can be divided into two major categories of static and dynamic. Hovav et al has established a process model for describing protocol adopted by users and evaluated the impact of various factors on the deployment of the IPv6 protocol from environmental triggers and ites features two aspects\[12\]. Gyarmati et al applied game theory for transition and deployment of IPv6 is modeled analysis and research, they take the Internet ASs as interconnect and independent players and treat these ASs can choose their own running network protocol. The study shows that if all the ASs running IPv6 will be Nash Equilibrium, and if there are some ASs deployed IPv6 at the beginning in the Internet then the whole network will be deployed IPv6 faster and more feasible\[13\]. The author modeled the LOC/ID protocol, if the LOC/ID in order to applied in large scale, not only about its own technical advantages, and economic factors encountered during its deployment. The scale of LOC/ID depends on the reduced price and the efficiency of deployment, and the price of LOC/ID deployment must be less than BGP protocol. They use a differential equation for the deployment of converters, and other economic factors affecting the migration of network technology were analyzed.  The authors assume that there are two different architectures, and the proportion of deployment is x1 and x2, then they consider the technical quality, the proportion of deployment architecture, the price factor affect on different user utility. Build a dynamic economic model of technology deployment,and find than both deployment technologies have a corresponding stable equilibrium point  even though they have different initial deployment\[15\]. These studies examined how the two incompatible protocols chose by users. The articles focuse on how the converter help the users who using incompatible protocols to interact. Studies indicates that the external network will lead more balanced, and the converter make a great different on balancing the deployment\[16\]\[17\]\[18\]. Farrel extended the above model to a new architecture,  this model evaluated TANP from a practical aspect to the user's perspective rather than an ISP or equipment supplier's point. The model assumes that there are N users, each user will choose a protocol A or B, so if the utility of B is greater than A, users who use protocol A switch to use protocol B, and A, B protocol can achieve the purpose of coexistence through the converter. Then we can evaluate TANP by analyzing one user's utility and all users' utility\[19\]. Zhu, etc proposed the evaluation method for the application of TANP based on its architecture,  and the corresponding evaluation model was constructed\[20\]. Two mechanisms about multimedia data application were evaluated in this paper, the result showed that both theoretically advantageous protocols should be deployed under certain restrictions in order to play their advantage. Users and ISP should combined with own application requirements choose the corresponding architecture and protocol to deploy. 

Because the static model cannot describe the dynamic process of the acceptance of the protocol, the researchers established a dynamic model of TANP and Internet protocol for analysis. They analyze the coexistence of more than one network technology and the dynamic of TANP in single user and system. The authors noted that when a plurality of equilibrium exist, the deployment of a small change in the parameters of the system will affect the balance significantly\[21\]. In order to demonstrate the problems during the deployment, Eardley proposed a architecture and applied it to the multipath TCP and Congestion Exposure analysis\[22\]. In this paper they use non-cooperative game theory for each data flow find the most suitable flow control protocol.  Each flow has a utility that depends on throughput and also has a disutility that is some function of the queue lengths encountered along the route taken. Flows will choose a combination of protocols that would maximize their payoffs, then the available bandwidth will be distributed to them in a fair game way\[23\]. They presented an approach to Internet Quality of Service that they believe is more migration-friendly than current network-based mechanisms in the stage of design a new network protocol\[24\]. Akhta present a simulation based model explaining a marketÃ¢â‚¬â„¢s tendency to lock- in by means of two factors: the strength of network effects and the network topology of potential adopters and analyze the difference of show the same network effect strength but face different actor network topologies\[25\]. Joe-Wong develop a model for user adoption of a base wireless technology and a bundle of the base plus a supplementary technology. This paper studies the effects of the maximum profit and the deployment coverage on the balance of a outcome\[26\]. Akhshabi established a abstract model EvoArch, which reflects the evolution of the OSI protocol stack. He says that there will be competition among the same layer protocols for providing the same services for upper protocols\[27\]. Li and Li et al extends the model\[13\], and apply the extended model to analyze trends in the triple play of Internet, telecommunications and television networks\[28\]. Studies shows that no matter what is the original proportion of the three networks, they will eventually converge to one or two networks and the the higher proportion of initial network  has more advantage. 

We proposed a model of TANP based on the existing analysis of adaptability, and simulated the evolution process. Then analyze the factors affect TANP and raise a new method which can improve the adaptability by researching the change of share in the evolution of a new protocol. Users establish a connection depend on the status, we will communicating

#### 2. Model Description

As is shown in Figure 1, the protocol evolution can divide into two stages. (1) The self-evolution stage, propose a evolution model in protocol stack according to the protocol location, competitiveness and vitality of the protocol before being deployed to the network, then we can get the initial permeability of a new protocol after being deployed in real networks. (2) The Internal evolution stage, after the deployment of the new protocol to the network, we must calculate the economic profits of each node firstly, then we can get the final permeability of the new protocol according to the state transition policy based on user protocol. When the internal evolution comes to the end, the nodes can establish network topology according to the states and the protocol communication strategies of them,  then evaluate TANP by calculating the communication efficiency. 

##### 2.1 Self- Evolution Model

The Internet protocol stack has a layered architecture that resembles an hourglass. Akhshabi also propose a model based on the hourglass-shaped Internet protocol stack to explain  how the model relates to protocol stacks and evolving network architectures. **The Evolution of Layered Protocol Stacks Leads to an Hourglass-Shaped Architecture**. That help us understand the self-evolution of the protocols. 

##### 2.2 Evolution Model Based on Dynamic Selection of User Behavior

As is shown in Figure 4, there are two kinds of nodes, User Nodes(UN) and Application Service Provider nodes(ASPN). The UN is someone who choose the service provided by a new protocol. The UNs are different according the protocols they chose.,for example, the network layer is a network composed of routers and ISP\[42\]. The ASPNs provide service for UNs, for example ISP can provide Internet service for users and they can get profits from users. A ASPN can provide service for dozens of UNs. The UNs can establish a physical topology, while the relationship between UNs and ASPNs form a logical network. The UNs have two states A and B, where A represents the user still use the current protocol, B states indicates that the UN use another new protocol which can provide the same service compared with the old one.  The more B states users, the better adaptability of the new protocol has. The ASPNs have four states, A, B, BA and AB, where states A represents that the ASPN can only provide the service of protocol A, service B cannot be provided, vice versa, while states AB indicates the the ASPN can provide the service of protocol A, and compatible conversion interface for protocol A users of protocol B, vice versa. 

The transition strategy between ASPN and UN is as follows:

The transition strategy between ASPN and UN depends on the utility of them, so the utility of a single UN in state A is

**[4.1]**

where alpha represents the utility provided by protocol A, NX indicates the amount of protocol A users who communicate to this protocol A user and beta NX represents the whole utility provided by NX useras of protocol A.  beta is the influence coefficient controls by network, where NXb represents the amount of protocol B users who communicate to this protocol A users and the betaN(1-q) represents the utility provided by protocol B users who choose the BA converter . Similarly understood, the utility of a single UN in state B is

**[4.2]**

The utility of the ASPN in state A:

**[4.3]**

where NXA is the amount of the users in state A while NXB is the mount  of users in state B, NX(1-q) represents  utility of the A state user who communicate to the nodes in BA state and the (1-q) indicates the utility of the A state user who communicate to the users. Similarly understood, the utility of ASPN in state B is

**[4.4]**

The utility of the ASPN in state AB:

**[4.5]**

where sigma is the for which the A and B  communication within ASPN who provided the AB converter, Ni represents the amount of B state user who communicate to the ith node. Similarly understood, the utility of the ASPN in state BA:

**[4.6]**

Whether the state of change at a time depending on the changed node can obtain the utility which cannot be obtain by the not-change nodes. For the UN, if the change the protocol from A to B, the following conditions must be met:

**[4.7]**

that is the sum of the utility  and the cost for the user from state A to state B less then the utility of state B. For ASPNs, there are four states of transformation, state A to state AB, state AB to state B, state A to B and state B to state BA, but the conditions must be met:

**[4.8]-[4.11]**

The following will introduce the model algorithm in detail.

Firstly, check the initial state of each user of the network according to the new protocol, then set the numbers and state of nodes. The dynamic evolution that user selected is a discrete-time evolution model, There are two following steps for every evolution process:

1. calculate all the UNs and ASPNs' utility.
2. revise the states for each node according to the transmission policy. 


Calculate the utility and revise the states according to the policy after the network reaches a steady state. 

##### 2.3 The ANP model of evaluation based on the network connection states

###### 2.3.1 Build the communication topology

Every node in the network will reaches to the final state within the dynamic evolution model, as is shown in Figure 5, the numbers of B state nodes in the final state. The numbers of B state users is the appearance of the ANP, while the deep reason that causes the protocol selecting is the communication efficiency provided by the protocols. So the relationship between the ANP and the final stage of evolution is that the UNs and ASPNs will establish a topology and communicate based on the transmission policy and the state pf the users in the final evolution stage. 

**Figure 5**

The connection among the ASPNs is already known to the UNs, and the connection among UNs in different areas charged by different ASPNs determined by the connection of ASPNs. The connection among the ASPNs is shown Figure 5.1, and the

- [ ] represents can build a connection between the converters


- [x] represents cannot build a connection between the converters

AS we can see from the chart, the ASPNs in different states can only establish connection between the UNs within the specific ASPN. We obtain the connection relationship as shown in Table 5.2 according to the connectivity rules. 

**Figure 5.2**

###### 2.3.2 Calculate the efficiency of communication

Assume a communication network topology is a graph G which has M edges, N points, so the communication efficiency is calculated as follows:

1. Firstly,  according to the position and the state of the nodes, we can establish a cost function F between two nodes,  so the communication efficiency of each edge is

2. Then, the communication efficiency between nodes pair is epsilon, which can be expressed as the sum of every edge's communication efficiency 

   **[5.1]**

   where k, r...s are the shortest path sequences which pass the i, j. 

3. The communication efficiency of G is

   **[5.2]**

   as you can see, the more close to 1 of E(G) , the better communication efficiency. We can get the indicators of the ANP by calculated the E(G), then evaluate the ANP. 

   ​


#### 3. Model Analysis

##### 3.1 Self-Evolution Model

**Table 3.1**

As is shown in Figure 3.8, 3.9, 3.10, the new protocol layer in the protocol stack 10, 50, 100, its initial proportion of the new protocol is the first after decreasing increasing trend. So the initial proportion is minimum of intermediate layer, while from the middle to upper or lower layer showing an increasing trend initial proportion. The protocols in the middle layer is hard to survive and has a small proportion, if the protocols are deployed in the network. The reason for this phenomenon is the protocol stack presented hourglass, the lower and higher layers tend to have more survival and the waist of the hourglass appear has less survival. 

**[x 100]**

##### 3.2 Evolution Model Based on Dynamic Selection of User Behavior

The basic parameters of the experiment described as shown in Table 4.1,

**[4.1]**

######  3.2.1 The Influence of the Protocol Utility to Adaptability 

As is shown in Figure 5, the ANP will increase if we increase the utility of protocol B, we can get the penetration changes with time of protocol B with the different alpha. The higher utility of a new protocol, the less time needed to get the whole penetration. You can see the penetration varying depending on the different alpha in Figure 4.4. When the new protocol provides for its own utility 1.8 times the current, the case of penetration of the new protocol dose not change. The reason is that the current utility is greater than the new protocol under the current network state. When the new protocol provides for its own utility is 1.8 times of the current and the simulation proceeds to the 50th,  the new protocol get 100 percent penetration, which entirely depends on the parameters of the experiments selected. When the new protocol provides for its own utility is 4 times of the current and the simulation proceeds to the 10th, the new protocol get 100 percent penetration. 

**[Figure 4.4]**

###### 3.2.2 The Influence of the External Network Utility to the Adaptability

As is shown in Figure 4.5,  the ANP will improve when the network utility increase, but the ANP will not ascend when it reaches the maximum. When the utility of the external network is too large, it will stop the increasing of the share. The acceptance of the new protocol can be ensured when alpha is 1.9. When B=0, the penetration of the new protocol is 67.4%. When the utility of the new protocol is high, state A will transit to state B to get higher utility. But some users will stay in state A if they cannot get much more utility in state B. If the utility of the external increase, more and more users will change their states to state B. When the utility of the external network is too large, it will stop the increasing of the share. If beta=0.001, the new protocol can get 100% penetration. When the beta=0.010, the penetration will not change because the A state users will not change their states to get more utility. The reason is that they can get enough utility since the user A have a large proportion in initial state. 

###### 3.2.3 The Influence of the Converter to the Adaptability

The result of simulation indicates that, the increasing utility of AB converter \[**错误**\]. As expected, the efficient AB converter can reduce the cost of state transition A to B. However, the efficient converter AB can bring utility of B to A from the perspective of individual, so there is not any incentive for A with or without converter BA. 

From the other hand, after the users changing the state A to B encouraged by BA converter, they can get the utility from other state A users and  B state users changed from state A. As is shown in the simulation results, at most cases, the ANP will improve if the utility of BA converter increase. The Figure 4.6 indicates that, when the efficiency of the BA converter is 92.5%, it will take more time for the new protocol to get to the full penetration than the efficiency of the converter is 98%. Besides, we draw the conclusion that penetration can be blocked when we improve the efficiency of the converter in some case. When BA converter efficiency from 92.5% to 94.5%,  the penetration of the new protocol will stop at 95%. The reason is when the simulation is stopped, the A state users will get more utility than cost for changing to state B. For the remaining A state users, since more and more users change to state B, they will get more utility from B state users.   Efficient BA converter will increase the utility generated by state B users, so more users will be encouraged to state B. Since the BA converter is bidirectional, efficient BA converter will increase the utility for remaining A state users and preventing them from converting to state B.The result suggests that the ANP will improve if we increase the efficiency of the converter BA and keep a low level. Furthermore, the efficiency of the BA converter must be maintained at a certain range in order to promote the new protocol fully penetrate. 

**[Figure 4.6]**

##### 3.3 Evaluation Model of the ANP Based on Network Connection Status

There 10 million nodes in the network topology, we take the cost of the connection between two nodes , so the communication efficiency is of any edge**[错误]**.

###### 3.3.1 The Influence on Communication Efficiency  of the Protocol Utility

Figure 5.2 shows the changes of the communication efficiency at different alpha,when beta= 0.001. As is shown in the picture, the communication efficiency of the network grows faster and has significantly improved with the development of the utility of the new protocols. It can be concluded that improving the efficiency of the new protocols will help to improve the communication efficiency of the network, that is, improving the efficiency of the new protocols will help to improve the ANP. 

**[Figure 5.2]**

###### 3.3.2 The Influence on Communication Efficiency of the External Network Utility

Figure 5.3 shows the changes of the communication efficiency at different betas. As is shown in the picture, the communication efficiency has improved with the improvement of the external utility of the network. But when the utility reaches to a certain value, the communication efficiency of the network significantly reduced. It can be conclude that improving the external network utility will help to improve the communication efficiency, but the efficiency will decrease when the external network utility is to high. So improving the external network utility appropriately helps to improve the ANP of new protocols. 

**[Figure 5.3]**

######  3.3.3 The Influence on Communication Efficiency of Converters

**[5.4]**

Figure 5.4 shows the changes of the communication efficiency while beta= 0.001, alpha =1 , at different conversion efficiency of the BA converter. As is shown in the picture using converter can improve the communication efficiency， but the communication efficiency of the network will decrease when the utility of BA converter grows to a certain range. While if the efficiency if the converter is high enough, it dose greatly improve the communication efficiency of the network. It can be concluded that improving the efficiency of the converters appropriately helps to improve the ANP.

#### 4. Simulation Analysis

##### 4.1 Comparative Experiments A and B

The basic experiment parameters are set as follows,

**[Table 6.3]**

The Figure 6.2 represents the average probability of IPv4 and IPv6 exist in the stack after modeling the self-evolution many times. As we can see from the result, the more the number of experiments, the probability of the final IPv6 protocol decreases in the protocol stack. It can be seen in the evolution of the protocol stack that the IPv4 protocol cannot be fully replaced by the IPv6. The reason is that, the greatest contribution of IPv6 is to provide more addresses not additional new services compared to IPv4. The upper layer service of IPv4 and IPv6 is almost no difference,  so there is competition between IPv4 and IPv6 protocol. IPv6 protocol is not widely deployed, so its quality indicators is lower than IPv4, that's why IPv4 is more competitive than IPv6. Much work need to be done if want replace the IPv4 by IPv6 protocol. On the one hand, IPv6 should provide some services that cannot provided by IPv4, which means that IP has more service nodes in the upper layer than IPv4. On the other hand, the competition should be avoided between IPv4 and IPv6, particularly in the deployment of the IPv4 is much higher than IPv6 protocol. Under these circumstances, we can make IPv6 as a "Second layer protocol" to provide services for the upper layer not a competitive protocol to IPv4. 

**[6.2]** **[6.3]**

As is shown in Figure 6.3, when the utility of external network beta=0.001, the efficiency of IPv6-IPv4 converter is 92.4% and the IPv4 and IPv6 protocol utility ratio is 2, the IPv6 can be accepted and completely replace IPv4 to achieve the full penetration, although it develops slowly.   The reason is that the government promote the deployment of IPv6 vigorously which can make up for the economic losses during the deployment. If the adaptability of the IPv6 wanted to be improved, we can do it in three ways: improve the utility of IPv6 protocol, to make it more competitive compared to IPv4; Improve the external utility of the protocol, the government can make up for the economic losses for deploying the IPv6 protocol; Improve the efficiency of IPv6-IPv4 converter, let the IPv4 users are willing to use the IPv6 protocol.

##### 4.3 The comparative Experiments of UDP and DCCP

The basic experiment parameters are set as follows,

**[Table 6.4]**

The Figure 6.4 represents the average probability of UDP and DCCP exist in the stack after modeling the self-evolution many times. As we can see from the result, the more the number of experiments, the probability of the final DCCP protocol decreases in the protocol stack.  It can be seen in the evolution of the protocol stack that the UDP protocol cannot be fully replaced by the DCCP.

**[6.5]** **[6.6]**

We build 7860000 UDP users and 2140000 DCCP users in the network which has 10000000 nodes, utilizing the UDP users share and DCCP users share from the protocol self-evolution model and according to the evolution model based on dynamic selection of user behavior. All the users reached to steady state after a period of evolution. As is shown in Figure 6.5,when the utility of external network beta=0.001, the efficiency of DCCP-UDP converter is 92.4% and the IPv4 and IPv6 protocol utility ratio is 1.8, the DCCP can be accepted and completely replace UDP to achieve the full penetration, although it develops slowly. Besides, when the DCCP share reaches around 39%, it will not change any more. If the adaptability of the DCCP wanted to be improved, we can do it in three ways: improve the utility of DCCP protocol, to make it more competitive compared to UDP; Improve the external utility of the protocol, the government can make up for the economic losses for deploying the DCCP protocol; Improve the efficiency of DCCP-UDP converter, let the UDP users are willing to use the DCCP protocol.

#### 5. Conclusion

We can draw some conclusions from the protocol self-evolution simulation. First,  the protocols at the waist of the hourglass appear to have less survival, while the lower and higher layers tend to live longer and easier. Second, if we improve the utility of the protocol, the external utility of the protocol and the efficiency of the converters appropriately can play important roles in improving the ANP. Third, the higher efficiency of the communication, the better ANP by establishing network topology based on the interact policy of the users and nodes. Forth and last, the network protocol adaptability evolution model we proposed can be applied to assess the ANP, according to the comparative experiments of IPv4, IPv6 and UDP and DCCP. The network protocol adaptability evolution model guiding significance for the development and deployment of the network protocols. 

Our model can simulate the dynamic evolution of the new protocols, furthermore, to measure the adaptability through the communication efficiency of the network topology established. In addition to this, we also proposed methods to improve the ANP. But we still have some shortcomings about the model need to be further refined and improved. In the future, we can establish a protocol dynamic evolution model and check by simulating,  then evaluate the ANP by deploying to the real networks. We can also focuse on other factors which affect on the ANP, increase the availability of the model.  

