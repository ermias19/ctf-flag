From ubuntu:18.04

# Intall Samba 
RUN apt-get update && \
    apt-get update -y && \
    apt-get install --no-install-recommends -y samba 
    # apt-get autoremove && \
    # apt-get clean && \
    # rm -rf /var/lib/apt/lists/* && 

COPY run.sh  /usr/bin/run.sh
RUN chmod 777 /usr/bin/run.sh
# RUN mkdir /data

# VOLUME [ "/data" ]
EXPOSE 139 445

CMD ["/usr/bin/run.sh"]
