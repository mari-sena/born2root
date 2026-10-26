__This project has been created as part of the 42 curriculum by mariafer__

## Description

O Born2beRoot é um projeto da 42 que tem como objetivo introduzir os conceitos básicos de administração de sistemas e virtualização.

Durante o projeto, aprendemos a criar e configurar uma máquina virtual Linux, utilizando apenas o terminal e aplicando regras de segurança.

Os principais conhecimentos adquiridos são:

- Virtualização: criação e configuração de uma máquina virtual;
- Sistemas operacionais: difereças entre Debian e Rocky Linux;
- Segurança: configuração de políticas de senhas, permissões e retrições de acesso;
- Firewall: controle das conexões de rede permitidas;
- SSH: acesso remoto seguro à máquina virtual;
- Gerenciamento de usuários: criação de usuários, grupos e permissões com _sudo_;
- Particionamento de discos: utilização do LVM para organizar volumes lógicos e criptografia para proteger os dados;
- Monitoramento: criação de um script Bash para apresentar informações do sistema periodicamente.

## Instruções

O projeto foi desenvolvido utilizando:
- Sistema operacional: Debian;
- Software de Virtualização: VirtualBox;
- Interface: terminal, sem ambiente gráfico;
- Acesso remoto: OpenSSH na porta 4242.

**Iniciando a máquina virtual:**
1. Abrir o VirtualBox;
2. Selecionar a máquina virtual clonada;
3. Inicializar;
4. Realizar login com o usuário configurado.

**Conectando via SSH:**
Com a máquina virtual ligada e o redirecionamento de portas configurado no VirtualBox, executar no terminal do computador anfitrião:
```
	ssh mariafer@127.0.0.1 -p 4242
```

## Resources
- [BTRFS Encryption On Debian Trixie - The Easy Way](https://www.youtube.com/watch?v=qNqKytIBvEA)
- [About EFI](https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/efi.html)

## AI Usage

A inteligência artificial foi utilizada como ferramenta de apoio para compreender conceitos técnicos, esclarecer dúvidas durante a configuração da máquina virtual e auxiliar na organização da documentação do projeto.

### Debian vs Rocky Linux

Debian e Rocky Linux são distribuições Linus que podem ser utilizadas em servidores.

**Debian**
- Utiliza o gerenciador de pacotes APT;
- Geralmente utiliza o AppArmor para controle de acesso;
- Pode utilizar o UFW para configurar o firewall;
- Possui uma grande comunidade e documentação;
- É conhecido pela estabilidade e simplicidade de adminitração.

**Rocky Linux**
- É compatível com o ecossistema Red Hat Enterprise Linux (RHEL);
- Utiliza o gerenciador de pacotes DNF;
- Geralmente utiliza SELinux como mecanismo de segurança;
- Utiliza o firewalld para gerenciar o firewall;
- É bastante direcionado a ambientes de servidores corporativos.

### AppArmor vs SELinux

AppArmor e SELinux são mecanismos de segurança do Linux que permitem restringir o acesso de programas aos recursos do sistema, mesmo quando as permissões tradicionais permitiriam determinadas operações.

**AppArmor:**
- Utiliza perfis para determinar o que cada programa pode acessar;
- Suas regras geralmente se baseiam em caminhos de arquivos;
- Costuma ser mais simples de configurar e compreender;
- É utilizado no Debian deste projeto.

**SELinux:**
- Utiliza políticas de segurança baseadas em rótulos e contextos;
- Permite um controle de acesso mais detalhado;
- Pode exigir maior conhecimento para configurar e solucionar problemas;
- É normalemente utilizado no Rocky Linux.

Ambos ajudam a proteger o sistema, limitando os recursos que um programa pode acessar.

### UFW vs firewalld

UFW e firewalld são ferramentas utilizadas para administrar regras de firewall no Linux.

**UFW (Uncomplicated Firewall):**
- Possui comandos simples;
- Facilita a liberação e o bloqueio de portas;
- É uma opção comum em sistemas Debian e Ubuntu.

**firewalld:**
- Utiliza conceitos como zonas, serviços e regras;
- Permite administrar diferentes níveis de confiança para conexões de rede;
- É bastante utilizado em distribuições como Rocky Linux.

Neste projeto utilizei o UFW para controlar as conexões de rede da máquina virtual, permitindo a porta 4242 para acesso SSH.

### VirtualBox vs UTM

VirtualBox e UTM são ferramentas utilizadas para criar e executar máquinas virtuais.

**VirtualBox:**
- Disponível para diferentes sistemas operacionais;
- Possui interface gráfica para configurar máquinas virtuais;
- Permite configurar memória, armazenamento e rede;
- É bastante utilizado em computadores com processadores x86-64.

**UTM:**
- Desenvolvido principalmente para macOS;
- Utiliza tecnologias como QEMU e o framework de virtualização da Apple;
- Permite virtualizar sistemas compatíveis e emular outras arquiteturas;
- É uma alternativa especialmente útil em Macs com Apple Silicon.

Escolhi VirtualBox pela facilidade de configuração.
