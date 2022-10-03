# 03: Assessment

## Finding information with whois

**Finding information with whois:**

1. Returns WHOIS data about Syddansk Universitet:

```
$ whois sdu.dk

# Hello 89.150.138.143. Your session has been logged.
#
# Copyright (c) 2002 - 2022 by DK Hostmaster A/S
#
# Version: 5.0.2
#
# The data in the DK Whois database is provided by DK Hostmaster A/S
# for information purposes only, and to assist persons in obtaining
# information about or related to a domain name registration record.
# We do not guarantee its accuracy. We will reserve the right to remove
# access for entities abusing the data, without notice.
#
# Any use of this material to target advertising or similar activities
# are explicitly forbidden and will be prosecuted. DK Hostmaster A/S
# requests to be notified of any such activities or suspicions thereof.

Domain:               sdu.dk
DNS:                  sdu.dk
Registered:           1997-10-09
Expires:              2023-12-31
Registration period:  5 years
VID:                  no
DNSSEC:               Signed delegation
Status:               Active

Registrant
Handle:               ***N/A***
Name:                 Syddansk Universitet (University of Southern Denmark)
Address:              Campusvej 55
Postalcode:           5230
City:                 Odense M
Country:              DK

Nameservers
Hostname:             ns1.sdu.dk
Hostname:             ns2.sdu.dk
Hostname:             ns3.sdu.dk
```

2. Returns WHOIS data about the ISP:

```
$ dig a +short www.sdu.dk
89.188.87.235

$ whois 89.188.87.235
% This is the RIPE Database query service.
% The objects are in RPSL format.
%
% The RIPE Database is subject to Terms and Conditions.
% See http://www.ripe.net/db/support/db-terms-conditions.pdf

% Note: this output has been filtered.
%       To receive output for a database update, use the "-B" flag.

% Information related to '89.188.80.0 - 89.188.87.255'

% Abuse contact for '89.188.80.0 - 89.188.87.255' is 'abuse@sentia.dk'

inetnum:        89.188.80.0 - 89.188.87.255
netname:        VENZOHOSTING-PRIMARYDATACENTER
descr:          VENZOHOSTING-PRIMARYDATACENTER
country:        DK
admin-c:        venz
tech-c:         venz
status:         ASSIGNED PA
mnt-by:         VENZO-MNT
mnt-lower:      VENZO-MNT
mnt-domains:    VENZO-MNT
created:        2012-09-19T11:12:55Z
last-modified:  2013-07-16T08:09:16Z
source:         RIPE

person:         Hosters AS NIC-Support
address:        Helsingforsgade 25
address:        8200 Aarhus N
phone:          +45 70200160
nic-hdl:        venz
mnt-by:         VENZO-MNT
created:        2012-08-03T07:51:06Z
last-modified:  2018-04-23T09:25:01Z
source:         RIPE # Filtered

% Information related to '89.188.80.0/20AS199213'

route:          89.188.80.0/20
origin:         AS199213
mnt-by:         JAYNET
created:        2022-03-02T14:20:51Z
last-modified:  2022-03-02T14:20:51Z
source:         RIPE

% Information related to '89.188.80.0/20AS47292'

route:          89.188.80.0/20
origin:         AS47292
mnt-by:         JAYNET
created:        2022-03-02T14:30:42Z
last-modified:  2022-03-02T14:30:42Z
source:         RIPE

% This query was served by the RIPE Database Query Service version 1.103 (BLAARKOP)

```