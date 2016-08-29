# Arvore do Repositório µOS++

O Projeto **µOS++ IIIe** _(micro oh ɛs plus plus terceira edição)_ é a 
terceira interação do **µOS++**, um sistema operacional de código aberto
livre de royalty, multi tarefa para sistemas embarcados, focado em dispositivos
Cortex-M.

Este repositório no GitHub é basicamente a arvore de referência para outros
projetos e não contem nenhum código fonte; para o código atual por favor
faça referência para os projetos lincados a este.

Para atingir a integração dos pacotes, este repositório faz uso extensivo
de módulos do `git`.

Este projeto é principalmente usado como uma conviniência durante o 
desenvolvimento.

## CMSIS++

O componente do núcleo do **µOS++** e o **CMSIS++**, uma proposta para a 
próxima geração  do **CMSIS**.

**µOS++** também fornece uma implementação de referência para o escalonador do 
CMSIS++ RTOS. Uma implementação sintética da plataforma em POSIX, e será 
fornecida na arquitetura POSIX xPack.

## Baseado em pacotes

**µOS++** é composto de multiplos pacotes separados, cada hospedado como um
projeto GitHub. Pacotes originais são hspedados em  
[µOS++](https://github.com/micro-os-plus) e pacotes baseados em código de 
terceiros são hospedados em [xPacks](https://github.com/xpacks).

## Hieraquia das pastas

De um pontos de vista funcional, a hierarquia das pastas não é relevante, 
desde que o conteúdo é agrupado em pacotes, e os pacotes de ferramentas 
automaticamente tratam dependências, independênte da localização atual na
hierarquia.

Como tal, a hierarquia é mantida relativamente simples:


```
author
└── group
    └── xpack
```

O modelo é remotamente influênciado pelo pacote CMSIS, (CMSIS PACK), enquanto os
pacotes são agrupados pelos fornecedores.

Porém, a convenção bastante rigida de nomes usado pelo  CMSIS PACK não
adotado, um pacote pode ter qual nome e cada autor é livre para usar sua 
hierarquia.

## Estatus

O projeto está atualmente em estágio de desenvolvimento.

Arquivos da versão anterior estão atualizados, empacotados como pacotes 
separados e lincados para este repositório.

Durante este estágio o foco está menospara contribuição no código original, e
mais na definição das varias camadas e APIs; a implementação inicial contará 
com código existente, como CMSIS RTOS, FreeRTOS, lwIP, FAT FS, etc.

As APIs do core são definidas no pacote CMSIS++. Em adição as APIs RTOS e 
Drivers, outro componente de maior importancia é a camada POSIX IO, que traz
junto, sobre uma API padrão, arquivos, sockets, dispositivos, etc.

