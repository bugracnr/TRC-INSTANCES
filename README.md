# TRC-INSTANCES

Instances used for the computational experiments of the paper entitled "The role of individual compensation and acceptance decisions in crowdsourced delivery."

---

**Static Experiments:** Folder containing instances used for the static experiments (Sections 7.1-7.3)  
- **File Names:** `[The number of ODs]_[The number of tasks]_[Penalty %]_[Utility %]_[Instance ID].txt`  
- **File Structure:**
    ```
    NUM_DRIVERS: [The number of ODs]
    NUM_TASKS: [The number of tasks]
    PENALTY: [Penalty %]
    UTILITY: [Utility %]

    DRIVERS
    ID             X                    Y              
    ...            ...                  ...

    TASKS
    ID             X              Y              COST           PENALIZED_COST 
    ...            ...            ...            ...            ...

    ALPHA
    [NUM_TASKS*NUM_DRIVERS MATRIX]    

    BETA
    [NUM_TASKS*NUM_DRIVERS MATRIX]

    LOGISTIC REGRESSION PARAMETERS
    INTERCEPT:                    ...     
    DRIVER DISTANCE:              ...     
    TASK DISTANCE:                ...   
    DELIVERY DISTANCE:            ...     
    DRIVER SENSITIVITY:           ...       
    COMPENSATION:                 ...
    ```

---

**Dynamic Experiments:** Folder containing instances used for the dynamic experiments (Section 7.4)  
- **File Names:** `instance_[TASK ARRIVAL RATE]_[TASK AVERAGE TIME IN SYSTEM]_[DRIVER_ARRIVAL_RATE]_[DRIVER AVERAGE TIME IN SYSTEM]_[INSTANCE ID].txt`  
- **File Structure:**
    ```
    Periods: [NUM PERIODS]
    Task Arrival Rate: [TASK ARRIVAL RATE]
    Task Average Time: [TASK AVERAGE TIME IN SYSTEM]
    Driver Arrival Rate: [DRIVER_ARRIVAL_RATE]
    Driver Average Time: [DRIVER AVERAGE TIME IN SYSTEM]

    Period: [PERIOD NO]
    Tasks: [NUM OF TASKS ARRIVE AT THE PERIOD]
    id      	x	            y	            end	                                c
    [TASK ID]	[TASK X COORD]	[TASK Y COORD]	[LAST ACTIVE PERIOD OF THE TASK]	[DELIVERY COST]

    Drivers: [NUM OF DRIVERS ARRIVE AT THE PERIOD]    
    id      	x	            y	            end	                                sensitivity
    [TASK ID]	[TASK X COORD]	[TASK Y COORD]	[LAST ACTIVE PERIOD OF THE TASK]	[DRIVER SENSITIVITY VALUE]
    ...
    ```
