BooktifuL requests failure
On all queries made on the platform routes, the BooktifuL platform was reportedly returning 500 Errors last week, and all of the services were unavailable. Ninety percent of users were impacted. The failure of our master server web-01 was the primary factor.


Timeline
On Saturday, February 26, around 1200 (East African Time), our site reliability engineer, Mr. Elie, noticed a performance issue with the master server. For additional system examination, our on-call experts unplugged the master server web-01 and routed all requests to client server web-02. They resolved the issue by Sunday, February 27, 2200 hours (East Africa Time).

Cause and effect and remedy
Two Ubuntu cloud servers provide service to the BooktifuL platform. The principal server web-02, the client server used in the previous test, had been briefly disconnected for testing and had not been reconnected to the load balancer, web-01 was connected to serve all requests but eventually ceased working owing to memory issues brought on by the sheer volume of requests.

The problem was resolved when the load balancer was restarted after the master server had been momentarily unplugged for memory cleanup, and the round-robin algorithm was set up so that both the master and client servers could handle an equal number of requests.

Future preventative measures against this issue
Select the ideal load-balancing method for your programs.
Continually monitor your servers to make sure they are functioning properly.
Have additional backup servers to avoid your program from falling entirely offline in the event of an issue

