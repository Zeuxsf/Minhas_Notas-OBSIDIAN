# BÁSICOS

### Como criar um banco de dados?
- Use o comando `CREATE DATABASE NOME_DADOS;` (O `;` é melhor pra quando for usar vários comandos de uma vez)
- Antes de executar qualquer comando nesse banco de dados, use o comando `USE NOME_DADOS`, pro workbench saber em qual banco de dados você está usando
- Para um Banco de Dados que aceite acentuações, mais usado pelo português brasileiro. use esses comandos:
![[Pasted image 20250613101327.png]]
### E como eu apago?
- Use o comando `DROP DATABASE NOME_DADOS`
- Esse comando também funciona para apagar tabelas: `DROP TABLE NOME_TABELA`
### Como criar tabelas?
- Use o comando `CREATE TABLE NOME_TABELA (`
campo1,
campo2,
campo3,
campo4
 );
 - E caso eu não saiba se a tabela q eu vou criar já existe?
 Use um `IF NOT EXISTS`. Ex.:
 ![[Pasted image 20250616104740.png]]
- Do lado dos campos, você tem que utilizar uns indicadores, um 'Oque é esse valor?'
EXEMPLOS de INDICADORES:
![[Pasted image 20250611103028.png]]
- Exemplo de criação de tabela real:
![[Pasted image 20250611103250.png]]
 - Uma tabela padronizada para cadastro de pessoas:
 ![[Pasted image 20250613103618.png]]
# FUNÇÕES
### Como inserir dados em tabelas?
 ![[Pasted image 20250613110500.png]]
### Como acesso os dados inseridos na tabela?
 ![[Pasted image 20250613110739.png]]
### Como editar uma tabela existente?
![[Pasted image 20250616093118.png]]
Use o comando `ALTER TABLE NOME_TABELA`
- Para renomear uma tabela, use `RENAME TO NOVO_NOME_TABELA`
![[Pasted image 20250616104042.png]]
- O comando  `ADD COLUMN` vai adicionar uma coluna nova na tabela (já existente)
- Para adicionar uma coluna do lado de uma coluna existente e não no final dos dados, use o comando `AFTER NOME_COLUNA`. Ex.:
![[Pasted image 20250616101105.png]]
- E se eu quiser adicionar uma coluna no começo da tabela?
![[Pasted image 20250616101509.png]]
Use o comando `FIRST`
- Para modificar os valores de uma coluna, use `MODIFY COLUMN NOME_COLUNA`. Ex.:
![[Pasted image 20250616101935.png]]
- Para modificar o nome da coluna, use `CHANGE COLUMN NOME_COLUNA_ANTIGO NOME COLUNA_NOVO`. Ex.:
![[Pasted image 20250616103814.png]]
- Para apagar uma coluna criada, como faz?
Use o comando `DROP COLUMN NOME_COLUNA` ( não esqueça de usar `ALTER TABLE` antes do drop )
### Como atualizar uma linha? (Dados da tabela)
- Use o comando `UPDATE NOME_TABELA`
Ex.:
![[Pasted image 20250618090240.png]]
Vai setar um nome novo nos campos onde o id (chave primária, mais fácil de lidar) for igual a 1
- Como atualizar vários campos de uma linha?
![[Pasted image 20250618090831.png]]
Só indicar oq vc quer alterar, após o SET 
- Caso você precise informar ao `MySQL` que você só quer mudar apenas uma linha, pra não afetar a tabela inteira sem querer, use o comando `LIMIT 1`. Ex.:
![[Pasted image 20250618091238.png]]
### Como deletar uma linha?
- Use o comando `DELETE FROM NOME_TABELA`
Ex.:
![[Pasted image 20250618092612.png]]
"Delete da tabela cursos, onde o ano for igual a 2055. Se limite á apenas as primeiras 2 linhas, mesmo se existir mais do que isso."
- E se eu quiser DELETAR TODAS as linhas?
Use o comando `TRUNCATE TABLE NOME_TABELA`
# MySQL no Terminal
- Para entrar no MySQL via terminal, use os seguintes comandos:
Esse comando para acessar a pasta do servidor (Verifique a pasta em que o seu servidor está e modifique o comando se for preciso):
`cd "C:\Program Files\MySQL\MySQL Server 8.0\bin"

Esse comando pra acessar o servidor, ele vai pedir a senha que você cadastrou:
`.\mysql.exe -u root -p

Obs: Esses comandos funcionam no PowerShell, terminal da microsoft, recomendo uma busca no GPT caso não funcione na sua máquina atual