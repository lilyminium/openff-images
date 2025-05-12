FROM condaforge/mambaforge:24.9.2-0


SHELL ["/bin/bash", "-c"]

ENV PATH /opt/conda/bin:$PATH
ENV PYTHON_VERSION=${python}
ENV DASK_VERSION=${release}
RUN mkdir /opt/app

COPY environment.yaml /tmp/environment.yaml

# update base environment
RUN mamba install -y -c conda-forge "mamba>=0.27.0" \
    && mamba env update -n base -f /tmp/environment.yaml

RUN mamba clean -tipy \
    && find /opt/conda/ -type f,l -name '*.a' -delete \
    && find /opt/conda/ -type f,l -name '*.pyc' -delete \
    && find /opt/conda/ -type f,l -name '*.js.map' -delete \
    && find /opt/conda/lib/python*/site-packages/bokeh/server/static -type f,l -name '*.js' -not -name '*.min.js' -delete \
    && rm -rf /opt/conda/pkgs

COPY prepare.sh /usr/bin/prepare.sh

ENTRYPOINT ["tini", "-g", "--", "/usr/bin/prepare.sh"]