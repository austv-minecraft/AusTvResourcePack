# Adicionar itens novos do ItemAdder
Quando um novo item for adicionado no ItemAdder, dois lugares são alterados:
- `/assets/ia_namespace` sendo "ia_namespace" o nome do diretório que os itens foram adicionados.
- `/assets/minecraft/models/item/material.json` sendo "material" o tipo do material que o item é.

Vamos começar **fazendo o download** da textura gerada pelo ItemAdder localizada em output, chamado de `gererated.zip`.

## Adicionar as alterações do namespace
Com a textura instalada, partindo do princípio que a textura gerada pelo ItemAdder está compatível com a nossa textura e basta apenas arrastar o namespace para a textura da AusTv, arraste o namespace para `assets`.

### Remover pasta `ia_auto_gen`
Os modelos dos itens criados ficam localizados em `nome_namespace/models/ia_auto_gen` o que torna um caminho grande e **causa problemas nas texturas Bedrock**. Por conta disso, transferimos todos os modelos localizados dentro desse diretório para a pasta `models`.

## Adicionar as alterações dos custons
Novos itens precisam estar registrados no `material.json` com o custom de cada. Basta pegar o que foi gerado pelo ItemAdder e adicionar nesse arquivo mas com um detalhe, precisamos remover o "ia_auto_gen/" já que fizemos um processo anterior. Depois disso está pronto e não é necessário mais nenhum outra modificação.