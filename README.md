# Introduction

I enjoy creating tools to automate manual tasks related to my interest in engineering and finance.

Below are the sample outputs of the tool that I built in my spare time.

## 1. Network Tools
#### Autonomous Systems, Internet Exchanges, and IP Subnet/Prefixes Information
##### Storyline: I don't want to search multiple websites for the information.


    Please select an option.
    0 - Exit
    1 - Network
    2 - System
    3 - Telecommunication
    4 - Finance
    Option: 1

    Network Tools > BGP View
    Please select an option.
    0 - Quit
    1 - Retrieve Autonomous System Number (ASN) Information
    2 - Retrieve Internet Exchange (IX) Information
    3 - Retrieve IPv4/IPv6 Prefix Information
    Option: 1

    Enter AS Number: 7610
    ********************************************************************************
    Retrieving AS7610's Information...
    ********************************************************************************
    ASN: 7610
    Name: NUS Gigapop
    Location: SG

    IPv4 & IPv6 PREFIXES
    ['1> 202.51.240.0/21', '2> 2402:400::/32']

    PEER AS : NAME : COUNTRY
    ['1> AS7575 : Australian Academic and Research Network (AARNet) : AU',
    '2> AS6939 : Hurricane Electric LLC : US',
    '3> AS23855 : Singapore Advanced Research and Education Network : SG',
    '4> AS4637 : Telstra Global : HK',
    '5> AS3758 : SingNet : SG',
    '6> AS7472 : NUS Information Technology : SG']

    UPSTREAM AS : NAME : COUNTRY
    ['1> AS3758 : SingNet : SG', '2> AS4637 : Telstra Global : HK']

    DOWNSTREAM AS : NAME : COUNTRY
    ['1> AS3758 : SingNet : SG', '2> AS4637 : Telstra Global : HK']

    IX-ID : NAME : COUNTRY : SPEED
    ['1> IX-IX-60 : Singapore Open Exchange : SG : 10000',
    '2> IX-IX-210 : Singapore Internet Exchange : SG : 10000']

    ################################################################################
    2 - Retrieve Internet Exchange (IX) Information
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

    ################################################################################
    3 - Retrieve IPv4/IPv6 Prefix Information
    Option: 3

    Enter IPv4/IPv6 Subnet: 216.228.224.0/23
    ********************************************************************************
    Retrieving Prefix 216.228.224.0/23's Information...
    ********************************************************************************
    Prefix: 216.228.224.0/23
    Name: Morningstar, Inc.
    Country: US
    AS Number: AS400537

## 2. System Tools
#### Calculate and Change System Buffer Settings
##### Storyline: The network got blamed too many times for slow file transfer.

    Please select an option.
    0 - Exit
    1 - Network
    2 - System
    3 - Telecommunication
    4 - Finance
    Option: 2
    
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

## 3. Telecommunication Tools
#### Phone Number Lookup
##### Storyline: I received too many texts from “beautiful ladies” and "investors." Andy can offer crypto investments too.

    Please select an option.
    0 - Exit
    1 - Network
    2 - System
    3 - Telecommunication
    4 - Finance
    Option: 3
    
    Telecommunication > Phone Number Lookup
    Please select an option.
    0 - Quit
    1 - Run Phone Number Lookup
    Option: 1

    Enter Phone Number (Example: 14158586273): 14087406382
    ********************************************************************************
    Internation Code: +1
    Local Format: 4087406382
    Country: United States of America
    Location: Saratoga
    Carrier Name:
    Line Type: landline
    ********************************************************************************

![Andy offers crypto investments](/images/20240424_005044000_iOS.png)