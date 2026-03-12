# Philosophers

A multithreaded simulation of the Dining Philosophers problem written in C, developed as part of the 42 School curriculum.  
The goal of this project is to learn concurrent programming using threads, mutexes, and synchronization while avoiding race conditions, deadlocks, and starvation.

This project focuses on low-level system programming, timing precision, and safe access to shared resources.

## Description

The Dining Philosophers problem is a classic concurrency problem where multiple philosophers sit around a table and alternate between eating, sleeping, and thinking.  
Each philosopher needs two forks to eat, but forks are shared resources, so the program must ensure correct synchronization between threads. :contentReference[oaicite:0]{index=0}  

The simulation must guarantee:

- No data races
- No deadlocks
- No starvation
- Accurate timing
- Safe thread execution

## Features

- Multithreading using pthread
- Mutex synchronization
- Precise time management
- Fork resource locking
- Death detection
- Optional eat limit
- Safe printing
- Error handling

## Program Arguments

```
./philo number_of_philosophers time_to_die time_to_eat time_to_sleep [must_eat]
```

Example

```
./philo 5 800 200 200
```

Arguments:

- number_of_philosophers — number of philosophers
- time_to_die — time before a philosopher dies without eating
- time_to_eat — eating duration
- time_to_sleep — sleeping duration
- must_eat — optional number of times each philosopher must eat

The simulation stops when a philosopher dies or when all philosophers have eaten enough times. :contentReference[oaicite:1]{index=1}  

## Project Structure

```
src/
philo/
threads/
utils/
time/
init/

include/

Makefile
```

## Build

```
make
```

Clean

```
make fclean
```

## Run

```
./philo 5 800 200 200
```

## Concepts Learned

- Threads (pthread)
- Mutex
- Shared memory
- Race conditions
- Deadlocks
- Process synchronization
- Timing control
- Low-level C programming

## Notes

This project follows the 42 subject rules and uses only allowed functions.  
The goal is educational and not a full production-ready implementation.

## Author

Abdellah Marouf  
Morocco  
https://github.com/amarouf-dev
