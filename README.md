# Como configurar/instalar/usar o `setoolkit` no `Kali Linux`

## Resumo

Neste documento estão contidos os principais comandos e configurações para configurar/instalar/usar o `setoolkit` no `Linux Ubuntu`.

## _Abstract_

_This document contains the main commands and settings for configuring/installing/using `setoolkit` on `Linux Ubuntu`._

## Descrição [2]

### Social-Engigeer Toolkit (SET, `setoolkit`)

O `"setoolkit"` (Social Engineering Toolkit) é uma poderosa ferramenta de código aberto utilizada principalmente para testar e simular ataques de engenharia social em sistemas de segurança. Desenvolvido em Python, o `setoolkit` oferece uma variedade de recursos e módulos para criar cenários de engenharia social, como setoolkit, obtenção de credenciais, criação de páginas web falsas e muito mais. Embora seja uma ferramenta legítima, o `setoolkit` também pode ser usada de forma maliciosa por indivíduos com más intenções, destacando a importância de seu uso responsável e ético, geralmente por profissionais de segurança de TI e equipes de teste de penetração, para avaliar a vulnerabilidade de sistemas e redes a ataques de engenharia social.

## 1. Como configurar/instalar/usar o `setoolkit` no `Linux Ubuntu` [1][3]

Para configurar/instalar o `setoolkit` no `Linux Ubuntu`, você pode seguir estes passos:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Certifique-se de que seu sistema esteja limpo e atualizado.

    2.1 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.2 Remover pacotes `.deb` antigos ou duplicados do cache local. É útil para liberar espaço, pois remove apenas os pacotes que não podem mais ser baixados (ou seja, versões antigas de pacotes que foram atualizados). Digite o seguinte comando: `sudo apt autoclean`

    2.3 Remover pacotes que foram automaticamente instalados para satisfazer as dependências de outros pacotes e que não são mais necessários. Digite o seguinte comando: `sudo apt autoremove -y`

    2.4 Buscar as atualizações disponíveis para os pacotes que estão instalados em seu sistema. Digite o seguinte comando e pressione `Enter`: `sudo apt update`

    2.5 **Corrigir pacotes quebrados**: Isso atualizará a lista de pacotes disponíveis e tentará corrigir pacotes quebrados ou com dependências ausentes: `sudo apt --fix-broken install`

    2.6 Limpar o `cache` do gerenciador de pacotes `apt`. Especificamente, ele remove todos os arquivos de pacotes (`.deb`) baixados pelo `apt` e armazenados em `/var/cache/apt/archives/`. Digite o seguinte comando: `sudo apt clean` 
    
    2.7 Para ver a lista de pacotes a serem atualizados, digite o seguinte comando e pressione `Enter`:  `sudo apt list --upgradable`

    2.8 Realmente atualizar os pacotes instalados para as suas versões mais recentes, com base na última vez que você executou `sudo apt update`. Digite o seguinte comando e pressione `Enter`: `sudo apt full-upgrade -y`
    

3. Instalar Dependências: O setoolkit requer algumas dependências. Instale-as com o seguinte comando: `sudo apt install -y git apache2 python3-pip`

4. **Permissões de Superusuário:** A maioria das operações de instalação requer privilégios de superusuário (root). Você pode usar o comando sudo antes dos comandos para adquirir essas permissões. Por exemplo:

    ```
    sudo git clone https://github.com/trustedsec/social-engineer-toolkit/ setoolkit/
    sudo pip3 install -r requirements.txt
    sudo python3 setup.py
    ```

    Certifique-se de fornecer sua senha de superusuário quando solicitado.

5. **Instalar Pacotes Python Locais:** Se você encontrar problemas com a instalação de pacotes Python (como `pycrypto`) devido à falta de permissões, você pode usar a opção --`user` para instalar pacotes localmente apenas para o seu usuário, sem a necessidade de permissões de superusuário. Por exemplo: `pip3 install --user -r requirements.txt`
`
    Isso instalará os pacotes Python na sua pasta pessoal e não exigirá permissões de superusuário.

6. **Executar o SET:** Para iniciar o SET, use: `sudo setoolkit
`
Lembre-se de que o SET é uma ferramenta poderosa usada para testes de engenharia social e pentesting. Use-a com responsabilidade e apenas em ambientes autorizados.

Lembre-se de que, em alguns casos, pode ser necessário reiniciar o terminal ou a sessão para que as alterações nas permissões tenham efeito. Certifique-se de que todos os comandos tenham sido executados com sucesso e, em seguida, você deve ser capaz de usar o `setoolkit`.



### 2. Código completo para configurar/instalar/usar

Para configurar/instalar o `setoolkit` no `Linux Ubuntu` sem precisar digitar linha por linha, você pode seguir estas etapas:

1. Abra o `Terminal Emulator`. Você pode fazer isso pressionando: `Ctrl + Alt + T`

2. Digite o seguinte comando e pressione `Enter`:

    ```
    sudo apt clean                                                            
    sudo apt autoclean
    sudo apt autoremove -y
    sudo apt update
    sudo apt --fix-broken install
    sudo apt clean
    sudo apt list --upgradable
    sudo apt full-upgrade -y
    sudo git clone https://github.com/trustedsec/social-engineer-toolkit/ setoolkit/
    sudo pip3 install -r requirements.txt
    sudo python3 setup.py
    pip3 install --user -r requirements.txt
    sudo setoolkit
    ```


## Referências

[1] OPENAI. ***Instalar set no xubuntu.*** Disponível em: <https://chat.openai.com/c/d899631e-ab79-4474-8e35-33a017ad1ae6> (texto adaptado). Acessado em: 01/02/2024 11:40.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). Acessado em: 01/02/2024 11:40.


