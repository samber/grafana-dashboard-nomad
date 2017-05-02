
# Grafana dashboards for Nomad (Docker orchestrator from Hashicorp)

:warning: Some PR on the nomad exporter are still in a pending state. Please use my fork:

```bash
$ docker pull samber/nomad-exporter
```

I didn't take time to make screenshots, because I will improve those dashobards often and my Grafana instance shows some confidentials informations ;)

If anybody want to print some screenshot, please send a PR ;)

Contributions welcomed !

## Nomad cluster resource usage

- Number of jobs
- Number of taskgroups
- Number of Unique Tasks
- Number of allocated Tasks
- Number of allocation per group

- Nodes memory:
  - Used memory (GB)
  - Used memory (%)
  - Avg memory used by taskgroup
  - Avg memory burst by taskgroup

- Nodes CPU:
  - Used CPU (GB)
  - Used CPU (%)
  - Avg CPU used by taskgroup
  - Avg CPU burst by taskgroup

- Total RAM on the cluster
  - Allocated
  - Used

## Nomad events

Displays nomad events, for each nomad task, such as:

- restarting
- terminated
- killing
- started
- received (meaning "nomad run <job>.nomad")
- driver
- ...

## Nomad tasks

Displays resources usages and events at the allocated task level (= instance level).

- Show node name where each task is allocated

Loop accross allocated tasks and displays a row with:

- Events of the allocated task
- Used memory of the allocated task
- CPU usage of the allocated task

You can filter allocated tasks by job name, taskgroup name, and task name.
