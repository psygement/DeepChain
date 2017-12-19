
FROM ubuntu
RUN     sed -i -e 's/archive\.ubuntu\.com/kr\.archive\.ubuntu\.com/g' /etc/apt/sources.list &&     apt-get update

RUN     apt-get install -y software-properties-common python-software-properties

RUN     add-apt-repository ppa:bitcoin/bitcoin &&     apt-get update &&     apt-get install -y bitcoind &&     mkdir -p /bitcoin

RUN     apt-get remove -y software-properties-common python-software-properties &&     apt-get autoremove -y

CMD ["/usr/bin/bitcoind", "-datadir=/bitcoin", "--printtoconsole"]

