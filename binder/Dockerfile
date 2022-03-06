FROM jupyter/all-spark-notebook:8ed745f793de as initial

ARG DELTA_CORE_VERSION="1.1.0"
RUN pip install --no-cache-dir delta-spark==${DELTA_CORE_VERSION} && \
     fix-permissions "${HOME}" && \
     fix-permissions "${CONDA_DIR}"


FROM initial as config

COPY startup.sh "${HOME}"

USER ${NB_UID}

WORKDIR "${HOME}"

ENTRYPOINT ["bash", "startup.sh"]