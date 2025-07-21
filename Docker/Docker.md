- Crie uma Dockerfile (com esse exato nome dentro da sua IDE) e use esses comandos dentro do arquivo:
![[Pasted image 20250721105205.png]]
Para escolher uma outra imagem (ali onde o `FROM` é chamado), vá no site: [dockerfiles python](https://hub.docker.com/_/python)
obs: para validar o código ou fazer um mais ajustado á sua aplicação, recomenda-se o uso de IA

+ Crie um .dockerignore para ignorar itens desnecessários na hora de criar a imagem
Ex.:
![[Pasted image 20250721105606.png]]

- Para criar uma imagem docker, rode esse comando no terminal:
`docker build -t nome-de-preferencia .`

dica: caso dê algum erro, tente trocar a dockerfile/imagem

- Para rodar a imagem docker, use:
`docker run -p 8000:8000 nome-escolhido`