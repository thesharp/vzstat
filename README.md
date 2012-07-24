vzstat
======

Description
-----------
**vzstat** is a little ``vzlist`` enhancer for vSwap-enabled OpenVZ kernels. It
shows the RAM usage in a human-readable way and makes a summary on your RAM/CPU
overcommitment. And it's just so damn easy to type ``vzstat`` instead of
``vzlist -o ctid,hostname,physpages.l,[skipped]``. :)

Dependencies
------------
- python 2.6 (I believe, it will work on 2.4, but hey...)
- vSwap-enabled OpenVZ kernel (2.6.32+, RHEL6 branch)
- vzlist (it comes with vzctl package)

Usage
-----
Just run it. If you will pass ``-a`` as an argument it adds stopped containers
to the output.

Bugs
----
- Please report.
