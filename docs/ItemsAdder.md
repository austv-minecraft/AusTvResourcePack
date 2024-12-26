# Adicionar itens novos do ItemAdder
Quando um novo item for adicionado no ItemAdder, dois lugares são alterados:
- `/assets/ia_namespace` sendo "ia_namespace" o nome do diretório que os itens foram adicionados.
- `/assets/minecraft/models/item/material.json` sendo "material" o tipo do material que o item é.

Vamos começar **fazendo o download** da textura gerada pelo ItemAdder localizada em output, chamado de `gererated.zip`.

![image](https://github.com/user-attachments/assets/f9eea0c6-9923-4857-a72a-474c78f66df2)

## Adicionar as alterações do namespace
Com a textura instalada, partindo do princípio que a textura gerada pelo ItemAdder está compatível com a nossa textura e basta apenas arrastar o namespace para a textura da AusTv, arraste o namespace para `assets`.

![image](https://github.com/user-attachments/assets/706f41cc-7ce6-41bf-8083-c3a3b0c300df)


### Remover pasta `ia_auto_gen`
Os modelos dos itens criados ficam localizados em `nome_namespace/models/ia_auto_gen` o que torna um caminho grande e **causa problemas nas texturas Bedrock**. Por conta disso, transferimos todos os modelos localizados dentro desse diretório para a pasta `models`. Depois pode apagar a pasta "ia_auto_gen" que deve estar vazia agora.

![image](https://github.com/user-attachments/assets/7fe20b8d-134d-43c3-9837-71e24304c353)


## Adicionar as alterações dos custons
Novos itens precisam estar registrados no `material.json` com o custom de cada. Basta pegar o que foi gerado pelo ItemAdder e adicionar nesse arquivo mas com um detalhe, precisamos remover o "ia_auto_gen/" já que fizemos um processo anterior. Depois disso está pronto e não é necessário mais nenhum outra modificação.

![image](https://github.com/user-attachments/assets/4729b3e8-f040-425b-8cd9-af28384ce4ed)
