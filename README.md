# Env Ansible

### Get Started

Buildar a docker do operador

````bash
$ docker build -t ansible:latest operator/
````

Crie suas credenciais de acesso.

````bash
$ ssh-keygen -t rsa -q -f "operator/ssh/id_rsa" -N "" -C operator
````

Execute a docker do operador

````bash
$ docker run -it -v ${PWD}/operator/ansible:/etc/ansible -v ${PWD}/operator/ssh:/home/operator/.ssh/ ansible:latest bash
````

Inicie o ambiente virtual que irá administrar

````bash
$ vagrant up
````

Cópie as chaves públicas para cada hosts:

````bash
$ ssh-copy-id -i ~/.ssh/id_rsa root@192.168.50.20
````

Verifique se todos os hosts estão respondendo:

````bash
$ ansible -m ping all
````
