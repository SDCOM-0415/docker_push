FROM ubuntu:20.04
MAINTAINER SDCOM sdcom@sdcom.asia
EXPOSE 8888 8888
RUN apt-get update
RUN apt-get install -y sudo
RUN sudo sed -i 's@//.*archive.ubuntu.com@//mirrors.ustc.edu.cn@g' /etc/apt/sources.list
RUN echo sed -i 's@//.*archive.ubuntu.com@//mirrors.ustc.edu.cn@g' /etc/apt/sources.list.d/ubuntu.sources
RUN sudo apt-get update
RUN sudo apt-get install -y wget curl
RUN sudo apt-get install -y expect
COPY install_panel.sh /root/install_panel.sh
COPY install_exc.sh /root/install_exc.sh
RUN chmod +x /root/install_panel.sh
RUN /root/install_panel.sh
CMD [ "bt", "3" ]
