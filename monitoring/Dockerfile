# Use the official Grafana image from Docker Hub
#FROM grafana/grafana:latest

# Run commands as root
#@USER root

# Ensure directory exists and set permissions
#RUN mkdir -p /var/lib/grafana \
#    && chown -R 472:472 /var/lib/grafana \
#    && chmod -R 755 /var/lib/grafana

# Switch back to the Grafana user
#USER grafana

# Use the official Grafana image from Docker Hub
FROM grafana/grafana:latest

# Create the grafana group with GID 472 if it doesn't exist
USER root
RUN getent group grafana >/dev/null || addgroup --gid 472 grafana

# Create the grafana user with UID 472 and add it to the grafana group
RUN getent passwd grafana >/dev/null || adduser --uid 472 --ingroup grafana --disabled-password grafana

# Set correct permissions and ownership for the Grafana data directory
RUN mkdir -p /var/lib/grafana && chown -R grafana:grafana /var/lib/grafana

# Switch back to the root user
USER root

