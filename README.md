# Simba Threading Library

A library for managing concurrent operations and scheduled tasks.

## Core Components

- **`TThreadManager`**: The primary interface for accessing both the thread pool and the scheduler.
- **`TThreadPool`**: Manages a pool of worker threads to execute one-off asynchronous tasks.
- **`TScheduler`**: Executes tasks at regular, fixed intervals using a dedicated pool.

## Fundamentals

- **Asynchronous Execution**: Submit tasks to run in the background without blocking the main script.
- **Task Scheduling**: Define procedures that run repeatedly at a specified interval.
- **Priority Queue**: Assign a priority to tasks to ensure more critical operations are processed first.
- **Callbacks**: Assign procedures to the `OnComplete` and `OnException` events to react to task completion or failure.
- **Graceful Shutdown**: The shutdown process waits for active tasks to finish before terminating worker threads.
- **Resource Management**: Idle worker threads enter a low-CPU sleep state with an exponential backoff to conserve resources.