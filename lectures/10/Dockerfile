FROM jupyter/datascience-notebook:2ce7c06a61a1

COPY Pipfile* ./
RUN pip install pipenv==2018.11.26 \
    && pipenv install --system

RUN conda install -c bioconda r-ggrepel

COPY install.R ./
RUN R -f install.R
