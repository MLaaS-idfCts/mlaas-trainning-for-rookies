FROM jupyterhub/jupyterhub

RUN apt-get update && apt-get install -y docker
RUN pip3 install notebook
RUN pip3 install dockerspawner

RUN useradd test && echo "test:test" | chpasswd && mkdir /home/test && chown test /home/test
RUN useradd admin && echo "admin:admin" | chpasswd && mkdir /home/admin && chown admin /home/admin

COPY jupyterhub_config.py /srv/jupyterhub/jupyterhub_config.py