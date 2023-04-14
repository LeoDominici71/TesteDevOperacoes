# Teste Dev SafeWay 

# Sobre o projeto

O projeto e um aplicativo a qual empresas conseguem acessar atraves de um login a lista de vendas e ver seus produtos, os clientes acessam os produtos dessas empresas, realizam compras e verificam a lista de itens comprados tambem. Ha tambem o usuario administrador a qual consegue acessar todas as empresas, seus produtos, lista de vendas e ver produtos. 

# Erros corrigidos

## Regras de negocio
1- Quando o administrador acessava com seu usuario, estava apenas acessando o aplicativo como um cliente. De acordo com a regra de negocio numero 2, o administrador devera ser quem acessa os dados da empresa alem da propria empresa. O erro acontecia por que nao havia um if else criado especificamente para o IsAdmin, entao ele acabava indo para o sistema de cliente.

![image](https://user-images.githubusercontent.com/110640214/232152107-ba6c8d00-628c-4de5-aae5-7e8b7e3eaff3.png)

Eu criei um else if para inserir o usuarioLogado.IsAdmin(). Com isso acessando o usuario voce tera as 3 opcoes da empresa usando System.out.println. Apos escolher, atraves de uma strem eu busquei, atraves do numero da empresa que digitou, a empresa correta do banco de dados. Com isso voce consegue acessar a lista e ver os produtos da empresa.

![image](https://user-images.githubusercontent.com/110640214/232153927-c924fab9-e92b-4bc4-b83d-2490900ad7a9.png)

2 - Um segundo erro na regra de negocios, era que quando um cliente entrava em seu usuario, acessava o comercio a qual gostaria de comprar, olhava a lista de produtos e por engano colocava o id de um produto que existia em outro comercio, ele realizava a compra e computava na empresa a qual o cliente nao escolheu. Isso fere o principio de que a empresa deve vender os produtos a qual esteja relacionada. Isso acontecia por que nao havia uma variavel confirmando que os produtos que voce deve buscar sao os da empresa em questao.

![image](https://user-images.githubusercontent.com/110640214/232154681-a3b51438-69da-4a5f-9895-c11ff446bf41.png)

A minha abordagem foi, confirmar novamente dentro do metodo de escolha da empresa e seus produtos, e adicionar uma variavel que confirma que os produtos que voce escolher deve ser da empresa em questao.

![image](https://user-images.githubusercontent.com/110640214/232155322-500bed23-3d96-4ed9-b98c-3d31519c3237.png)

## Melhorias de boas praticas
3 - Realizei a separacao das classes em dois pacotes distintos para melhora de boas praticas de programaçao.
![image](https://user-images.githubusercontent.com/110640214/232157516-f93f5322-e289-45ec-9a5f-e08933489d62.png)

4 - Inseri Codigo invalido caso nao exista a opçao que desejar.
![image](https://user-images.githubusercontent.com/110640214/232159211-f750b1c6-db4a-4deb-878c-d1ff4e2f2ffc.png)

5 - Tratei a excecao inputMismatchException.
![image](https://user-images.githubusercontent.com/110640214/232159411-74768f04-cbe6-400d-8c69-0da879420951.png)

6 - Caso digite uma opçao invalida ira surgir.


![image](https://user-images.githubusercontent.com/110640214/232159701-74ffe912-8806-43f5-a7c4-60cda7ee3029.png)


## Experiencia do Usuario
Realizei a mudança da ordem dos codigos da empresa para ficar mais intuitivo e nao induzir ao erro.
![image](https://user-images.githubusercontent.com/110640214/232157742-2c920874-90ae-4b1c-a4b3-bac924276c5f.png)

Inseri tambem a mensagem compra realizada com sucesso para melhor experiencia do usuario.
![image](https://user-images.githubusercontent.com/110640214/232158084-e46b3aae-4627-4a2b-90f6-0a7fb63beaee.png)

Inseri a frase Escolha uma opçao para iniciar e escolha uma empresa para consultar. Para melhor entendimento do usuario, seja empresa, administrador ou cliente.

![image](https://user-images.githubusercontent.com/110640214/232158461-e5d82e78-d802-4d26-b3d7-8e5d53ef6756.png)

![image](https://user-images.githubusercontent.com/110640214/232158755-cd53ef47-b1dd-451e-a89c-a49077cbda1d.png)

![image](https://user-images.githubusercontent.com/110640214/232158897-03ca44c1-ee57-48ec-b486-460a38d08475.png)







# Tecnologias utilizadas
## Back end
- Java
- Spring Boot
- JPA / Hibernate
- Maven
## Front end
- HTML / CSS / JS / TypeScript
- ReactJS
- React Native
- Apex Charts
- Expo
## Implantação em produção
- Back end: Heroku
- Front end web: Netlify
- Banco de dados: Postgresql

# Como executar o projeto

## Back end

```bash
# clonar repositório
git clone https://github.com/devsuperior/sds1-wmazoni

