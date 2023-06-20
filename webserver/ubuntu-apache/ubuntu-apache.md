```bash
docker build -t <image-name> .
docker build -t ubuntu/apache .
```

```bash
docker run -it --name <container-name> -p 80:80 <image-name>
docker run -it --name apache -p 80:80 ubuntu/apache
```

```bash
cd /etc/init.d
sudo service apache2 start
```