# Spring Boot WebRTC Peer-to-Peer Video Communication Room Based

#### Technologies:

- WebRTC
- Socket.IO
- BootStrap

### Instructions

#### write your local ip for each step

1) **Generate certificates:** \
   you can use git bash \
   write your local ip address of your computer/host like `192.168.0.3`

`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ssl/private_key.pem -out ssl/certificate.pem -subj "//C=US//ST=California//L=San Francisco//O=MyOrganization//OU=MyDepartment//CN=<YOUR_LOCAL_IP>"`

2) **update nginx.conf**

change `<YOUR_LOCAL_IP>` with your local ip same as step 1

file location: `src/main/resources/static/client.js`

```let socket = io.connect("https://<YOUR_LOCAL_IP>", {secure: true});```

3) **build docker image**

`docker-compose up -d --build`

#### phone + computer connection example

![./images/image3.png](./images/image3.png)

![./images/image1.png](./images/image1.png)

![./images/image2.png](./images/image2.png)


