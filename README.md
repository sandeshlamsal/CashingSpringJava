# CashingSpringJava
At its core, the abstraction applies caching to Java methods, reducing thus the number of executions based on 
the information available in the cache. That is, each time a targeted method is invoked, the abstraction will 
apply a caching behavior checking whether the method has been already executed for the given arguments. If it has, 
then the cached result is returned without having to execute the actual method; if it has not, then method is executed, 
the result cached and returned to the user so that, the next time the method is invoked, the cached result is returned. 
This way, expensive methods (whether CPU or IO bound) can be executed only once for a given set of parameters and the result
reused without having to actually execute the method again. 
The caching logic is applied transparently without any interference to the invoker.
