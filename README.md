# Ackee GCP Elasticsearch image with GCE discovery service + GCS backup plugin

This image is meant to be used together with https://github.com/AckeeDevOps/docker-elasticsearch, which will utilize preinstalled GCE discovery plugin for Elasticsearch and will make cluster ES cluster available from GKE cluster.

There is also Terraform module which should handle the deployment of instances : https://github.com/AckeeDevOps/terraform-elasticsearch

This image is build on top of official Ubuntu 16.04 image with these extras preinstalled :
* GCS repository plugin for backups - https://www.elastic.co/guide/en/elasticsearch/plugins/6.4/repository-gcs.html
* GCE discovery plugin for hosts discovery - https://www.elastic.co/guide/en/elasticsearch/plugins/6.4/discovery-gce-usage-long.html
* Stackdriver agent for advanced Stackdriver monitoring
* Google fluentd plugin for Stackdriver logs ingestion
