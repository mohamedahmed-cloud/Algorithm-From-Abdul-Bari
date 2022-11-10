# Algorithm-From-abdl-Albrary
Summary for Our algorithm &amp; Data Structure course 

----

### Most Of codes in this summary will be with Python language and psuedo code  

## <a href="#1">Vidoe 1</a>
## <a href="#2">Vidoe 2</a>
## <a href="#3">Vidoe 3</a>
## <a href="#4">Vidoe 4</a>
## <a href="#5">Vidoe 5</a>
## <a href="#6">Vidoe 6</a>
## <a href="#7">Vidoe 7</a>


----
### <p id=1> introduction To Aglorithm </p>
- [Vidoe](https://www.youtube.com/watch?v=0IAPZzGSbME&list=PLDN4rrl48XKpZkf03iYFl-O29szjTrs_O&index=1)
- Summary 
  - `Algorithm` => is a step by step precedure for solving computational problem.
  - `software cycle ` most important of it is
    - . design phase & implementation phase 


|Agorithm | Program |
|------|-----------|
| design time| implementation time|
|Domain knowledge | programmer|
| use any programming lagnuage | use speific language| 
|not hdepend on Hard ware & OS | depend on Hard ware & OS|
|analze the algorithm | testing algorithm|
 
----------
### <p id=2>Priori Analysis and Posteriori Testing</p>

- `Priori Analysis` => Means we wil do the analysis to find time & space.
- `Posteriori Testing` => Done on the program. We run and check it to know number of millsecond token and memeory consuming.
----

### <p id=3>Characteristics of Algorithm.</p>

- `input` => take `0` or more 
- `output` => at least 1 O/P
- Definiteness =>  use know value not like `sqrt(-1)` and `0/1` and so on.
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
    CPU Registers consumption
- 
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
        c =<> n^2
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
            for(i=0;j<n;j++) //n*(n+1)
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
<p id=6>Time Complexity 1</p>

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
    for(i=1;i<n;i=i*2>)
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
    for(i=0;i*i<n;i++)
        // code here
    for(i=0;i<n;i++)
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
        i+=;
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
## <p id=9>Types of Time function</#p>

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
    Ω Big omega 
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
- `people` think taht big was used for `upper bound` as wrost case and Omega for `lower bound` as best case no. You Can use any notaion for best case any notation for wrost case.
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
---
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
    f(n)=n^2log(n)          g(n)=n(log(n))^10
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
        
        3n^sqrt(n)              2^[log2(n)^sqrt(n)] 
        3n^sqrt(n)              n^sqrt(n)
        then first is bigger.
    */
```
----
<p id=15>Comparison of Function 2</p>

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

    ._______________________________________________>
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
<p id=16>Best & Worst and Average case Analysis</p>



