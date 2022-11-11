# Algorithm-From-abdl-Albrary
Summary for Our algorithm &amp; Data Structure course 

----

### Most Of codes in this summary will be with Python language and psuedo code  
## Videos on Youtube 

- From [here](https://www.youtube.com/playlist?list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O)

## Summary of vidoe 
- <a href="#1">Vidoe 1</a>
- <a href="#2">Vidoe 2</a>
- <a href="#3">Vidoe 3</a>
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


----
### <p id=1> introduction To Aglorithm </p>

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
### <p id=2>Priori Analysis and Posteriori Testing</p>

- `Priori Analysis` => Means we wil do the analysis to find time & space.
- `Posteriori Testing` => Done on the program. We run and check it to know number of millsecond token and memeory consuming.
----

### <p id=3>Characteristics of Algorithm.</p>

- `input` => take `0` or more 
- `output` => at least 1 O/P
- Definiteness =>  use known value not like `sqrt(-1)` and `0/1` and so on.
- `finiteness` => all algorithm must stop at some point.
- `Effectiveness` => don't use unnecessary thing. 

----
### <p id=4>How to Write an Agorithm</p>

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
### <p id=5>Frequency Count Methods</p>
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
### <p id=7>Time Complexity 2</p>

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
            O(n^log(n)) & Omega(n^2log(n)) & theta(n^2log(n))
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
        sqrt(log(n))=O(loglog(n))   --> false. -ask some one.
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
<p id=18>Divide and Conquer</p>

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
### <p id=20>Recurrence Relation</p>

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
<p id=21>Recurrance Relation</p>

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

<p id=23>Master Theorem for Decreasing Function</p>

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
        T(n)=a(t-b)+f(n)
        assume a>0 and b>0 and f(n) =O(n^k) while k>=0
            -> note b>0 should be greater than 0.

        if a=1          -> O(n^(k+1)) or 
                        -> O(n*f(n))

        if a>1          ->O((n^k)*(a^(n/b)))

        if a<1          -> O((n^k)*a^(n/b)) or 
                        -> O(f(n)*a^(n/b))

    */
``` 
<p id=24>Reurrance Relation Dividing Function</p>

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
## <p id=28></p>

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
        T(n)=T(n/2)+n           -> O(nlogn)
        T(n)=T(n/2)+nlog(n)     -> O(nlog(n)^2)
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
<p id=31>Binary Search Recursive Method</p>

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
<p id=32>Heap heap Sort</p>

- Time complexity for `best & average & worst`   O(nlogn)
- Space Complecity  O(1)
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
