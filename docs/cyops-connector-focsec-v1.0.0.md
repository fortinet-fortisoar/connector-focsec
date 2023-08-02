## About the connector
Focsec help to real-time threat intelligence API, powered by proprietary Artificial Intelligence algorithms,for detecting VPNs,Proxys,Bots, and TOR requests,enabling prompt identification of suspicious logins,fraud, and abuse.
<p>This document provides information about the Focsec Connector, which facilitates automated interactions, with a Focsec server using FortiSOAR&trade; playbooks. Add the Focsec Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Focsec.</p>

### Version information

Connector Version: 1.0.0


Authored By: spryIQ.co

Certified: No
## Installing the connector
<p>From FortiSOAR&trade; 5.0.0 onwards, use the <strong>Connector Store</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.<br>You can also use the following <code>yum</code> command as a root user to install connectors from an SSH session:</p>
`yum install cyops-connector-focsec`

## Prerequisites to configuring the connector
- You must have the URL of Focsec server to which you will connect and perform automated operations and credentials to access that server.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Focsec server.

## Minimum Permissions Required
- N/A

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Focsec</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations&nbsp;</strong> tab enter the required configuration details:&nbsp;</p>
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>Server URL<br></td><td>Specify the URL of the focsec server to connect and perform automated operations.<br>
<tr><td>API key<br></td><td>Specify the API key to access the endpoint to which you will connect and perform the automated operations.<br>
</tbody></table>

## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function<br></th><th>Description<br></th><th>Annotation and Category<br></th></tr></thead><tbody><tr><td>Get IP Details<br></td><td>Retrieves a list of IP indicators from focsec.<br></td><td>get_ip_details <br/>Investigation<br></td></tr>
</tbody></table>

### operation: Get IP Details
#### Input parameters
<table border=1><thead><tr><th>Parameter<br></th><th>Description<br></th></tr></thead><tbody><tr><td>IP Address<br></td><td>Specify the IP address whose you want to retrieve from focsec.<br>
</td></tr></tbody></table>

#### Output
The output contains the following populated JSON schema:
<code><br>{
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "ip": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_vpn": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_proxy": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_bot": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_tor": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_datacenter": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "city": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "country": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "iso_code": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "is_in_european_union": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "flag": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "autonomous_system_number": "",
</code><code><br>&nbsp;&nbsp;&nbsp;&nbsp;    "autonomous_system_organization": ""
</code><code><br>}</code>
## Included playbooks
The `Sample - focsec - 1.0.0` playbook collection comes bundled with the Focsec connector. These playbooks contain steps using which you can perform all supported actions. You can see bundled playbooks in the **Automation** > **Playbooks** section in FortiSOAR<sup>TM</sup> after importing the Focsec connector.

- Get IP Details

**Note**: If you are planning to use any of the sample playbooks in your environment, ensure that you clone those playbooks and move them to a different collection, since the sample playbook collection gets deleted during connector upgrade and delete.
