<pre><code>
!Command: show running-config
!Running configuration last done at: Sat Jan  9 19:34:14 2021
!Time: Sat Jan  9 19:38:49 2021

version 9.2(2) Bios:version  
hostname a-nxos-sp1
vdc a-nxos-sp1 id 1
  limit-resource vlan minimum 16 maximum 4094
  limit-resource vrf minimum 2 maximum 4096
  limit-resource port-channel minimum 0 maximum 511
  limit-resource u4route-mem minimum 248 maximum 248
  limit-resource u6route-mem minimum 96 maximum 96
  limit-resource m4route-mem minimum 58 maximum 58
  limit-resource m6route-mem minimum 8 maximum 8

feature ospf
feature isis
feature bfd

no password strength-check
username admin password 5 $5$h3YGHkM.$/bOUMJv7dJQHVGV1ibyTXc52oD3qy64HIeTie9QN/35  role network-admin
ip domain-lookup
copp profile strict
snmp-server user admin network-admin auth md5 0x77f2063bdc1123059c9aa923936b8a24 priv 0x77f2063bdc1123059c9aa923936b8a24 localizedkey
rmon event 1 description FATAL(1) owner PMON@FATAL
rmon event 2 description CRITICAL(2) owner PMON@CRITICAL
rmon event 3 description ERROR(3) owner PMON@ERROR
rmon event 4 description WARNING(4) owner PMON@WARNING
rmon event 5 description INFORMATION(5) owner PMON@INFO

vlan 1

vrf context management

interface Ethernet1/1
  no switchport
  duplex full
  no ip redirects
  ip address 10.77.1.13/30
  isis network point-to-point
  isis circuit-type level-2
  ip router isis 1
  no shutdown

interface Ethernet1/2
  no switchport
  no ip redirects
  ip address 10.77.1.1/30
  isis network point-to-point
  isis circuit-type level-1
  ip router isis 1
  no shutdown

interface Ethernet1/3
  no switchport
  no ip redirects
  ip address 10.77.1.5/30
  isis network point-to-point
  isis circuit-type level-1
  ip router isis 1
  no shutdown

interface Ethernet1/4
  no switchport
  no ip redirects
  ip address 10.77.1.9/30
  isis network point-to-point
  isis circuit-type level-1
  ip router isis 1
  no shutdown

interface Ethernet1/5

interface Ethernet1/6

interface Ethernet1/7

interface Ethernet1/8

interface Ethernet1/9

interface Ethernet1/10

interface Ethernet1/11

interface Ethernet1/12

interface Ethernet1/13

interface Ethernet1/14

interface Ethernet1/15

interface Ethernet1/16

interface Ethernet1/17

interface Ethernet1/18

interface Ethernet1/19

interface Ethernet1/20

interface Ethernet1/21

interface Ethernet1/22

interface Ethernet1/23

interface Ethernet1/24

interface Ethernet1/25

interface Ethernet1/26

interface Ethernet1/27

interface Ethernet1/28

interface Ethernet1/29

interface Ethernet1/30

interface Ethernet1/31

interface Ethernet1/32

interface Ethernet1/33

interface Ethernet1/34

interface Ethernet1/35

interface Ethernet1/36

interface Ethernet1/37

interface Ethernet1/38

interface Ethernet1/39

interface Ethernet1/40

interface Ethernet1/41

interface Ethernet1/42

interface Ethernet1/43

interface Ethernet1/44

interface Ethernet1/45

interface Ethernet1/46

interface Ethernet1/47

interface Ethernet1/48

interface Ethernet1/49

interface Ethernet1/50

interface Ethernet1/51

interface Ethernet1/52

interface Ethernet1/53

interface Ethernet1/54

interface Ethernet1/55

interface Ethernet1/56

interface Ethernet1/57

interface Ethernet1/58

interface Ethernet1/59

interface Ethernet1/60

interface Ethernet1/61

interface Ethernet1/62

interface Ethernet1/63

interface Ethernet1/64

interface Ethernet1/65

interface Ethernet1/66

interface Ethernet1/67

interface Ethernet1/68

interface Ethernet1/69

interface Ethernet1/70

interface Ethernet1/71

interface Ethernet1/72

interface Ethernet1/73

interface Ethernet1/74

interface Ethernet1/75

interface Ethernet1/76

interface Ethernet1/77

interface Ethernet1/78

interface Ethernet1/79

interface Ethernet1/80

interface Ethernet1/81

interface Ethernet1/82

interface Ethernet1/83

interface Ethernet1/84

interface Ethernet1/85

interface Ethernet1/86

interface Ethernet1/87

interface Ethernet1/88

interface Ethernet1/89

interface Ethernet1/90

interface Ethernet1/91

interface Ethernet1/92

interface Ethernet1/93

interface Ethernet1/94

interface Ethernet1/95

interface Ethernet1/96

interface Ethernet1/97

interface Ethernet1/98

interface Ethernet1/99

interface Ethernet1/100

interface Ethernet1/101

interface Ethernet1/102

interface Ethernet1/103

interface Ethernet1/104

interface Ethernet1/105

interface Ethernet1/106

interface Ethernet1/107

interface Ethernet1/108

interface Ethernet1/109

interface Ethernet1/110

interface Ethernet1/111

interface Ethernet1/112

interface Ethernet1/113

interface Ethernet1/114

interface Ethernet1/115

interface Ethernet1/116

interface Ethernet1/117

interface Ethernet1/118

interface Ethernet1/119

interface Ethernet1/120

interface Ethernet1/121

interface Ethernet1/122

interface Ethernet1/123

interface Ethernet1/124

interface Ethernet1/125

interface Ethernet1/126

interface Ethernet1/127

interface Ethernet1/128

interface mgmt0
  vrf member management

interface loopback1
  ip address 10.77.255.1/32
line console
line vty
boot nxos bootflash:/nxos.9.2.2.bin 
router isis 1
  net 49.0001.0000.0001.0001.00
  address-family ipv4 unicast
    distribute level-1 into level-2 all
    advertise interface loopback1


</code></pre>