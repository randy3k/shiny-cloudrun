FROM randy3k/shiny-cloudrun
COPY . /srv/shiny-server/

# install dependencies
WORKDIR /srv/shiny-server/
RUN Rscript -e "install.packages('renv')"
RUN Rscript -e "install.packages(setdiff(renv::dependencies(quiet = TRUE)[, 'Package'], .packages(all.available = TRUE)))"
