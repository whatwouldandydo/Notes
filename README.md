# Introduction

I enjoy creating tools to automate manual tasks related to my interest in networks, systems, and finance.

## Network Tools

    Network Tools > BGP View
    Please select an option.
    0 - Quit
    1 - Retrieve Autonomous System Number (ASN) Information
    2 - Retrieve Internet Exchange (IX) Information
    3 - Retrieve IPv4/IPv6 Prefix Information
    Option: 1

    Enter AS Number: 1234
    ********************************************************************************
    Retrieving AS1234's Information...
    ********************************************************************************
    ASN: 1234
    Name: Fortum
    Location: EU

    IPv4 & IPv6 PREFIXES
    ['1> 132.171.0.0/16', '2> 137.96.0.0/16', '3> 193.110.32.0/21']

    PEER AS : NAME : COUNTRY
    ['1> AS1759 : Telia Finland Oyj : FI', '2> AS719 : Helsinki, Finland : FI']

    UPSTREAM AS : NAME : COUNTRY
    ['1> AS1759 : Telia Finland Oyj : FI', '2> AS719 : Helsinki, Finland : FI']

    DOWNSTREAM AS : NAME : COUNTRY
    'No Data'

    IX-ID : NAME : COUNTRY : SPEED
    'No Data'

    Option: 2

    Enter Internet Exchange Number: 60
    ********************************************************************************
    Retrieving IX-60's Information...
    ********************************************************************************
    IX: 60
    Name: Singapore Open Exchange
    City, Country: Singapore, SG
    AS Members Count: 17

    ASN : NAME : COUNTRY : SPEED
    ['1> AS38181 : Institute of Molecular and Cell Biology, Lifescience : SG : '
    '1000',
    '2> AS15169 : Google LLC : US : 20000',
    '3> AS4844 : SuperInternet ACCESS Pte Ltd : SG : 1000',
    '4> AS55818 : MC-IX Matrix Internet Exchange RS-1 : ID : 1000',
    '5> AS7575 : Australian Academic and Research Network (AARNet) : AU : 1000',
    '6> AS8075 : Microsoft Corporation : US : 20000',
    '7> AS703 : Verizon Business : US : 1000',
    '8> AS26163 : Datagram, Inc. : US : 10000',
    '9> AS7610 : NUS Gigapop : SG : 10000',
    '10> AS9877 : Ngee Ann Polytechnic Computer Center : SG : 1000',
    '11> AS4775 : Globe Telecoms : PH : 1000',
    '12> AS6939 : Hurricane Electric LLC : US : 10000',
    '13> AS23711 : Internet Systems Consortium, Inc. : SG : 1000',
    '14> AS23711 : Internet Systems Consortium, Inc. : SG : 1000',
    '15> AS131475 : Singapore Institute of Technology : SG : 1000',
    '16> AS45133 : Singapore Polytechnic : SG : 1000',
    '17> AS16509 : Amazon.com, Inc. : US : 20000',
    '18> AS23855 : Singapore Advanced Research and Education Network : SG : 1000',
    '19> AS16509 : Amazon.com, Inc. : US : 20000']

    Option: 3

    Enter IPv4/IPv6 Subnet: 216.228.224.0/23
    ********************************************************************************
    Retrieving Prefix 216.228.224.0/23's Information...
    ********************************************************************************
    Prefix: 216.228.224.0/23
    Name: Morningstar, Inc.
    Country: US
    AS Number: AS400537

## System Tools

    Systems Tools > TCP Buffer
    Please select an option.
    0 - Quit
    1 - Run System TCP Buffer Tuning
    Option: 1


        ==========================================================================
        | WARNING: This works only on Linux, UNIX, and AIX systems. Run command  |
        | below so you have a backup to restore the system to its original state.|
        |                                                                        |
        | sudo sysctl -a | egrep "[wr]mem" | egrep "core|tcp"                    |
        |                                                                        |
        ==========================================================================
        
    Enter Network Speed in Mbit/second: 45
    Enter Network Latency in Millisecond: 22

    ********************************************************************************
    Recommended window size 123750 for 45.0 Mbps with 22.0 ms latency.
    Commands to change system window sizes.
    <No Change> means do not modify this value.

    Line 1> sudo sysctl -w net.ipv4.tcp_wmem="<No Change> <No Change> 123750"
    Line 2> sudo sysctl -w net.core.wmem_max=495000
    Line 3> sudo sysctl -w net.ipv4.tcp_wmem="<No Change> <No Change> 123750"
    Line 4> sudo sysctl -w net.core.wmem_max=495000