obs: Eu escrevi as funções dentro de uma classe, então, se quiser replicar o projeto, lembre-se de criar uma classe.
## Imports
- ==SHUTIL==: É uma biblioteca que vai facilitar o processo de enviar os arquivos pras pastas criadas
- ==PATH (de pathlib)==: Vai ser a biblioteca responsável por criar as pastas e verificar o caminho
## Programa
### Inicio
 - Definir um caminho da pasta downloads do sistema, pra operação acontecer lá dentro
 Utilizando a biblioteca `PATH`, escreva:
 `self._downloads = Path.home() / 'Downloads'` 

- Agora você precisa dar um nome as pastas que vão ser criadas e definir os tipos de arquivo que elas vão comportar
Escreva:
`self._pastas = {'NomeDaPasta': ['.tipo', '.tipo2']}`

Exemplo de tipos:
'Imagens': ['.png', '.jpg', '.jpeg', '.gif', '.bmp', '.tiff', '.ico', '.svg', '.webp'],
'Videos': ['.mp4', '.mkv', '.avi', '.mov', '.wmv', '.flv', '.webm'],
'Documentos': ['.pdf', '.docx', '.doc', '.xlsx', '.xls', '.pptx', '.ppt', '.txt', '.rtf', '.odt', '.ods', '.odp'], 
'Audio': ['.mp3', '.wav', '.aac', '.flac', '.ogg', '.wma'],  
'Compactados': ['.zip', '.rar', '.7z', '.tar', '.gz', '.bz2'], 
'Executaveis': ['.exe', '.msi', '.dmg', '.app'],
'ISOs': ['.iso'],
'Outros': []`

### Função para criar as pastas
 Aqui você vai fazer o programa criar as pastas com os nomes que você decidiu, para que, na próxima função o programa organize os arquivos dentro delas
 Escreva dentro da função: 
 `for pasta in self._pastas.keys():`
	 `caminho = self._downloads / pasta`
	 `caminho.mkdir(exists_ok = True)`

### Função organizadora
Vai mover os arquivos para dentro das pastas
Escreva dentro da função:
`for arquivo in self._downloads.iterdir():`
	 `if arquivo.is_file():`
		 `for pasta, extensoes in self._pastas.items():`
			 `if arquivo.suffix.lower() in extensoes`
				 `destino = self._downloads / pasta / arquivo.name`
				 `shutil.move(str(arquivo), str(destino))`
				 `print(f'{arquivo.nome} foi movido para {pasta}') `
				 `break`