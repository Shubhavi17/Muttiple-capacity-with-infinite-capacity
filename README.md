# Multiple server with infinite capacity - (M/M/c):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 10 seconds, serivice time of two lathe machine follow exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](https://user-images.githubusercontent.com/103921593/203238035-1c8109bc-cbf2-4c77-baea-c5b682a752ef.png)

## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203238265-176740b0-eae2-4772-90be-5449869ac9b0.png)




## Experiment:


## Program
```
# Given data
mean_interarrival_time = 10  # seconds
mean_service_time_lathe = 1  # seconds
mean_service_time_robot = 7  # seconds

# Calculate arrival rate (λ)
arrival_rate = 1 / mean_interarrival_time

# Calculate service rate for lathe machines (μ)
service_rate_lathe = 1 / mean_service_time_lathe

# Calculate service rate for robot (μ)
service_rate_robot = 1 / mean_service_time_robot

# Check if the system is stable (λ < μ)
if arrival_rate >= (service_rate_lathe + service_rate_robot):
    print("The system is unstable. Arrival rate is greater than or equal to service rate.")
else:
    # Calculate average number of materials in the system (L)
    L = arrival_rate / (service_rate_lathe + service_rate_robot - arrival_rate)

    # Calculate average number of materials in the conveyor (Lq)
    Lq = (arrival_rate ** 2) / (service_rate_lathe + service_rate_robot) / (service_rate_lathe + service_rate_robot - arrival_rate)

    # Calculate waiting time of each material in the system (W)
    W = 1 / (service_rate_lathe + service_rate_robot - arrival_rate)

    # Calculate waiting time of each material in the conveyor (Wq)
    Wq = arrival_rate / ((service_rate_lathe + service_rate_robot) * (service_rate_lathe + service_rate_robot - arrival_rate))

    print("Average number of materials in the system (L):", L)
    print("Average number of materials in the conveyor (Lq):", Lq)
    print("Waiting time of each material in the system (W):", W)
    print("Waiting time of each material in the conveyor (Wq):", Wq)
```

## Output :
![Screenshot 2024-03-29 201905](https://github.com/Shubhavi17/Muttiple-capacity-with-infinite-capacity/assets/150005085/df44b0e7-2aa3-4f72-ba32-e88f0d596e19)


## Result : 
Thus the average number of materials in the system and conveyor, waiting time of each material in the system and conveyor is found successfully.

