# Algorithm-From-abdl-Albrary
Summary for Our algorithm &amp; Data Structure course 

----

### Most Of codes in this summary will be with Python language and psuedo code  
## Videos on Youtube 

- From [here](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

## Summary of vidoe 
|Vidoe Summary | Video Name | Video Summary | Video Name |
|------|----------|------------|----------|
| <a href="#1">Vidoe 1</a> | Introduction To Algorith| <a href="#2">Vidoe 2</a>| Priori Analysis and Posteriori|
| <a href="#3">Vidoe 3</a>| Characteristics of Algorith | <a href="#4">Vidoe 4</a> |How Write and Analyze Algorithm|

- 
- <a href="#4">Vidoe 4</a>
- <a href="#5">Vidoe 5</a>
- <a href="#6">Vidoe 6</a>
- <a href="#7">Vidoe 7</a>
- <a href="#8">Vidoe 8</a>
- <a href="#9">Vidoe 9</a>
- <a href="#10">Vidoe 10</a>
- <a href="#11">Vidoe 11</a>
- <a href="#12">Vidoe 12</a>
- <a href="#13">Vidoe 13</a>
- <a href="#14">Vidoe 14</a>
- <a href="#15">Vidoe 15</a>
- <a href="#16">Vidoe 16</a>
- <a href="#17">Vidoe 17</a>
- <a href="#18">Vidoe 18</a>
- <a href="#19">Vidoe 19</a>
- <a href="#20">Vidoe 20</a>
- <a href="#21">Vidoe 21</a>
- <a href="#22">Vidoe 22</a>
- <a href="#23">Vidoe 23</a>
- <a href="#24">Vidoe 24</a>
- <a href="#25">Vidoe 25</a>
- <a href="#26">Vidoe 26</a>
- <a href="#27">Vidoe 27</a>
- <a href="#28">Vidoe 28</a>
- <a href="#29">Vidoe 29</a>
- <a href="#30">Vidoe 30</a>
- <a href="#31">Vidoe 31</a>
- <a href="#32">Vidoe 32</a>
- <a href="#33">Vidoe 33</a>
- <a href="#34">Vidoe 34</a>
- <a href="#35">Vidoe 35</a>
- <a href="#36">Vidoe 36</a>
- <a href="#37">Vidoe 37</a>

----
## <p id=1> introduction To Aglorithm </p>

- Summary 
  - `Algorithm` => is a step by step precedure for solving computational problem.
  - `software cycle ` most important of it is
    - . design phase & implementation phase 


|Agorithm | Program |
|------|-----------|
| design time| implementation time|
|Domain knowledge | programmer|
| use any programming lagnuage | use speific language| 
|not depend on Hard ware & OS | depend on Hard ware & OS|
|analze the algorithm | testing algorithm|
 
----------
## <p id=2>Priori Analysis and Posteriori Testing</p>

- `Priori Analysis` => Means we wil do the analysis to find time & space.
- `Posteriori Testing` => Done on the program. We run and check it to know number of millsecond token and memeory consuming.
----

## <p id=3>Characteristics of Algorithm.</p>

- `input` => take `0` or more 
- `output` => at least 1 O/P
- Definiteness =>  use known value not like `sqrt(-1)` and `0/1` and so on.
- `finiteness` => all algorithm must stop at some point.
- `Effectiveness` => don't use unnecessary thing. 

----
## <p id=4>How to Write an Agorithm</p>

- in writing psuedo code don't have to make `variable declaration`
```c
    Aglorithm swap(a,b)
    begin
        temp <- a;
        a <- b;
        b <- temp;
    end
    // Time => O(1)
    // space =>  O(1)

```
- How to Analyse an Algorithm 
  - Find :
  
    1.Time

    2.space

    3.Network consumption 

    4.Power consumption

    5.CPU Registers consumption
  
----
## <p id=5>Frequency Count Methods</p>
```c
    // sum all element in one dimension array.
    Algorithm sum(A,b) 
        s=0; //1
//repeated for(1 ,n+1 ,n)
        for(i=0 ;i<n ;i++) //n+1
            s+=A[i]     //n
        return s;   //1
    /*
        Analyse algorithm 
            Time
                T(n)= 2n+3 
                Then Time = O(n)
            Space
                A = n
                n = 1
                s = 1
                i=1
                S(n) = n+3
                Then space is =>  O(n)
    */
```
```c
    // Sum Two Dimension Array 
    Algorithm Add(A,B,n)
     for(i=0;i<n;i++) // n +1
        for (j=0;j<n;j++) // n (n+1)
            c[i,j]=A[i,j]+B[i,j] // n*n
    /*
    Analyse Algorithm
    Time
        f(n)=2n^2 +2n+1
        then Time is O(n^2)
    Space
        A =>  n^2
        B => n^2
        c => n^2
        n =>1
        i =>1
        j =>1
        space is (3n^2 +3)
            O(n^2)
    */
```
```c
// Martix Multiplication.
    Algorithm multiply(A,B,n)
        for(i=0;i<n;i++) //n+1
            for(j=0;j<n;j++) //n*(n+1)
                c[i,j]=0; //n*(n)
                for(k=0;k<n;k++)//n*n*(n+1)
                    c[i,j]=c[i,j]+A[i,k]*B[k,j];//n*n*n
        /*
            Analyse Algorithm
                f(n) => 2n^3+3n^2+2n+1
                Time => O(n^3)
            Analyse Space
                A => n^2
                B => n^2
                C => n^2
                n => 1
                i => 1
                j => 1
                k => 1
            S(n) => 3n^2 +4
                O(n^2)
        */
```
----
## <p id=6>Time Complexity 1</p>

```c
    for(i=0;i<n;i++)
        // code here
    // Time is O(n)

    for(i=n;i>n;i--)
        // code here
    // Time is O(n)

    for(i=1;i<n;i=i+20)
        // code here
    // Time is O(n/20) equal O(n)

    for(i=0;i<n;i++)
        for(j=0;j<n;j++)
            // code here
    // Time is O(n^2)
```

```c
    for(i=0;i<n;i++)
        for(j=0;j<i;j++)
            // code here
        /*
            i   |   j
            --------
            0   | 0
            1   | 1
            2   | 2
            3   | 3
            n   | n
        */
    // Then Time is  =>  O(n^2)
            
```
```c
    p=0;
    for(i=1;p<=n;i++)
        p+=i
        /*
            Assume p>n
            p=k(k+1)/2
            k(k+1)/2>n
            k^2>n
            k>sqrt(n)
        */  
    // Finally Time => O(sqrt(n))
```
----
## <p id=7>Time Complexity 2</p>

```c
    for(i=1;i<n;i=i*2)
        // code here
    /*
    analyze Algorithm
        assume i>=n 
            i=2^k
            2^k==n
            k=log2(n)
        Then Time Complexity => O(log2(n)) => we take ceil value if it's value is a float value.
    */
```

```c
    for(i=n;i>=1;i=i/2)
        // code here
    /*
    Analyze Algorithm
        i<1
        n/2^k<1
        n/2^k==1
        n=2^k
        k=log2(n)
    Then Time Complexity => O(log2(n))
    */
```
```c
    for(i=0;i*i<n;i++)
        // code here
    /*
    Analyze Algorithm
        i*i<n
        i^2<n
        i=sqrt(n)
    */
```

```c
    for(i=0;i<n;i++)
        // code here
    for(j=0;j<n;j++)
        // code here
    /*
    Analyze Algorithm
        i<n
        time one O(n)
        j<n
        Time two O(n)
        then all time is 2n
        means O(n)
        Note we ignore all cofficient of high effective value and ignore all value 
    */

```

```c
    p=0
    for(i=1;i<n;i=i*2)
        p++  //p => log2(n)
    for(j=1;j<p;j=j*2)
        code here ///log2(log2(n))
    // Then Time complexity is log2(log2(n))
```

```c
    for(i=0;i<n;i++) //n
        for(j=1;j<n;j*=2)//nlog2(n)
            // code here => nlog2(n)

        // Time => n+2nlog2(n)
    // Time complexity is nlog2(n)
```
```c
    for(i=0;i<n;i++) //O(n)
    for(i=0;i<n;i+=20) //O(n)
    for(i=n;i>1;i--) //O(n)
    for(i=0;i<n;i*=2) //O(log2(n))
    for(i=0;i<n;i*=3) //O(log3(n))
    for(i=n;i>1;i/=2) //O(log2(n))
```
----
## <p id=8>Time Complexity of While and if </p>
```c
    i=0 //1
    while (i<n) //n+1
        // code here     n
        i++ //n
    /*
        Analyze algorithm 
            3n+2
    */
    // Then Time complexity is O(n)
// ----------------------
    // note it the same as for loop
        // 1  n+1  n
    for (i=0;i<n;i++)
        code here //n
    // s(n) => 3n+2
``` 
```c
    a=1; //1
    while (a<b) //log2(b)+1
        // code here => log2(b)
        a=a*2 //log2(b)
    // S(n) => 3log2(b)+2
    // Then Time complexity is O(log2(b))
```
```c
    i=1;
    k=1;
    while (k<n)
        // code here 
        k=k+i;
        i+=1;
    /*
        analyze algorithm 
        i   k
        1   1
        2   1+1
        3   2+2
        4   2+2+3
        and so on.
        1+2+3+4+5+....m => m(m+1)/2
        m^2>=n
        then m=sqrt(n)
        then time complexity is O(sqrt(n))
    */
```
```c
    while(m!=n)
        if (m>n)
            m-=n
        else
            n-=m 
    // Time complexity is  => O(n)
```
----
## <p id=9>Types of Time function</p>

```c
    // f(n)=40000 then time complexity is constant => o(1)

    /*
        O(1) => constant
        O(log(n)) => logrithemic
        O(n) => linear 
        O(n^2) => quadratic
        O(n^3) => Cubic  
        O(2^n) => Exponential.
    */
```
----
## <p id=10>Compare Class of Function</p>

```c
    /*
        1<log(n)<n<nlog(n)<n^2<n^3<......2^n ....n^n
    */
```
----

## <p id=11>asymptotic Notaion 1</p>

```c
    /*
    O => big-Oh => upper bound of a fucntion
    Ω => Omega =>  Lower bound.
    Θ => Theta  => Average bound. Useful one of three.
    */
```
```c
    /*
    Big o notation
    - f(n)<=c*g(n) then big o notation is O(n)
        f(n)=2n+3
            2n+3<=10n => c*g(n) => means big o is O(n)
            2n+3<=5n^3  => Means big O is O(n^2) and so on.

            [1<log(n)<n]    n       [n <nlog(n)<n^2<n^3<......2^n ....n^n]
            Lower bound     & Average bound & Upper bound.
    */
```
```c
    /*
    Ω omega 
    - f(n)>=c*g(n) then Ω is Ω(n)
        f(n)=2n+3   
        2n+3 >=1*n then Ω is Ω(n) or Ω(logn) or O(1)
    */
```
```c
    /*
    Θ theta Notation
    c1*g(n) <=f(n)<= c2*g(n) then theta is Θ(n)
        
        f(n)=2n+3
        1*n<=2n+3<=5*n
        then theta is Θ(n) we can't use n^2 or log2(n)
    */
```
- `people` think that big O was used for `upper bound` as wrost case and Omega for `lower bound` as best case no. You Can use any notaion for best case any notation for wrost case.
-----
## <p id=12> asymptotic Notaion 2</p>

```c
/*
    f(n)=2n^2+3n+4
    - big O    2n^2+3n+4 <= 2n^2+3n^2+4n^2 then => 9n^2 then O(n^2)
    - Omega 2n^2+3n+4 >=1*n^2 ->then Omega(n^2)
    - Theta 1*n^2 <=2n^2+3n+4M<=9n^2  ->then theta (n^2)
    */
```
```c
    /*
        f(n)=n^2log(n)+n
            O(n^2log(n)) & Omega(n^2log(n)) & theta(n^2log(n))
    */
```
```c
    /*
        f(n)=n! => n(n-1)(n-2) ....3*2*1
            1*2*3.....(n-2)(n-1)n

        1<n!<n^n
        O(n^n)
        omega(1)
        theta() => we can't found theta bound
    */
```
```c
    /*
    f(n)=log(n)!
    
        1<log(n)!>log(n^n)
        1<log(n)!<nlogn
    then
        O(nlogn)
        omega(1)
    */
```
---
## <p id=13>properity of Asymptotic Notation</p>

```c
/*
    if f(n) is O(g(n)) => then c*f(n) is O(g(n))
        e.g f(n)=2n^2+4 => O(n^2)
            f(n)=8n^2+32 => O(n^2)
    reflexive
        if f(n) is given then f(n) is O(f(n))
            f(n)=n^2
                O(n^2)
    transitive 
        if   f(n) is O(g(n)) 
        and  g(n) is O(h(n)) 
        then f(n)=O(h(n))

        e.g => f(n)=n 
            and g(n)=n^2 
            and  h(n)=n^3

             n is  O(n) 
        and  n^2 is O(n^2) 
        then n is O(n^3)
        means if one small notation is upper bound for f(n).
        then the bigger  of it is also upper bound for same f(n)
*/  
```
```c
    /*
        symmetric
            if f(n) is O(g(n)) then g(n) is O(f(n))
        e.g
            f(n)=n^2    g(n)=n^2
            f(n)=O(n^2)
            g(n)=O(n^2)
    */
```
```c
     /*
     if f(n)=O(g(n))
     and f(n)=omega(g(n))
     then theta (n)=theta(g(n)) 
     */
``` 

----
## <p id=14>Comparison of Function</p>

```c
    /*
    To compare which function is small and which is bigger
    e.g n^2 and n^3 use substitute or use log() for each of them.
    */
    /*
    log(ab)=log(a)+log(b)
    log(a/b)=log(a)-log(b)
    log(a^b)=blog(a)
    a^(logc(b)) => b^(logc(a))
    */
```
```c
    /*
    f(n)=(n^2)log(n)          g(n)=n(log(n))^10
    apply log
    log[n^2log(n)]          log[nlog(n)^10]
    log(n^2) +log[log(n)]   log(n) +log[log(n)^10]
    
    2log(n)+loglog(n)       log(n)+10loglog(n)
    Then check the domination bound in the function here is log(n)
    then frist one is bigger.
    */
```
```c
    /*
        f(n)=3n^(sqrt(n))       g(n)=2^(sqrt(n)*log(n))
        
        3n^sqrt(n)              2^[log2(n)*sqrt(n)] 
        3n^sqrt(n)              n*sqrt(n)
        then first is bigger.
    */
```
----
## <p id=15>Comparison of Function 2</p>

```c
    /*
    f(n)=n^log(n)        g(n)=2^sqrt(n)
    apply log

    log[n^log(n)]        log[2^sqrt(n)]
    log(n)*log(n)       sqrt(n)log(2)
    log(n)^2            sqrt(n)log(2) => log2(2)=> 1
    apply log again

    2log(log(n))        log(n^1/2)
    2loglog(n)             1/2log(n) 
    Then second is bigger.
    */
```
```c
    /*
    f(n)=2^[log(n)]         g(n)=n^[sqrt(n)]
    apply log

    log(n)log(2)            sqrt(n)log(n)
    log(n)                  sqrt(n)log(n)

    then second is bigger.
    */
```
```c
    /*
    f(n)=2^n     g(n)=2^2n
    apply log

    nlog(2)      2nlog(2)

    second is bigger
    
    */
```
```c
    /*
    g1(n)=n^3    ->  n<100
    g1(n)=n^2    ->  n>=100

    g2(n)=n^2    ->  n<10_000
    g2(n)=n^3    ->  n>=10_000

    |________|_________________|_______________|____
    1       100             10_000          finite
    g1>g2       g1=g2               g2>g1

    then g2 is greater than g1.
    */
```
```c
    /* k => is constant
    find true or false
        (n+k)^m =O(n^m)             --> true.
        (2^(n+1))=O(2^n)            --> true.
        (2^2n)=O(2^n)               --> false.
        sqrt(log(n))=O(loglog(n))   --> false.
        n(log(n))=O(2^n)            --> true.
    */
```
---
## <p id=16>Best & Worst and Average case Analysis</p>

```c
    /*
        linear search 
            means make a for loop and search for a specific element in an array or something else.
        B(n) =O(1)
        W(n)=O(n)
        average case =all possible cases /no.of cases
        =1+2+3+....n/(n)
        means -> n(n+1)/2*n
        means -> (n+1)/2
    */
    /*
    again there is no fixed notation for best case and worst case and average case.
    */
```

```c
    /*
    binary search 
        time is log(n) => length of tree.
                20
        10              30
    5       15      25      40
    for Search algorithm 
        Min  Worst case is =log(n) -> length of tree -> in binary search.
        Max Worst Case is =n => height of tree -> in linear serach 

    */
```
----

## <p id=17>Disjoint Sets</p>
```c
    /* what are the disjoint set.
        Dis-joint set data structure also known as the union or 
        find data structure is used to partition set of elements
        into dis-joint sets according to some criteria. 
        Disjoint-set data structure provides nearly about 
        constant time operations for adding a new set,
    */
    /*
    implementation
        Some of them are based on the linked list and some are based on rooted trees
    */
    /*
    uses of it
        - It is used to keep track of connected component in an undirected graph.
        - It is used to detect cycles in the graph.
        - It is used to calculate the minimum spanning tree in Kruskal's algorithm.
        - It is used in Maze generation problems.
        - Calculating mutual friends.
    */
```
---
## <p id=18>Divide and Conquer</p>

```c
    /*
    Divide and conquer is a strategy like :
        greedy algorithm 
        dynamic programming.
        backtracking .
        branch and bound.
    */
    /*
    strategy -> is a approach or a design for solving a problem.
    */
    /*
    divide means that you divide your problem into small
    thing then solve it and then combine the solution.
    */
```
```c
    // Divide and conquer main algorithm 
    DA(p) {
        if(small(p))
            s(p);
        else{
            divide p into p1,p2,p3,.....
            apply DA(p1),DA(p2),....
            combine (DA(p1) DA(p2))
        }
    }
```
- Topic of Divide and conquer   
  - Binary Search
  - Finding Maximun and Minimum
  - Merge Sort
  - Quick Sort
  - Strassens Martrix Multiplication.
- all Divide and conquer depend on recurrance algorithm so
we will study recurrane(recursive) algorithm first.

-----

## <p id=19>Recurrence Relation</p>

- code by c
```c
    void test(int n){   //t(n)
        if (n>0){       
            printf("%d",n); //1
            test(n-1); //T(n-1)
        }
    }
    /*
    number of calls make is n+1 call.
    Time complexity --> O(n)

    for the currance relation we call f(n) is T(n)

             1         n=0
    T(n)
            T(n-1)+1   n>0
    */
     /*
     Find time complexity by substitute methods
        t(n)=t(n-1)+1
        t(n-1)=t(n-2)+1 
then    t(n-1)=t(n-2)+2     and so on.

        t(n-1)=t(n-k)+k
        assume  n-k=0
                n=k
        T(n)=T(n-n)+n
        T(n)=T(0)+n
        t(n)=1+n
finally time complexity is O(n)
     */
```
---
## <p id=20>Recurrence Relation</p>

```c
    void test(int n){
        if(n>0){ //1
            for(i=0;i<n;i++){ //n+1
                print("%d",n); //n
            }
            test(n-1); //T(n-1)
        }
    }
    /*
    T(n)=T(n-1)+2n+2    ->take asymoptic notation for 2n+2
    T(n)=T(n-1)+n

            1           n=0
    T(n)=
            T(n-1)+ n   n>0
    
    Time by tree method
            t(n)                                n
        n           t(n-1)
                n-1             t(n-2)          n-1
                            n-2         t(n-3)  n-2 and so on.

    then time is 0+1+...n-1+n => n(n+1)/2 
    then time complexity is O(n^2)
    */
    /*
    find time complexity by substitute
                1           n=0
    T(n)=
            T(n-1)+ n   n>0
    
    t(n)=t(n-1)+n
    t(n-1)=t(n-2)+n-1
    t(n-2)=t(n-3)+n-2 and so on.
    t(n-n)=t(0)+n-n
    then t(n)=t(n-n)+(n-n+1)+(n-n+2)+......+(n-1)+n
    then t(n)=t(0) +0 +1+2+3+..n
    then t(n)=1+n*(n+1)/2
    then time complexity is O(n^2)
    */
```
---
## <p id=21>Recurrance Relation</p>

```c
    void test(int n){
        if (n>0){ //1
            for(i=0;i<n;i=i*2){ //log(n)
                print("%d",i);  // log(n)
            }
            test(n-1)//t(n-1)
        }
    }
    /*

            1               n=0
    t(n)=
            t(n-1)+log(n)   n>0

    t(n)=t(n-1)+log(n)
    Time by tree
            t(n)                                    
        log(n)  t(n-1)                              log(n)

            log(n-1)    t(n-2)                      log(n-1)

                    log(n-2)    t(n-3)              log(n-2)

                            log(n-3)    t(n-4)      log(n-4)
        
    t(n)=log(n)+log(n-1)+log(n-2)
        log[n*(n-1)*(n-2).....2*1]
        log(n*n)
        nlog(n)
    */
    /*
    Find time complexity by substitute

        t(n)=t(n-1)+log(n)
        t(n)=t(n-2)+log(n-1)+log(n)
        t(n)=t(n-3)+log(n-2)+log(n-1)+log(n)
        t(n)=t(0)+log(n!)
        t(n)=log(n!) => log(n^n) 
        O(nlog(n))
    */
```
```c
    /*
    t(n)=t(n-1)+1       -> O(n)
    t(n)=t(n-1)+n       ->O(n^2)
    t(n)=t(n-1)+log(n)  ->O(nlog(n))
    t(n)=t(n-1)+n^2     ->O(n^3)
    t(n)=t(n-2)+1        ->O(n)
    t(n)=t(n-100)+n     ->O(n^2)
    t(n)=2t(n-1)+1      ->answer in next video   
    */
```
----
## <P id=22>Recurrance Relation</P>

```c
    test(int n){ //t(n)
        if(n>0){ 
            print("%d",n);  //1
            test(n-1);      //t(n-1)
            test(n-1);      //t(n-1)
        }
    }
    /*
    t(n)=2t(n-1)+1

            1           n=0
    t(n)=
            2t(n-1)+1   n>0
    */
    /*
    Time using tree method 
                        t(n)                                1
    1       t(n-1)                  t(n-1)                  2
        1  t(n-2)     t(n-2)   1  t(n-2)  t(n-2) and so on. 4
    
    time is 1   2   4   8   16 ---> total time is 2^k
            1   2   2^2 2^3 2^4    ..k  -> (2^k-1)/(2-1)
    formula a1   a2   a2^2 a2^3 a2^4    ..k  -> a((2^k)-1)/(2-1)
    */
    /*
    solve using substitute method
             1           n=0
    t(n)=
            2t(n-1)+1   n>0
    
    t(n)=2t(n-1)+1
        =2[2t(n-2)+1]+1
        =2^2[t(n-2)]+2+1
        =2^2[2t(n-3)+2]+2+1
        =2^3[t(n-3)]+2^2+2+1
    t(n)=2^k(t(n-k)+2^(k-1)+........2^2+2+1
    let k=n
        =2^n*1+1+2+2^2+2^3......2^k-1
        =2^n+2^k -> n=k
        =2^(n+1)
    then time is 2^k or 2^n
    Time complexity is O(2^k)
    */
```
----

## <p id=23>Master Theorem for Decreasing Function</p>

```c
    /*
    t(n)=t(n-1)+1       -> O(n)
    t(n)=t(n-1)+n       -> O(n^2) 
    t(n)=t(n-1)+log(n)  -> O(nlog(n))
    t(n)=2t(n-1)        -> O(2^n)
    t(n)=3t(n-1)        -> O(3^n) -> and so on.
    t(n)=2t(n-1)+n      -> O(n2^n)
    */

    /*
    Master theory 
        T(n)=at(n-b)+f(n)
        assume a>0 and b>0 and f(n) =O(n^k) while k>=0
            -> note b>0 should be greater than 0.

        if a=1          -> O(n^(k+1)) or 
                        -> O(n*f(n))

        if a>1          ->O((n^k)*(a^(n/b)))

        if a<1          -> O((n^k))

    */
``` 
## <p id=24>Reurrance Relation Dividing Function</p>

```c
    test(int n){ //1
        if(n>1){
            printf("%d",n); //1
            test(n/2) //n/2-1
        }
    }
    /*
    Recurrance relation

                1           n=1
        t(n)=
                t(n/2)+1    n>1
    */

    /*
        using tree method
            t(n)                            
        1           t(n/2)                  
                1           t(n/2)          
                        1           t(n/4)  
    finally t(n/2^k)=t(1)
    n/2^k =n=2^k ->     k=log(n)
    time is the length of the tree then time is log2(n)
    Time complexity is -> O(log(n))
    */

    /*
    by subtitution
    t(n)=t(n/2)+1
        =t(n/4)+1
        =t(n/8)+1
        =t(n/2^k)+2
        then time complexity is -> O(log(n))
    */ 
```
----

## <p id=25>Recurrance Relation</p>

```c

    /*
    recurrance relation
            1           n=1
    t(n)=  
            t(n/2)+n    n>1
    */

    /*
    find by tree methods
            t(n)                                        
        n           t(n/2)                              n
                n/2           t(n/4)                    n/2
                    n/4           t(n/8)                n/4
                                n/8           t(n/16)   n/8
        
        finally reach to t(n/2^k)
        n+n/2+n/2^2 ...... n/2^k
        n[1+1/2+1/2^2....1/2^k]
        n*2
        then time complexity is O(n)
    */
```
----
## <p id=26>Recurrance Relation</p>

```c
    
    test(int n){
        if(n>1){  //1
            for(i=0;i<n;i++){ //n
                // code here    
            }
            test(n/2) //t(n/2)
            test(n/2) //t(n/2)
        }
    }
    /*
    recurrance relation.

                1               n=1
        t(n)=  
                2t(n/2)+n     n>1
    */
    /*
        Find time by tree method.
                t(n)            
        t(n/2)                  t(n/2)                   n                              -> n
    t(n/4)  t(n/4)  n/2    t(n/4)   t(n/4)  n/2     n/2          n/2    and so on.      -> n

    this operation will to for n/2^k times
    n/2^k=1
    2^k=n
    k=log(n)
    all of these operation will take n times
    then time complexity is O(nlog(n))
    */
```
---
## <p id=27>Master theory for Dividing Function</p>

```c
    /*
    Formula
        T(n)=aT(n/b)+f(n)
    assume a>=1 and b>1 and f(n)=O( n^k X log(n)^p)

    case 1:
        if logb(a)>k then -> O(n^[logb(a)])
    case 2:
        if logb(a)=k    
            if p>-1  -> O(n^k X log(n)^(p+1))
            if p=-1->  O(n^k X loglog(n))
            if p<-1 ->  O(n^k)
    case 3:
        if logb(a) <k:
            if p>=0:
                O(n^k X log(n)^p)
            if p<0:
                O(n^k)
    */
```
```c
    /*
    T(n)=2T(n/2)+1
        a=2
        b=2
        f(n)=O(1)
            =O(n^0 X log(n)^0)
    log2(2)>k=0
    Then time is O(n)
    */
```
```c
    /*
    T(n)=4T(n/2)+n

    log2(4)=2>k=1 p=0
    O(n^2)    
    */
```
```c
    /*
    T(n)=8T(n/2)+n
    log2(8)=3
    k=1
    Then Time complexity is O(n^3)


    T(n)=8T(n/2)+n^2
    log2(8)=3
    k=2
    Then Time complexity is O(n^3)
    */
```
```c
    /*
    T(n)=4T(n/2)+n
    log2(4)=2
    k=1
    then Time complexity is O(n^2)
    */
```
```c
    /*
    T(n)=2T(n/2)+n
        log2(2)=1
        k=1
        then k=logb(a) and p=0
        then Time  n^1 log(n)
        O(nlogn) 
    */
```
```c
    /*
    T(n)=2T(n/2)+n/log(n)
    log2(2)=1
    k=1
    p=-1
    then Time O(nloglog(n))
    */
```
```c
    /*
        T(n)=T(n/2)+n^2
        log2(1)=0
        k=2
        p=0
        then time complexity is O(n^2)
    */
```
---
## <p id=28>Example for Master theory</p>

```c
    /*
        T(n)=2T(n/2)+1 
        log2(2)=1
        k=0
        o(n)
    */
    /*
        t(n)=4T(n/2)+1  
        log2(4)=2
        k=0
        O(n^2)
    */
    /*
    t(n)=4t(n/2)+n
        log2(4)=2
        k=1
        O(n^2)
    */
```
```c
    /*
        T(n)=T(n/2)+n           -> O(n)
        T(n)=2T(n/2)+n^2        -> O(n^2)
        T(n)=2T(n/2)+n^2logn    ->O(n^2logn)
    */
```
```c
    /*
        T(n)=T(n/2)+1           -> o(log(n))
        T(n)=2T(n/2)+n          -> O(nlogn)
        T(n)=2T(n/2)+nlog(n)    -> O(nlog(n)^2)
        T(n)=2T(n/2)+n/log(n)   -> O(nloglog(n))
        T(n)=2T(n/2)+n/log(n)^2 -> O(n)
    */
```
----
## <p id=29>Root Function</p>

```c
    /*
    T(n)=T(sqrt(n))+1
    t(n)=T(n^1/2)+1
    t(n)=T(n^1/2^2)+2 
    t(n)=t(n^1/2^k)+k

    assume n=2^m
    t(n)=t(2^m/2^k)+k
    assume t(2^m/2^k) =t(2)
    m/2^k=1
    m=2^k
    then k=log2(m)
    n=2^m
    m=log2(n)
    then k=log2log2(n)
    Time complexity     ---->   O(loglog(n))
    */
```
---
## <p id=30>Binary Search </p>
- Code With python
```py
#   To use binary search array should be sorted.
#   Time complexity ----> O(log2(n))
#   Average time is time for each element/number of element 
    # Then average time is also O(logn)
    def binary_Search(arr,l,h,key):
        while l<=h:
            mid=(l+h)//2
            if key>arr[mid]:
                l=mid+1
            elif key<arr[mid]:
                h=mid-1
            elif key=arr[mid]:
                return mid
        return -1
```
- by pseudo code
```c
    int binary_Search(A,n,key){
        l=1;h=n;
        while(l<=h){
            mid=(l+h)/2;
            if (key=A[mid])
                return mid;
            
            else if (key<A[mid])
                h=mid-1;
            else 
                l=mid+1;
        }
        return -1
    }
```
------
## <p id=31>Binary Search Recursive Method</p>

- code by python

```py
    def binary search(arr,l,h,key):
        mid=(l+h)//2
        if l<=h:
            if key<arr[mid]:
                return binary_search(arr,l,mid-1,key)
            elif key>arr[mid]:
                return binary_search(arr,mid+1,h,key)
            else:
                return mid
        else:return -1
```
- pseudo code 
```c
    binary_search(l,h,key){     //1
        if(l<=h){
            mid=(l+h)/2         //1
            if (key=A[mid])
                return mid
            else if (key<A[mid])
                h=mid-1
            else
                l=mid+1
            return binary_search(l,h,key) //n/2
        }
        else
            return -1 //means element not found.
    }
    /*
    recurrance relation.

            1           n=1
    T(n)=
            t(n/2)+1    n>1
    
    Then time is O(log(n))
    */
```
---
## <p id=32>Heap heap Sort</p>

- Time complexity for `best & average & worst`   O(nlogn)
- Space Complex./.ity  O(1)
- heap help us to build heapsort & priority queue.
- This summary form Adel Nasim [video](https://www.youtube.com/watch?v=REOsj0nYWKE&t=10s)

```c
    /*
    to use heap 
        should use complete binary tree.
        complete binary tree.
            when create tree we complete tree from left to right.
        we can represent complete binary tree as an array.
        To know if array start from 1-index:
            parent of node of index i   -> i//2
            left node of index i        -> 2*i
            right node of index i       -> 2*i+1
        To know if array start from 0-index:
            parent of node of index i   -> i//2-1
            left node of index i        -> 2*i+1
            right node of index i       -> 2*i+2
    */
    /*
    heap -> is a complete binary tree.
    types:  Max heap -> every parent greater than or equal it's child.
            Min Heap -> every parent smaller than or equal it's child.

    notes: not all complete binary tree is a heap.
    to convert complete binary tree to heap use heapify function [in python use heapq module]
    */
```
- code with python 
```py
# Time is nlog(n)
    def heapify(arr, n, i):
        largest = i 
        l = 2 * i + 1 
        r = 2 * i + 2 
        if l < n and arr[i] < arr[l]:
            largest = l
        if r < n and arr[largest] < arr[r]:
            largest = r
        if largest != i:
            (arr[i], arr[largest]) = (arr[largest], arr[i])  
            heapify(arr, n, largest)
    def heapSort(arr):
        n = len(arr)
        # build heap
        # time is O(n)
        for i in range(n // 2 - 1, -1, -1):
            heapify(arr, n, i)
        # to sort.
        # time is O(n)
        for i in range(n - 1, 0, -1):
            (arr[i], arr[0]) = (arr[0], arr[i]) 
            heapify(arr, i, 0)
    arr = [12, 11, 13, 5, 6, 7]
    heapSort(arr)
    n = len(arr)
    print('Sorted array is')
    for i in range(n):
        print(arr[i])
```
----
- summary from Dr.Abdul Bari.
  - comming soon.

----
## <p id=33>Merge Sort</p>

- time complexity is O(nlogn)
- space complexity is O(n+log(n)) -> O(n)
```c
    /*
    merge is combining a two sorted list in one single list
    merge two array at same time called -> 2-way margin.
    merge three array at same time called -> 3-way margin.and so on.

    2-way merge sort take O(nlog(n)) time complexity.
    n       -> for comparing each element
    logn    -> number of repeated times 
    */
    merge(A,B,n,m){
        i=1;j=1;k=1;
    while i<=m and j<=n{
        if A[i]<B[j]:
            c[k++]=A[i++];
        else:
            c[k++]=B[j++];
    }
    for(;i<=m;i+=)
        c[k++]=A[i];
    for(;j<=n;j++)
        c[k++]=B[j];
    }
```
---
## <p id=34>Merge Sort</p>

```c
    mergeSort(l,h){ //t(n)

        if l<h{
            mid=(l+h)/2  //1
            mergeSort(l,mid);    //t(n/2)
            mergeSort(mid+1,h);  //t(n/2)
            merge(l,mid,h); //n
        }
    }
    /*
    then time complexity is 
        
        t(n)=2t(n/2)+n
    using master theory.
    time complexity is -> O(nlog(n))
    */
```
- full code using python.

```py
# code taken from geeks for geeks website.

    def merge(arr, l, m, r):
        n1 = m - l + 1
        n2 = r - m
        # create temp arrays
        L = [0] * (n1)
        R = [0] * (n2)
        # Copy data to temp arrays L[] and R[]
        for i in range(0, n1):
            L[i] = arr[l + i]

        for j in range(0, n2):
            R[j] = arr[m + 1 + j]

        # Merge the temp arrays back into arr[l..r]
        i = 0	 # Initial index of first subarray
        j = 0	 # Initial index of second subarray
        k = l	 # Initial index of merged subarray

        while i < n1 and j < n2:
            if L[i] <= R[j]:
                arr[k] = L[i]
                i += 1
            else:
                arr[k] = R[j]
                j += 1
            k += 1

        # Copy the remaining elements of L[], if there
        # are any
        while i < n1:
            arr[k] = L[i]
            i += 1
            k += 1

        # Copy the remaining elements of R[], if there
        # are any
        while j < n2:
            arr[k] = R[j]
            j += 1
            k += 1

    # l is for left index and r is right index of the
    # sub-array of arr to be sorted
    def mergeSort(arr, l, r):
        if l < r:

            # Same as (l+r)//2, but avoids overflow for
            # large l and h
            m = l+(r-l)//2

            # Sort first and second halves
            mergeSort(arr, l, m)
            mergeSort(arr, m+1, r)
            merge(arr, l, m, r)


    # Driver code to test above
    arr = [12, 11, 13, 5, 6, 7]
    n = len(arr)
    print("Given array is")
    for i in range(n):
        print("%d" % arr[i],end=" ")

    mergeSort(arr, 0, n-1)
    print("\n\nSorted array is")
    for i in range(n):
        print("%d" % arr[i],end=" ")


```
---
## <p id=35>Merge Sort in depth analysis</p>

```c
    /*
    Pros 
        1.is suitable for large size list.
        2.suitable for linked list.
        3.External sorting.
        4.stable
        5.
    */
    /*
    cons:
        1.Extra space (not inplace sort)
        2.No small problem.[for small size list is smaller]
            . insertion sort    ->O(n^2)[may use with linked list]
            . merge sort        ->O(nlog(n))
            . mergesort slower than insertion sort if n<=15
    */
    /*
    All the recursive algorithm use stack.
    what could be the maximum size of the stack
        depend on the tracing height of our tracing tree of merge sort
    */
```
---
## <p id=36>Quick Sort</p>

```c 
    partition(l,h){
        pivot=A[l];
        i=l,j=h;
        while (i>j){
        do {
            i++;
        }while(A[i]<=pivot);
        do {
            j--;
        }while(A[j]>pivot);
        if(i<j)
            swap(A[i],A[j]);
        }
        swap(A[l],A[j]);
        return j;
    }
    QuickSort(l,h){
        if(l<h){
            if(l<h){
                j=partition(l,h);
                QuickSort(l,j);
                QuickSort(j+1,h);
            }
        }
    }
```
---
## <p id=37>Quick Sort Analysis</p>

- best case & average case time ->` O(nlog(n))`
- worst case -> `O(n^2)` => when array is sorted.
- space -> `inplace algorithm`  `O(1)`
```c
      QuickSort(l,h){
        if(l<h){
            if(l<h){
                j=partition(l,h);   
                QuickSort(l,j);     
                QuickSort(j+1,h);   
            }
        }
    }
    /*
        To improve quick sort in worst case 
            don't use first element as a pivot.
    improveing  ->  you can use the middle element in array.
                ->  Select a Random element as pivot here again worst case is O(n^2)

        The size of stack that used in quick sort 
            best case is -> O(logn)
            worst case is -> O(n)
    */
```
----

## <p id=39>Greedy method Introduction</p>

```c
    /*
    Greedy method: is one of approach for solving problem
    using for solving optimization problem[problems that need max and min result]

    fessible Solution : means a solution which is satisfied some constraints.

    optimal solution : a solution which need min result or max result

    strategy for solving optimization problem: 
        1.Greedy Method.
        2.Dynamic programming.
        3.Branch and Bound.
    */
```
```c
    /*
    greedy method approach : Says that a problem should be solved in stage in each stage consider one input from a given problem and if that input is fessible then include in the solution.
    */
    for i= 1 to n do {
        x=select(a);
        if fessible(x) then
            solution =solution + x
    }
```
----
## <p id=39>Knapsack Problem </p>

- This a an easy version from `knapsank problem`

```c
    /*
    Problem Discription : 
    
        we have a bag called knapsack and want to full it with somethings 
        every thing has a value.
        we want to full this page value be maximum value.
        - note we can make a divide for any thing we put in the bag 
            let say we have a thing called x it weight is 4 it's value is 50
            here we can take a 2 weight of it and take 25 as a value.     
    */
    /*
    bag capacity is 15. --> m=15
        - we divide a [profit/weight] the take the max one first and second and so on.

    */
```
---
## <p id=40>Job Sequencing with Deadlines </p>

```c
    /*
    problem Description :
        we take number of jobs.
        every task have a profit and deadline:
            to take profit of each task you should finish task before deadlines
        each job take one unit of time for completion.
    */
    /*
    n => number of jobs:
    n=5
    jobs        : j1    j2     j3   j4   j5
    profits     : 20    15     10   5    1 
    deadlines   : 2     2      1    3    3

    0______1_______2__________3  -> is the time i can complete tasks on it.
       j2     j1        j4
    time start from zero and end on the last task time.
    */
```
- code with python.
```py
    import sys,math
    n=int(input())
    jobs=list(map(int,sys.stdin.readline().split()))
    profits=list(map(int,sys.stdin.readline().split()))
    all=[0]*n
    for i in range(n):
        all[i]=[profits[i],jobs[i]]
    all.sort(reverse=True)
    print(all)
    check=[0]*max(jobs)
    ans=0
    for i in range(n):
        if check[all[i][1]-1]==0:
            check[all[i][1]-1]=1
            ans+=all[i][0]
            print(all[i][0])
            # print(check)
        else:
            j=1
            while j<=all[i][1] and all[i][1]-j-1>=0:
                if check[all[i][1]-j-1]==0:
                    check[all[i][1]-j-1]=1
                    ans+=all[i][0]
                    break
                # print(check,"from here")
                j+=1

    print(check)
    print(ans)
```
---
## <p id=42>Optimal Merge Pattern</p>

```c
    /*
    remember to make a merge between two array the two array should be sorted.
    to make a merge for more than two array there are more ways to do it.
        - First : merge Random first one with second then merge result with three and so on.
        - Second : merge only two array with other until reach to only two array and merge them.
        - Thrid : optimal solution -> on each merge choose the smallest two array and merge them until reach to only two array and then merge them.
    */
```
---
## <p id=43>Huffman Coding</p>

```c
    /*
    Huffman -> is a comparison technique it use for reducing the size of data or message.
    remember -> each char represent in 8 bits.
    A -> 65 ->0100_0001 and so on.
    we can use huffman approach to make encode for these char and save size.
    */
```
- message `BCCABBDDAECCBBAEDDCC` without encoding use `20*8=160bit`

| Char | Count/Frequecy | Code|
|------|----------------|------|
| A | 3|000|
|B|5|001|
|C|6|010|
|D|4|011|
|E|2|100|

- Message After encoding use `20*3=60bits`
- table char take `5*8 + 5*3=55bits`
- total size of massege is `115bit`
- huffman size you can't use the fixed size of code for alphabets some char may appear few time so use only needed code for it.

- Huffman for previous example.

| Char | Count/Frequecy | Code| bits
|------|----------------|------|--|
|A  |3  |001|3*3=9|
|B  |5  |10|5*2=10|
|C  |6  |11|6*2=12|
|D  |4  |01|4*2=8|
|E  |2  |000|2*3=6|
```c
    /*
          20
       9
     5
           11
    2 3 4 5 6 
    E A D B C 
    combine each small one with each other then for each line in right but 1 and each line in left but zero and then complete your table.
    */
    /*
    
    size of message is 45bits from table.
    size of table is 5*8bits + 12 bits=52bits.
    then total message size is 97bits.
    */
    /*
    this operation like zip file or compressed files.
    */
```
---

- ## <p id=44>Minimum cost spanning True.</p>
- 
```c
/*
    Graph is represented as -> G=(V,E)
    v -> is a set of points like -> v={1,2,3}
    E -> is a set of edges. -> E -> {(1,2),(2,3),(3,4)}
    spanning Tree is a graph of a graph.[subgraph of a graph.]
    spanning Tree don't contain any cycle in a graph.

    differnt spanning Tree can Generate from a graph is  [nCp] -number of cycles.
        n is number of edges in a  graph
        p is number of points[vertices الرؤوس] in a spanning Tree - 1.
        C is a combination.    
*/
/*
    MInimum Cost spanning Tree.
    - To find it We Have a to method: Prim's Method.
                                    : Kruskals Method.
*/
/*
    prim's call -> First of all you select a minimum Cost Edge but make sure that it should be connected by all the Selected vertice.
    - Note we can't find a spanning Tree for not connected Graph.

*/
/*
    Kruskal's Method -> Follow A greedy approach[algorithm]
    it says that always select a minimum Cost Edge without forming[making] a cycle
Time complexity :
    Total Time to find a spanning Tree is :
        O(|V|*|E|)  -> V number of Vertices[points]
                    -> E number of Edges.
        O(n^2) if E=V=n

    We can improve time complexity of Kruskal's by :
    using a data sstucture give you a minimum value : 
        it's a min heap. -> Take a log time.
     so the time complextity will be nlog(n) 
*/
/*
    if give a graph and tell you he already created his spanning tree by the known edges of in the graph.
    Question: tell you find the minimum value of unknown edges.
    Answer: Value of unknown edges Must be  Max of Max value of edges that can make with all of them a cycle
*/
```
---
- ## <p id=45>Dijktra Algorithm</p>

```c
    /*
    Dijktra -> for single source shortest path problem. 
    in greedy method there are a prefined procedures and we follow these procedures to get optimal solution. 
    Dijktra Algorithm give a procedure for getting an optimal solution.
    */
    /*
    Dijktra -> can work with directed graphs and non directed graphs.
    Dijktra work by relaxation method 
points Value        2       4
     points    1       2       3
points Name            u       v
        Relaxation Means -> if(d[u]+c(u,v)< d[v])
                                d[v]=d[u]+d(c,v) 
    */
    /*
    Worth Case for dijstra Algorithm is O(n^2)
    n -> number of points. 
    */
    /*
    non directed graph -> means you can walk from point 1 to point 2 and vice versa. 
    To make non directed graphs to directed graphs
     -> change the non directed arrow that is on edge to directed arrow in both side .
    */
    /*
    Dijktra Algorithm Work when the edges value are positive
     and if the edge values are negative it give us wrong
     Answer[it might give us correct answer but still the way 
     of Dijktra is wrong to solve it.]
     
    - Greedy Approach Failed when the edge is negative.
    - There is another solution for it with Billman force algorithm that we will see in Dynamic programming.
    */
``` 
----
- ## <p id=46>Dynamic Programming</p>

```c

```