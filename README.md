# Job sequencing with deadlines

## Overview
The goal is to schedule a set of jobs, each with a deadline and profit, in such a way that the total profit is maximized. Each job takes exactly one unit of time, and no two jobs can be scheduled at the same time.

## Problem Definition

Given:
- A list of jobs, where each job \( j \) has:
  - A deadline \( d_j \)
  - A profit \( p_j \)
- Each job takes exactly one unit of time.
- The maximum deadline among all jobs.

Objective:
- Schedule jobs to maximize total profit.
- Each job must be completed by its deadline.

## Example

Consider the following set of jobs:

| Job ID | Deadline | Profit |
|--------|----------|--------|
|   1    |    4     |   20   |
|   2    |    1     |   10   |
|   3    |    2     |   40   |
|   4    |    2     |   30   |

A possible optimal schedule is to complete jobs 3, 4, and 1, earning a total profit of 90.

## Implementation

The implementation involves the following steps:

1. **Sort Jobs by Profit**: Sort the jobs in decreasing order of profit.
2. **Initialize Time Slots**: Create an array to keep track of free time slots.
3. **Schedule Jobs**: Iterate through the sorted list of jobs and place each job in the latest available time slot before its deadline.


## Input Format

The input will consist of a list of jobs, where each job has three attributes: Job ID, Deadline, and Profit. These can be provided as follows:

1. **Job Class**: Each job is represented as an instance of the `Job` class.
2. **List of Jobs**: A list of `Job` objects.


## Output Format

The output will consist of two elements:

1. **Scheduled Jobs**: A list of Job IDs that are scheduled.
2. **Total Profit**: The total profit from the scheduled jobs.

