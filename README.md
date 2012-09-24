nagios-plugins
==============

Miscellaneous Nagios plugins.

check_minecraft
---------------

Plugin for checking availability, response time and number of players on a Minecraft server.

The plugin queries the server by sending a 0xFE Server List Ping packet. The server is not required to have enable-query or enable-rcon enabled.

    usage: check_minecraft.py [-h] -H ADDRESS [-p INTEGER] [-n INTEGER]
                              [-m STRING] [-f] [-w DOUBLE] [-c DOUBLE] [-t DOUBLE]
                              [-v]
    
    optional arguments:
        -h, --help      show this help message and exit
        -H ADDRESS, --hostname ADDRESS
                        host name or IP address
        -p INTEGER, --port INTEGER
                        port number (default: 25565)
        -n INTEGER, --number-of-checks INTEGER
                        number of checks to get stable average response time
                        (default: 5)
        -m STRING, --motd STRING
                        expected motd in server response (default: A Minecraft
                        Server)
        -f, --warn-on-full
                        generate warning if server is full
        -w DOUBLE, --warning DOUBLE
                        response time to result in warning status (seconds)
        -c DOUBLE, --critical DOUBLE
                        response time to result in critical status (seconds)
        -t DOUBLE, --timeout DOUBLE
                        seconds before connection times out (default: 10)
        -v, --verbose   show details for command-line debugging (Nagios may
                        truncate output)

License
=======

Plugins released under the MIT license:

* http://www.opensource.org/licenses/MIT
