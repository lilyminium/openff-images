FROM condaforge/mambaforge:23.3.1-1


SHELL ["/bin/bash", "-c"]

ENV PATH /opt/conda/bin:$PATH
ENV PYTHON_VERSION=${python}
ENV DASK_VERSION=${release}

COPY environment.yaml /tmp/environment.yaml

RUN cat /tmp/environment.yaml

# update base environment
RUN mamba install -y -c conda-forge "mamba>=0.27.0"
RUN mamba env update -n base -f /tmp/environment.yaml


RUN mkdir -p ~/.config/dask
COPY distributed.yaml ~/.config/dask/distributed.yaml

RUN mkdir /opt/app
