# vzstat

## Description
**vzstat** is a little ``vzlist`` enhancer for vSwap-enabled OpenVZ kernels. It shows the RAM usage
in a human-readable way and makes a summary on your RAM/CPU overcommitment.

## Sample output
    CTID     HOSTNAME                      USED   / TOTAL          LOADAVG     CPUS   CPUUNITS
    1001     [xxxxxx.ru                ]      371 / 1024 MB    0.22/0.27/0.27     0       1000
    1002     [xxxxxxxx.ru              ]      570 / 2048 MB    0.35/0.47/0.50     1        600
    1003     [xxxxxxxxxxxxxxxxxxxx.ru  ]     2638 / 3072 MB    5.71/7.41/8.36     0     166666
    1005     [xxxxxxxxxxxxx            ]      421 / 1024 MB    0.26/0.22/0.14     0       1000
    1006     [xxxxxxxxxxxx             ]      264 / 2561 MB    0.14/0.17/0.11     0     250000
    1007     [xxxxxxxxxxxxx.com        ]       30 / 4096 MB    0.00/0.00/0.00     4        600
    1009     [xxxxxxxxxxx              ]       70 / 4003 MB    0.00/0.00/0.00     0     166666
    1010     [xxxxxxxxxxxxxxxxxxxxx    ]       32 /  512 MB    0.00/0.00/0.00     0         99
    1012     [xxxxxxxxxx               ]     4541 / 5120 MB    2.12/2.12/2.34     0     166666
    1013     [xxxxxxxxxxxxxx           ]      227 / 1536 MB    0.00/0.00/0.00     0     166666
    1014     [xxxxxxxxxx               ]      970 / 2048 MB    0.44/0.50/0.48     1        600
    1015     [(stopped) None           ]        0 / 1024 MB              None     0     133308
    1016     [(stopped) None           ]        0 / 1024 MB              None     0     133308
    1018     [(stopped) None           ]        0 / 1024 MB              None     0     133308
    1019     [xxxxxxxxxx               ]      696 / 1024 MB    0.00/0.00/0.00     0     166666
    1021     [xxxxxxxxxxxxxxx          ]     1022 / 1024 MB    1.82/1.58/0.90     0       1000
    1024     [xxxxxx                   ]      158 / 1536 MB    0.00/0.00/0.00     0       1000
    1025     [xxxxxxxxxxxxxxxxxxxxx.ru ]     5980 / 6144 MB    0.62/0.62/0.56     0       1000
    1026     [xxxxxxxxx                ]      261 /  512 MB    0.10/0.16/0.13     0        500
    1039     [xxxxxxxxxxxxxxxxxxx      ]     3114 / 4096 MB    0.18/0.27/0.24     0       1000
    1066     [xxxxxxxxxxxxxxxxxxxxxx   ]     3587 / 4096 MB    0.48/0.66/0.79     0       1000

    Node loadavg: 13.09/13.14/13.72
    Allocated cores: 6 / 12
    Allocated memory: 48548 / 48172 MB (overcommitment: 376 MB)

## Installation on RHEL6 boxes
- [Enable Vortex RPM repository](http://vortex-rpm.org) (``yum install -y http://vortex-rpm.org/el6/noarch/vortex-release-6-1.vortex.el6.noarch.rpm``)
- ``yum install vzstat``

## Dependencies
- Python 2.6
- vSwap-enabled OpenVZ kernel (2.6.32+, RHEL6 branch)
- vzlist (comes with vzctl package)

## Usage
Simply run it. If you will pass ``-a`` as an argument, all containers (including stopped ones) will be shown.
