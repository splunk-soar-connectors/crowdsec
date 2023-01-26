<div id="doc">

# CrowdSec

Publisher: CrowdSec  
Contributors: N/A  
App Version: 5.2.0  
Product Vendor: CrowdSec  
Product Name: CrowdSec  
Product Version Supported (regex): ".*"  

CrowdSec

<html> <head></head> <body>Replace this text in the app's **readme.html** to contain more detailed information</body> </html> <style>tr.plain th { text-align: center; }</style>

### Configuration Variables

The below configuration variables are required for this App to operate on **CrowdSec**. These are specified when configuring an asset in Splunk SOAR.

<table>

<tbody>

<tr class="plain">

<th style="padding-right:5px;">VARIABLE</th>

<th style="padding-right:5px;">REQUIRED</th>

<th style="padding-right:5px;">TYPE</th>

<th>DESCRIPTION</th>

</tr>

<tr>

<td>**CROWDSEC_CTI_API_KEY**</td>

<td>required</td>

<td>string</td>

<td>API key for CrowdSec CTI API</td>

</tr>

</tbody>

</table>

### Supported Actions

[<span class="link">lookup ip</span>](#) - Check for the presence of an IP in a threat intelligence feed  
[<span class="link">test connectivity</span>](#) - Validate the asset configuration for connectivity using supplied configuration  

<a id="lookup-ip"></a>

## action: 'lookup ip'

Check for the presence of an IP in a threat intelligence feed

Type: **investigate**

Read only: **True**

### Action Parameters

<table>

<tbody>

<tr class="plain">

<th style="padding-right:5px;">PARAMETER</th>

<th style="padding-right:5px;">REQUIRED</th>

<th style="padding-right:5px;">DESCRIPTION</th>

<th style="padding-right:5px;">TYPE</th>

<th>CONTAINS</th>

</tr>

<tr>

<td>**ip**</td>

<td>required</td>

<td>IP to lookup</td>

<td>string</td>

<td><span class="highlight">ip</span></td>

</tr>

</tbody>

</table>

### Action Output

<table>

<tbody>

<tr class="plain">

<th>DATA PATH</th>

<th>TYPE</th>

<th>CONTAINS</th>

<th>EXAMPLE VALUES</th>

</tr>

<tr>

<td>action_result.parameter.ip</td>

<td>string</td>

<td><span class="highlight">ip</span></td>

<td></td>

</tr>

<tr>

<td>action_result.status</td>

<td>string</td>

<td></td>

<td></td>

</tr>

<tr>

<td>action_result.message</td>

<td>string</td>

<td></td>

<td></td>

</tr>

<tr>

<td>action_result.data.*.location.country</td>

<td>string</td>

<td></td>

<td></td>

</tr>

<tr>

<td>action_result.data.*.attack_details.*.name</td>

<td>string</td>

<td></td>

<td></td>

</tr>

<tr>

<td>summary.total_objects</td>

<td>numeric</td>

<td></td>

<td></td>

</tr>

<tr>

<td>summary.total_objects_successful</td>

<td>numeric</td>

<td></td>

<td></td>

</tr>

</tbody>

</table>

<a id="test-connectivity"></a>

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test**

Read only: **True**

### Action Parameters

No parameters are required for this action

### Action Output

No Output

</div>
