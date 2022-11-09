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
  - `Algorithm` => is a step by step precdure for solving computational problem.
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

- Sum Algorithm of array.
```c
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
<p id=6>Time Complexity </p>
