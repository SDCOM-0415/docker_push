FROM ubuntu
MAINTAINER SDCOM sdcom@sdcom.asia
EXPOSE 8888 8888
RUN apt-get update
RUN apt-get install -y sudo
RUN sudo apt-get install -y wget curl
RUN sudo apt-get install -y expect
COPY install_panel.sh /root/install_panel.sh
RUN chmod +x /root/install_panel.sh
RUN /root/install_panel.sh
CMD [ "bt", "3" ]
