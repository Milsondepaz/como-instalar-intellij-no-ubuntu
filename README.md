# Como Instalar o IntelliJ IDEA no Ubuntu

O IntelliJ IDEA é uma das IDE's (Ambiente de Desenvolvimento Integrado) mais popular para Java e outras linguagens de programação. Aqui esta um guia passo-a-passo de como instalar a Edição Comunity do IntelliJ IDEA no Ubuntu.

## Passos de Instalação

1. Baixe o IntelliJ IDEA Comunity Edition em [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/).

2. verifique se o arquivo baixado está na pasta "Downloads". Você pode fazer isso executando o seguinte comando no terminal:

    ```bash
    ls Downloads/
    ```

3. Extraia o arquivo baixado, substituia `ideaIC-2023.2.2.tar.gz` ou o `nome-do-seu-arquivo.tar.gz` pelo nome do arquivo real que você baixou:

    ```bash
    tar -xzf ideaIC-2023.2.2.tar.gz
    ```

4. Mova o diretório extraído para o diretório `/opt`, substituindo `idea-IC-232.9921.47` ou o `nome-do-seu-arquivo.tar.gz` pelo nome real do diretório:

    ```bash
    sudo mv idea-IC-232.9921.47 /opt/intellij-idea
    ```

5. Crie um link de acesso fácil para facilitar a execução do IntelliJ IDEA a partir do terminal:

    ```bash
    sudo ln -s /opt/intellij-idea/bin/idea.sh /usr/local/bin/idea
    ```

6. Agora você pode iniciar o IntelliJ IDEA digitando no terminal: `idea`

7. Crie um atalho na área de trabalho, abra o terminal e crie um novo arquivo de entrada na área de trabalho:

    ```bash
    sudo nano /usr/share/applications/intellij-idea.desktop
    ```

8. No editor de texto, cole o o texto abaixo:

    ```ini
    [Desktop Entry]
    Name=IntelliJ IDEA
    Comment=Edição Comunitária do IntelliJ IDEA
    Exec=/opt/intellij-idea/bin/idea.sh
    Icon=/opt/intellij-idea/bin/idea.png
    Terminal=false
    Type=Application
    Categories=Desenvolvimento;IDE;
    StartupWMClass=jetbrains-idea
    ```

9. Salve e fecha o editor.

10. Atualize o banco de dados de área de trabalho para registrar a nova entrada de área de trabalho:

    ```bash
    sudo update-desktop-database
    ```

Agora você tem o IntelliJ IDEA instalado no Ubuntu, com um comando no terminal (`idea`) e um atalho na área de trabalho disponíveis para acesso fácil.

Boa sorte na sua jornada como Java Developer!!!
