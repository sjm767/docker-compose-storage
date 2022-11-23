FROM fluent/fluentd:edge-debian
 
# Use root account to use apt
USER root
 
RUN buildDeps="sudo make gcc g++ libc-dev" \
 && apt-get update \
 && apt-get install -y --no-install-recommends $buildDeps \
 && apt-get install -y build-essential \
 && apt-get install -y libmariadb-dev \
 && apt-get update \
 && sudo gem install fluent-plugin-mysql-replicator \
 && sudo gem install fluent-plugin-kafka
