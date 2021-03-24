# Zabbix Cassandra Templates

## Overview
For Zabbix version: 4.4

## Requirements
Jolokia

## Zabbix configuration

No specific Zabbix configuration is required.

### Macros used

|Name|Description|Default|
|----|-----------|-------|
| {$CASSANDRA_JOLOKIA_PORT} |<p>Maximum percentage of used connections</p> |`8888 ` |
| {$CASSANDRA_PHIVALUE_HIGH} |<p>Maximum value for high trigger</p> |`20` |
| {$CASSANDRA_PHIVALUE_DISASTER} |<p>Maximum value for high trigger"</p> |`50` |
## Template links

There are no template links in this template.

## Discovery rules

|Name|Description|Type|Key and additional info|
|----|-----------|----|----|
| Cassandra: Cache Count Discovery | <p>Collect Cache Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Cache,*/Count",,,^{.*}$] |
| Cassandra: Cache Value Discovery | <p>Collect Cache Value metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Cache,*/Value",,,^{.*}$] |
| Cassandra: ClientRequest Count Discovery | <p>Collect ClientRequest Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ClientRequest,*/Count",,,^{.*}$] |
| Cassandra: ClientRequest FifteenMinuteRate Discovery | <p>Collect ClientRequest FifteenMinuteRate metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ClientRequest,*/FifteenMinuteRate",,,^{.*}$] |
| Cassandra: ClientRequest Mean Discovery | <p>Collect ClientRequest Mean metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ClientRequest,*/Mean",,,^{.*}$] |
| Cassandra: ColumnFamily Count Discovery | <p>Collect  ColumnFamily Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ColumnFamily,*/Count",,,^{.*}$] |
| Cassandra: ColumnFamily Value Discovery | <p>Collect ColumnFamily Value metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ColumnFamily,*/Value",,,^{.*}$] |
| Cassandra: Compaction Count Discovery | <p>Collect Compaction Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Compaction,*/Count",,,^{.*}$] |
| Cassandra: Compaction OneMinuteRate Discovery | <p>Collect Compaction OneMinuteRate metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Compaction,*/OneMinuteRate",,,^{.*}$] |
| Cassandra: Compaction Value Discovery | <p>Collect Compaction Value metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Compaction,*/Value",,,^{.*}$] |
| Cassandra: Connection Count Discovery | <p>Collect Connection Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Connection,*/Count",,,^{.*}$] |
| Cassandra: CQL Count Discovery | <p>Collect CQL Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=CQL,*/Count",,,^{.*}$] |
| Cassandra: DroppedMessage Discovery | <p>Collect DroppedMessage metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=DroppedMessage,name=Dropped,*",,,^{.*}$]	 |
| Cassandra: FailureDetector Discovery | <p>Collect FailureDetector metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.net:type=FailureDetector/PhiValues",,,^{.*}$] |
| Cassandra: GarbageCollector Discovery | <p>Collect GarbageCollector metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/java.lang:type=GarbageCollector,*/CollectionTime",,,^{.*}$] |
| Cassandra: Keyspace Count Discovery | <p>Collect Keyspace Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Keyspace,*/Count",,,^{.*}$] |
| Cassandra: Keyspace Value Discovery | <p>Collect Keyspace Value metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Keyspace,*/Value",,,^{.*}$] |
| Cassandra: Memory Discovery | <p>Collect Memory metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/java.lang:type=Memory,*",,,^{.*}$] |
| Cassandra: ReadRepair Discovery | <p>Collect ReadRepair metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ReadRepair,*",,,^{.*}$] |
| Cassandra: Storage Discovery | <p>Collect Storage metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=Storage,*",,,^{.*}$] |
| Cassandra: ThreadPools Count Discovery | <p>Collect ThreadPools Count metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ThreadPools,*/Count",,,^{.*}$] |
| Cassandra: ThreadPools Value Discovery | <p>Collect ThreadPools Value metrics.</p> | ZABBIX_ACTIVE | web.page.regexp["http://localhost:{$CASSANDRA_JOLOKIA_PORT}/jolokia/read/org.apache.cassandra.metrics:type=ThreadPools,*/Value",,,^{.*}$] |

