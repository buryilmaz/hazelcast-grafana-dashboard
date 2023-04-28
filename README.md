# hazelcast-grafana-dashboard
Shows Hazelcast Community, Hazelcast JVM and usage metrics

PROMETHEUS_PORT

The port of the JMX Prometheus agent. For example, if you set PROMETHEUS_PORT=8080, then you can access metrics at: http://<hostname>:8080/metrics. You can also use PROMETHEUS_CONFIG to set a path to the custom configuration.

docker env:

 -e PROMETHEUS_PORT=8080
 
 -p 8080:8080 
 

prometheus.yaml:

- job_name: 'hazelcast'

scrape_interval: 10s

static_configs:

- targets: ['IP_ADRESS:8080']
 
