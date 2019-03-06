# utl-fun-calculating-the-double-sum-matrix-operation
Fun calculating the double sum matrix operation 
    Fun calculating the double sum matrix operation                                        
                                                                                           
           2           2                                                                   
       +-------> +------->                                                                 
        \         \                                                                        
         \         \                                                                       
          \         \                                                                      
          /         /     i * j                                                            
         /         /                                                                       
        /         /                                                                        
        +------>  +------>                                                                 
          i= 1       j=1                                                                   
                                                                                           
                                                                                           
       1*1 + 1*2 + 2*1 + 2*2 = 1+2+2+4 = 9                                                 
                                                                                           
       1 * (1+2) + 2*(1+2)   ** due to the associative rule                                
                                                                                           
                                                                                           
       Three Solutions                                                                     
                                                                                           
               1. R                                                                        
               2. datastep                                                                 
               3. sql                                                                      
                                                                                           
                                                                                           
    https://stackoverflow.com/questions/55011693/double-variable-summation                 
                                                                                           
    https://stackoverflow.com/users/8245406/rui-barradas                                   
                                                                                           
    *_                   _                                                                 
    (_)_ __  _ __  _   _| |_                                                               
    | | '_ \| '_ \| | | | __|                                                              
    | | | | | |_) | |_| | |_                                                               
    |_|_| |_| .__/ \__,_|\__|                                                              
            |_|                                                                            
    ;                                                                                      
                                                                                           
    data i;                                                                                
     do i=1 to 4;                                                                          
        output;                                                                            
     end;                                                                                  
    run;quit;                                                                              
                                                                                           
    /*                                                                                     
    WORK.I total obs=4                                                                     
                                                                                           
      I                                                                                    
                                                                                           
      1                                                                                    
      2                                                                                    
      3                                                                                    
      4                                                                                    
    */                                                                                     
                                                                                           
    data j;                                                                                
     do j=1 to 3;                                                                          
        output;                                                                            
     end;                                                                                  
    run;quit;                                                                              
                                                                                           
    WORK.J total obs=3                                                                     
                                                                                           
       J                                                                                   
                                                                                           
       1                                                                                   
       2                                                                                   
       3                                                                                   
                                                                                           
    *            _               _                                                         
      ___  _   _| |_ _ __  _   _| |_                                                       
     / _ \| | | | __| '_ \| | | | __|                                                      
    | (_) | |_| | |_| |_) | |_| | |_                                                       
     \___/ \__,_|\__| .__/ \__,_|\__|                                                      
                    |_|                                                                    
    ;                                                                                      
                                                                                           
    RULE                                                                                   
                                                                                           
     1*(1+2+3) + 2*(1+2+3) + 3*(1+2+3) + 4*(1+2+3) =6+12+18+24 = 60                        
                                                                                           
                                                                                           
     TOT=60                                                                                
                                                                                           
    *          _       _   _                                                               
     ___  ___ | |_   _| |_(_) ___  _ __  ___                                               
    / __|/ _ \| | | | | __| |/ _ \| '_ \/ __|                                              
    \__ \ (_) | | |_| | |_| | (_) | | | \__ \                                              
    |___/\___/|_|\__,_|\__|_|\___/|_| |_|___/                                              
                                                                                           
    ;                                                                                      
                                                                                           
    =========                                                                              
    1. R                                                                                   
    =========                                                                              
                                                                                           
    %utl_submit_r64('                                                                      
    i <- 1:4;                                                                              
    j <- 1:3;                                                                              
    sum(outer(i, j));                                                                      
    ');                                                                                    
                                                                                           
    > i <- 1:4;j <- 1:3;sum(outer(i, j));                                                  
    [1] 60                                                                                 
    >                                                                                      
                                                                                           
    ===========                                                                            
    2. DATASTEP                                                                            
    ===========                                                                            
                                                                                           
    data _null_;                                                                           
      retain tot 0;                                                                        
      array ii[4] (1,2,3,4);                                                               
      array jj[3] (1,2,3);                                                                 
      do i=1 to 4;                                                                         
         tot=tot+i*sum(of jj[*]);                                                          
      end;                                                                                 
      put tot=;                                                                            
    run;quit;                                                                              
                                                                                           
    ===========                                                                            
    3. SQL                                                                                 
    ===========                                                                            
                                                                                           
    proc sql;                                                                              
      select                                                                               
          SUM(l.i * r.subtot) as tot                                                       
      from                                                                                 
         i as l ,                                                                          
         (select                                                                           
            sum(j) as subtot                                                               
          from                                                                             
            j                                                                              
         ) as r                                                                            
    ;quit;                                                                                 
                                                                                           
                                                                                           
