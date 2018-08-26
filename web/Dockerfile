FROM python:3.6.5

# Install and start Filebeat which will send log output to LogStash
RUN curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-6.4.0-amd64.deb
RUN dpkg -i filebeat-6.4.0-amd64.deb
COPY filebeat.yml /etc/filebeat/filebeat.yml
RUN chmod 644 /etc/filebeat/filebeat.yml

RUN mkdir -p /home/
WORKDIR /home/
COPY . /home/

#RUN pip install --no-cache-dir -r requirements.txt