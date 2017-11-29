# sleep-v - similar to `sleep`(1) but more verbose

Example:

```
hayasaka@darkao% time (sleep-v .1; echo)      # sleeps 0.1 seconds

( sleep-v .1; echo; )  0.06s user 0.04s system 50% cpu 0.201 total
hayasaka@darkao% time (sleep-v 1.1; echo)     # sleeps 1.1 seconds
1
( sleep-v 1.1; echo; )  0.07s user 0.03s system 8% cpu 1.199 total
hayasaka@darkao% time (sleep-v 11.1; echo)    # sleeps 11.1 seconds
:987654321
( sleep-v 11.1; echo; )  0.07s user 0.03s system 0% cpu 11.196 total
hayasaka@darkao% time (sleep-v 1m 11.1; echo) # sleeps 71.1 seconds
1m:::::987654321
( sleep-v 1m 11.1; echo; )  0.08s user 0.02s system 0% cpu 1:11.22 total
hayasaka@darkao% time (sleep-v 3.2m; echo)    # sleeps 192 seconds
3m2m1m:::::987654321
( sleep-v 3.2m; echo; )  0.07s user 0.03s system 0% cpu 3:12.10 total
hayasaka@darkao%
```
