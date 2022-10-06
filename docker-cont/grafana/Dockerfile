# Import grafana from Docker Hub
FROM grafana/grafana

# Copy files on Docker containers for configuration DashBoard and Datasource (Prometheus)
COPY dashboards.yml /etc/grafana/provisioning/dashboards/dashboards.yml
COPY datasources.yml /etc/grafana/provisioning/datasources/datasources.yml
COPY node-exporter-full.json /etc/grafana/provisioning/dashboards/default.json

EXPOSE 3000

