FROM ghcr.io/lilyminium/openff-images:tmp-evaluator-base-v0

COPY prepare.sh /usr/bin/prepare.sh

ENTRYPOINT ["tini", "-g", "--", "/usr/bin/prepare.sh"]