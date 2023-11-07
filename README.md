![240579349-2960ee3e-7325-4e09-85e1-ae816ceaaab3](https://github.com/Bmohamedathil/Single-server-infinite-capacity---Markov-Model/assets/119560261/1a82fab7-51e7-4436-903a-9a8eb4f6db10)# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)

## Experiment:
 ![240579349-2960ee3e-7325-4e09-85e1-ae816ceaaab3](https://github.com/Bmohamedathil/Single-server-infinite-capacity---Markov-Model/assets/119560261/7e2d333d-ac78-42c8-becd-513078ca8fbd)
 ![240579443-f5b111fa-a1b3-47ce-b862-a071560beec0](https://github.com/Bmohamedathil/Single-server-infinite-capacity---Markov-Model/assets/119560261/b5878f1f-2abf-442f-a88a-3767413ce3df)


## Program
```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```
## Output :
![276934939-0426dc3d-6479-410f-852c-85da8728e2b9](https://github.com/Bmohamedathil/Single-server-infinite-capacity---Markov-Model/assets/119560261/3303ad0d-7e06-42b6-8255-6c001e6d75f0)

## Result :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
