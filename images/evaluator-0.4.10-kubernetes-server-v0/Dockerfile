FROM ghcr.io/lilyminium/openff-images:evaluator-0.4.10-kubernetes-base-v0

COPY server.py /usr/bin/server.py
COPY run-server.sh /usr/bin/run-server.sh

ENTRYPOINT ["tini", "-g", "--", "/usr/bin/run-server.sh"]
