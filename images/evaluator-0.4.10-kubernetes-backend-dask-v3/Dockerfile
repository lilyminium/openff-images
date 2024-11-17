FROM ghcr.io/lilyminium/openff-images:evaluator-0.4.10-kubernetes-backend-base-v3

COPY prepare.sh /usr/bin/prepare.sh

ENTRYPOINT ["tini", "-g", "--", "/usr/bin/prepare.sh"]