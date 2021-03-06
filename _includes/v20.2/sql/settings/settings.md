<table>
<thead><tr><th>Setting</th><th>Type</th><th>Default</th><th>Description</th></tr></thead>
<tbody>
<tr><td><code>cloudstorage.gs.default.key</code></td><td>string</td><td><code></code></td><td>if set, JSON key to use during Google Cloud Storage operations</td></tr>
<tr><td><code>cloudstorage.http.custom_ca</code></td><td>string</td><td><code></code></td><td>custom root CA (appended to system's default CAs) for verifying certificates when interacting with HTTPS storage</td></tr>
<tr><td><code>cloudstorage.timeout</code></td><td>duration</td><td><code>10m0s</code></td><td>the timeout for import/export storage operations</td></tr>
<tr><td><code>cluster.organization</code></td><td>string</td><td><code></code></td><td>organization name</td></tr>
<tr><td><code>cluster.preserve_downgrade_option</code></td><td>string</td><td><code></code></td><td>disable (automatic or manual) cluster version upgrade from the specified version until reset</td></tr>
<tr><td><code>diagnostics.forced_sql_stat_reset.interval</code></td><td>duration</td><td><code>2h0m0s</code></td><td>interval after which SQL statement statistics are refreshed even if not collected (should be more than diagnostics.sql_stat_reset.interval). It has a max value of 24H.</td></tr>
<tr><td><code>diagnostics.reporting.enabled</code></td><td>boolean</td><td><code>true</code></td><td>enable reporting diagnostic metrics to cockroach labs</td></tr>
<tr><td><code>diagnostics.reporting.interval</code></td><td>duration</td><td><code>1h0m0s</code></td><td>interval at which diagnostics data should be reported</td></tr>
<tr><td><code>diagnostics.sql_stat_reset.interval</code></td><td>duration</td><td><code>1h0m0s</code></td><td>interval controlling how often SQL statement statistics should be reset (should be less than diagnostics.forced_sql_stat_reset.interval). It has a max value of 24H.</td></tr>
<tr><td><code>enterprise.license</code></td><td>string</td><td><code></code></td><td>the encoded cluster license</td></tr>
<tr><td><code>external.graphite.endpoint</code></td><td>string</td><td><code></code></td><td>if nonempty, push server metrics to the Graphite or Carbon server at the specified host:port</td></tr>
<tr><td><code>external.graphite.interval</code></td><td>duration</td><td><code>10s</code></td><td>the interval at which metrics are pushed to Graphite (if enabled)</td></tr>
<tr><td><code>jobs.retention_time</code></td><td>duration</td><td><code>336h0m0s</code></td><td>the amount of time to retain records for completed jobs before</td></tr>
<tr><td><code>kv.allocator.load_based_lease_rebalancing.enabled</code></td><td>boolean</td><td><code>true</code></td><td>set to enable rebalancing of range leases based on load and latency</td></tr>
<tr><td><code>kv.allocator.load_based_rebalancing</code></td><td>enumeration</td><td><code>leases and replicas</code></td><td>whether to rebalance based on the distribution of QPS across stores [off = 0, leases = 1, leases and replicas = 2]</td></tr>
<tr><td><code>kv.allocator.qps_rebalance_threshold</code></td><td>float</td><td><code>0.25</code></td><td>minimum fraction away from the mean a store's QPS (such as queries per second) can be before it is considered overfull or underfull</td></tr>
<tr><td><code>kv.allocator.range_rebalance_threshold</code></td><td>float</td><td><code>0.05</code></td><td>minimum fraction away from the mean a store's range count can be before it is considered overfull or underfull</td></tr>
<tr><td><code>kv.bulk_io_write.max_rate</code></td><td>byte size</td><td><code>1.0 TiB</code></td><td>the rate limit (bytes/sec) to use for writes to disk on behalf of bulk io ops</td></tr>
<tr><td><code>kv.closed_timestamp.follower_reads_enabled</code></td><td>boolean</td><td><code>true</code></td><td>allow (all) replicas to serve consistent historical reads based on closed timestamp information</td></tr>
<tr><td><code>kv.protectedts.reconciliation.interval</code></td><td>duration</td><td><code>5m0s</code></td><td>the frequency for reconciling jobs with protected timestamp records</td></tr>
<tr><td><code>kv.range_split.by_load_enabled</code></td><td>boolean</td><td><code>true</code></td><td>allow automatic splits of ranges based on where load is concentrated</td></tr>
<tr><td><code>kv.range_split.load_qps_threshold</code></td><td>integer</td><td><code>2500</code></td><td>the QPS over which, the range becomes a candidate for load based splitting</td></tr>
<tr><td><code>kv.rangefeed.enabled</code></td><td>boolean</td><td><code>false</code></td><td>if set, rangefeed registration is enabled</td></tr>
<tr><td><code>kv.replication_reports.interval</code></td><td>duration</td><td><code>1m0s</code></td><td>the frequency for generating the replication_constraint_stats, replication_stats_report and replication_critical_localities reports (set to 0 to disable)</td></tr>
<tr><td><code>kv.snapshot_rebalance.max_rate</code></td><td>byte size</td><td><code>8.0 MiB</code></td><td>the rate limit (bytes/sec) to use for rebalance and upreplication snapshots</td></tr>
<tr><td><code>kv.snapshot_recovery.max_rate</code></td><td>byte size</td><td><code>8.0 MiB</code></td><td>the rate limit (bytes/sec) to use for recovery snapshots</td></tr>
<tr><td><code>kv.transaction.max_intents_bytes</code></td><td>integer</td><td><code>262144</code></td><td>maximum number of bytes used to track locks in transactions</td></tr>
<tr><td><code>kv.transaction.max_refresh_spans_bytes</code></td><td>integer</td><td><code>256000</code></td><td>maximum number of bytes used to track refresh spans in serializable transactions</td></tr>
<tr><td><code>server.auth_log.sql_connections.enabled</code></td><td>boolean</td><td><code>false</code></td><td>if set, log SQL client connect and disconnect events (note: may hinder performance on loaded nodes)</td></tr>
<tr><td><code>server.auth_log.sql_sessions.enabled</code></td><td>boolean</td><td><code>false</code></td><td>if set, log SQL session login/disconnection events (note: may hinder performance on loaded nodes)</td></tr>
<tr><td><code>server.clock.forward_jump_check_enabled</code></td><td>boolean</td><td><code>false</code></td><td>if enabled, forward clock jumps > max_offset/2 will cause a panic</td></tr>
<tr><td><code>server.clock.persist_upper_bound_interval</code></td><td>duration</td><td><code>0s</code></td><td>the interval between persisting the wall time upper bound of the clock. The clock does not generate a wall time greater than the persisted timestamp and will panic if it sees a wall time greater than this value. When cockroach starts, it waits for the wall time to catch-up till this persisted timestamp. This guarantees monotonic wall time across server restarts. Not setting this or setting a value of 0 disables this feature.</td></tr>
<tr><td><code>server.consistency_check.max_rate</code></td><td>byte size</td><td><code>8.0 MiB</code></td><td>the rate limit (bytes/sec) to use for consistency checks; used in conjunction with server.consistency_check.interval to control the frequency of consistency checks. Note that setting this too high can negatively impact performance.</td></tr>
<tr><td><code>server.eventlog.ttl</code></td><td>duration</td><td><code>2160h0m0s</code></td><td>if nonzero, event log entries older than this duration are deleted every 10m0s. Should not be lowered below 24 hours.</td></tr>
<tr><td><code>server.host_based_authentication.configuration</code></td><td>string</td><td><code></code></td><td>host-based authentication configuration to use during connection authentication</td></tr>
<tr><td><code>server.rangelog.ttl</code></td><td>duration</td><td><code>720h0m0s</code></td><td>if nonzero, range log entries older than this duration are deleted every 10m0s. Should not be lowered below 24 hours.</td></tr>
<tr><td><code>server.remote_debugging.mode</code></td><td>string</td><td><code>local</code></td><td>set to enable remote debugging, localhost-only or disable (any, local, off)</td></tr>
<tr><td><code>server.shutdown.drain_wait</code></td><td>duration</td><td><code>0s</code></td><td>the amount of time a server waits in an unready state before proceeding with the rest of the shutdown process</td></tr>
<tr><td><code>server.shutdown.lease_transfer_wait</code></td><td>duration</td><td><code>5s</code></td><td>the amount of time a server waits to transfer range leases before proceeding with the rest of the shutdown process</td></tr>
<tr><td><code>server.shutdown.query_wait</code></td><td>duration</td><td><code>10s</code></td><td>the server will wait for at least this amount of time for active queries to finish</td></tr>
<tr><td><code>server.time_until_store_dead</code></td><td>duration</td><td><code>5m0s</code></td><td>the time after which if there is no new gossiped information about a store, it is considered dead</td></tr>
<tr><td><code>server.user_login.timeout</code></td><td>duration</td><td><code>10s</code></td><td>timeout after which client authentication times out if some system range is unavailable (0 = no timeout)</td></tr>
<tr><td><code>server.web_session_timeout</code></td><td>duration</td><td><code>168h0m0s</code></td><td>the duration that a newly created web session will be valid</td></tr>
<tr><td><code>sql.defaults.default_int_size</code></td><td>integer</td><td><code>8</code></td><td>the size, in bytes, of an INT type</td></tr>
<tr><td><code>sql.defaults.results_buffer.size</code></td><td>byte size</td><td><code>16 KiB</code></td><td>default size of the buffer that accumulates results for a statement or a batch of statements before they are sent to the client. This can be overridden on an individual connection with the 'results_buffer_size' parameter. Note that auto-retries generally only happen while no results have been delivered to the client, so reducing this size can increase the number of retriable errors a client receives. On the other hand, increasing the buffer size can increase the delay until the client receives the first result row. Updating the setting only affects new connections. Setting to 0 disables any buffering.</td></tr>
<tr><td><code>sql.defaults.serial_normalization</code></td><td>enumeration</td><td><code>rowid</code></td><td>default handling of SERIAL in table definitions [rowid = 0, virtual_sequence = 1, sql_sequence = 2]</td></tr>
<tr><td><code>sql.distsql.max_running_flows</code></td><td>integer</td><td><code>500</code></td><td>maximum number of concurrent flows that can be run on a node</td></tr>
<tr><td><code>sql.log.slow_query.latency_threshold</code></td><td>duration</td><td><code>0s</code></td><td>when set to non-zero, log statements whose service latency exceeds the threshold to a secondary logger on each node</td></tr>
<tr><td><code>sql.metrics.statement_details.dump_to_logs</code></td><td>boolean</td><td><code>false</code></td><td>dump collected statement statistics to node logs when periodically cleared</td></tr>
<tr><td><code>sql.metrics.statement_details.enabled</code></td><td>boolean</td><td><code>true</code></td><td>collect per-statement query statistics</td></tr>
<tr><td><code>sql.metrics.statement_details.plan_collection.enabled</code></td><td>boolean</td><td><code>true</code></td><td>periodically save a logical plan for each fingerprint</td></tr>
<tr><td><code>sql.metrics.statement_details.plan_collection.period</code></td><td>duration</td><td><code>5m0s</code></td><td>the time until a new logical plan is collected</td></tr>
<tr><td><code>sql.metrics.statement_details.threshold</code></td><td>duration</td><td><code>0s</code></td><td>minimum execution time to cause statistics to be collected</td></tr>
<tr><td><code>sql.metrics.transaction_details.enabled</code></td><td>boolean</td><td><code>true</code></td><td>collect per-application transaction statistics</td></tr>
<tr><td><code>sql.notices.enabled</code></td><td>boolean</td><td><code>true</code></td><td>enable notices in the server/client protocol being sent</td></tr>
<tr><td><code>sql.stats.automatic_collection.enabled</code></td><td>boolean</td><td><code>true</code></td><td>automatic statistics collection mode</td></tr>
<tr><td><code>sql.stats.automatic_collection.fraction_stale_rows</code></td><td>float</td><td><code>0.2</code></td><td>target fraction of stale rows per table that will trigger a statistics refresh</td></tr>
<tr><td><code>sql.stats.automatic_collection.min_stale_rows</code></td><td>integer</td><td><code>500</code></td><td>target minimum number of stale rows per table that will trigger a statistics refresh</td></tr>
<tr><td><code>sql.stats.histogram_collection.enabled</code></td><td>boolean</td><td><code>true</code></td><td>histogram collection mode</td></tr>
<tr><td><code>sql.stats.multi_column_collection.enabled</code></td><td>boolean</td><td><code>true</code></td><td>multi-column statistics collection mode</td></tr>
<tr><td><code>sql.stats.post_events.enabled</code></td><td>boolean</td><td><code>false</code></td><td>if set, an event is logged for every CREATE STATISTICS job</td></tr>
<tr><td><code>sql.temp_object_cleaner.cleanup_interval</code></td><td>duration</td><td><code>30m0s</code></td><td>how often to clean up orphaned temporary objects</td></tr>
<tr><td><code>sql.trace.log_statement_execute</code></td><td>boolean</td><td><code>false</code></td><td>set to true to enable logging of executed statements</td></tr>
<tr><td><code>sql.trace.session_eventlog.enabled</code></td><td>boolean</td><td><code>false</code></td><td>set to true to enable session tracing. Note that enabling this may have a non-trivial negative performance impact.</td></tr>
<tr><td><code>sql.trace.txn.enable_threshold</code></td><td>duration</td><td><code>0s</code></td><td>duration beyond which all transactions are traced (set to 0 to disable)</td></tr>
<tr><td><code>timeseries.storage.enabled</code></td><td>boolean</td><td><code>true</code></td><td>if set, periodic timeseries data is stored within the cluster; disabling is not recommended unless you are storing the data elsewhere</td></tr>
<tr><td><code>timeseries.storage.resolution_10s.ttl</code></td><td>duration</td><td><code>240h0m0s</code></td><td>the maximum age of time series data stored at the 10 second resolution. Data older than this is subject to rollup and deletion.</td></tr>
<tr><td><code>timeseries.storage.resolution_30m.ttl</code></td><td>duration</td><td><code>2160h0m0s</code></td><td>the maximum age of time series data stored at the 30 minute resolution. Data older than this is subject to deletion.</td></tr>
<tr><td><code>trace.debug.enable</code></td><td>boolean</td><td><code>false</code></td><td>if set, traces for recent requests can be seen in the /debug page</td></tr>
<tr><td><code>trace.lightstep.token</code></td><td>string</td><td><code></code></td><td>if set, traces go to Lightstep using this token</td></tr>
<tr><td><code>trace.zipkin.collector</code></td><td>string</td><td><code></code></td><td>if set, traces go to the given Zipkin instance (example: '127.0.0.1:9411'); ignored if trace.lightstep.token is set</td></tr>
<tr><td><code>version</code></td><td>custom validation</td><td><code>20.1-13</code></td><td>set the active cluster version in the format '<major>.<minor>'</td></tr>
</tbody>
</table>
