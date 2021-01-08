FROM phusion/baseimage

LABEL maintainer "christiandavbid@gmail.com"

CMD ["/sbin/my_init"]

# New user is added without login and root access to only have access to the application.
RUN groupadd -r devops && useradd -r -g devops -d /var/www devops

# Install core packages
RUN apt-get update -q
RUN apt-get upgrade -y -q
RUN apt-get install -y zip unzip git-core nano
RUN apt-get clean -q && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*