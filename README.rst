ThreatBook\_API Resource Storage SDK for Python
===============================================

1 Introduction
--------------

This release provides access to the corresponding functionality through
both public API\_KEY and private API\_KEY.

The public API\_KEY can access the file detection function of the cloud
sandbox. You need to register for a ThreatBook online account and view
your API Key through the Personal Center, which will be used for all
your API operations without submitting via the web, uploading the
file/URL for analysis and extracting the completed analysis. Report
data. The ThreatBook Online Sandbox API is a free service available for
free websites and programs. Please do not use the API for any commercial
product or service, as an alternative to an anti-virus product, or for
any project that may directly or indirectly damage the anti-virus
industry.

The private API\_KEY provides an easy way to invoke data from the Threat
Analytics Platform database and its detection and analysis capabilities
from any client. It includes the following functions: file digital
signature identification, new registered domain query, email
registration information query, domain analysis, IOC detection, IP
analysis, IP reputation query, etc. As our business customer or partner,
we will deliver your corresponding apikey by mail.

2 Installation
--------------

| ``$ pip install threatbook_API``

| Once you have successfully installed the package, you can use it by

importing it. The following example shows how to get the current whois
information for a domain:

::

    from threatbook_API.domain_analysis_query import DomainAnalysis

    # create an instance object
    test = DomainAnalysis('your private api_key')

    # Get the current whois information of the domain
    info = test.get_cur_whois('domain to be queried  ')
    print(info)

3 Features
----------

1. Structure
~~~~~~~~~~~~

::

    .
    ├── LICENSE
    ├── MANIFEST.in
    ├── README.rst
    ├── setup.py
    └── threatbook_api
        ├── domain_analysis_query.py
        ├── email_analysis_query.py
        ├── file_analysis_query.py
        ├── ioc_query.py
        ├── ip_analysis_query.py
        ├── ip_reputation_query.py
        └── example
            ├── get_all_fields.py
            ├── get_one_field.py
            └── get_some_fields.py

2. Function
~~~~~~~~~~~

-  domain\_analysis\_query.py: This module provides the IP address
   corresponding to the domain name, the IP address related geographical
   location information, the current Whois information, the threat type,
   the related attack gang or security event information.
-  email\_analysis\_query.py:This module provides a list of domain names
   registered with an email based on email. See the documentation for
   details.
-  file\_analysis\_query.py:This module provides the following features:
    1 Upload the file you want to analyze.
    2 Get a detailed report or a specified report of the uploaded file.
    3 Get the digital signature information of the file.
-  ioc\_query.py:This module provides a judgment based on the domain
   name or IP whether it has threat information such as C2.
-  ip\_analysis\_query.py:This module provides geographic location
   information related to IP addresses, bound domain name information,
   threat types, related attack gangs or security event information, and
   so on.
-  ip\_reputation\_query.py:This module provides real-time access to IP
   information and portrait information based on IP, and obtains basic
   IP attribute information such as IDC host, dynamic IP, downtime, VPN,
   proxy IP, and so on.
-  example:Some examples for easier use.

For more detailed information, please see the corresponding
documentation for each module.

4 Problem Description
---------------------

This SDK uses the python 3.x version by default. If you need to use
python 2.x version, Chinese may not display the problem properly. To
solve this problem, please refer to this link:

::

    https://blog.csdn.net/qq_42281053/article/details/80702852.

5 Code License
--------------

The MIT License (MIT).
