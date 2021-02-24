# docker run --restart=always -v ~/.config/unity3d/IronGate/Valheim:/home/valheim/.config/unity3d/IronGate/Valheim -p 2456:2456/udp -p 2457:2457/udp -p 2458:2458/udp valheim

FROM debian:stable-slim

RUN apt-get -y update && \
    apt-get -y install lib32gcc1 lib32stdc++6 curl
    
RUN useradd -m valheim
COPY . /home/valheim
WORKDIR /home/valheim
USER valheim
STOPSIGNAL SIGINT
ENTRYPOINT ["/home/valheim/start_valheim.sh"]
