# utl-fun-calculating-the-double-sum-matrix-operation
    Fun calculating the double sum matrix operation                                                                             
                                                                                                                                
    Two Solution                                                                                                                
                                                                                                                                
        1. Double sum of product i*j                                                                                            
        2. Double sum of product times a function of i i*sqrt(j)                                                                
                                                                                                                                
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
                                                                                                                                
       1 * (1+2) + 2*(1+2)                                                                                                      
       (1+2)*(1+2) = 3*3 = 9  ** due to the associative rule                                                                    
                                                                                                                                
           2           2                                                                                                        
       +-------> +------->                                                                                                      
        \         \                                                                                                             
         \         \                                                                                                            
          \         \                                                                                                           
          /         /     i * sqrt(j)                                                                                           
         /         /                                                                                                            
        /         /                                                                                                             
        +------>  +------>                                                                                                      
          i= 1       j=1                                                                                                        
                                                                                                                                
                                                                                                                                
       1*sqrt(1) + 1*sqrt(2) + 2*sqrt(1) + 2*sqrt(2) =  1*(sqrt(1)+sqrt(2)) + 2*(sqrt(1)+sqrt(2))                               
       1*(sqrt(1)+sqrt(2)) + 2*(sqrt(1)+sqrt(2)) - (1+2)*(sqrt(1)+sqrt(2))                                                      
       3*2.4142135624 = 7.2426406872                                                                                            
                                                                                                                                
      github                                                                                                                    
      https://tinyurl.com/yy8xpgd2                                                                                              
      https://github.com/rogerjdeangelis/utl-populate-or-operate-on-each-element-of-datastep-temporary-or-permanent-array       
                                                                                                                                
                                                                                                                                
       Three Solutions                                                                                                          
                                                                                                                                
               1. R                                                                                                             
               2. datastep                                                                                                      
               3. sql                                                                                                           
                                                                                                                                
                                                                                                                                
    github                                                                                                                      
    https://tinyurl.com/y275jcjh                                                                                                
    https://github.com/rogerjdeangelis/utl-fun-calculating-the-double-sum-matrix-operation                                      
                                                                                                                                
    macros ( macro on the end)                                                                                                  
    https://tinyurl.com/y9nfugth                                                                                                
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories                                  
                                                                                                                                
    https://stackoverflow.com/questions/55011693/double-variable-summation                                                      
                                                                                                                                
    Rui Barradas                                                                                                                
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
     (1+2+3+4)*(1+2+3) = 60                                                                                                     
                                                                                                                                
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
                                                                                                                                
    %utl_submit_r64('                                                                                                           
    i <- 1:2;                                                                                                                   
    j <- 1:2;                                                                                                                   
    sum(outer(i, sqrt(j)));                                                                                                     
    ');                                                                                                                         
    > i <- 1:2;j <- 1:2;sum(outer(i, sqrt(j)));                                                                                 
    [1] 7.242641                                                                                                                
                                                                                                                                
    ===========                                                                                                                 
    2. DATASTEP                                                                                                                 
    ===========                                                                                                                 
                                                                                                                                
    data _null_;                                                                                                                
      array ii[4] (1,2,3,4);                                                                                                    
      array jj[3] (1,2,3);                                                                                                      
      tot=sum(of ii[*])*sum(of jj[*]);                                                                                          
      put tot=;                                                                                                                 
    run;quit;                                                                                                                   
                                                                                                                                
    data _null_;                                                                                                                
      array ii[2] (1,2);                                                                                                        
      array jj[2] (1,2);                                                                                                        
      %utl_aryFil(jj,2,fun=%str(sqrt));                                                                                         
      tot=sum(of ii[*])*sum(of jj[*]);                                                                                          
      put tot=;                                                                                                                 
    run;quit;                                                                                                                   
                                                                                                                                
    ===========                                                                                                                 
    3. SQL                                                                                                                      
    ===========                                                                                                                 
                                                                                                                                
                                                                                                                                
    data i;                                                                                                                     
     do i=1 to 4;                                                                                                               
        output;                                                                                                                 
     end;                                                                                                                       
    run;quit;                                                                                                                   
                                                                                                                                
    data j;                                                                                                                     
     do j=1 to 3;                                                                                                               
        output;                                                                                                                 
     end;                                                                                                                       
    run;quit;                                                                                                                   
                                                                                                                                
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
                                                                                                                                
    /*                                                                                                                          
         tot                                                                                                                    
    --------                                                                                                                    
          60                                                                                                                    
    */                                                                                                                          
                                                                                                                                
    data i;                                                                                                                     
     do i=1 to 2;                                                                                                               
        output;                                                                                                                 
     end;                                                                                                                       
    run;quit;                                                                                                                   
                                                                                                                                
    data j;                                                                                                                     
     do j=1 to 2;                                                                                                               
        output;                                                                                                                 
     end;                                                                                                                       
    run;quit;                                                                                                                   
                                                                                                                                
    proc sql;                                                                                                                   
      select                                                                                                                    
          SUM(l.i * r.subtot) as tot                                                                                            
      from                                                                                                                      
         i as l ,                                                                                                               
         (select                                                                                                                
            sum(sqrt(j)) as subtot                                                                                              
          from                                                                                                                  
            j                                                                                                                   
         ) as r                                                                                                                 
    ;quit;                                                                                                                      
                                                                                                                                
         tot                                                                                                                    
    --------                                                                                                                    
    7.242641                                                                                                                    
                                                                                                                                
    *                                                                                                                           
     _ __ ___   __ _  ___ _ __ ___                                                                                              
    | '_ ` _ \ / _` |/ __| '__/ _ \                                                                                             
    | | | | | | (_| | (__| | | (_) |                                                                                            
    |_| |_| |_|\__,_|\___|_|  \___/                                                                                             
                                                                                                                                
    ;                                                                                                                           
                                                                                                                                
     %macro utl_aryFil(ary,len,fun=%str(**2))/                                                                                  
       des="sum an array after appling an arbitrary function to each element";                                                  
                                                                                                                                
      %let rc=%sysfunc(dosubl('                                                                                                 
         data chk;                                                                                                              
            length lst $32756;                                                                                                  
            do idx=1 to symgetn("len");                                                                                         
              ara=cats(symget("ary"),"[",idx,"]");                                                                              
              if notalpha(substr(symget("fun"),1,1)) then do;                                                                   
                lst=cats(lst,ara,'=',ara,symget("fun"),";");                                                                    
              end;                                                                                                              
              else do;                                                                                                          
                lst=cats(lst,ara,'=',symget("fun"),"(",ara,");");                                                               
              end;                                                                                                              
            end;                                                                                                                
            call symputx("lst",lst,"G");                                                                                        
         run;quit;                                                                                                              
         '));                                                                                                                   
      &lst                                                                                                                      
                                                                                                                                
    %mend utl_aryFil;                                                                                                           
                                                                                                                                
    data _null_;                                                                                                                
      array ii[2] (1,2);                                                                                                        
      array jj[2] (1,2);                                                                                                        
      %utl_aryFil(jj,2,fun=%str(sqrt));                                                                                         
      tot=sum(of ii[*])*sum(of jj[*]);                                                                                          
      put tot=;                                                                                                                 
    run;quit;                                                                                                                   
                                                                                                                                
    TOT=7.2426406871                                                                                                            
                                                                                                                                
                                                                                                                                
    * generated code;                                                                                                           
                                                                                                                                
    134  data _null_;                                                                                                           
    135  array ii[2] (1,2);                                                                                                     
    136  array jj[2] (1,2);                                                                                                     
                                                                                                                                
    137  jj[1]=sqrt(jj[1]);                                                                                                     
    138  jj[2]=sqrt(jj[2]);                                                                                                     
                                                                                                                                
    139  ;                                                                                                                      
    140  tot=sum(of ii[*])*sum(of jj[*]);                                                                                       
                                                                                                                                
    141  put tot=;                                                                                                              
    142  run;                                                                                                                   
                                                                                                                                
