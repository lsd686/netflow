最简单 的 处理是  只处理 router，算法大致如下：
```
FOR lines IN file:
	GET router & next_hop FROM line;
	IF router EXISTS IN router_list:
		GET index_of_the_router_in_list:
		IF next_hop EXISTS IN router's neighbor_list:
			continue;
		ELSE
			ADD next_hop IN router's neighbor_list;
	ELSE
    	ADD router IN router_list;
        ADD next_hop IN router's neighbor_list;
END FOR
```
