# slooo: The DepFast Fail-slow Injection Testing Infrastructure

This is a new repo for the depfast slow-injection testing infrastructure. It will be a new build from scratch.

The old code can be found at: https://github.com/WolfDOS/depfast-inj

The goal of this project is to build a generic, reusable testing infrastructure that can be effectively used for any distributed systems (we can start from Raft or other consensus systems), rather than a bunch of ad hoc scripts.

IMPORTANT:  
Only works with Microsoft Azure (so far).

Command:
```
usage: run.xsh [-h] [--system SYSTEM] [--iters ITERS] [--workload WORKLOAD] [--server-configs SERVER_CONFIGS] [--runtime RUNTIME] [--exps EXPS] [--exp-type EXP_TYPE] [--swap] [--ondisk ONDISK] [--threads THREADS] [--diagnose] [--output-path OUTPUT_PATH] [--cleanup]

optional arguments:
  -h, --help            show this help message and exit
  --system SYSTEM       mongodb/rethinkdb
  --iters ITERS         number of iterations
  --workload WORKLOAD   workload path
  --server-configs SERVER_CONFIGS
                        server config path
  --runtime RUNTIME     runtime
  --exps EXPS           experiments to be ran saperated by commas(,)
  --exp-type EXP_TYPE   leader/follower
  --swap                Swapniess on
  --ondisk ONDISK       in memory(mem) or on disk (disk)
  --threads THREADS     no. of logical clients
  --diagnose            collect diagnostic data
  --output-path OUTPUT_PATH
                        results output path
  --cleanup             clean's up the servers
  ```