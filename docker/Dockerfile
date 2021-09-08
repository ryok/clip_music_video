FROM nvcr.io/nvidia/pytorch:21.05-py3

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update 
# RUN apt update && apt-get install -y tzdata
# timezone setting
# ENV TZ=Asia/Tokyo 

RUN apt install -y imagemagick

ADD requirements.txt /tmp/requirements.txt

RUN pip install -r /tmp/requirements.txt

RUN git clone https://github.com/openai/CLIP.git

ADD policy.xml /etc/ImageMagick-6/policy.xml
