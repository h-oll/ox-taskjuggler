# ox-taskjuggler
Orgmode exporter for Taskjuggler. 

Please see this [tutorial](https://orgmode.org/worg/org-tutorials/org-taskjuggler.html) for an intro to taskjuggler and its orgmode exporter.

## 2025-08-14
In reply to [Issue #1](https://github.com/h-oll/ox-taskjuggler/issues/1), the exporter does not anymore create default resources and accounts when none are present, and don't allocate resources to tasks if none are allocated by the user. As a consequence, this breaks the tutorial in the sense that to obtain the first GANTT chart, the user needs to create at least one resource and allocates it to tasks. 

The reason behind the change, is that taskjuggler is performing checks and will detect missing allocations etc. I don't believe this is the role of the exporter to check a minor part of the overall structure of projects and then silently (and quite randomly) create defaults that are non configurable when this structure is not complete.
