# httpenv

Tiny HTTP server showing the environment variables on TCP 8888.

Images for `linux/x86_64` (amd64), `linux/arm64` (v8), and `linux/arm/v7`

This can be used for various container learnings like how DNS round-robin works, rolling updates, etc.
It can be easier to use than something large and resource hungary like elasticsearch, while still providing
a way to check which container you're seeing in browser (or `curl`) by viewing the env vars it returns in HTTP.

Run it from Docker Hub on host port 8888:

`docker run -d -p 8888:8888 rumeysakdogan/httpenv`

If you `curl` it, you should get back its environment variables, including the container name:

```shell
curl http://localhost:8888

{"HOME":"/root","HOSTNAME":"c9d8d26bda3a","PATH":"/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"}```
