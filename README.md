# ![LOGO](logo.png) MonitorManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the MonitorManagementClient API (version 2018-01-01).

Generated from: https://api.apis.guru/v2/specs/azure.com/monitor-metrics_API/2018-01-01/swagger.json<br/>
Generated at: 2019-05-07T17:38:28+03:00

## API Description



## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### **Lists the metric values for a resource**.

*Tags:* `Metrics`

#### Input Parameters
* `resourceUri` - _required_ - The identifier of the resource.
* `timespan` - _optional_ - The timespan of the query. It is a string with the following format 'startDateTime_ISO/endDateTime_ISO'.
* `interval` - _optional_ - The interval (i.e. timegrain) of the query.
* `metricnames` - _optional_ - The names of the metrics (comma separated) to retrieve.
* `aggregation` - _optional_ - The list of aggregation types (comma separated) to retrieve.
* `top` - _optional_ - The maximum number of records to retrieve.
Valid only if $filter is specified.
Defaults to 10.
* `orderby` - _optional_ - The aggregation to use for sorting results and the direction of the sort.
Only one order can be specified.
Examples: sum asc.
* `$filter` - _optional_ - The **$filter** is used to reduce the set of metric data returned.<br>Example:<br>Metric contains metadata A, B and C.<br>- Return all time series of C where A = a1 and B = b1 or b2<br>**$filter=A eq 'a1' and B eq 'b1' or B eq 'b2' and C eq '*'**<br>- Invalid variant:<br>**$filter=A eq 'a1' and B eq 'b1' and C eq '*' or B = 'b2'**<br>This is invalid because the logical or operator cannot separate two different metadata names.<br>- Return all time series where A = a1, B = b1 and C = c1:<br>**$filter=A eq 'a1' and B eq 'b1' and C eq 'c1'**<br>- Return all time series where A = a1<br>**$filter=A eq 'a1' and B eq '*' and C eq '*'**.
* `resultType` - _optional_ - Reduces the set of data collected. The syntax allowed depends on the operation. See the operation's description for details.
    Possible values: Data, Metadata.
* `api-version` - _required_ - Client Api Version.
* `metricnamespace` - _optional_ - Metric namespace to query metric definitions for.

## License

**flow**ground :- Telekom iPaaS / azure-com-monitor-metrics-api-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
