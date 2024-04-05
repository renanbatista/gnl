# Get Next Line (GNL) - Eficiência em Leitura de Arquivos

## Visão Geral
O projeto **Get Next Line (GNL)** é uma função em C meticulosamente desenvolvida para ler uma linha de texto de um arquivo ou stream. Este projeto nasceu da necessidade de manipular dados de forma eficiente, tornando-se uma ferramenta valiosa para programadores que buscam soluções robustas e confiáveis em C.

## Funcionalidades
- **Leitura Eficiente**: `get_next_line` permite ler linhas de um arquivo de maneira otimizada, garantindo eficiência em diferentes contextos.
- **Versatilidade**: Funciona com diversos tipos de arquivos e streams, facilitando a leitura de dados linha por linha.
- **Código Claro**: Seguindo as boas práticas de codificação para manter o código acessível e manutenível.

## Como Utilizar
Para incorporar o GNL em seus projetos e melhorar a manipulação de arquivos, siga estes passos:

1. Clone o repositório:
   ```
   git clone https://github.com/renanbatista/gnl.git
   ```
2. Inclua `get_next_line.h` em seu projeto para acessar a função.

## Exemplo de Implementação
```c
#include "get_next_line.h"
#include <fcntl.h>
#include <stdio.h>

int main(void)
{
    int fd = open("example.txt", O_RDONLY);
    char *line;

    while ((line = get_next_line(fd)) != NULL)
    {
        printf("%s", line);
        free(line);
    }
    close(fd);
    return (0);
}
```

## Contribuições
Contribuições para o projeto são muito bem-vindas. Se você tem sugestões para melhorar o Get Next Line, sinta-se à vontade para fazer um fork do repositório, realizar alterações e enviar um pull request. Toda contribuição, seja para otimizar o código, corrigir bugs ou melhorar a documentação, ajudará a fazer do GNL uma ferramenta ainda mais robusta.

## Observações
Este projeto foi desenvolvido seguindo as normas de codificação da 42 School, com foco em código limpo, eficiente e modular, refletindo uma abordagem cuidadosa e detalhista no desenvolvimento de software.

## Licença
O Get Next Line é disponibilizado sob a MIT License, permitindo uso e distribuição livre.
