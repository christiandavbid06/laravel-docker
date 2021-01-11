FROM phusion/baseimage:0.9.22

LABEL maintainer "christiandavbid@gmail.com"

CMD ["/sbin/my_init"]

# Agregar el usuario laravel que realizará los cambios
RUN groupadd -g 1000 devops
RUN useradd -u 1000 -ms /var/www -g devops devops
# Nuevo usuario es agregagado sin login y root access solamente tiene acceso a la aplicacion
# RUN groupadd -r devops && useradd -r -g devops -d /var/www devops

# Instalacion de core packages
RUN apt-get update -q
#RUN apt-get upgrade -y -q
RUN apt-get install -y zip unzip git-core nano
RUN apt-get clean -q && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*