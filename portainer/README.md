frontend portainer.lolcat.home
    mode http
    stats enable
    bind *:80
    bind *:443 ssl crt /home/vintobolt/Projects/containers/portainer/haproxy.pem
    default_backend portainer_backend

backend portainer_backend
    stats enable
    option forwardfor
    option http-keep-alive
    server portainer 127.0.0.1:8080