
version: "3.9"
services:
 web:
  build: .
  working_dir: /data
  command: python aulamvc.py
  links:
    - db
  volumes:
    - .:/data
  ports:
    - "5000:5000"

 db:
  image: mysql:5.7
  environment:
      MYSQL_ROOT_PASSWORD: mudar123
  ports:
    - "3309:3309"
