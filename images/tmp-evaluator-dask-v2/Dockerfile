FROM ghcr.io/lilyminium/openff-images:tmp-evaluator-base-v2

COPY prepare.sh /usr/bin/prepare.sh

ENTRYPOINT ["tini", "-g", "--", "/usr/bin/prepare.sh"]