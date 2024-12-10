# Kubernetes Context Switcher

Um script bash interativo para alternar facilmente entre diferentes contextos do Kubernetes usando uma interface de diálogo TUI (Text User Interface).

## Características

- Interface interativa usando dialog
- Exibe o contexto atual
- Lista todos os contextos disponíveis
- Feedback visual após a troca de contexto
- Limpeza automática de arquivos temporários
- Tratamento de erros robusto

## Pré-requisitos

- kubectl
- dialog
- bash
- awk
- grep

## Instalação

1. Primeiro, crie o diretório bin local em seu home se ele ainda não existir:

```bash
mkdir -p ~/.local/bin
```

2. Baixe o script e mova-o para o diretório:

```bash
mv kube-context-switch.sh ~/.local/bin/kube-context-switch
```

3. Torne o script executável:

```bash
chmod +x ~/.local/bin/kube-context-switch
```

4. Adicione o diretório ~/.local/bin ao seu PATH. Dependendo do seu shell:

Para bash (adicione ao ~/.bashrc):
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

Para zsh (adicione ao ~/.zshrc):
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## Uso

Após a instalação e configuração do PATH, você pode executar o script simplesmente digitando:

```bash
kube-context-switch
```

Use as setas para cima/baixo para navegar entre os contextos disponíveis e pressione Enter para selecionar. Pressione ESC ou Cancel para sair sem fazer alterações.

## Estrutura do Projeto

```
~/.local/bin/
└── kube-context-switch     # Script executável
```

## Contribuindo

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

## Resolução de Problemas

Se você encontrar o erro "command not found", verifique se:

1. O diretório ~/.local/bin está no seu PATH
2. O script tem permissões de execução
3. Todos os pré-requisitos estão instalados

Para verificar se o diretório está no PATH:
```bash
echo $PATH | grep ~/.local/bin
```

## Licença

Este projeto está licenciado sob a MIT License - veja o arquivo LICENSE para detalhes.
