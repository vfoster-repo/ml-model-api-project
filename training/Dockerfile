FROM quay.io/jupyter/base-notebook:python-3.13

USER root

COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

RUN mkdir -p /home/jovyan/work/data && \
    mkdir -p /home/jovyan/work/models && \
    chown -R jovyan:users /home/jovyan/work

USER jovyan
WORKDIR /home/jovyan/work
