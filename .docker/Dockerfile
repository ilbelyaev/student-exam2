FROM centos:7
ENV LC_ALL=en_US.utf-8
ENV LANG=en_US.utf-8
WORKDIR /app
RUN yum -y update && yum -y install python3 python3-pip && python3 -m venv venv
COPY . ./
ENV FLASK_APP=js_example
RUN source venv/bin/activate && pip3 install --upgrade pip && pip3 install -e .
ENTRYPOINT /bin/bash -c "source venv/bin/activate && flask run --host 0.0.0.0"
EXPOSE 5000