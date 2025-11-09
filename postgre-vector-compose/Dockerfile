FROM postgres:17

# Cài pgvector
RUN apt-get update && apt-get install -y --no-install-recommends \
      build-essential ca-certificates git postgresql-server-dev-17 \
    && git clone --depth 1 https://github.com/pgvector/pgvector.git /tmp/pgvector \
    && cd /tmp/pgvector && make && make install \
    && rm -rf /var/lib/apt/lists/* /tmp/pgvector
