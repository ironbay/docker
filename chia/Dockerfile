FROM python:3.9.2

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install sudo -y

WORKDIR /app

RUN git clone https://github.com/Chia-Network/chia-blockchain.git .
RUN pip install --upgrade pip
RUN pip install wheel
RUN pip install --extra-index-url https://pypi.chia.net/simple/ miniupnpc==2.1
RUN pip install -e . --extra-index-url https://pypi.chia.net/simple/
RUN pip install -e .

CMD chia init && chia start all && tail -f /dev/null
