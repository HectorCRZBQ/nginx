FROM python:3.11
COPY ./ /webpage
WORKDIR /webpage
RUN pip install mkdocs
EXPOSE 8000
CMD ["mkdocs", "serve", "--dev-addr=0.0.0.0:8000"]
