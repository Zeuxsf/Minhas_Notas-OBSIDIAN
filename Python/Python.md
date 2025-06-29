[Site de mapas mentais sobre Programação](https://roadmap.sh/)
[Site do Python para pegar documentação](https://www.python.org/doc/) 
[StackOverflow](https://pt.stackoverflow.com/?tags=python)
[Vídeos sobre IA em Python](https://youtu.be/10fp0U0Xrbw?si=wFhZWeXSnmDLKfO2)
# BÁSICOS
## Anotações Base
- Toda ==Váriavel== é um objeto para o python
- caso eu queira deletar uma variável no meio do programa : del(variável)
- print == escreva
-  1 [=] significa ==RECEBE==(Atribui valor)
- 2 [ == ] significa ==IGUAL==(Sinal de igualdade)

- o comando `váriavel.isnumeric()` indica verdadeiro e falso se o valor for ou não um número, interessante para menus interativos e etc.
- O mesmo vale pro comando `variável.isalpha` que indica quando o valor é alfabético
- E o comando `variável.isalnum` verifica quando os dois tipos estão presentes
- `isinstance` pra saber se o objeto é de determinado tipo. ex.: `isinstance(obj, tipo)`
- Existem vários comandos com o ==is==, vale testar
## Ordem de precedência das Equações

- 1 - parênteses ==()==
- 2 - potência ==duasestrelas**==
- 3 - multiplicação ==estrela*==, divisão ==/== , divisão inteira ==//.== e resto da divisão ==%==
- 4 - adição ==+== e subtração ==-==
## Valores Primitivos
- (==DICA==: para descobrir o tipo de algum objeto, nome, numero etc, digite: print(type(variável)))

- int = inteiro
- float = real
- bool = logico (True, false)
- str = string, caractere
## Comandos Interessantes
- Comando pra verificar o local de instalação dos executáveis. Abaixo, terá um exemplo desse comando usando o exe do Python:
![[Pasted image 20250619210218.png]]
O comando é o: `gcm python` 
# CORES PARA O TERMINAL

- Códigos para por cores no terminal de python:
` \033[style;text;back m`
![[Pasted image 20250212090443.png]]
- É possível fazer uma variável para chamar toda vez que quiser usar cores, sem precisar escrever os códigos toda hora. Ex.:
 ![[Pasted image 20250212091852.png]]

# IMPORT'S (Bibliotecas Python)
- DICA: Todos os seus arquivos `.py` são módulos importáveis
Ex.:
![[Pasted image 20250618115704.png]]
O exemplo acima mostra import's q eu fiz de um outro código meu, importando funções que estavam lá dentro e que seriam úteis pro meu código principal

--- 
## Math
- Biblioteca Matemática/De equações do Python
- `import math` : para importar todos os comandos de uma vez da biblioteca 
- `from math import comando` : para importar algum comando específico da biblioteca
- `variável = math.comando(variável)` : para alocar o comando em uma variável

## Random
- Biblioteca para mexer com SemiAleatoriedades/Resultados aleatórios baseados em dados existentes no código 

- Para gerar um conteúdo semiAleatório:
![[Pasted image 20250406151446.png]]
 (Vai gerar uma 'Senha' de 5 caracteres, com os dados dentro da variável 'senha'. Ex.: kioko, kiooi,  iikki e etceteras)
- Outro comando interessante do random é o `random.shuffle(lista)`, ele embaralha as variáveis de dentro da lista, trocando elas de posição/ordem 
- O comando `random.randint(de numero tal , até numero tal)` serve para gerar um número aleatório porém com limites definidos

## Datetime
 - A biblioteca Datetime auxilia o código com a questão de Horários/Datas, as atuais em específico. Ex.:  
  ![[Pasted image 20250406154536.png]]

## Time
- Biblioteca usada para definir espaços de tempo entre um comando e outro. Ex.:
 ![[Pasted image 20250406155701.png]]

## String
- Biblioteca de Caracteres em String. Ex.:
Chamar:
 ![[Pasted image 20250406155930.png]]
Vai printar:
 ![[Pasted image 20250406155952.png]]
## Urllib e Urllib.request
- Serve para funções que utilizam sites reais
- Ex. de uso: Verificar se um site está Aberto/Funcionando
 ![[Pasted image 20250320092808.png]]
## Regex
- **Regex** é uma técnica que permite buscar e manipular textos baseados em padrões. Você pode usá-lo para identificar palavras-chave, validar formatos, ou até para extrair dados de frases.
- Como usar o Regex:
![[Pasted image 20250603210952.png]]
- É obrigatório usar o `r` na frente dos padrões pro `regex` funcionar
- Padrões básicos:
 ![[Pasted image 20250603211041.png]]
 ![[Pasted image 20250603215049.png]]
 ![[Pasted image 20250603215107.png]]
- Funções interessantes com Regex:
![[Pasted image 20250603211116.png]]

## FuzzyMatching
- O **Fuzzy Matching** é uma técnica que permite comparar strings de forma imprecisa (levando em conta erros de digitação ou variações). Para isso, a biblioteca mais usada em Python é o **`fuzzywuzzy`**.
- Modo de uso do Fuzzy Wuzzy:
![[Pasted image 20250603211843.png]]
- Funções importantes:
![[Pasted image 20250603211914.png]]


# TRATAMENTO DE STRINGS

 (==DICA==: Os exercícios da aula 9 (Curso de python mundo 1) contém resoluções que podem ajudar na fixação/aprendizagem dos comandos) 
 (==DICA2==: Os comandos podem ter variações de funcionamento quando colocadas as letras ==R== ou ==L== na frente (fazem o comando funcionar apenas para a direita ou para a esquerda))
 - --
## Print
- Para escrever um texto ==grande== em python, é recomendável usar ==3 aspas==:
 ![[Pasted image 20250217092312.png]]
- Para centralizar uma palavra:
 ![[Pasted image 20250218083006.png]] 
 Ou
 ![[Pasted image 20250406145904.png]]
 Resultado: 
  ![[Pasted image 20250218083038.png]]
- Para chamar um variável dentro de um print:  
 ![[Pasted image 20250406150121.png]]
 - Função interessante pra se usar em prints longos: 
 ![[Pasted image 20250512093554.png]]
 O `sep='-'` vai adicionar algum caractere de sua escolha para ser o separador das palavras, letras dentro de uma string. Interessante para datas e etc.
 - Função interessante pra não salvar um número caso o python tire o `0` dele:
 ![[Pasted image 20250615202305.png]]
 O `ZFILL` vai incrementar zeros no espaço que falta da string (só funciona em strings, se for usar em int, vai ter q transformar ele em str primeiro)
 Ex.:
 numero = '2'     | numero2 = '2'
 numero.zfill(2)   | numero2.zfill(5)
 numero == '02' | numero2 == '00002'
## Fatiamento
- O fatiamento de strings serve para usar partes específicas de uma Frase/Código etc. 
- Para fatiar uma string é bem simples, se ela estiver dentro de uma variável faça o seguinte: 
`print(variável=[numero referente a letra em que vai começar : numero referente a letra em que vai terminar :  numero de casas q irão ser puladas])
Ex.:
   ![[Pasted image 20250406161035.png]]
  
## Análise

- O comando `len(variável ou frase)` vai verificar quantas letras a string possui.
- O comando `variável ou frase.count('letra desejada')` vai procurar quantas letras iguais a letra desejada existem dentro da string e vai contar. 
  Esse comando pode ser fatiado: `frase.count('letra',numero referente a letra em q vai começar, numero referente a letra em q vai terminar)`
- O comando `variavel ou frase.find("palavra desejada")`, funciona como o comando de cima, a diferença é que ele caça a palavra e ao invés de contar, ele mostra em qual momento da string ela começou. Se a palavra não existir dentro da string, esse comando retorna o valor `-1`
- Comando ==in==: `'palavra' in variavel ou frase`, vai questionar se a palavra escrita existe ou não dentro da string, retorna false ou true
  Um uso interessante para esse comando é:
  ![[Pasted image 20250217083143.png]] 
  EX.: Se o nome for algum desses acima: Ana, claudia, jessica ou juliana, o programa vai reconhecer e dar o print 
## Transformação

- Comando `variavel ou frase.replace('palavra que existe na string','palavra q vai entrar no lugar da que existe')`: esse comando vai substituir um palavra existente por uma de sua preferência. OBS: ele não vai substituir na variável diretamente, apenas quando o comando for chamado, de forma superficial.
- Os comandos `.upper()` ou `.lower()` são autoexplicativos (transforma tudo em maiusculo ou minusculo)
- O comando `.captalize()` vai fazer a frase inteira ficar em minusculo e deixar em maiusculo somente a primeira letra da frase (ex.: Curso em video)
- O comando `.title()` é basicamente o comando de cima, a diferença é que ele vai fazer esse esquema a cada vez q houver um espaço (ex.: Curso Em Video)
- Comando `.strip()` vai remover todos os espaços inuteis do início e/ou fim da frase. Existem variações desse comando, o `Rstrip()` e o `Lstrip()`, eles fazem exatamente a mesma coisa, só q o R vai fazer o trabalho pela direita somente, e o L vai fazer somente pela esquerda
## Divisão

- O comando `.split()` vai separar cada palavra da frase e transformar elas em strings próprias. Ou seja: toda vez q houver um espaço, a palavra a seguir se torna uma string nova (Pra ir pro ultimo objeto da lista direto: é só colocar -1)

## Junção

 - O comando `'-'.join(frase ou variavel)` vai espaçar toda palavra utilizando oque estiver dentro das aspas
 Ex.:
 ![[Pasted image 20250406165843.png]]
 
# CONDICIONAIS
 - Os comandos `if, elif, else` podem ser usados de diversas maneiras, geralmente são comandos primordiais que aplicam lógica no seu código
 Ex.:
 `if variável == 10:
	 `print('X')
 `elif variável == 5:
	 `print('V')`
`else:
	`print('A variável não é igual a 10 e nem a 5')`

O if vai fazer uma pergunta, caso a variável não responda corretamente, o elif vai perguntar outra coisa pra variável, se a variável também errar, ele vai executar o else

---
 - Algo interessante a ser lembrado é que o comando pode ser escrito em apenas uma linha se for o caso de uma atividade mais simples. Ex.: print('escreva algo' if condição <=3 else 'escreva algo2')
 - Condicional interessante a ser usada: `MATCH E CASE`
 Exemplo de uso:
 ![[Pasted image 20250616225220.png]]
 No comando `match` você atribui a variável que vai ser modelo de comparação
 No `case`, você vai colocar a condicional ( caso ação == start: print(iniciando))
# COMANDOS DE REPETIÇÃO (Iteradores)

## FOR IN
 - Uso mais comum:
![[Pasted image 20250218101006.png]] 
 É auto explicativo, vai rodar a palavra 'oi' 10x

- Caso precise fazer uma contagem de números:
 ![[Pasted image 20250218101459.png]]

-  Caso precise de uma contagem regressiva:
![[Pasted image 20250218101649.png]]

- O for in consegue receber variáveis, tuplas, listas, dicionários (iteráveis)
Ex.:
 ![[Pasted image 20250227095841.png]]
 E assim também: 
 ![[Pasted image 20250227100133.png]]
 
- Caso eu queira mostrar a posicâo dos itens dentro de um iterável: ![[Pasted image 20250227100908.png]]

O de baixo é bem mais compacto e profissional, bom para projetos grandes e complexos

## WHILE
- O while não é nada mais nada menos que um loop, que vai rodar mediante uma condicional. Ex.:
`While True:` == Enquanto o while não receber um `Break`, ele vai rodar infinitamente
`While Variável != 10:` == Enquanto a variável for diferente de 10, ele vai continuar rodando

- O while é muito útil para programas em terminal, mas em libs gráficas como o CustomTKinter, ele não funciona muito bem pois entra em conflito com o loop da janela, nesse caso, geralmente o for é mais usado


# VARIÁVEIS DE ARMAZENAMENTO

Dicas:
- Para desempacotar algum iterável, use `*` na frente da variável de armazenamento. Ex.:
![[Pasted image 20250521080824.png]]
## TUPLAS
- ![[Pasted image 20250227093406.png]]
- variável = ( 'tupla', 'tupla', 'tupla' )
- caso eu queira organizar a ordem da tupla:
- ![[Pasted image 20250227101401.png]]
- resp: ![[Pasted image 20250227101454.png]]
- Caso eu queira somar as tuplas e transformar em uma só:
- ![[Pasted image 20250227101806.png]]
- resp: ![[Pasted image 20250227101826.png]]

- Caso eu queira procurar um numero ou palavra específica na tupla: ![[Pasted image 20250227102256.png]]
- Caso eu queira saber quantas vezes aparece  um elemento:
- ![[Pasted image 20250227102337.png]]
- As tuplas aceitam Palavras e números juntos: ![[Pasted image 20250227102511.png]]
- Gerador de números aleatórios na tupla, ele printa sem os colchetes e aspas: ![[Pasted image 20250228091440.png]]
- Para saber o menor e o maior valor sem dor de cabeça: ![[Pasted image 20250228091634.png]]
- O ==EX05 AU16.py== é uma boa aula para ser estudada, pois apresenta conceitos estéticos usando uma tupla:
- ![[Pasted image 20250228094505.png]]
- Cada palavra pode pode ser considerada uma 'Lista', oque permite fazer coisas parecidas ao ==exercício 6 da aula 16==:
- ![[Pasted image 20250228100135.png]]
- As tuplas podem ser criadas com base em outras:
![[Pasted image 20250422092155.png]]



## LISTAS
- variável = ['Lista', 'lista', 'lista']
- ==AS LISTAS SÃO MUTÁVEIS==
- Para criar um elemento novo na lista, é só usar: ![[Pasted image 20250303092324.png]]
- O comando ==append== vai adicionar o elemento diretamente no final da lista. Se a lista tinha 3 espaços, agora ela vai ter 4
-  Para adicionar um item em uma posiçâo específica sem excluir os itens já existentes (ele vai reposicionar todos automaticamente), o comando ==insert== é o mais recomendado: ![[Pasted image 20250303092700.png]]
- Para remover itens de listas existem os comandos: ![[Pasted image 20250303093122.png]]
- Caso eu precise ==Organizar== uma lista: ![[Pasted image 20250303093554.png]]
- Caso eu precise ==Organizar de Trás pra frente==: ![[Pasted image 20250303093650.png]]
- Para criar uma lista cópia de outra lista, é só fazer desse jeito:
- ![[Pasted image 20250303101303.png]]
==OU== usar: ==ListaNome.copy()==
- como é uma ==lista composta:==
- ![[Pasted image 20250305091417.png]]

### List Comprehension
- Uma sintaxe mais curta para criar uma lista com base em uma lista já existente no código
- Sintaxe: `novaLista = [expressão for item in interable if condition == True]`
- Ex. de Uso:
![[Pasted image 20250421090543.png]]

Ex.2:
![[Pasted image 20250421091437.png]]

Ex.3 e 4:
![[Pasted image 20250421092803.png]]
## DICIONÁRIOS
 - variável = {'dicionário', 'dicionário', 'dicionário'}
 - Como declarar um dicionário:
 - ![[Pasted image 20250307083707.png]]
 - Para ==adicionar um elemento no meio do código==, o dicionário não usa o append, ele usa:
 - ![[Pasted image 20250307084129.png]]
 - Para remover elementos:
 ![[Pasted image 20250307084529.png]]
 
 - Para deletar um item de dicionário dentro de um iterável (for, while etc):
 Use um `list` antes do dicionário. Ex.:
 ![[Pasted image 20250615221649.png]]
 E caso for fazer essa técnica dentro de um JSON, lembre-se de carregar o dicionário antes de excluir o item e de salvar logo após. Ex.:
 ![[Pasted image 20250615221748.png]]
 
 - O . ==values()== vai printar apenas o conteúdo das chaves. o .==keys()== vai printas apenas as chaves. O .==items()== vai printar tudo de uma vez:
 - ![[Pasted image 20250307084909.png]]
 - Complemento sobre Keys, Values e Items:
 ![[Pasted image 20250423101047.png]]
 ![[Pasted image 20250423101012.png]]
 
- ==Dá pra colocar dicionários dentro de listas e tuplas, e vice versa.==
- Quando precisar organizar um dicionário, usar o ==ITEMGETTER==
- ![[Pasted image 20250310093730.png]]
- Método para apresentar um dicionário de maneira organizada:
![[Pasted image 20250422103018.png]]
- Como saber se um item está presente no dicionário ou em alguma chave do dicionário:
![[Pasted image 20250422104338.png]]
- Comando `SetDefault`
![[Pasted image 20250423094633.png]]
Vai adicionar a chave e o item caso não existam no dicionário. Caso exista, não vai fazer nada.
- Update
![[Pasted image 20250423095052.png]]
Vai pegar o segundo dicionário e adicioná-lo ao primeiro, os tornando apenas um só
Atualizando.
- Copy e DeepCopy:
### `copy.copy()` (cópia rasa ou **shallow copy**):

- Cria uma nova **referência de alto nível** (cópia do objeto "de fora"), mas **mantém as referências internas iguais**.
- Ou seja, se você copiar uma lista com outras listas dentro, essas listas internas continuam apontando pro mesmo lugar.

```python
import copy

original = [[1, 2], [3, 4]]
copia_rasa = copy.copy(original)

copia_rasa[0][0] = 99
print(original)  # [[99, 2], [3, 4]]  => o original foi afetado!
```
### `copy.deepcopy()` (cópia profunda ou **deep copy**):

- Cria **uma cópia completa**, incluindo todos os objetos internos recursivamente.
- As mudanças na cópia não afetam o original.

```python
import copy

original = [[1, 2], [3, 4]]
copia_profunda = copy.deepcopy(original)

copia_profunda[0][0] = 99
print(original)  # [[1, 2], [3, 4]] => o original permanece intacto
```
### Quando usar:

- Use `copy()` quando estiver trabalhando com objetos simples ou não se importar que objetos internos sejam compartilhados.
- Use `deepcopy()` quando quiser garantir que **nenhuma parte da estrutura original será modificada** pela cópia.
## SET
- É um modo de armazenamento que não salva palavras repetidas
- Usa chaves, igual aos dicionários
- Ex.:
![[Pasted image 20250422092857.png]]
Vai printar: `{'melancia','banana','uva','maça'}`
- Sempre vai printar em ordem aleatória 
- Não funciona o fatiamento e nem indexação
- Funciona: perguntar se um item está nessa lista. 
Ex.: `('maçã' in cesta)`
Resp.: `True`
- Existem diversas funções:
![[Pasted image 20250422094027.png]]
- Para fatiar uma palavra e ver suas letras, pode também se usar o método *set*:
![[Pasted image 20250422094855.png]]
O método não ordenas as letras, apenas as mostra
- Da pra usar listComprehension aqui:
![[Pasted image 20250422095420.png]]
# FUNÇÕES

## Função Def
- Como criar uma função?
Use o comando: `def nome_função():`
- As funções podem receber diversos parâmetros dentro dela, parâmetros opcionais e parâmetros obrigatórios
Ex.:
Função com parâmetro obrigatório: `def nome_função(texto):`
Função com parâmetro opcional: `def nome_função(texto='O texto não foi digitado'):`

- Como chamar a função?
Use: `nome_função()`
Caso a função tenha parâmetro obrigatório, não esqueça de colocar algo pra função receber. Ex.: `nome_função('Digitei um texto')`

- Qual é a diferença de funções que executam algo pra funções que retornam valores?

Exemplo de função que retorna valor:
`def nome_func():`
	`dados = 2077`
	 `return dados`
`número_func = nome_func()`
`print(número_func)` 
Vai imprimir no terminal o número retornado pela função: 2077

Exemplo de função que executa algo:
`def nome_func():`
	`dados = 2077`
	 `print(dados)`
`nome_func()`
Vai imprimir o número 2077 assim que a função for executada

## Lambda
- É uma função Anônima, não tem nome
- Recebe quantos parâmetros forem necessários, porém só podem executar uma única função
- Sintaxe: `lambda parâmetro(s) : expressão`
Ex.: `X = lambda a:a*3`
	`print(x(4))`
ou
Ex.2: `soma = lambda a,b:a+b` 
(`a,b` são os parâmetros que a lambda vai receber)(`:` é igual  "Vai retornar")(`a+b` é oque a função vai executar)
## Variáveis que são funções (Datado)
- São funções criadas a partir de variáveis
- Não é muito usado nos dias atuais pois não aceitam códigos complexos, como o Def por exemplo, que aceita parâmetros e etc.
 ![[Pasted image 20250225102237.png]]
 ex.: exec(ponto) vai executar o comando dentro das aspas de ponto
# TRANSFORMAR CÓDIGO EM .EXE
- Seção a ser editada futuramente, por enquanto vai ter apenas os códigos a serem colados no terminal

lembrar de executar esse programa dentro da pasta em que o código se encontra, o ícone tem q estar em formato .ico e também tem que estar na pasta

`pyinstaller --onefile --windowed(caso queira sem o terminal) --icon=meu_icone.ico nome-do_programa.py`

- Para adicionar imagens:
`pyinstaller --add-data "imagens/foto.png;imagens" seu_programa.py`
# HELP()

- O comando ==help()== é uma ótima pedida quando se quiser aprender alguma função nova e aprender mais sobre a linguagem:
 ![[Pasted image 20250313085643.png]]
- Também existe outra maneira de aprender sobre os comandos, é só por:
 ![[Pasted image 20250313090045.png]]
(Input pode ser trocado por qualquer outro comando)
- Para ==Documentar== uma função criada é só utilizar uma docstring:
 ![[Pasted image 20250313091145.png]]


# TRATAMENTO DE ERROS

- ![[Pasted image 20250319084551.png]]
- Serve para identificar problemas e deixar o programa mais apresentável caso dê algum erro:
- ![[Pasted image 20250319085130.png]]
-  o ==finally== vai funcionar independente se o programa der erro ou não
- ![[Pasted image 20250319085640.png]]
- Para saber qual problema em específico ocorreu:
- ![[Pasted image 20250319090153.png]]
- Caso queira especificar uma mensagem para um problema em específico:
- ![[Pasted image 20250319090557.png]]
- ![[Pasted image 20250319090812.png]]
- Como lançar erros de propósito no programa:
![[Pasted image 20250530100902.png]]
Use o comando `Raise` + o erro que você quer lançar OU uma string de sua escolha

# ARQUIVO
 - Métodos de arquivo:
 Read(`num de elementos`), Readline()  -  Open()
 Read(), Readlines()  -  
- Ex. de uso dos métodos de ler (read):
![[Pasted image 20250425074038.png]]
- Como Chamar um arquivo:
`Nome-do-arquivo = open('arquivoname.txt(pode ser txt, json e qualquer formato q for trabalhar)' , 'r' )`
 
A letra `R` vai servir para ler o arquivo

- Como Fechar um arquivo:  
`with open('arquivoname.txt (ou outros)' , 'w' ) as arquivo_file (é um nome simbólico):
	 `arquivo_file.write(conteúdo a ser salvo)`

 A letra `W` vai servir para escrever no arquivo
`
- Como Editar um arquivo existente:
`with open('arquivoname.txt (ou outros)' , 'a' ) as arquivo_file (é um nome simbólico):
	 `arquivo_file.write(conteúdo a ser salvo)`

A letra `A` vai servir para adicionar o conteúdo no arquivo sem apagar o anterior

- Como ler quantas palavras tem em um arquivo:
 ![[Pasted image 20250425074517.png]]
 Vai retornar o número de palavras no arquivo.

Use o método `SET` para poder filtrar palavras repetidas:
![[Pasted image 20250425074936.png]] 
Vai retornar apenas o número de palavras diferentes, sem palavras repetidas
- Exercício Interessante para ser usado em programas:
![[Pasted image 20250426090814.png]]
Vai Gerar um log toda vez que o usuário conectar, informando data e hora. Fica mais interessante se adicionar mais funções.
# JSON

Tutorial da net: https://medium.com/@renatojlelis/trabalhando-com-json-no-python-1eb0f97c0c50

==JSON: Explicado e Resumido por ChatGPT:==
### **1. O que é JSON?**

**JSON (JavaScript Object Notation)** é um formato de texto leve para armazenar e transmitir dados estruturados. Ele é baseado em pares **chave:valor** e listas de dados.

Exemplo:

![[Pasted image 20250507105030.png]]
---

### **2. JSON em Python — o módulo `json`**

Python tem um módulo embutido chamado `json` para manipular dados JSON:

`import json`

---

### **3. Serializar (Salvar JSON em arquivos ou texto)**

### a) `json.dump()` → Salvar diretamente em um arquivo:

![[Pasted image 20250507105114.png]]

- `indent=4`: deixa o arquivo bonito (legível)
    
- `ensure_ascii=False`: permite acentuação e caracteres especiais no JSON
    

### b) `json.dumps()` → Converte em string JSON (útil pra enviar via API, por exemplo)

![[Pasted image 20250507105156.png]]

#### Oque é uma string JSON?
Uma **string JSON** é um **texto formatado de acordo com as regras do JSON** (JavaScript Object Notation). Ou seja, é uma **representação textual de dados estruturados** — como dicionários e listas — em um formato padronizado, que pode ser salvo em arquivos ou enviado entre sistemas.

### Exemplo de string JSON:

![[Pasted image 20250507111055.png]]

Note que:

- É uma **string normal** (entre aspas simples ou duplas no Python).
    
- Mas seu conteúdo está em **formato JSON válido**.
    

### Pra que serve?

- É usada para **trocar dados entre sistemas** (por exemplo, entre um backend e frontend).
    
- Permite **salvar dados** de forma padronizada em arquivos `.json`.
    

### Como usar em Python:

Você pode **converter uma string JSON para dicionário Python** com `json.loads()`:

![[Pasted image 20250507111152.png]]

E o contrário: transformar um dicionário em string JSON:
###### ![[Pasted image 20250507111210.png]]
---

### **4. Desserializar (Carregar JSON de arquivos ou texto)**

### a) `json.load()` → Lê direto de um arquivo

![[Pasted image 20250507105214.png]]

### b) `json.loads()` → Converte uma string JSON para dicionário

![[Pasted image 20250507105254.png]]

---

### **5. Erros comuns e tratamento**

### a) Arquivo inexistente:

![[Pasted image 20250507105317.png]]

### b) Arquivo corrompido ou vazio:

![[Pasted image 20250507105330.png]]
---

### **6. Atualizar dados no JSON**

![[Pasted image 20250507110039.png]]

---

### **7. `w`, `w+`, `a` — diferenças no modo de abrir arquivos**

- `'w'`: sobrescreve o arquivo (zera tudo antes de escrever)
    
- `'w+'`: sobrescreve e também permite leitura
    
- `'a'`: adiciona ao final do arquivo (sem apagar o conteúdo)
    

No JSON, usamos mais o **`'w'`** (para sobrescrever o arquivo com os dados atualizados). Evite `'a'` com JSON, porque JSON só pode ter **um único objeto ou array raiz**, e o `append` quebra o formato.

---

### **8. Exemplo completo de ciclo JSON:**

![[Pasted image 20250507110151.png]]

---

### **9. JSON com listas de objetos**

![[Pasted image 20250507110211.png]]

---

### **Resumo prático: quando usar o quê**

| Tarefa                              | Função         |     |
| ----------------------------------- | -------------- | --- |
| Salvar JSON em arquivo              | `json.dump()`  |     |
| Carregar JSON de arquivo            | `json.load()`  |     |
| Converter dicionário em string JSON | `json.dumps()` |     |
| Converter string JSON em dicionário | `json.loads()` |     |
==Daqui pra baixo, foram informações sem ChatGPT==
## Usando JSON para ler API´s 
Vídeo usado para a aprendizagem [Aqui](https://www.youtube.com/watch?v=-e7Jh2Cy3Os)
Site de API´s de fácil acesso [Aqui](https://docs.awesomeapi.com.br)

- Requisitando uma API na prática:
![[Pasted image 20250507094815.png]]
Vai usar o `Import requests` para extrair a API fornecida, e editar as informações no link depois de copiá-lo (EX.: Eu coloquei meu cep no final do link pro código poder pesquisar ele)
O `Print` tem que ter o `.json()` pra ele poder imprimir o conteúdo da API, se não, ele só vai printar um Código: 
`200` == Funcionou direitinho
`404` == Deu erro
- A resposta que o código vai gerar:
![[Pasted image 20250507095301.png]]
![[Pasted image 20250507095324.png]]
![[Pasted image 20250507095338.png]]
- Ou você pode formatar o código pra printar de um jeito mais agradável:
![[Pasted image 20250507095701.png]]
 ![[Pasted image 20250507095720.png]]

# VENV - Ambientes Virtuais

- Ambientes virtuais são uma forma de fazer o seu código ser 'portátil', ou seja, usá-lo em outras máquinas sem maiores empecilhos, sem ficar instalando biblioteca por biblioteca e refazer na mão configurações específicas.

- Como criar um Ambiente Virtual?
Use o seguinte código no terminal (dentro da pasta do seu código, ou de preferência, dentro do terminal da sua IDE (VScode e afins)):
`python -m venv venv`

- E se eu criar um ambiente virtual em um código já Existente?
Antes de criar o venv, use: `pip freeze > requirements.txt` no terminal. Esse código vai detectar todas libs que o projeto ta usando e vai salvar dentro do txt.

Depois de ativar o venv, use: `pip install -r requirements.txt`. O comando vai instalar todas as libs do requirements.txt pra dentro do venv

OBS: Sempre que terminar o proj, user o `pip freeze > requirements.txt` pra salvar as libs instaladas depois do ultimo comando

- Como eu ativo o Ambiente?
Bom, no powershell, terminal da Windows, que eu usei dentro do VScode
O comando é esse: `.\venv\Scripts\Activate.ps1`

Se der algum erro, vale pesquisar pra tentar resolver
- E como eu desativo?
Use o comando `deactivate` no terminal/powershell
O terminal vai voltar a usar o Python Global

Caso não funcione, você pode procurar maneiras pra resolver isso, ou, desativar pela própria IDE:
VScode
![[Pasted image 20250619220724.png]]
# POO - Programação Orientada a Objetos
- O python permite trabalhar tanto em POO quanto em programação estruturada
- Os objetos vão ter métodos e atributos
- A classe é um projeto de um objeto, é o rascunho
- Criando uma classe e adicionando um objeto á ela:
![[Pasted image 20250429103218.png]]
- Colocando atributos no objeto diretamente:
![[Pasted image 20250429103401.png]]
- Colocando os atributos na classe:
![[Pasted image 20250429104948.png]]
- Para criar Métodos/Ações para aquela classe:
![[Pasted image 20250429105639.png]]
- Como Criar uma SubClasse:
![[Pasted image 20250429112548.png]]
A subclasse em questão é a 'Anjo' e ela ganha um atributo especial de voar. Ela também pode usar os atributos de 'Pessoa', porquê ela é uma SubClasse direta, ela ganha todos os atributos sem precisar copiar e colar.

- Não é necessário criar uma classe externa apenas para uma habilidade:
![[Pasted image 20250501113146.png]]

- Para criar um SubClasse, não necessáriamente, é preciso de colocar um `def __init__` veja:
![[Pasted image 20250501112410.png]]
O `func2` vai funcionar normalmente, como se fizesse parte da classe empregado
O método construtor (`def __init__`) só entra quando a classe precisa receber algum atributo que a diferencia da outra, igual o exemplo da classe `anjo`

### DECORATOR:
- Você pode criar o seu próprio decorator. Ex.:
![[Pasted image 20250609111222.png]]

Exemplos de decorator:
@property (usado no getter)
@AtributoDeClasse.setter (usado no setter)

- GETTER:
O getter pega o valor de um atributo dado a uma classe

- SETTER:
Modifica o valor pego pelo getter

- Explicação de getter, setter e decorator dada pelo ChatGPT:
**Getters e setters** são métodos usados para acessar (`get`) ou modificar (`set`) atributos privados de uma classe de forma controlada.
Decorator são funções especiais que **modificam o comportamento de outras funções ou métodos**, sem alterar seu código diretamente.  
No contexto de POO, os decoradores `@property`, `@setter` e `@classmethod` são usados para controlar como atributos e métodos são acessados ou modificados.

Exemplo Prático feito por mim:
![[Pasted image 20250430133632.png]]
Oque esse exemplo faz: Caso o usuário, na hora de declarar a altura, declare ela em string (assim: altura = '1.70') o programa vai transformar essa string em um valor Real/Float e então, qualquer cálculo ou função que precise de um valor numérico vindo da altura, não irá dar erro. 

- Na hora de colocar `print(obj_nome)`, geralmente vai printar algo assim: 
![[Pasted image 20250501110934.png]]
Porém, caso queira tratar pra dar uma função/printar uma string customizada quando pedir pra printar o obj diretamente:
![[Pasted image 20250501111140.png]]
O `def __str__(self):` vai fazer o trabalho de customizar essa saída, caso seja interessante ter isso configurado no programa

## Métodos Especiais em POO (Com a Ajuda do ChatGpt):

### Construtor e destrutor
__init__(self, ...)       # Inicializa o objeto ao ser criado
__del__(self)             # Executa algo quando o objeto é destruído

### Representações do objeto
__str__(self)             # Retorna string amigável para print()
__repr__(self)            # Retorna string oficial (debug), ex: no console

### Comparações
__eq__(self, other)       # ==
__ne__(self, other)       # !=
__lt__(self, other)       # <
__le__(self, other)       # <=
__gt__(self, other)       # >
__ge__(self, other)       # >=

### Operadores aritméticos
__add__(self, other)      # +
__sub__(self, other)      # -
__mul__(self, other)      # *
__truediv__(self, other)  # /
__floordiv__(self, other) # //
__mod__(self, other)      # %
__pow__(self, other)      # **

### Operadores inversos (quando o operando está à direita)
__radd__, __rsub__, etc.  # Ex: 5 + obj → __radd__(self, other)

### Operadores unários
__neg__(self)             # -obj
__pos__(self)             # +obj
__abs__(self)             # abs(obj)

### Conversão de tipos
__int__(self)             # int(obj)
__float__(self)           # float(obj)
__bool__(self)            # bool(obj)

### Indexação e slicing
__getitem__(self, key)    # obj[key]
__setitem__(self, key, value)  # obj[key] = value
__delitem__(self, key)   # del obj[key]

### Tamanho e iteração
__len__(self)             # len(obj)
__iter__(self)            # for x in obj
__next__(self)            # next(obj)

### Callable (como função)
__call__(self, ...)       # Permite usar o objeto como se fosse uma função

### Context manager
__enter__(self)           # with obj as x → início do bloco
__exit__(self, exc_type, exc_val, exc_tb)  # Fim do bloco "with"

### Controles extras
__contains__(self, item)  # item in obj
__hash__(self)            # hash(obj), usado para dicionários e sets
__copy__(self)            # copy(obj)
__deepcopy__(self, memo)  # deepcopy(obj)

## Herança
- Um novo objeto (objeto filho) irá herdar as características do obj pai
- Método de criar subclasses

# CUSTOMTKINTER - CTK

## Criando a janela:
- ![[Pasted image 20250331100529.png]]
- Janela 2:
![[Pasted image 20250413201429.png]]
## Configurações básicas:
- ![[Pasted image 20250331100433.png]]
- O comando ==janela.iconify()== é um comando para mandar o código minimizar a janela assim que ele for acionado
- O comando ==janela.deiconify()== é um comando para mandar o código abrir a janela assim que ele for acionado
- Use o comando `janela.destroy()` para mandar o código fechar a janela
- Para adicionar uma imagem no titulo do programa, assim:
![[Pasted image 20250417080709.png]]
Use:
![[Pasted image 20250417080812.png]]
A imagem obrigatóriamente tem que ser `.ico`
## Label - 'Print' do CTK
- Para imprimir uma frase na tela:
`ctk.CTkLabel(janela,text='Texto a ser imprimido', font=('Nome da fonte', Tamanho da fonte)).pack()`
### Fontes para o CTK:
```
System
Terminal
Fixedsys
Modern
Roman
Script
Courier
MS Serif
MS Sans Serif
Small Fonts
Bell Gothic Std Black
Bell Gothic Std Light
Eccentric Std
Stencil Std
Tekton Pro
Tekton Pro Cond
Tekton Pro Ext
Trajan Pro
Rosewood Std Regular
Prestige Elite Std
Poplar Std
Orator Std
OCR A Std
Nueva Std Cond
Minion Pro SmBd
Minion Pro Med
Minion Pro Cond
Mesquite Std
Lithos Pro Regular
Kozuka Mincho Pro R
@Kozuka Mincho Pro R
Kozuka Mincho Pro M
@Kozuka Mincho Pro M
Kozuka Mincho Pro L
@Kozuka Mincho Pro L
Kozuka Mincho Pro H
@Kozuka Mincho Pro H
Kozuka Mincho Pro EL
@Kozuka Mincho Pro EL
Kozuka Mincho Pro B
@Kozuka Mincho Pro B
Kozuka Gothic Pro R
@Kozuka Gothic Pro R
Kozuka Gothic Pro M
@Kozuka Gothic Pro M
Kozuka Gothic Pro L
@Kozuka Gothic Pro L
Kozuka Gothic Pro H
@Kozuka Gothic Pro H
Kozuka Gothic Pro EL
@Kozuka Gothic Pro EL
Kozuka Gothic Pro B
@Kozuka Gothic Pro B
Hobo Std
Giddyup Std
Cooper Std Black
Charlemagne Std
Chaparral Pro
Brush Script Std
Blackoak Std
Birch Std
Adobe Garamond Pro
Adobe Garamond Pro Bold
Adobe Kaiti Std R
@Adobe Kaiti Std R
Adobe Heiti Std R
@Adobe Heiti Std R
Adobe Fangsong Std R
@Adobe Fangsong Std R
Adobe Caslon Pro
Adobe Caslon Pro Bold
Adobe Arabic
Adobe Devanagari
Adobe Hebrew
Adobe Ming Std L
@Adobe Ming Std L
Adobe Myungjo Std M
@Adobe Myungjo Std M
Adobe Song Std L
@Adobe Song Std L
Kozuka Gothic Pr6N B
@Kozuka Gothic Pr6N B
Kozuka Gothic Pr6N EL
@Kozuka Gothic Pr6N EL
Kozuka Gothic Pr6N H
@Kozuka Gothic Pr6N H
Kozuka Gothic Pr6N L
@Kozuka Gothic Pr6N L
Kozuka Gothic Pr6N M
@Kozuka Gothic Pr6N M
Kozuka Gothic Pr6N R
@Kozuka Gothic Pr6N R
Kozuka Mincho Pr6N B
@Kozuka Mincho Pr6N B
Kozuka Mincho Pr6N EL
@Kozuka Mincho Pr6N EL
Kozuka Mincho Pr6N H
@Kozuka Mincho Pr6N H
Kozuka Mincho Pr6N L
@Kozuka Mincho Pr6N L
Kozuka Mincho Pr6N M
@Kozuka Mincho Pr6N M
Kozuka Mincho Pr6N R
@Kozuka Mincho Pr6N R
Letter Gothic Std
Minion Pro
Myriad Hebrew
Myriad Pro
Myriad Pro Cond
Myriad Pro Light
Rosewood Std Fill
Marlett
Arial
Arabic Transparent
Arial Baltic
Arial CE
Arial CYR
Arial Greek
Arial TUR
Batang
@Batang
BatangChe
@BatangChe
Gungsuh
@Gungsuh
GungsuhChe
@GungsuhChe
Courier New
Courier New Baltic
Courier New CE
Courier New CYR
Courier New Greek
Courier New TUR
DaunPenh
DokChampa
Estrangelo Edessa
Euphemia
Gautami
Vani
Gulim
@Gulim
GulimChe
@GulimChe
Dotum
@Dotum
DotumChe
@DotumChe
Impact
Iskoola Pota
Kalinga
Kartika
Khmer UI
Lao UI
Latha
Lucida Console
Malgun Gothic
@Malgun Gothic
Mangal
Meiryo
@Meiryo
Meiryo UI
@Meiryo UI
Microsoft Himalaya
Microsoft JhengHei
@Microsoft JhengHei
Microsoft YaHei
@Microsoft YaHei
MingLiU
@MingLiU
PMingLiU
@PMingLiU
MingLiU_HKSCS
@MingLiU_HKSCS
MingLiU-ExtB
@MingLiU-ExtB
PMingLiU-ExtB
@PMingLiU-ExtB
MingLiU_HKSCS-ExtB
@MingLiU_HKSCS-ExtB
Mongolian Baiti
MS Gothic
@MS Gothic
MS PGothic
@MS PGothic
MS UI Gothic
@MS UI Gothic
MS Mincho
@MS Mincho
MS PMincho
@MS PMincho
MV Boli
Microsoft New Tai Lue
Nyala
Microsoft PhagsPa
Plantagenet Cherokee
Raavi
Segoe Script
Segoe UI
Segoe UI Semibold
Segoe UI Light
Segoe UI Symbol
Shruti
SimSun
@SimSun
NSimSun
@NSimSun
SimSun-ExtB
@SimSun-ExtB
Sylfaen
Microsoft Tai Le
Times New Roman
Times New Roman Baltic
Times New Roman CE
Times New Roman CYR
Times New Roman Greek
Times New Roman TUR
Tunga
Vrinda
Shonar Bangla
Microsoft Yi Baiti
Tahoma
Microsoft Sans Serif
Angsana New
Aparajita
Cordia New
Ebrima
Gisha
Kokila
Leelawadee
Microsoft Uighur
MoolBoran
Symbol
Utsaah
Vijaya
Wingdings
Andalus
Arabic Typesetting
Simplified Arabic
Simplified Arabic Fixed
Sakkal Majalla
Traditional Arabic
Aharoni
David
FrankRuehl
Levenim MT
Miriam
Miriam Fixed
Narkisim
Rod
FangSong
@FangSong
SimHei
@SimHei
KaiTi
@KaiTi
AngsanaUPC
Browallia New
BrowalliaUPC
CordiaUPC
DilleniaUPC
EucrosiaUPC
FreesiaUPC
IrisUPC
JasmineUPC
KodchiangUPC
LilyUPC
DFKai-SB
@DFKai-SB
Lucida Sans Unicode
Arial Black
Calibri
Cambria
Cambria Math
Candara
Comic Sans MS
Consolas
Constantia
Corbel
Franklin Gothic Medium
Gabriola
Georgia
Palatino Linotype
Segoe Print
Trebuchet MS
Verdana
Webdings
Haettenschweiler
MS Outlook
Book Antiqua
Century Gothic
Bookshelf Symbol 7
MS Reference Sans Serif
MS Reference Specialty
Bradley Hand ITC
Freestyle Script
French Script MT
Juice ITC
Kristen ITC
Lucida Handwriting
Mistral
Papyrus
Pristina
Tempus Sans ITC
Garamond
Monotype Corsiva
Agency FB
Arial Rounded MT Bold
Blackadder ITC
Bodoni MT
Bodoni MT Black
Bodoni MT Condensed
Bookman Old Style
Calisto MT
Castellar
Century Schoolbook
Copperplate Gothic Bold
Copperplate Gothic Light
Curlz MT
Edwardian Script ITC
Elephant
Engravers MT
Eras Bold ITC
Eras Demi ITC
Eras Light ITC
Eras Medium ITC
Felix Titling
Forte
Franklin Gothic Book
Franklin Gothic Demi
Franklin Gothic Demi Cond
Franklin Gothic Heavy
Franklin Gothic Medium Cond
Gigi
Gill Sans MT
Gill Sans MT Condensed
Gill Sans Ultra Bold
Gill Sans Ultra Bold Condensed
Gill Sans MT Ext Condensed Bold
Gloucester MT Extra Condensed
Goudy Old Style
Goudy Stout
Imprint MT Shadow
Lucida Sans
Lucida Sans Typewriter
Maiandra GD
OCR A Extended
Palace Script MT
Perpetua
Perpetua Titling MT
Rage Italic
Rockwell
Rockwell Condensed
Rockwell Extra Bold
Script MT Bold
Tw Cen MT
Tw Cen MT Condensed
Tw Cen MT Condensed Extra Bold
Algerian
Baskerville Old Face
Bauhaus 93
Bell MT
Berlin Sans FB
Berlin Sans FB Demi
Bernard MT Condensed
Bodoni MT Poster Compressed
Britannic Bold
Broadway
Brush Script MT
Californian FB
Centaur
Chiller
Colonna MT
Cooper Black
Footlight MT Light
Harlow Solid Italic
Harrington
High Tower Text
Jokerman
Kunstler Script
Lucida Bright
Lucida Calligraphy
Lucida Fax
Magneto
Matura MT Script Capitals
Modern No. 20
Niagara Engraved
Niagara Solid
Old English Text MT
Onyx
Parchment
Playbill
Poor Richard
Ravie
Informal Roman
Showcard Gothic
Snap ITC
Stencil
Viner Hand ITC
Vivaldi
Vladimir Script
Wide Latin
Century
Wingdings 2
Wingdings 3
Arial Unicode MS
@Arial Unicode MS
Arial Narrow
Rupee Foradian
Rupee
DevLys 010
Calibri Light
Monoton
Ubuntu Medium
Ubuntu
Ubuntu Light
Yatra One
HelvLight
Lato
Great Vibes
```

## Botões:
- Para adicionar botões, digite o comando ==ctk.CTkButton(master=janela de origem,text='Texto do botão', command= comando que vai ser executado).place(x= eixo x, y= eixo y )==
- O command só vai executar a função desejada caso essa função seja declarada ==def== antes:
![[Captura de tela 2025-04-01 095214.png]]
- Se puser um `state=disabled`, o botão deixa de funcionar
- Caso você importe os comandos de um Botão de outro bloco `.py`, use a função `lambda`, pro comando não ser executado antes do botão ser clicado. Ex.:
  ![[Pasted image 20250518205712.png]]
## Frames

- Código para criar frames: 
- ![[Pasted image 20250402100443.png]]
- Comandinhos de frame:
- master = janela em que vai aparecer
- width = tamanho horizontal
- height = tamanho vertical
- fg_color='nome da cor em inglês' = cor do frame
- border_color='nome da cor em inglês' = cor da borda
- border_width = tamanho da borda
- bg_color='nome da cor em inglês' = cor das arestas
- corner_radius = define o tamanho das arestas, quanto maior o tamanho, mais o frame fica arredondado
- (existe um atributo chamado 'transparent', basta colocar dentro dos 'color', esse atributo deixa oque foi declarado transparente (as arestas por exemplo))
## Tabview - Abas
- Comando para a criação das abas:
- ![[Pasted image 20250404091416.png]]
- Comandinhos básicos:
- ctk.CTkTabview = cria a tela onde as abas irão ficar
- add('Nome da aba') = cria as abas clicáveis
- Adicionando elementos de texto nas abas:
- ![[Pasted image 20250404092652.png]]
- Para mudar as cores de botão(abas):
- ![[Pasted image 20250404093417.png]]
- (adicione esse comando nos parênteses do CTkTabview)
## Textbox - Caixa de texto
- Comando para a criação de text box:
![[Pasted image 20250408093130.png]]
- Para inserir uma mensagem já programada na textbox:
![[Pasted image 20250408093221.png]]
- Para pegar a mensagem de dentro do txtbox:
![[Pasted image 20250525195338.png]]
## Caixa de diálogo - Dialog
O Dialog só serve apenas para adquirir uma informação de cada vez, não podendo ter duas caixas na mesma tela

- Criando uma caixa de diálogo:
![[Pasted image 20250409091745.png]]
title = 'nome da janela'
text = 'nome em cima da caixa de diálogo'
- Para pegar o conteúdo gerado dentro da caixa de diálogo:
![[Pasted image 20250409092411.png]]
Vai pegar oque foi digitado para usar como uma informação

## Entry - Entrada de informações
- Vai servir para pegar logins, senhas e todo o tipo de informação
- Para pegar a informação de dentro, é só usar o comando `nome-da-entry.get()` (E não pode esquecer de colocar `pass` no final da função)
Ex.: ![[Pasted image 20250410111239.png]]
Esse código acima, vai pegar o `entry` e vai fazer uma `label` dele na tela, ou seja, você vai escrever na caixa de entrada, apertar o botão de enviar e o texto vai aparecer na sua interface
- Para por um texto de espera enquanto a entry estiver vazia, coloque dentro do código do entry: 
`placeholder_text='texto'`
Resultado:
![[Pasted image 20250411102748.png]]
- Para apagar oque está escrito na box da entry:
![[Pasted image 20250411104828.png]]
## Menu de opções - Option menu
- Para criar um menu de opções:
![[Pasted image 20250409101848.png]]
- Para definir uma mensagem no menu antes do usuário escolher algo:
![[Pasted image 20250409102654.png]]
- Para fazer a escolha ser funcional, deve se declarar uma função e depois chamar o command na hora  de criar o menu. Ex.:
![[Pasted image 20250409103215.png]]
A função 'mes' vai receber o value escolhido na interface
## Cores (Todas as cores disponíveis)
  Site para verificação [aqui](https://wiki.tcl-lang.org/page/Color+Names,+running,+all+screens)
![[Pasted image 20250408094834.png]]
![[Pasted image 20250408094844.png]]
![[Pasted image 20250408094853.png]]
![[Pasted image 20250408094903.png]]

## Adicionar Imagens ao programa
- Primeiramente, importe a biblioteca `PIL`
`from PIL import image`
- Caso não tenha essa biblioteca, instale pelo PIP: `pip install pillow`
- Agora, coloque a foto que você deseja usar na pasta onde seu código está (para facilitar)
- Dê uma variável para essa imagem:
`img = ctk.CTkImage(Image.open('./nome-da-imagem.png'))`
- Depois é só chamar a variável da imagem em algum lugar:
Ex. do Botão:
![[Pasted image 20250411100801.png]]
Resultado:
![[Pasted image 20250411100821.png]]

## Slider - Barra de Volume
- Para criar um slider:
![[Pasted image 20250414095837.png]]
- Para conseguir retirar um valor, informação do slider:
![[Pasted image 20250414100123.png]]
Vai criar uma função e depois vai colocar `command=nome-da-função` dentro das configurações do slider
Esse exemplo, vai imprimir valores de 0 a 100 no terminal, conforme você deslize o slider

## Segmented Button - Múltipla Escolha
- Ex. de Segmented Button:
![[Pasted image 20250415091319.png]]
- Como fazer um:
![[Pasted image 20250415091341.png]]
- Para deixar uma opção setada antes de executar o programa, use:
![[Pasted image 20250415092305.png]]
- Para poder usar cada botão com uma função diferente, crie uma função e bote o parâmetro 'Value' dentro dela, aí depois só usar if,else comparando com os valores setados:
![[Pasted image 20250415092927.png]]
## Switch - Liga/Desliga
- Para criar um Botão de Switch:
![[Pasted image 20250415095646.png]]
- Para dar uma funcionalidade a ele:
![[Pasted image 20250415101052.png]]
Vai imprimir `O switch está: Ativado` quando estiver ON e `O switch está: Desativado` quando estiver OFF.

## CheckBox - Caixinhas de Escolha
- Como criar um CheckBox:
![[Pasted image 20250416090631.png]]
- Como dar funcionalidade ao CheckBox:
![[Pasted image 20250416090657.png]]
Nessa função, assim que o usuário escolher o checkbox de 'Comida', vai printar no terminal: 'O usuário escolheu comida'
- Funciona de maneira semelhante ao switch
## Radio Button - Botões de escolha
- Como criar um Radio Button:
![[Pasted image 20250416093428.png]]
- Como dar funcionalidade ao Radio Button:
![[Pasted image 20250416093700.png]]
Nessa função, vai printar '1' no terminal se for Masculino e '2' se for Feminino
- É interessante sempre ter mais de um
- Não é possível deixar desmarcado depois que escolhe

## Progress Bar - Barra de progresso
- Como criar uma Progress Bar:
![[Pasted image 20250417090202.png]]
- Como fazer a Progress Bar funcionar:
Para uso contínuo (a animação fica se repetindo eternamente): `barra.start()`
Caso precise pará-la: `barra.stop()`
Para downloads, ou progresso regulado: `barra.step()`

## Variáveis de Posicionamento
### Pack()
- Serve mais para testes, não precisa configurar, vai colocar sempre abaixo do último widget
### Place()
- O mais utilizado (por mim) em programas completos, fácil de configurar, só usar:
`.place(y=Localização vertical, x=Localização horizontal)`
- Para ter responsividade no redimensionamento da tela:
`.place(rely=Localização em float ex.:0.2, relx=Localização em float ex.: 0.1)`
Essa mudança vai fazer que, na hora que a tela for redimensionada, botar ela em tela cheia e etc, vai fazer que os widgets sejam movidos automaticamente para se ajustar ao tamanho da tela
### Grid()
- Parecido com o place, porém com mais funcionalidades
- Configuração inicial:
![[Pasted image 20250418072649.png]]
O app seria o nome da sua janela principal, etc
- Montagem:
![[Pasted image 20250418071814.png]]
- Row == Linha
- Column == Coluna
- Pady == Eixo `Y`
- Padx == Eixo `X`
- Sticky == Aumenta o widget automaticamente para preencher a linha



# SQLITE3 - Banco de Dados SQL
## Criando Banco de Dados

- Para criar o arquivo `.db`, o banco de dados em si, primeiro você deve importar o sqlite3 no seu código:
![[Pasted image 20250623230708.png]]
E depois usar o comando de `conexão`, esse comando que vai criar o seu banco de dados/arquivo
Ex.:
![[Pasted image 20250623230806.png]]
(O nome 'usuarios.db' pode receber qualquer nome, o importante é estar entre aspas e ter `.db` no final)

## Executando Comandos

### Básico
- O primeiro passo antes de executar quaisquer comando, é criar um cursor
O cursor é oque vai pegar o seu comando e enviar pra sua conexão, seu banco de dados
Ex.:
![[Pasted image 20250624221916.png]]
E para executar seus comandos SQL use:
![[Pasted image 20250624222159.png]]

- Para salvar os dados no banco de dados, use `conexao.commit()` toda vez que fizer uma alteração no Banco (Insert, update, delete etc) (==é uma etapa importante==)
- Para encerrar o código, a conexão com o Banco, use `conexao.close()` após o commit
Ex.:
![[Pasted image 20250624225819.png]]

### Tabelas

 - Para criar uma tabela é semelhante a criar uma tabela em um Banco MySQL tradicional, a diferença é que o código fica dentro do cursor execute
 Ex.:
 ![[Pasted image 20250624222900.png]]
 Vai criar a tabela pessoas SE ela não existir dentro do banco. Isso garante que não crie um tabela do 0 toda vez quer for rodar esse comando no código

- Para inserir dados em uma tabela, use:
![[Pasted image 20250624224903.png]]
Declare os campos que você vai preencher e coloque os valores entre aspas, dentro do `VALUES`

- Para inserir dados de variáveis dentro de uma tabela, coloque `?` dentro de `VALUES`, um pra cada item que você for adicionar, e depois das aspas triplas do comando `EXECUTE`, chame as variáveis
Ex.:
![[Pasted image 20250624232320.png]]


### SELECT - Extrair os dados

- Primeiro vou te mostrar um exemplo básico de como extrair os dados:
![[Pasted image 20250624233210.png]]
Esse é um comando simples de `SELECT`, o que realmente importa aqui é o `cursor.FETCHALL()`
O `FETCHALL` vai buscar todos os dados recebidos da última consulta de select feita e vai retornar em formato de `TUPLA`
Alguns comandos `FETCH` que podem ser úteis:
![[Pasted image 20250624233623.png]]
## Tipos de dados SQLite (Os mais usados)

- ID auto numérico = `INTEGER PRIMARY KEY AUTOINCREMENT` -> Só pode haver um por tabela

- Texto (nome, email...) = `TEXT`	-> Equivale a VARCHAR no MySQL

- Número inteiro = `INTEGER` -> Substitui INT, TINYINT, etc

- Número decimal = `REAL` -> Para valores com casas decimais

- Data/Hora = `TEXT` -> Formato 'YYYY-MM-DD HH:MM:SS'

- Booleano	= `INTEGER` = 1 -> True, 0 = False

- Arquivos binários = `BLOB` -> Para imagens, PDFs, etc



