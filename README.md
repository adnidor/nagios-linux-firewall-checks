# nagios-linux-firewall-checks

A handful of useful Nagios checks for firewalls and routers.

Requirements: python 2.7 or python-argparse

## check_bird

<pre>
usage: check_bird [-h] [--control-socket CONTROL_SOCKET]
                  {interfaces,bfd,ospf,bgp}

Check various aspects of a running BIRD daemon (interface states, several
routing protocols) by interrogating the daemon via its control socket.
Intended to be run from nagios. Michael Fincham
&lt;michael.fincham@catalyst.net.nz&gt;.

positional arguments:
  {interfaces,bfd,ospf,bgp}
                        which check to run

optional arguments:
  -h, --help            show this help message and exit
  --control-socket CONTROL_SOCKET
                        location of BIRD control socket, defaults to
                        /run/bird/bird.ctl
</pre>

## check_conntrack

<pre>
usage: check_conntrack [-h] [--warning PERCENT] [--critical PERCENT]

Compare the number of entries in the netfilter conntrack table to the maximum
number permitted. Return warning and critical states for nagios at
configurable thresholds. Michael Fincham
&lt;michael.fincham@catalyst.net.nz&gt;.

optional arguments:
  -h, --help          show this help message and exit
  --warning PERCENT   percentage threshold for warning state, defaults to 50
  --critical PERCENT  percentage threshold for critical state, defaults to 75
</pre>

## check_neighbour_tables

<pre>
usage: check_neighbour_tables [-h] [--warning PERCENT] [--critical PERCENT]

Compare the number of entries in the ARP and NDISC caches to the maximum
number permitted by the garbage collector. Return warning and critical states
for nagios at configurable thresholds. Michael Fincham
&lt;michael.fincham@catalyst.net.nz&gt;.

optional arguments:
  -h, --help          show this help message and exit
  --warning PERCENT   percentage threshold for warning state, defaults to 50
  --critical PERCENT  percentage threshold for critical state, defaults to 75
</pre>
