# CA Certificate Store for CFMS clients

This code repository is a certificate store used to host trusted root CA 
and intermediate CA certificates. By adding certificates from these 
repositories to `verify_locations`, clients will be able to trust certificates 
issued by developers of CFMS.

As a system administrator, it can be useful to fork the repository at the same 
time when you are trying to fork a proprietary version of the client for your 
organization, because this allows you to control which sources of certificates 
the proprietary client can trust, while excluding others.

Additionally, clients can be configured to accept Certificate Revocation Lists 
(CRLs) in PEM format, provided they follow a specific naming format when 
joining this repository. 

## Naming Convention

The `c_rehash` tool provided by OpenSSL can be used to quickly generate certificate 
files that meet the naming requirements. However, if the aforementioned tools are 
not available on your platform, the same effect can be achieved manually. 

For more information, please refer to OpenSSL's naming conventions on this topic.

## CONTRIBUTION

For security reasons, this code repository is unlikely to accept certificate 
addition requests from outside sources. For system administrators, maintaining 
a proprietary certificate store is likely a better practice.