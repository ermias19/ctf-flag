From ubuntu:18.04

# Intall Samba 
COPY samba-4.5.9.tar.gz /home
RUN apt-get update && \
    apt-get update -y && \
    apt install python && \
    apt install build-essential && \
    apt-get install manpages-dev && \
    apt-get install -y python-dev && \
    apt-get -y install gnutls* && \
    apt-get -y install gnutls-bin && \
    pkg-config --modversion gnutls && \
    apt-get install -y pkg-config && \
    apt-get install -y libacl1-dev && \
    apt install slapd ldap-utils && \
    apt install slapd ldap-utils && \
    apt install apt-util &&\
    # apt-get install --no-install-recommends -y samba \ 
    # apt-get install -f -o  samba=4.6.4 
    #apt-get install -y ssh
    # apt install openssh-server
    # apt-get autoremove && \
    # apt-get clean && \
    # rm -rf /var/lib/apt/lists/* && 
    cd /home/sama-4.6.4/
    ./configure   &&\
    make &&\
    install && \

    cp -r /home/samba-4.6.4/ctdb/tests/eventscripts/etc/ /etc/
    #service samba/smbd restart is not working 
    smba -D
    smbd -D
     
COPY run.sh  /usr/bin/run.sh
RUN chmod 777 /usr/bin/run.sh
# RUN mkdir /data

# VOLUME [ "/data" ]
EXPOSE 139 445 

CMD ["/usr/bin/run.sh"]
