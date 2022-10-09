
### Raft consensus algorithm:

To begin with, Raft states that each node in a replicated state machine(server cluster) can stay in any of the three states, namely, leader, candidate, follower. The image below will provide the necessary visual aid. 
 
Under normal conditions, a node can stay in any one of the above three states. Only a leader can interact with the client; any request to the follower node is redirected to the leader node. A candidate can ask for votes to become the leader. A follower only responds to candidate(s) or the leader. 

To maintain these server status(es), the Raft algorithm divides time into small terms of arbitrary length. Each term is identified by a monotonically increasing number, called term number. 
Term number 
This term number is maintained by every node and is passed while communications between nodes. Every term starts with an election to determine the new leader. The candidates ask for votes from other server nodes(followers) to gather majority. If the majority is gathered, the candidate becomes the leader for the current term. If no majority is established, the situation is called a split vote and the term ends with no leader. Hence, a term can have at most one leader. 
Purpose of maintaining term number 

Following tasks are executed by observing the term number of each node:<br/> 
 

    1.Servers update their term number if their term number is less than the term numbers of other servers in the cluster. This means that when a new term starts, the term numbers are tallied with the leader or the candidate and are updated to match with the latest one(Leader’s)
    2.Candidate or Leader demotes to the Follower state if their term number is out of date(less than others). If at any point of time, any other server has a higher term number, it can become the Leader immediately.
    3.As we said earlier that the term number of the servers are also communicated, if a request is achieved with a stale term number, the said request is rejected. This basically means that a server node will not accept requests from server with lower term number.
    
    
    
    
--------

### Leader Election:

In order to maintain authority as a Leader of the cluster, the Leader node sends heartbeat to express dominion to other Follower nodes. A leader election takes place when a Follower node times out while waiting for a heartbeat from the Leader node. At this point of time, the timed out node changes it state to Candidate state, votes for itself and issues RequestVotes RPC to establish majority and attempt to become the Leader. The election can go the following three ways: 
 

    1.The Candidate node becomes the Leader by receiving the majority of votes from the cluster nodes. At this point of time, it updates its status to Leader and starts sending heartbeats to notify other servers of the new Leader.
    2.The Candidate node fails to receive the majority of votes in the election and hence the term ends with no Leader. The Candidate node returns to the Follower state.
    3.If the term number of the Candidate node requesting the votes is less than other Candidate nodes in the cluster, the AppendEntries RPC is rejected and other nodes retain their Candidate status. If the term number is greater, the Candidate node is elected as the new Leader.
