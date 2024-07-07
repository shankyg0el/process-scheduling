# Process-scheduling-algorithms

This repository implements various CPU scheduling algorithms in C++. The algorithms included are:

- **First Come First Serve (FCFS)**
- **Round Robin (RR)**
- **Shortest Process Next (SPN)**
- **Shortest Remaining Time (SRT)**
- **Highest Response Ratio Next (HRRN)**
- **Feedback (FB)**
- **Aging**

## Input Format

To run the CPU scheduling simulation, follow these input format guidelines:

1. **Line 1**: Specify whether to output "trace" or "stats".
   - `"trace"`: Outputs the timeline trace for each process.
   - `"stats"`: Outputs statistics about each scheduling algorithm.

2. **Line 2**: Comma-separated list specifying the CPU scheduling policies to analyze/visualize.
   - Each algorithm is represented by a number or abbreviation as listed in the introduction section.

     Example:
     - `1`: First Come First Serve (FCFS)
     - `2-4`: Round Robin (RR) with time quantum `4`
     - `3`: Shortest Process Next (SPN)
     - `4`: Shortest Remaining Time (SRT)
     - `5`: Highest Response Ratio Next (HRRN)
     - `6`: Feedback (FB)
     - `7`: Feedback with varying time quantum (FBV)
     - `8-1`: Aging with initial priority `1`

3. **Line 3**: An integer specifying the last instant for simulation and timeline display.
   - This defines the maximum time frame for the simulation.

4. **Line 4**: An integer specifying the number of processes to simulate.

5. **Line 5 onwards**: Description of each process, formatted based on the chosen scheduling algorithms:
   - For algorithms `1` to `7` (FCFS to Feedback):
     - Each process is described using a comma-separated list: `Process Name, Arrival Time, Service Time`.
   - For the Aging algorithm (`8-1`):
     - Each process is described using a comma-separated list: `Process Name, Arrival Time, Priority`.
   
   **Note:**
   - Processes should be sorted based on arrival time. If two processes have the same arrival time, the process with the lower priority (for Aging) or default order (for others) is assumed to arrive first.

### Example Input

Here’s an example of how the input might look:

```plaintext
trace
1,2-4,3,4,5,6,8-1
100
5
P1,0,5
P2,1,3
P3,2,7
P4,3,2
P5,5,4

