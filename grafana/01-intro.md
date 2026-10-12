# INTRO

## What is observability

Observability - the degree in which one can determine the state of the system by looking at its outputs.

Observability:
- provides context for what's wrong
- helps with cost optimization
- helps with capacity planning
- informs of user behavior

### Types

Three plus one types:
1. metrics
   - a numeric timestamped measurement
   - what is broken; but not why
2. logs
   - timestamped records of events
3. traces
   - end-to-end path through a system - spans
4. profiles
   - measurement of a resource usage and duration


## Grafana stack

- Mimir - metrics
- Loki - logging
- Tempo - tracing
- Pyroscope - profiling