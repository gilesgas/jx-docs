---
date: 2018-09-17T16:50:47Z
title: "jx step verify"
slug: jx_step_verify
url: /commands/jx_step_verify/
---
## jx step verify

Performs deployment verification in a pipeline

### Synopsis

This pipeline step performs deployment verification

```
jx step verify [flags]
```

### Examples

```
  jx step verify
```

### Options

```
      --after int32      The time in seconds after which the application should be ready (default 60)
  -h, --help             help for verify
  -p, --pods int32       Number of expected pods to be running (default 1)
  -r, --restarts int32   Maximum number of restarts which are acceptable within the given time
```

### SEE ALSO

* [jx step](/commands/jx_step/)	 - pipeline steps

###### Auto generated by spf13/cobra on 17-Sep-2018
