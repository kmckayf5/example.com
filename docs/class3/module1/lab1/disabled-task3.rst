LTM - VLAN's
=====================

Create the WAF vlan on each LTM

.. note::  **It is required to complete the following task on bigip1.site1 and bigip2.site1**

Navigate to: **Network  ››  VLANs : VLAN List**

Create a new vlan according to the following table.

.. csv-table::
   :header: "Setting", "Value"
   :widths: 15, 15

   "Name", "site1_waf_vlan"
   "Tag", "50"
   "Interface", "1.7 - Untagged"

https://bigip1.site1.example.com/tmui/Control/jspmap/tmui/locallb/network/vlan/create.jsp

https://bigip2.site1.example.com/tmui/Control/jspmap/tmui/locallb/network/vlan/create.jsp

TMSH command for both bigip1.site1 and bigip2.site1:

.. admonition:: TMSH

  tmsh create net vlan site1_waf_vlan { interfaces add { 1.7 { } } tag 50 }

.. note::  **It is required to complete the following task on both bigip1.site2 bigip2.site2**

Navigate to: **Network  ››  VLANs : VLAN List**

Create a new vlan according to the following table.

.. csv-table::
   :header: "Setting", "Value"
   :widths: 15, 15

   "Name", "site2_waf_vlan"
   "Tag", "60"
   "Interface", "1.7 - Untagged"

https://bigip1.site2.example.com/tmui/Control/jspmap/tmui/locallb/network/vlan/create.jsp

https://bigip2.site2.example.com/tmui/Control/jspmap/tmui/locallb/network/vlan/create.jsp

TMSH command for both bigip1.site2 and bigip2.site2:

.. admonition:: TMSH

  tmsh create net vlan site2_waf_vlan { interfaces add { 1.7 { } } tag 60 }

