ALGORITHMS
* Algorithm: method for solving a problem.
* Data structure: method to store information.

Why study algorithms?
* Their impact is broad and far-reaching.
* Old roots, new opportunities.  
* To solve problems that could not otherwise be addressed.
    * Ex. Network connectivity.
* For intellectual stimulation.
* To become a proficient programmer.
* They may unlock the secrets of life and of the universe.
* For fun and profit.

Steps to developing a usable algorithm.
* Model the problem.
* Find an algorithm to solve it.
* Fast enough? Fits in memory?
* If not, figure out why.
* Find a way to address the problem.
* Iterate until satisfied.

UNION - FIND
1. DYNAMIC CONNECTIVITY
    * Union command:  
      - connect two objects.
    * Find/connected query:  
      - is there a path connecting the two objects?
    * 'Is connected to' relation:
      * Reflective:
        
        p is connected to p.
      * Symmetric:
        
        if p is connected to q, then q is connected to p.
      * Transitive: 
        
        if p is connected to q and q is connected to r, then p is connected to r.

Implementing the operations
  * Find query.  
    
    Check if two objects are in the same component.
  * Union command.  
    
    Replace components containing two objects with their union.

Union-Find data-type
      
      public class UF
      * UF(int N) => initialize union-find data structure with  N objects (0 to N – 1)
      * void union(int p, int q) => add connection between p and q
      * boolean connected(int p, int q) => are p and q in the same component?
      * int find(int p) => component identifier for p (0 to N – 1)
      * int count() => number of components


2. QUICK FIND

  