# veego-stack

![Version: 0.0.2](https://img.shields.io/badge/Version-0.0.2-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.16.0](https://img.shields.io/badge/AppVersion-1.16.0-informational?style=flat-square)

A Helm chart for Kubernetes

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| file://../agent-disconnect-detector | agent-disconnect-detector | 0.X.X |
| file://../agent-event-hooks-handler | agent-event-hooks-handler | 0.X.X |
| file://../agent-registration-handler | agent-registration-handler | 0.X.X |
| file://../agent-statistics-handler | agent-statistics-handler | 0.X.X |
| file://../agents-dispatcher | agents-dispatcher | 0.X.X |
| file://../aggregated-telemetry-handler | aggregated-telemetry-handler | 0.X.X |
| file://../aggregation-ignitor | aggregation-ignitor | 0.X.X |
| file://../api-gateway | api-gateway | 0.X.X |
| file://../charter-veego-agents-handler | charter-veego-agents-handler | 0.X.X |
| file://../command-result-handler | command-result-handler | 0.X.X |
| file://../command-topic-creator | command-topic-creator | 0.X.X |
| file://../cp-schema-registry | cp-schema-registry | 0.X.X |
| file://../device-collector | device-collector | 0.X.X |
| file://../device-uptime-handler | device-uptime-handler | 0.X.X |
| file://../doxi-veego-agents-disconnect-detector | doxi-veego-agents-disconnect-detector | 0.X.X |
| file://../doxi-veego-agents-handler | doxi-veego-agents-handler | 0.X.X |
| file://../doxi-veego-devices-handler | doxi-veego-devices-handler | 0.X.X |
| file://../doxi-veego-notifications-handler | doxi-veego-notifications-handler | 0.X.X |
| file://../doxi-veego-service-status-handler | doxi-veego-service-status-handler | 0.X.X |
| file://../doxi-veego-service-usages | doxi-veego-service-usages | 0.X.X |
| file://../doxi-veego-services-handler | doxi-veego-services-handler | 0.X.X |
| file://../doxi-veego-telemetry-aggregations | doxi-veego-telemetry-aggregations | 0.X.X |
| file://../global-service-by-type-data-collector | global-service-by-type-data-collector | 0.X.X |
| file://../global-service-by-type-score-handler | global-service-by-type-score-handler | 0.X.X |
| file://../home-score-devices-data-handler | home-score-devices-data-handler | 0.X.X |
| file://../home-score-handler | home-score-handler | 0.X.X |
| file://../login | login | 0.X.X |
| file://../malfunctions-counters-cleaner | malfunctions-counters-cleaner | 0.X.X |
| file://../mobile-api | mobile-api | 0.X.X |
| file://../monitor-connections | monitor-connections | 0.X.X |
| file://../notifications-handler | notifications-handler | 0.X.X |
| file://../notifications-telemetry-collector-ignitor | notifications-telemetry-collector-ignitor | 0.X.X |
| file://../notifications-telemetry-collector | notifications-telemetry-collector | 0.X.X |
| file://../probe-notifications-telemetry-handler | probe-notifications-telemetry-handler | 0.X.X |
| file://../probe-telemetry-handler | probe-telemetry-handler | 0.X.X |
| file://../services-name-resolver | services-name-resolver | 0.X.X |
| file://../speedtest-handler | speedtest-handler | 0.X.X |
| file://../telemetry-aggregator | telemetry-aggregator | 0.X.X |
| file://../telemetry-handler | telemetry-handler | 0.X.X |
| file://../wifi-global-malfunctions-statistics-builder | wifi-global-malfunctions-statistics-builder | 0.X.X |
| file://../wifi-malfunctions-counters-cleaner | wifi-malfunctions-counters-cleaner | 0.X.X |
| file://../wifi-malfunctions-data-collector | wifi-malfunctions-data-collector | 0.X.X |
| file://../wifi-score-handler | wifi-score-handler | 0.X.X |
| https://charts.bitnami.com/bitnami | oauth2-proxy | 2.0.1 |

## Chart Repo

Add the following repo to use the chart:

```console
helm repo add veego https://veegoteam.github.io/helm-charts-public
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| agent-disconnect-detector.configMap.AGENT_DISCONNECT_DETECTION_SCHEDULING | string | `"0 0/10 * * * ?"` |  |
| agent-disconnect-detector.configMap.AGENT_MAX_DISCONNECT_TIME_MILLIS | string | `"1209600000"` |  |
| agent-disconnect-detector.configMap.DOXI_SUPPORT | string | `"true"` |  |
| agent-disconnect-detector.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"agent-disconnect-detector-main"` |  |
| agent-disconnect-detector.extraConfigMap[0] | string | `"veego-stack"` |  |
| agent-disconnect-detector.extraSecret[0] | string | `"veego-stack"` |  |
| agent-disconnect-detector.image.repository | string | `"veego/agent-disconnect-detector"` |  |
| agent-disconnect-detector.image.tag | string | `"stage"` |  |
| agent-disconnect-detector.replicaCount | int | `1` |  |
| agent-event-hooks-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"agent-event-hooks-main"` |  |
| agent-event-hooks-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"agent_event_hooks"` |  |
| agent-event-hooks-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| agent-event-hooks-handler.extraSecret[0] | string | `"veego-stack"` |  |
| agent-event-hooks-handler.image.repository | string | `"veego/agent-event-hooks-handler"` |  |
| agent-event-hooks-handler.image.tag | string | `"stage"` |  |
| agent-event-hooks-handler.replicaCount | int | `1` |  |
| agent-registration-handler.configMap.VEEGO_KAFKA_COMMAND_TOPIC_CREATOR_TOPIC | string | `"command_topic_creator"` |  |
| agent-registration-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"agent-registration-main"` |  |
| agent-registration-handler.configMap.VEEGO_KAFKA_EVENT_HOOKS_TOPIC | string | `"agent_event_hooks"` |  |
| agent-registration-handler.configMap.VEEGO_KAFKA_NOTIFICATIONS_TOPIC | string | `"notifications"` |  |
| agent-registration-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"agent_registration"` |  |
| agent-registration-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| agent-registration-handler.extraSecret[0] | string | `"veego-stack"` |  |
| agent-registration-handler.image.repository | string | `"veego/agent-registration-handler"` |  |
| agent-registration-handler.image.tag | string | `"stage"` |  |
| agent-registration-handler.replicaCount | int | `1` |  |
| agent-statistics-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"agent-statistics-main"` |  |
| agent-statistics-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"statistics"` |  |
| agent-statistics-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| agent-statistics-handler.extraSecret[0] | string | `"veego-stack"` |  |
| agent-statistics-handler.image.repository | string | `"veego/agent-statistics-handler"` |  |
| agent-statistics-handler.image.tag | string | `"stage"` |  |
| agent-statistics-handler.replicaCount | int | `1` |  |
| agents-dispatcher.configMap.AGENTS_BLACK_LIST | string | `""` |  |
| agents-dispatcher.configMap.AGENT_CONFIG_FILE_PATH | string | `"/dispatcher/agent/agent.config.json"` |  |
| agents-dispatcher.configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| agents-dispatcher.configMap.KAFKA_BOOTSTRAP_SERVERS | string | `""` |  |
| agents-dispatcher.configMap.KAFKA_CONSUMER_GROUP_ID | string | `"agents_dispatcher"` |  |
| agents-dispatcher.configMap.KAFKA_CONSUME_TOPIC | string | `"raw_metrics"` |  |
| agents-dispatcher.configMap.REDIS_DATABASE | string | `"0"` |  |
| agents-dispatcher.configMap.SERVER_AGENT_BINARY_PATH | string | `"/dispatcher/agent/deviceagentrun"` |  |
| agents-dispatcher.extraConfigMap[0] | string | `"veego-stack"` |  |
| agents-dispatcher.extraSecret[0] | string | `"veego-stack"` |  |
| agents-dispatcher.image.repository | string | `"veego/agents-dispatcher"` |  |
| agents-dispatcher.image.tag | string | `"stage"` |  |
| agents-dispatcher.replicaCount | int | `1` |  |
| aggregated-telemetry-handler.configMap.IS_APP_NAME_ANONYMIZATION_ON | string | `"false"` |  |
| aggregated-telemetry-handler.configMap.VEEGO_KAFKA_AGGREGATOR_CONSUMER_GROUP_ID | string | `"aggregated-telemetry-aggregator;"` |  |
| aggregated-telemetry-handler.configMap.VEEGO_KAFKA_AGGREGATOR_TOPIC | string | `"aggregation_ignitor"` |  |
| aggregated-telemetry-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"aggregated-telemetry-handler-main"` |  |
| aggregated-telemetry-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry_aggregation"` |  |
| aggregated-telemetry-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| aggregated-telemetry-handler.extraSecret[0] | string | `"veego-stack"` |  |
| aggregated-telemetry-handler.image.repository | string | `"veego/aggregated-telemetry-handler"` |  |
| aggregated-telemetry-handler.image.tag | string | `"stage"` |  |
| aggregated-telemetry-handler.replicaCount | int | `1` |  |
| aggregation-ignitor.configMap.VEEGO_AGGREGATOR_TOPIC | string | `"aggregation_ignitor"` |  |
| aggregation-ignitor.extraConfigMap[0] | string | `"veego-stack"` |  |
| aggregation-ignitor.extraSecret[0] | string | `"veego-stack"` |  |
| aggregation-ignitor.image.repository | string | `"veego/aggregation-ignitor"` |  |
| aggregation-ignitor.image.tag | string | `"stage"` |  |
| aggregation-ignitor.replicaCount | int | `1` |  |
| api-gateway.configMap.QUICKSIGHT_ANALYTICS_DASHBOARD_ID | string | `"4528f4b2-8572-48d9-9b4c-39cb260a42ff"` |  |
| api-gateway.configMap.QUICKSIGHT_EXTENDER_DASHBOARD_ID | string | `"a19c43d3-5f95-4bbd-a2e6-97dde48aa3e1"` |  |
| api-gateway.configMap.QUICKSIGHT_GAMERS_DASHBOARD_ID | string | `"03361e8d-1dc9-439f-a6d9-ed9d8a4dc718"` |  |
| api-gateway.configMap.QUICKSIGHT_IOS_FANS_DASHBOARD_ID | string | `"f7b2d939-111d-43dd-b88f-bf9ada619a0d"` |  |
| api-gateway.configMap.QUICKSIGHT_MARKETING_DASHBOARD_ID | string | `"d55d71f0-afdd-4756-81c7-4755c1856c04"` |  |
| api-gateway.configMap.QUICKSIGHT_MY_EXPERIENCE_DASHBOARD_ID | string | `"fa1d6820-9b74-4813-8588-82cc4272850f"` |  |
| api-gateway.configMap.QUICKSIGHT_MY_HOME_DASHBOARD_ID | string | `"9ab49ef1-8a43-4210-bf03-adfd6b7233ae"` |  |
| api-gateway.configMap.QUICKSIGHT_MY_MALFUNCTIONS_DASHBOARD_ID | string | `"70db539c-735f-45f8-b161-c1024bd76c00"` |  |
| api-gateway.configMap.QUICKSIGHT_MY_SERVICES_DASHBOARD_ID | string | `"37ab9085-56d8-4bc6-b284-54d5962fb080"` |  |
| api-gateway.configMap.QUICKSIGHT_NEW_DEVICE_DASHBOARD_ID | string | `"8cdc7cc8-536b-4eea-b312-3cc3f6513785"` |  |
| api-gateway.configMap.QUICKSIGHT_NEW_EXTENDER_DASHBOARD_ID | string | `"9b675a48-6cd5-42c1-9b40-882a0bed23ad"` |  |
| api-gateway.configMap.QUICKSIGHT_NEW_ROUTER_DASHBOARD_ID | string | `"f8765825-346f-402c-813e-dd9dd0371c72"` |  |
| api-gateway.configMap.QUICKSIGHT_OVERVIEW_DASHBOARD_ID | string | `"ce7722e1-762c-4648-9103-81c3fadb99ec"` |  |
| api-gateway.configMap.QUICKSIGHT_SMART_HOME_DASHBOARD_ID | string | `"dc9d3a64-ed81-4858-97c7-7ebd53ec9dd2"` |  |
| api-gateway.configMap.QUICKSIGHT_STREAMING_SERVICE_DASHBOARD_ID | string | `"8a6e7077-7b0f-4312-a879-e434a95d9f60"` |  |
| api-gateway.configMap.QUICKSIGHT_SUFFERING_HOMES_DASHBOARD_ID | string | `"8bcb665b-5279-4caf-8492-516b35e4c7bc"` |  |
| api-gateway.configMap.QUICKSIGHT_UPGRADE_BROADBAND_PLAN_DASHBOARD_ID | string | `"7802bfd6-fbd1-4296-8617-8f96ba4d573a"` |  |
| api-gateway.configMap.QUICKSIGHT_UPGRADE_DEVICE_DASHBOARD_ID | string | `"ff61e9bc-222a-4dbd-8859-072f96e774fb"` |  |
| api-gateway.configMap.QUICKSIGHT_WFH_DASHBOARD_ID | string | `"04e89bdd-efbd-46ee-a157-f890a4852ee7"` |  |
| api-gateway.configMap.VEEGO_HIDE_SV02_RECOMMENDATION_FLAG_ON | string | `"true"` |  |
| api-gateway.configMap.VEEGO_SHOW_ANALYTICS | string | `"true"` |  |
| api-gateway.extraConfigMap[0] | string | `"veego-stack"` |  |
| api-gateway.extraSecret[0] | string | `"veego-stack"` |  |
| api-gateway.image.repository | string | `"veego/api-gateway"` |  |
| api-gateway.image.tag | string | `"stage"` |  |
| api-gateway.replicaCount | int | `1` |  |
| charter-veego-agents-handler.configMap.VEEGO_CHARTER_AGENTS_FOR_FILTERING | string | `"TZ2J8JPV1L9"` |  |
| charter-veego-agents-handler.configMap.VEEGO_KAFKA_CHARTER_VEEGO_AGENTS_TOPIC | string | `"charter-telemetry"` |  |
| charter-veego-agents-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"charter-handler-main2"` |  |
| charter-veego-agents-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| charter-veego-agents-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| charter-veego-agents-handler.extraSecret[0] | string | `"veego-stack"` |  |
| charter-veego-agents-handler.image.repository | string | `"veego/charter-veego-agents-handler"` |  |
| charter-veego-agents-handler.image.tag | string | `"stage"` |  |
| charter-veego-agents-handler.replicaCount | int | `1` |  |
| command-result-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"command-result-main"` |  |
| command-result-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"command_result"` |  |
| command-result-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| command-result-handler.extraSecret[0] | string | `"veego-stack"` |  |
| command-result-handler.image.repository | string | `"veego/command-result-handler"` |  |
| command-result-handler.image.tag | string | `"stage"` |  |
| command-result-handler.replicaCount | int | `1` |  |
| command-topic-creator.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"command-topic-creator-main"` |  |
| command-topic-creator.configMap.VEEGO_KAFKA_EVENT_HOOKS_TOPIC | string | `"agent_event_hooks"` |  |
| command-topic-creator.configMap.VEEGO_KAFKA_TOPIC | string | `"command_topic_creator"` |  |
| command-topic-creator.extraConfigMap[0] | string | `"veego-stack"` |  |
| command-topic-creator.extraSecret[0] | string | `"veego-stack"` |  |
| command-topic-creator.image.repository | string | `"veego/command-topic-creator"` |  |
| command-topic-creator.image.tag | string | `"stage"` |  |
| command-topic-creator.replicaCount | int | `1` |  |
| configMap.AWS_ACCOUNT_ID | string | `""` |  |
| configMap.AWS_REGION | string | `""` |  |
| configMap.LOGSTASH_HOST | string | `""` |  |
| configMap.VEEGO_KAFKA_HOSTS | string | `""` |  |
| configMap.VEEGO_KAFKA_SCHEMA_REGISTRY_URL | string | `""` |  |
| configMap.VEEGO_MONGO_DB_NAME | string | `""` |  |
| configMap.VEEGO_REDIS_HOSTS | string | `""` |  |
| configMap.VEEGO_SERVER_TIME_ZONE | string | `""` |  |
| configMap.VEEGO_SIGN_OUT_URL | string | `""` |  |
| configMap.VEEGO_SQL_URL | string | `""` |  |
| configMap.VEEGO_ZIPKIN_BASE_URL | string | `""` |  |
| cp-schema-registry.extraConfigMap[0] | string | `"veego-stack"` |  |
| cp-schema-registry.extraSecret[0] | string | `"veego-stack"` |  |
| cp-schema-registry.replicaCount | int | `1` |  |
| device-collector.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"device_collector"` |  |
| device-collector.configMap.VEEGO_KAFKA_TOPIC | string | `"device_collector"` |  |
| device-collector.extraConfigMap[0] | string | `"veego-stack"` |  |
| device-collector.extraSecret[0] | string | `"veego-stack"` |  |
| device-collector.image.repository | string | `"veego/device-collector"` |  |
| device-collector.image.tag | string | `"stage"` |  |
| device-collector.replicaCount | int | `1` |  |
| device-uptime-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"device-uptime-main"` |  |
| device-uptime-handler.configMap.VEEGO_KAFKA_NOTIFICATIONS_TOPIC | string | `"notifications"` |  |
| device-uptime-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| device-uptime-handler.extraSecret[0] | string | `"veego-stack"` |  |
| device-uptime-handler.image.repository | string | `"veego/device-uptime-handler"` |  |
| device-uptime-handler.image.tag | string | `"stage"` |  |
| device-uptime-handler.replicaCount | int | `1` |  |
| domain-json.extraConfigMap.BIND | string | `"[::]:80"` |  |
| domain-json.image.repository | string | `"veego/domain-json"` |  |
| domain-json.image.tag | string | `"stage"` |  |
| domain-json.replicaCount | int | `1` |  |
| doxi-veego-agents-disconnect-detector.configMap.AGENT_DISCONNECT_DETECTION_SCHEDULING | string | `"0 * * * * *"` |  |
| doxi-veego-agents-disconnect-detector.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-agents-disconnect-detector.configMap.VEEGO_KAFKA_DOXI_VEEGO_AGENTS_TOPIC | string | `"doxi_veego_agents"` |  |
| doxi-veego-agents-disconnect-detector.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-agents-disconnect-detector.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-agents-disconnect-detector.image.repository | string | `"veego/doxi-veego-agents-disconnect-detector"` |  |
| doxi-veego-agents-disconnect-detector.image.tag | string | `"stage"` |  |
| doxi-veego-agents-disconnect-detector.replicaCount | int | `1` |  |
| doxi-veego-agents-handler.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-agents-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi-veego-agents-handler"` |  |
| doxi-veego-agents-handler.configMap.VEEGO_KAFKA_DOXI_VEEGO_AGENTS_TOPIC | string | `"doxi_veego_agents"` |  |
| doxi-veego-agents-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"agent_registration"` |  |
| doxi-veego-agents-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-agents-handler.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-agents-handler.image.repository | string | `"veego/doxi-veego-agents-handler"` |  |
| doxi-veego-agents-handler.image.tag | string | `"stage"` |  |
| doxi-veego-agents-handler.replicaCount | int | `1` |  |
| doxi-veego-devices-handler.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-devices-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi-veego-devices-main"` |  |
| doxi-veego-devices-handler.configMap.VEEGO_KAFKA_DOXI_VEEGO_DEVICES_TOPIC | string | `"doxi_veego_devices"` |  |
| doxi-veego-devices-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications"` |  |
| doxi-veego-devices-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-devices-handler.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-devices-handler.image.repository | string | `"veego/doxi-veego-devices-handler"` |  |
| doxi-veego-devices-handler.image.tag | string | `"stage"` |  |
| doxi-veego-devices-handler.replicaCount | int | `1` |  |
| doxi-veego-notifications-handler.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-notifications-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi-veego-notifications-main"` |  |
| doxi-veego-notifications-handler.configMap.VEEGO_KAFKA_DOXI_VEEGO_NOTIFICATIONS_TOPIC | string | `"doxi_veego_notifications"` |  |
| doxi-veego-notifications-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications"` |  |
| doxi-veego-notifications-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-notifications-handler.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-notifications-handler.image.repository | string | `"veego/doxi-veego-notifications-handler"` |  |
| doxi-veego-notifications-handler.image.tag | string | `"stage"` |  |
| doxi-veego-notifications-handler.replicaCount | int | `1` |  |
| doxi-veego-service-status-handler.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-service-status-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi-veego-service-status-main"` |  |
| doxi-veego-service-status-handler.configMap.VEEGO_KAFKA_DOXI_VEEGO_SERVICES_TOPIC | string | `"doxi_veego_services"` |  |
| doxi-veego-service-status-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications"` |  |
| doxi-veego-service-status-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-service-status-handler.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-service-status-handler.image.repository | string | `"veego/doxi-veego-service-status-handler"` |  |
| doxi-veego-service-status-handler.image.tag | string | `"stage"` |  |
| doxi-veego-service-status-handler.replicaCount | int | `1` |  |
| doxi-veego-service-usages.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-service-usages.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi-veego-service-usages-main"` |  |
| doxi-veego-service-usages.configMap.VEEGO_KAFKA_DOXI_VEEGO_SERVICE_USAGES_TOPIC | string | `"doxi_veego_service_usages"` |  |
| doxi-veego-service-usages.configMap.VEEGO_KAFKA_TOPIC | string | `"aggregation_ignitor"` |  |
| doxi-veego-service-usages.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-service-usages.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-service-usages.image.repository | string | `"veego/doxi-veego-service-usages"` |  |
| doxi-veego-service-usages.image.tag | string | `"stage"` |  |
| doxi-veego-service-usages.replicaCount | int | `1` |  |
| doxi-veego-services-handler.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-services-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"doxi_veego_services-main"` |  |
| doxi-veego-services-handler.configMap.VEEGO_KAFKA_DOXI_VEEGO_SERVICES_TOPIC | string | `"doxi_veego_services"` |  |
| doxi-veego-services-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| doxi-veego-services-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-services-handler.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-services-handler.image.repository | string | `"veego/doxi-veego-services-handler"` |  |
| doxi-veego-services-handler.image.tag | string | `"stage"` |  |
| doxi-veego-services-handler.replicaCount | int | `1` |  |
| doxi-veego-telemetry-aggregations.configMap.VEEGO_AGENTS_FOR_FILTERING | string | `"6401T02599828,6401T02599831,64601T0000000,64601T0065342,64601T0065342,64601T0259834,64601T0259847,64601T0259870,64601T0259883,64601T0259885,64601T0259888,64601T0259894,64601T0259901,64601T0259903,64601T0259916,64601T0259919,64601T0259933,64601T0259941,64601T0259943,64601T0259943,64601T0259944,64601T0259945,64601T0259946,64601T0259947,64601T0259948,64601T0259950,64601T0259952,64601T0259954,64601T0259955,64601T0259958,64601T0259959,64601T0259962,64601T0259962,64601T0259963,64601T0259964,64601T0259967,64601T0259969,64601T0259973,64601T0259977,64601T0259978,64601T0259980,64601T0259981,64601T0259982,64601T0259984,64601T0259987,64601T0259990,64601T0259991,64601T0259992,64601T0259996,64601T0259997,64601T0259998,64601T0260000,64601T0260002,64601T0260003,64601T0260005,64601T0260006,64601T0260008,64601T0260010,64601T0260011,64601T0260021,64601T0260024,64601T0260025,64601T0260031,64601T0260031,64601T0260036,64601T0260038,64601T0260041,64601T0260042,64601T0260044,64601T0260044,64601T0260049,64601T0260052,64601T0260056,64601T0260062,64601T0260087,64601T0260095,64601T0260095,64601T0261536,64601T0261560,64601T0261614,64601T0261620,64601T0261799,64601T0261817,72601T0000060,72601T0000126,72601T0000126,72601T0000129,72601T0000129,72601T0000142,72601T0000149,72601T0000150,72601T0000150,72601T0000152,72601T0000156,72601T0000156,72601T0000158,72601T0000158,72601T0000165,72601T0000169,72601T0000176,72601T0000176,72601T0000177,72601T0000180,72601T0000208,72601T0000208,72601T0000209,72601T0000217,72601T0000236,72601T0000239,72601T0000317,72601T0000361,72601T0000362,72601T0000363"` |  |
| doxi-veego-telemetry-aggregations.configMap.VEEGO_KAFKA_DOXI_VEEGO_TELEMETRY_AGGREGATIONS_TOPIC | string | `"doxi_veego_telemetry_aggregations"` |  |
| doxi-veego-telemetry-aggregations.extraConfigMap[0] | string | `"veego-stack"` |  |
| doxi-veego-telemetry-aggregations.extraSecret[0] | string | `"veego-stack"` |  |
| doxi-veego-telemetry-aggregations.image.repository | string | `"veego/doxi-veego-telemetry-aggregations"` |  |
| doxi-veego-telemetry-aggregations.image.tag | string | `"stage"` |  |
| doxi-veego-telemetry-aggregations.replicaCount | int | `1` |  |
| global-service-by-type-data-collector.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"global-service-by-type-data-collector-main"` |  |
| global-service-by-type-data-collector.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| global-service-by-type-data-collector.extraConfigMap[0] | string | `"veego-stack"` |  |
| global-service-by-type-data-collector.extraSecret[0] | string | `"veego-stack"` |  |
| global-service-by-type-data-collector.image.repository | string | `"veego/global-service-by-type-data-collector"` |  |
| global-service-by-type-data-collector.image.tag | string | `"stage"` |  |
| global-service-by-type-data-collector.replicaCount | int | `1` |  |
| global-service-by-type-score-handler.configMap.GLOBAL_SERVICE_SCORE_SCHEDULING | string | `"0 0/5 * * * ?"` |  |
| global-service-by-type-score-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| global-service-by-type-score-handler.image.repository | string | `"veego/global-service-by-type-score-handler"` |  |
| global-service-by-type-score-handler.image.tag | string | `"stage"` |  |
| global-service-by-type-score-handler.replicaCount | int | `1` |  |
| global.imagePullSecrets | list | `[]` | imagePullSecrets Example --> imagePullSecrets: [ "secret" ] |
| global.pullPolicy | string | `"Always"` |  |
| global.registry | string | `"347694409649.dkr.ecr.us-west-2.amazonaws.com"` |  |
| home-score-devices-data-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"home-score-devices-data-handler"` |  |
| home-score-devices-data-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"aggregation_ignitor"` |  |
| home-score-devices-data-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| home-score-devices-data-handler.extraSecret[0] | string | `"veego-stack"` |  |
| home-score-devices-data-handler.image.repository | string | `"veego/home-score-devices-data-handler"` |  |
| home-score-devices-data-handler.image.tag | string | `"stage"` |  |
| home-score-devices-data-handler.replicaCount | int | `1` |  |
| home-score-handler.configMap.AGENT_HOME_SCORE_SCHEDULING | string | `"0 0 0 * * ?"` |  |
| home-score-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| home-score-handler.extraSecret[0] | string | `"veego-stack"` |  |
| home-score-handler.image.repository | string | `"veego/home-score-handler"` |  |
| home-score-handler.image.tag | string | `"stage"` |  |
| home-score-handler.replicaCount | int | `1` |  |
| kafka-websocket.image.repository | string | `"veego/kafka-websocket"` |  |
| kafka-websocket.image.tag | string | `"stage"` |  |
| kafka-websocket.replicaCount | int | `1` |  |
| login.extraConfigMap[0] | string | `"veego-stack"` |  |
| login.extraSecret[0] | string | `"veego-stack"` |  |
| login.image.repository | string | `"veego/login"` |  |
| login.image.tag | string | `"stage"` |  |
| login.replicaCount | int | `1` |  |
| malfunctions-counters-cleaner.configMap.AGENT_MALFUNCTIONS_CLEANER_SCHEDULING | string | `"0 0/10 * * * ?"` |  |
| malfunctions-counters-cleaner.extraConfigMap[0] | string | `"veego-stack"` |  |
| malfunctions-counters-cleaner.extraSecret[0] | string | `"veego-stack"` |  |
| malfunctions-counters-cleaner.image.repository | string | `"veego/malfunctions-counters-cleaner"` |  |
| malfunctions-counters-cleaner.image.tag | string | `"stage"` |  |
| malfunctions-counters-cleaner.replicaCount | int | `1` |  |
| mobile-api.configMap.VEEGO_CELLCOM_AGENT_PREFIX | string | `"C"` |  |
| mobile-api.configMap.VEEGO_CURRENT_ENV | string | `"S"` |  |
| mobile-api.configMap.VEEGO_DEV_AGENT_PREFIX | string | `"D"` |  |
| mobile-api.configMap.VEEGO_IGNORED_MAC_ADDRESSES | string | `"22:48:7c"` |  |
| mobile-api.configMap.VEEGO_JWT_EXPIRATION | string | `"360000000"` |  |
| mobile-api.configMap.VEEGO_LOGIN_URL_DEV | string | `""` |  |
| mobile-api.configMap.VEEGO_RAKUTEN_AGENT_PREFIX | string | `"R"` |  |
| mobile-api.configMap.VEEGO_SMTP_HOST | string | `"smtp.gmail.com"` |  |
| mobile-api.configMap.VEEGO_SMTP_REGISTRATION_SENDER | string | `""` |  |
| mobile-api.configMap.VEEGO_SMTP_REGISTRATION_SUBJECT | string | `""` |  |
| mobile-api.configMap.VEEGO_SMTP_SMTP_DEBUG | string | `"false"` |  |
| mobile-api.configMap.VEEGO_SMTP_SMTP_PORT | string | `"587"` |  |
| mobile-api.configMap.VEEGO_SMTP_USERNAME | string | `""` |  |
| mobile-api.configMap.VEEGO_STAGING_AGENT_PREFIX | string | `"S"` |  |
| mobile-api.extraConfigMap[0] | string | `"veego-stack"` |  |
| mobile-api.extraSecret[0] | string | `"veego-stack"` |  |
| mobile-api.image.repository | string | `"veego/mobile-api"` |  |
| mobile-api.image.tag | string | `"stage"` |  |
| mobile-api.replicaCount | int | `1` |  |
| mobile-api.secret.VEEGO_JWT_SECRET | string | `""` |  |
| mobile-api.secret.VEEGO_SMTP_PASSWORD | string | `""` |  |
| monitor-connections.configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| monitor-connections.configMap.INFLUX_AUTH_TOKEN | string | `""` |  |
| monitor-connections.configMap.INFLUX_SERVER | string | `"http://influxdb.default:8086"` |  |
| monitor-connections.configMap.KAFKA_CONNTRACK_TOPIC | string | `"conntrack"` |  |
| monitor-connections.configMap.KAFKA_CONSUMER_GROUP_ID | string | `"monitor_conntrack"` |  |
| monitor-connections.configMap.KAFKA_TELEMETRY_SERVICES_TOPIC | string | `"telemetry_services"` |  |
| monitor-connections.extraConfigMap[0] | string | `"veego-stack"` |  |
| monitor-connections.image.repository | string | `"veego/monitor-connections"` |  |
| monitor-connections.image.tag | string | `"stage"` |  |
| monitor-connections.replicaCount | int | `1` |  |
| notifications-handler.configMap.VEEGO_KAFKA_NOTIFICATIONS_CONSUMER_GROUP_ID | string | `"notifications-main"` |  |
| notifications-handler.configMap.VEEGO_KAFKA_NOTIFICATIONS_TOPIC | string | `"notifications"` |  |
| notifications-handler.configMap.VEEGO_KAFKA_SSL | string | `"false"` |  |
| notifications-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| notifications-handler.extraSecret[0] | string | `"veego-stack"` |  |
| notifications-handler.image.repository | string | `"veego/notifications-handler"` |  |
| notifications-handler.image.tag | string | `"stage"` |  |
| notifications-handler.replicaCount | int | `1` |  |
| notifications-telemetry-collector-ignitor.configMap.NOTIFICATIONS_TELEMETRY_DELAY_MIN | string | `"3"` |  |
| notifications-telemetry-collector-ignitor.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"notifications_telemetry_ignitor"` |  |
| notifications-telemetry-collector-ignitor.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications_telemetry_ignitor"` |  |
| notifications-telemetry-collector-ignitor.extraConfigMap[0] | string | `"veego-stack"` |  |
| notifications-telemetry-collector-ignitor.extraSecret[0] | string | `"veego-stack"` |  |
| notifications-telemetry-collector-ignitor.image.repository | string | `"veego/notifications-telemetry-collector-ignitor"` |  |
| notifications-telemetry-collector-ignitor.image.tag | string | `"stage"` |  |
| notifications-telemetry-collector-ignitor.replicaCount | int | `1` |  |
| notifications-telemetry-collector.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"notifications-telemetry-collector"` |  |
| notifications-telemetry-collector.configMap.VEEGO_KAFKA_PROBE_COLLECTOR_TOPIC | string | `"probe_telemetry_collector"` |  |
| notifications-telemetry-collector.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications_telemetry_ignitor"` |  |
| notifications-telemetry-collector.configMap.VEEGO_TELEMETRY_SEND_TO_PROBE | string | `"true"` |  |
| notifications-telemetry-collector.extraConfigMap[0] | string | `"veego-stack"` |  |
| notifications-telemetry-collector.extraSecret[0] | string | `"veego-stack"` |  |
| notifications-telemetry-collector.image.repository | string | `"veego/notifications-telemetry-collector"` |  |
| notifications-telemetry-collector.image.tag | string | `"stage"` |  |
| notifications-telemetry-collector.replicaCount | int | `1` |  |
| oauth2-proxy.configuration.clientID | string | `"stack"` |  |
| oauth2-proxy.configuration.clientSecret | string | `""` |  |
| oauth2-proxy.configuration.cookieSecret | string | `""` |  |
| oauth2-proxy.extraArgs[0] | string | `"--set-authorization-header=true"` |  |
| oauth2-proxy.extraArgs[1] | string | `"--oidc-jwks-url=https://keycloak.stack.exmpl.io/auth/realms/veego/protocol/openid-connect/certs"` |  |
| oauth2-proxy.extraArgs[2] | string | `"--auth-logging=true"` |  |
| oauth2-proxy.extraArgs[3] | string | `"--profile-url=https://keycloak.stack.exmpl.io/auth/realms/veego/protocol/openid-connect/userinfo"` |  |
| oauth2-proxy.extraArgs[4] | string | `"--skip-jwt-bearer-tokens=true"` |  |
| oauth2-proxy.extraArgs[5] | string | `"--pass-authorization-header=true"` |  |
| oauth2-proxy.extraArgs[6] | string | `"--oidc-issuer-url=https://keycloak.stack.exmpl.io/auth/realms/veego"` |  |
| oauth2-proxy.extraEnvVars[0].name | string | `"OAUTH2_PROXY_SCOPE"` |  |
| oauth2-proxy.extraEnvVars[0].value | string | `"openid roles web-origins email profile"` |  |
| oauth2-proxy.extraEnvVars[10].name | string | `"OAUTH2_PROXY_COOKIE_SECURE"` |  |
| oauth2-proxy.extraEnvVars[10].value | string | `"true"` |  |
| oauth2-proxy.extraEnvVars[11].name | string | `"OAUTH2_PROXY_PASS_ACCESS_TOKEN"` |  |
| oauth2-proxy.extraEnvVars[11].value | string | `"false"` |  |
| oauth2-proxy.extraEnvVars[12].name | string | `"OAUTH2_PROXY_REVERSE_PROXY"` |  |
| oauth2-proxy.extraEnvVars[12].value | string | `"true"` |  |
| oauth2-proxy.extraEnvVars[13].name | string | `"OAUTH2_PROXY_SET_XAUTHREQUEST"` |  |
| oauth2-proxy.extraEnvVars[13].value | string | `"true"` |  |
| oauth2-proxy.extraEnvVars[14].name | string | `"OAUTH2_PROXY_SKIP_AUTH_PREFLIGHT"` |  |
| oauth2-proxy.extraEnvVars[14].value | string | `"true"` |  |
| oauth2-proxy.extraEnvVars[15].name | string | `"OAUTH2_PROXY_SHOW_DEBUG_ON_ERROR"` |  |
| oauth2-proxy.extraEnvVars[15].value | string | `"true"` |  |
| oauth2-proxy.extraEnvVars[1].name | string | `"OAUTH2_PROXY_PROVIDER"` |  |
| oauth2-proxy.extraEnvVars[1].value | string | `"oidc"` |  |
| oauth2-proxy.extraEnvVars[2].name | string | `"OAUTH2_PROXY_LOGIN_URL"` |  |
| oauth2-proxy.extraEnvVars[2].value | string | `"https://keycloak.stack.exmpl.io/auth/realms/veego/protocol/openid-connect/auth"` |  |
| oauth2-proxy.extraEnvVars[3].name | string | `"OAUTH2_PROXY_REDEEM_URL"` |  |
| oauth2-proxy.extraEnvVars[3].value | string | `"https://keycloak.stack.exmpl.io/auth/realms/veego/protocol/openid-connect/token"` |  |
| oauth2-proxy.extraEnvVars[4].name | string | `"OAUTH2_PROXY_VALIDATE_URL"` |  |
| oauth2-proxy.extraEnvVars[4].value | string | `"https://keycloak.stack.exmpl.io/auth/realms/veego/protocol/openid-connect/userinfo"` |  |
| oauth2-proxy.extraEnvVars[5].name | string | `"OAUTH2_PROXY_COOKIE_DOMAINS"` |  |
| oauth2-proxy.extraEnvVars[5].value | string | `".stack.exmpl.io"` |  |
| oauth2-proxy.extraEnvVars[6].name | string | `"OAUTH2_PROXY_WHITELIST_DOMAINS"` |  |
| oauth2-proxy.extraEnvVars[6].value | string | `".stack.exmpl.io"` |  |
| oauth2-proxy.extraEnvVars[7].name | string | `"OAUTH2_PROXY_COOKIE_HTTPONLY"` |  |
| oauth2-proxy.extraEnvVars[7].value | string | `"false"` |  |
| oauth2-proxy.extraEnvVars[8].name | string | `"OAUTH2_PROXY_EMAIL_DOMAINS"` |  |
| oauth2-proxy.extraEnvVars[8].value | string | `"*"` |  |
| oauth2-proxy.extraEnvVars[9].name | string | `"OAUTH2_PROXY_COOKIE_SAMESITE"` |  |
| oauth2-proxy.extraEnvVars[9].value | string | `"lax"` |  |
| oauth2-proxy.ingress.annotations | object | `{}` |  |
| oauth2-proxy.ingress.apiVersion | string | `""` |  |
| oauth2-proxy.ingress.enabled | bool | `false` |  |
| oauth2-proxy.ingress.hostname | string | `"oauth.stack.exmpl.io"` |  |
| oauth2-proxy.ingress.ingressClassName | string | `"nginx"` |  |
| oauth2-proxy.ingress.pathType | string | `"ImplementationSpecific"` |  |
| oauth2-proxy.service.type | string | `"NodePort"` |  |
| probe-notifications-telemetry-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"probe-notifications-telemetry-handler"` |  |
| probe-notifications-telemetry-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"probe_telemetry_collector"` |  |
| probe-notifications-telemetry-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| probe-notifications-telemetry-handler.extraSecret[0] | string | `"veego-stack"` |  |
| probe-notifications-telemetry-handler.image.repository | string | `"veego/probe-notifications-telemetry-handler"` |  |
| probe-notifications-telemetry-handler.image.tag | string | `"stage"` |  |
| probe-notifications-telemetry-handler.replicaCount | int | `1` |  |
| probe-telemetry-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"probe-telemetry-handler"` |  |
| probe-telemetry-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| probe-telemetry-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| probe-telemetry-handler.extraSecret[0] | string | `"veego-stack"` |  |
| probe-telemetry-handler.image.repository | string | `"veego/probe-telemetry-handler"` |  |
| probe-telemetry-handler.image.tag | string | `"stage"` |  |
| probe-telemetry-handler.replicaCount | int | `1` |  |
| secret.AWS_ACCESS_KEY_ID | string | `""` |  |
| secret.AWS_SECRET_ACCESS_KEY | string | `""` |  |
| secret.VEEGO_KAFKA_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_PASSWORD | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_SERVICE_NAME | string | `""` |  |
| secret.VEEGO_KAFKA_SASL_USERNAME | string | `""` |  |
| secret.VEEGO_KAFKA_USERNAME | string | `""` |  |
| secret.VEEGO_REDIS_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_PASSWORD | string | `""` |  |
| secret.VEEGO_SQL_USERNAME | string | `""` |  |
| services-name-resolver.configMap.MONGODB_COLLECTION | string | `"records"` |  |
| services-name-resolver.configMap.MONGODB_DATABASE | string | `"services-name-resolver"` |  |
| services-name-resolver.extraConfigMap[0] | string | `"veego-stack"` |  |
| services-name-resolver.extraSecret[0] | string | `"veego-stack"` |  |
| services-name-resolver.image.repository | string | `"veego/services-name-resolver"` |  |
| services-name-resolver.image.tag | string | `"v0.1.0"` |  |
| services-name-resolver.replicaCount | int | `1` |  |
| speedtest-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"speedtest-handler-main"` |  |
| speedtest-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"speedtest"` |  |
| speedtest-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| speedtest-handler.extraSecret[0] | string | `"veego-stack"` |  |
| speedtest-handler.image.repository | string | `"veego/speedtest-handler"` |  |
| speedtest-handler.image.tag | string | `"stage"` |  |
| speedtest-handler.replicaCount | int | `1` |  |
| telemetry-aggregator.configMap.IS_APP_NAME_ANONYMIZATION_ON | string | `"false"` |  |
| telemetry-aggregator.configMap.VEEGO_KAFKA_AGGREGATOR_CONSUMER_GROUP_ID | string | `"telemetry-aggregator"` |  |
| telemetry-aggregator.configMap.VEEGO_KAFKA_AGGREGATOR_TOPIC | string | `"aggregation_ignitor"` |  |
| telemetry-aggregator.extraConfigMap[0] | string | `"veego-stack"` |  |
| telemetry-aggregator.extraSecret[0] | string | `"veego-stack"` |  |
| telemetry-aggregator.image.repository | string | `"veego/telemetry-aggregator"` |  |
| telemetry-aggregator.image.tag | string | `"stage"` |  |
| telemetry-aggregator.replicaCount | int | `1` |  |
| telemetry-handler.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"telemetry-handler"` |  |
| telemetry-handler.configMap.VEEGO_KAFKA_DEVICE_COLLECTOR_TOPIC | string | `"device_collector"` |  |
| telemetry-handler.configMap.VEEGO_KAFKA_TOPIC | string | `"telemetry"` |  |
| telemetry-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| telemetry-handler.extraSecret[0] | string | `"veego-stack"` |  |
| telemetry-handler.image.repository | string | `"veego/telemetry-handler"` |  |
| telemetry-handler.image.tag | string | `"stage"` |  |
| telemetry-handler.replicaCount | int | `1` |  |
| veeng.configMap.APP_FING_API | string | `"https://service.fing.io/2/devrecog"` |  |
| veeng.configMap.APP_LOG_LEVEL | string | `"debug"` |  |
| veeng.configMap.APP_MONGO_DB | string | `"veeng"` |  |
| veeng.configMap.APP_MONGO_URI | string | `"veeng"` |  |
| veeng.configMap.SLACK_HOOK | string | `""` |  |
| veeng.extraConfigMap[0] | string | `"veego-stack"` |  |
| veeng.extraSecret[0] | string | `"veego-stack"` |  |
| veeng.image.repository | string | `"veego/veeng"` |  |
| veeng.image.tag | string | `"stage"` |  |
| veeng.replicaCount | int | `1` |  |
| veeng.secret.APP_FING_KEY | string | `""` |  |
| wifi-global-malfunctions-statistics-builder.configMap.WIFI_GLOBAL_MF_STATISTICS_SCHEDULING | string | `"0 0/10 * * * ?"` |  |
| wifi-global-malfunctions-statistics-builder.extraConfigMap[0] | string | `"veego-stack"` |  |
| wifi-global-malfunctions-statistics-builder.extraSecret[0] | string | `"veego-stack"` |  |
| wifi-global-malfunctions-statistics-builder.image.repository | string | `"veego/wifi-global-malfunctions-statistics-builder"` |  |
| wifi-global-malfunctions-statistics-builder.image.tag | string | `"stage"` |  |
| wifi-global-malfunctions-statistics-builder.replicaCount | int | `1` |  |
| wifi-malfunctions-counters-cleaner.configMap.WIFI_MALFUNCTIONS_CLEANER_SCHEDULING | string | `"0 0 1 * * MON"` |  |
| wifi-malfunctions-counters-cleaner.extraConfigMap[0] | string | `"veego-stack"` |  |
| wifi-malfunctions-counters-cleaner.extraSecret[0] | string | `"veego-stack"` |  |
| wifi-malfunctions-counters-cleaner.image.repository | string | `"veego/wifi-malfunctions-counters-cleaner"` |  |
| wifi-malfunctions-counters-cleaner.image.tag | string | `"stage"` |  |
| wifi-malfunctions-counters-cleaner.replicaCount | int | `1` |  |
| wifi-malfunctions-data-collector.configMap.VEEGO_KAFKA_CONSUMER_GROUP_ID | string | `"wifi-malfunctions-collector-main"` |  |
| wifi-malfunctions-data-collector.configMap.VEEGO_KAFKA_TOPIC | string | `"notifications"` |  |
| wifi-malfunctions-data-collector.extraConfigMap[0] | string | `"veego-stack"` |  |
| wifi-malfunctions-data-collector.extraSecret[0] | string | `"veego-stack"` |  |
| wifi-malfunctions-data-collector.image.repository | string | `"veego/wifi-malfunctions-data-collector"` |  |
| wifi-malfunctions-data-collector.image.tag | string | `"stage"` |  |
| wifi-malfunctions-data-collector.replicaCount | int | `1` |  |
| wifi-score-handler.configMap.AGENT_WIFI_SCORE_SCHEDULING | string | `"0 0 0 * * ?"` |  |
| wifi-score-handler.extraConfigMap[0] | string | `"veego-stack"` |  |
| wifi-score-handler.extraSecret[0] | string | `"veego-stack"` |  |
| wifi-score-handler.image.repository | string | `"veego/wifi-score-handler"` |  |
| wifi-score-handler.image.tag | string | `"stage"` |  |
| wifi-score-handler.replicaCount | int | `1` |  |