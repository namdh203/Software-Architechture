FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y \
    tightvncserver \
    xfce4 \
    xfonts-base \
    xfonts-100dpi \
    xfonts-75dpi \
    xterm \
    vim \
    && rm -rf /var/lib/apt/lists/*

ENV USER=root \
    PASSWORD=nam2003 \
    DISPLAY=:1 \
    VNC_PORT=5901

RUN mkdir -p /root/.vnc && \
    echo "$PASSWORD" | vncpasswd -f > /root/.vnc/passwd && \
    chmod 600 /root/.vnc/passwd

RUN mkdir -p /usr/share/fonts/X11/75dpi/ \
    && mkdir -p /usr/share/fonts/X11/100dpi/

RUN touch /root/.Xresources

EXPOSE $VNC_PORT

CMD ["sh", "-c", "vncserver $DISPLAY -geometry 1280x800 -depth 24 && tail -f /root/.vnc/*.log"]
