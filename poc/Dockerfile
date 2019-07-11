FROM python:3.7-slim-stretch

RUN pip install pipenv

COPY Pipfile Pipfile.lock /

RUN pipenv install --system --deploy \
 && rm -f /Pipfile /Pipfile.lock

COPY bin/* /usr/bin/

ENTRYPOINT ["/usr/bin/kapow"]
