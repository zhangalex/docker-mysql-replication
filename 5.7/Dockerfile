FROM mysql:5.7
ENV REPLICATION_USER replication
ENV REPLICATION_PASSWORD replication_pass
COPY replication-entrypoint.sh /usr/local/bin/
COPY init-slave.sh /
RUN chmod +x /usr/local/bin/replication-entrypoint.sh
RUN chmod +x /init-slave.sh
ENTRYPOINT ["replication-entrypoint.sh"]
CMD ["mysqld"]
