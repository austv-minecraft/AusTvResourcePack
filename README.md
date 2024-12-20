# AusTv ResourcePack
Repositório da textura da AusTv que criptografa usando PackSquash automaticamente. A textura fica armazenada dentro do diretório `/textura` e cada alteração deve ser armazenada e alterada ali.

## Textura criptografada
Esse repositório **automatiza o PackSquash** para otimizar e corromper a textura a cada alteração feita. O resultado da textura é postada [aqui](https://github.com/leogianfagna/AusTvResourcePack/actions/workflows/packsquash.yml). Clique no último tópico gerado dentro desse link, que ele terá o mesmo nome do commit feito por você.

![image](https://github.com/user-attachments/assets/392eeb6c-a0bc-417a-a0ef-b496da25cab3)
![image](https://github.com/user-attachments/assets/a2306a9c-999c-4875-94e2-db4dbd17ffad)

Clicar neste ícone faz o download da textura pronta, depois das ações do PackSquash. O seu processo precisa concluir por completo, isso é possível perceber quando há o **ícone verde**.

## Fazendo alterações na textura
Basta ter esse repositório instalado no seu computador e usar alguma IDE para fazer as modificações necessárias.

### Comandos GitHub
Antes de começar qualquer alteração, use no terminal:
1. `git pull origin main`

Ao finalizar suas alterações, use no terminal:
1. `git add .`
2. `git commit -m "Mensagem do que foi alterado"`.
3. `git push origin main`

### Mensagem do commit
É importante colocar uma boa mensagem em cada alteração, pois assim podemos diferenciar cada alteração e qual é o pack certo para instalar depois da criptografia. Alguns exemplos que você pode seguir:
- Adicionado novos emblemas
- Corrigido CustomModelData das skins de natal
- Renomeado nome de alguns diretórios

Repare que cada mensagem é respectivo a **um assunto somente**, isso também é importante. Se você precisar adicionar novos emblemas e também adicionar novos cosméticos, faça duas operações distintas: primeiro adicione os cosméticos (fazendo todo o processo do git) e depois adicione todos os emblemas (e faça o mesmo processo novamente).
