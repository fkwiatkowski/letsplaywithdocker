FROM ubuntu
RUN apt-get update && apt-get -y install python3 python curl wget git
WORKDIR /tmp
COPY ./oecore-x86_64-armv6-vfp-toolchain-qte-nodistro.0.sh /tmp/oecore-x86_64-armv6-vfp-toolchain-qte-nodistro.0.sh 
RUN cd /tmp && chmod +x /tmp/oecore-x86_64-armv6-vfp-toolchain-qte-nodistro.0.sh && /tmp/oecore-x86_64-armv6-vfp-toolchain-qte-nodistro.0.sh -y
RUN rm /tmp/oecore-x86_64-armv6-vfp-toolchain-qte-nodistro.0.sh