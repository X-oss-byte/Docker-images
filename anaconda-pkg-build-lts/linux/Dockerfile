# Dockerfile for container images that Anaconda, Inc. uses to build conda
# packages released on the "defaults" (repo.anaconda.com) channels.

FROM continuumio/anaconda-pkg-build:2023.03.28@sha256:0799f8ea6151b33c94c4007213858efea186321d10cc8c164e1dd8260e394099

RUN /opt/conda/bin/conda install --quiet --yes jcmorin-ana-org::anaconda-time-machine=0.5.0 \
    && /opt/conda/bin/conda update --quiet --yes conda conda-build \
    && /opt/conda/bin/conda clean --index-cache --yes

ENV PATH="/opt/conda/bin:${PATH}"

CMD [ "/bin/bash" ]
