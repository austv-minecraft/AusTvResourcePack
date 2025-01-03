# Adicionar mobs novos do ModelEngine
Quando uma nova entidade for adicionada no ModelEngine, dois lugares são alterados:
- `/assets/ausmobs` pois "ausmobs" é o nome do namespace que geramos no ME.
- `/assets/minecraft/models/item/material.json` sendo "material" o tipo do material que o item é.
- `/assets/minecraft/sounds` possa ser que o mob específico tenha sons.

A textura é gerada na pasta do plugin, **contudo**, ele integra com a textura do ItemAdder automaticamente. Portanto, é mais fácil utilizar a textura do ItemAdder gerada, principalmente por conta do arquivo ´blocks.json´ que junta um monte de coisa. Vamos começar **fazendo o download** da textura gerada pelo ItemAdder localizada em output, chamado de `gererated.zip`.

![image](https://github.com/user-attachments/assets/f9eea0c6-9923-4857-a72a-474c78f66df2)

## Adicionar as alterações do namespace
Em vez de arrastar toda a pasta, vamos adicionar apenas o que foi alterado, isso porque as texturas são sobrescritas com as importações do plugin e isso daria um [problema](https://github.com/austv-minecraft/AusTv/issues/1082). De forma simples, arraste o arquivo `sounds.js` e mais as pastas referentes aos novos pets.

![image](https://github.com/user-attachments/assets/0382c479-58ce-4138-ae59-d6ccd7cb7708)


## Adicionar as alterações dos custons
Novos itens precisam estar registrados no `material.json` com o custom de cada. O processo é o mesmo para o ItemAdder, [veja aqui](https://github.com/leogianfagna/AusTvResourcePack/blob/main/docs/ItemsAdder.md).

## Adicionar blocks.json
Pode haver alterações neste arquivo que é responsável por muitos itens funcionarem. Atualize com a nova versão localizada em `assets/minecraft/atlases/blocks.json`.

# Modificando os caminhos do model
Essa etapa é sobre o desenvolvimento dos pets e não adição na textura (ou seja, processo ANTES da textura). Os nomes de pets ficam extremamente longos e precisam ser renomeados por dois motivos: melhor reconhecimento/organização e caminhos menores para evitar bugs. Portanto, para fazer isso, devemos:
1. **[ModelEngine]** Alterar o nome do blueprint, o arquivo `.bbmodel`.
2. **[ModelEngine]** Dentro desse mesmo blueprint, alterar o path do model para o mesmo nome. Vai estar localizado dessa forma: `"name":"mirko"`.
3. **[ModelEngine]** Na pasta do plugin, em `resourcepack/ausmobs/models`, alterar o nome da pasta do mob para o mesmo nome escolhido no blueprint.
4. **[MythicMobs]** Alterar o model que estava com o nome antigo do blueprint para o novo. Isso é nas configuraçõs do mob, procurar onde estão seus arquivos.
5. Reiniciar os plugins.
