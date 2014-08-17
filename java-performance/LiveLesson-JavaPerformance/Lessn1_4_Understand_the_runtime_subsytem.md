1.4 Understand the runtime system.

**Commands Used **

	java -version

	java -XX:+PrintFlagsFinal -version

	java -XX:+PrintFlagsFinal -version | more


### Types of Flag
1. product flag
2. platform dependent product flag
3. C1 Product
4. manageable 
    
    java -XX:+PrintFlagsFinal -XX:+PrintGCDetails -version | more

Overridden properties file are shown with := sign

     bool PrintGCDetails                           := true            {manageable}


