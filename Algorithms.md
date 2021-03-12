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


2. QUICK FIND (eager approach)
* Data structure:
    * Integer array id[] of length N.
    * Interpretation:  p and q are connected iff they have the same id.
    * Union: To merge components containing p and q, change all entries whose id equals id[p] to id[q].
* Java Implementation:
```java
public class QuickFindUF{
    private int[] id;
    //set id of each object to itself
    // (N array accesses)
    public QuickFindUF(int N)   {      
        id = new int[N];      
        for (int i = 0; i < N; i++)         
            id[i] = i;   
    }   
    //check whether p and qare in the same component
    //(2 Array accesses)
    public boolean connected(int p, int q)   {  
        return id[p] == id[q];  
    }   
    //change all entries with id[p] to id[q]
    public void union(int p, int q)   {     
        int pid = id[p];      
        int qid = id[q];      
        for (int i = 0; i < id.length; i++)       
            if (id[i] == pid) id[i] = qid;  
    }
}
``` 

3. QUICK UNION (lazy approach)
* Data structure:
    * Integer array id[] of length N.
    * Interpretation: id[i] is parent of i.
    * Root of i is id[id[id[...id[i]...]]].

* Find:

  Check if p and q have the same root.
* Union:
  
    To merge components containing p and q,set the id of p's root to the id of q's root.

* Java implementation
```java
class QuickUnionUF {
    private int[] id;

    public QuickUnionUF(int N) {
        id = new int[N];
        //set id of each object to itself(N array accesses)
        for (int i = 0; i < N; i++) {
            id[i] = i;
        }
        private int root ( int i){
            //chase parent pointers until reach root(depth of i array accesses) 
            while (i != id[i]) i = id[i];
            return i;
        }
        public boolean connected ( int p, int q){
            check if p and q have same root (depth of p and q array accesses)
            return root(p) == root(q);
        }
        public void union ( int p, int q){
            change root of p to point to root of q (depth of p and q array accesses)
            int i = root(p);
            int j = root(q);
            id[i] = j;
        }
    }
}    
```

* Quick-find defect.
    * Union too expensive (N array accesses).
    * Trees are flat, but too expensive to keep them flat.
* Quick-union defect.
    * Trees can get tall.
    * Find too expensive (could be N array accesses).
    
*  QUICK UNION IMPROVEMENTS
1. WEIGHTING
* Weighted quick-union.
     * Modify quick-union to avoid tall trees.
     * Keep track of size of each tree (number of objects).
     * Balance by linking root of smaller tree to root of larger tree.

* Data structure.  
  * Same as quick-union, but maintain extra array sz[i] to count number of objects in the tree rooted at i.
* Find.  
  * Identical to quick-union.
                    
        return root(p) == root(q);
* Union.  
    * Modify quick-union to:
        * Link root of smaller tree to root of larger tree.
        * Update the sz[] array. 
          
            
        int i = root(p); 
        int j = root(q); 
        if (i == j) return; 
        if  (sz[i] < sz[j]){ 
            id[i] = j; 
            sz[j] += sz[i]; 
        }  else { 
            id[j] = i; 
            sz[i] += sz[j]; 
        }  

* Running time.
    * Find:  
        takes time proportional to depth of p and q.
    * Union:
        takes constant time, given roots.
      
* Proposition.
  * Depth of any node x is at most lg N. (base 2 log)

When does depth of x increase?
* Increases by 1 when tree T1 containing x is merged into another tree T2.
* The size of the tree containing x at least doubles since |T 2 | ≥|T 1 |.
* Size of tree containing x can double at most lg N times. Why?

2. PATH COMPRESSION

* Quick union with path compression.   
  Just after computing the root of p,set the id of each examined node to point to that root.

* Java implementation
  
  * Two-pass implementation: 
  
    add second loop to root() to set the id[]of each examined node to the root.
  *  Simpler one-pass variant:  
       Make every other node in path point to its grandparent (thereby halving path length).
 
    
    private int root(int i){
        while(i!=id[i]){
            id[i]=id[id[i]];
            i=id[i];
        }
        return i;
    }   

    

