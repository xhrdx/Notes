# Thu Oct 23 

* The compiler doesn't necesserily know how to re-order the instructions because it doesn't know if there's gonna be a cache miss or not.

* Also(average basic block is 5 instructions in SPARC) so branch prediction is important (static prediction is fine if you profile, but dynamic prediciton is better)


On SPARC we can only do one load per cycle
	
    for loop{
	    ld $1 <- 8 3 (3 cycles) # issued on first cycle
        add x <-1 # it's gonna be dependent on the load  3rd cycle
        
    	BNE 4 5 OUT  # 3rd cycle
    	ld $2 <- 6 7 # 3rd cycle 
		
        B top  # if we don't take the branch then this is issued on 4th
	}


We would like to do the following:


    for loop{
	    ld $1 <- 8 3 (3 cycles) # issued on first cycle
        
        
        ld $2 <- 6 7 # 2nd cycle (since it's not dependent on anyting else) 
        			 # but it might cause an exception 
        
        add x <-1 # it's gonna be dependent on the load  3rd cycle
        
    	BNE 4 5 OUT  # 3rd cycle
    	
		
        B top  # if we don't take the branch then this is issued on 4th
	}