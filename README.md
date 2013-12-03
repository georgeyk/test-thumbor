test-thumbor
============

* Instalar [docker](http://www.docker.io/gettingstarted/)

* Baixar imagem:

$ sudo docker pull georgeyk/thumbor

* Iniciar serviço:

$ sudo docker run -p 8888:8888 -i -t georgeyk/thumbor thumbor -l DEBUG

* Em outro terminal:

$ curl -XPOST -i -H "Slug: foo" http://127.0.0.1:8888/image --data-binary @mu.jpg


HTTP/1.1 100 (Continue)

HTTP/1.1 201 Created

Date: Tue, 03 Dec 2013 16:41:55 GMT

Content-Length: 0

Content-Type: text/html; charset=UTF-8

Location: /image/89f061b9fd20493f85b380a6b5f917cf/foo

Server: TornadoServer/3.1.1

* No browser (note o valor de Location):

http://127.0.0.1:8888/unsafe/100x100/89f061b9fd20493f85b380a6b5f917cf/foo
