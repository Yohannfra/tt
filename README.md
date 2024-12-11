# TT (Time Tracker)

A simple cli time tracker inspired by [timetrace](https://github.com/dominikbraun/timetrace).

## Example

Start tracking a project

```
$ tt start myapp
Started tracking time for myapp

# or with a specific task
$ tt start task1@myapp
Started tracking time for task1@myapp
```

Stop tracking a project

```
$ tt stop
Stoped tracking time
```

Show report

```
$ tt report

┏━━━━━━━━━┳━━━━━━━┳━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━┓
┃ Project ┃ Task  ┃ Start           ┃ End             ┃     Total ┃
┡━━━━━━━━━╇━━━━━━━╇━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━┩
│ myapp   │       │ 12/12/24 02:39  │ 12/12/24 03:40  │     1h:1m │
│         │ task1 │ 12/12/24 04:41  │ 12/12/24 06:19  │    1h:38m │
│         │       │                 │ TOTAL           │    2h:39m │
│         │       │                 │                 │           │
│         │       │                 │                 │           │
│         │       │                 │ TOTAL           │ 0d 2h:39m │
└─────────┴───────┴─────────────────┴─────────────────┴───────────┘
```

## Install

```bash
$ git clone https://github.com/Yohannfra/tt

$ sudo cp tt /usr/local/bin
```

## Usage

```bash
$ ./tt -h
usage: tt [-h] {start,edit,stop,reset,cancel,delete,report,list,status} ...

options:
  -h, --help            show this help message and exit

commands:
  {start,edit,stop,reset,cancel,delete,report,list,status}
                        Available commands
    start               Start tracking time
    edit                Edit a project with $EDITOR
    stop                Stop tracking your time
    reset               Reset the current tracking
    cancel              Cancel the current tracking
    delete              Delete a project
    report              Display report
    list                List projects
    status              Display the current tracking status
```

## Format

```bash
$ uv run ruff format ./tt
```

## Lint

```bash
$ uv run ruff check ./tt
```
