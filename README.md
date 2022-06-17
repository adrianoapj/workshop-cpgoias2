# Configuração de Ambiente para o workshop de Nix e NixOS

Olá! Este arquivo contém as informações de como configurar o ambiente para seguir os passos do workshop de Nix e NixOS na #CPGoiáS2.

O Nix só funciona no macOS ou Linux (mesmo que via WSL), mas eu particularmente não recomendo o uso do Mac, porque requer uma série de passos adicionais

## Máquina Virtual Presencialmente

Disponho de um pendrive com algumas máquinas virtuais com o Nix já instalado para participantes que não dispõem de um sistema Linux para instalação ou não conseguirem instalar o Nix por algum motivo.

## Utilizando o Linux em uma Maquina Virtual

### Em Cloud

Para se conectar a uma máquina virtual Linux disponível na nuvem, é necessário um cliente SSH para isso.
Em sistemas Linux e macOS, o cliente SSH já deve estar disponível, enquanto no Windows, normalmente não, por isso, recomendo o Termius nesse caso.  

Acesse https://termius.com e faça o download ou pegue o arquivo baixado de meu pendrive aqui na Campus Party.

### Localmente

Localmente, você vai precisar de um programa para inicializar sua máquina virtual Linux. Para o Windows, eu recomendo o VirtualBox da Oracle, enquanto para o macOS eu recomendo o Parallels, ambos disponíveis nos links abaixo:

- [VirtualBox](https://www.virtualbox.org)
- [Parallels](https://www.parallels.com/br/)

## Instalação do Zero

A depender do sistema, as instruções são um pouco diferentes:

### Linux

Abra o terminal do sistema e execute o comando:
```bash
sh <(curl -L https://nixos.org/nix/install) --daemon
```

### macOS

Abra o terminal do sistema e execute o comando:
```bash
sh <(curl -L https://nixos.org/nix/install)
```

### Windows (WSL)

Abra o terminal do sistema e execute o comando:
```bash
sh <(curl -L https://nixos.org/nix/install) --no-daemon
```

### Docker

Abra o terminal do sistema e execute o comando para criar um container com o Nix:
```bash
docker run -it nixos/nix
```