# lifecycle

An mrepo brought into service and back: made ready, its door opened, closed, shut down.

A service-managed mrepo starts `booted`. Each action is allowed in one
state and moves it on; its hooks do the work of the transition.

## Steps

The script, [steps.haicc](steps.haicc): each line as typed after `haicc`, what it answers under it; run with `howto/run`, shown here at info extraction.

## Notes

- **An action in the wrong state** is refused, `not now`, with the
  state the service is in: `not now: service start (the service is
  started)`.
- **Behind the door**: `boot` and `crud` in a host, refused while it is
  not started.
- **Received, not held**: a request its state does not allow is taken
  in and answered refused at once; it does not wait for the state.
- **The mrepo's own lines pass**: a hook's lines, its commission's, are
  not asked whether a protocol is active: the door is closed to the
  outside.
