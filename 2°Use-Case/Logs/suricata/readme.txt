Within this folder we reported all the gathered logs from suricata.
They presents both the rules, that can be specified by the administrator, and the logs related to the requests monitored. In particular we configured suricata to print all the details of the http requests.
Within the ``curl.json`` are presented the request and the relative response of a curl.
The other files were preliminary tests with different configuration of the ``suricata.yaml`` file, that we left as archive.

The ``iptables-rules`` file represents the rules used to perform the routing within one of the SF in the chain. Starting from this file and considering the interfaces, reported within the ``Templates`` folder in the ``setup-terminal`` files, is possible to recreate the traffic flow.
