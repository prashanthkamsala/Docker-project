FROM continuumio/miniconda3:4.10.3p1
WORKDIR /project

COPY requirements.txt .

RUN conda install --file requirements.txt

RUN	apt-get update && apt-get -y install curl

#Google cloud commnad line
RUN wget -qO- https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-381.0.0-linux-x86_64.tar.gz | tar xvz -C /opt  \
    && cd /opt/google-cloud-sdk && ./install.sh --usage-reporting false --quiet


# Azure installation command
RUN	curl -sL https://aka.ms/InstallAzureCLIDeb | bash


# Installing prerequisite packages
RUN DEBIAN_FRONTEND="noninteractive" apt-get update && apt-get install -y tzdata keyboard-configuration
RUN apt-get -y install curl unzip groff less
# AWS CLI installation commands
RUN	curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
RUN	unzip awscliv2.zip && ./aws/install


CMD ["jupyter-lab","--ip=0.0.0.0","--no-browser","--allow-root"]