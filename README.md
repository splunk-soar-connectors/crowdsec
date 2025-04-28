# CrowdSec

Publisher: CrowdSec \
Connector Version: 1.0.2 \
Product Vendor: CrowdSec \
Product Name: CrowdSec \
Minimum Product Version: 5.5.0

Splunk SOAR App which integrates with CrowdSec. It provides the ability to lookup an IP address in CrowdSec's threat intelligence feed

### Configuration variables

This table lists the configuration variables required to operate CrowdSec. These variables are specified when configuring a CrowdSec asset in Splunk SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**CROWDSEC_CTI_API_KEY** | required | string | API key for CrowdSec CTI API |

### Supported Actions

[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration \
[lookup ip](#action-lookup-ip) - Check for the presence of an IP in a threat intelligence feed

## action: 'test connectivity'

Validate the asset configuration for connectivity using supplied configuration

Type: **test** \
Read only: **True**

#### Action Parameters

No parameters are required for this action

#### Action Output

No Output

## action: 'lookup ip'

Check for the presence of an IP in a threat intelligence feed

Type: **investigate** \
Read only: **True**

#### Action Parameters

PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** | required | IP to lookup | string | `ip` |

#### Action Output

DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.status | string | | success failed |
action_result.parameter.ip | string | `ip` | |
action_result.data.\*.as_name | string | | |
action_result.data.\*.as_num | string | | |
action_result.data.\*.background_noise_score | string | | |
action_result.data.\*.behaviors.\*.description | string | | |
action_result.data.\*.behaviors.\*.label | string | | |
action_result.data.\*.behaviors.\*.name | string | | |
action_result.data.\*.history.days_age | string | | |
action_result.data.\*.history.first_seen | string | | |
action_result.data.\*.history.full_age | string | | |
action_result.data.\*.history.last_seen | string | | |
action_result.data.\*.ip | string | | |
action_result.data.\*.ip_range | string | | |
action_result.data.\*.ip_range_score | string | | |
action_result.data.\*.location.city | string | | |
action_result.data.\*.location.country | string | | |
action_result.data.\*.location.latitude | string | | |
action_result.data.\*.location.longitude | string | | |
action_result.data.\*.reverse_dns | string | | |
action_result.data.\*.scores.last_day.aggressiveness | numeric | | |
action_result.data.\*.scores.last_day.anomaly | numeric | | |
action_result.data.\*.scores.last_day.threat | numeric | | |
action_result.data.\*.scores.last_day.total | numeric | | |
action_result.data.\*.scores.last_day.trust | numeric | | |
action_result.data.\*.scores.last_month.aggressiveness | numeric | | |
action_result.data.\*.scores.last_month.threat | numeric | | |
action_result.data.\*.scores.last_week.aggressiveness | numeric | | |
action_result.data.\*.scores.overall.aggressiveness | numeric | | |
action_result.data.\*.scores.overall.anomaly | numeric | | |
action_result.data.\*.scores.overall.threat | numeric | | |
action_result.data.\*.scores.overall.total | numeric | | |
action_result.data.\*.scores.overall.trust | numeric | | |
action_result.summary | string | | |
action_result.message | string | | |
summary.total_objects | numeric | | |
summary.total_objects_successful | numeric | | |

______________________________________________________________________

Auto-generated Splunk SOAR Connector documentation.

Copyright 2025 Splunk Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and limitations under the License.
