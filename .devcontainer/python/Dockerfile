ARG VER="3.8"
FROM python:${VER}-slim

RUN apt-get update && apt-get install -y tzdata \
&& apt-get install -y git && apt-get install -y unzip \
&& apt-get -y install gcc \
&& rm -rf /var/lib/apt/lists/*

WORKDIR /tmp/work
COPY requirements.txt ${PWD}
COPY kaggle.json /root/.kaggle/
RUN pip install -r requirements.txt

EXPOSE 8888

ENV TZ=Asia/Tokyo

