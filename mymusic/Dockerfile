FROM httpd:2.4

ADD ./requirements.txt ./
RUN apt-get update \
&& apt-get install -y \
python3-pip python3-venv \
libapr1 libapr1-dev \
libaprutil1-dev \
libapache2-mod-wsgi-py3 \
&& python3 -m venv /.venv \
&& /.venv/bin/pip install --no-cache-dir -r requirements.txt \
&& rm -rf /var/lib/apt/lists/*

