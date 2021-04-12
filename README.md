### DESAFIO 2 IMERSÃO FULL STACK E FULL CYCLE

Para rodar esse proejeto vá faça um clone em um diretório, e no terminal do mesmo digite,
 `docker-compose up`

0BS: Devido a inserção de imagens pode aparecer um erro durante o Build, aperte `y` e irá proceder normalmente.

### Desafio - 3 

Informações do desafio
Nesse desafio, você deverá gerar os manifestos yaml do Kubernetes (deployment e service) para o backend e o frontend que criados no desafio 2.


Você NÃO precisa utilizar um Cloud Provider como AWS, GCP e Azure para realizar essa tarefa. Você pode realizar localmente a instalação do cluster utilizando o Kind (https://kind.sigs.k8s.io/).


Crie uma pasta chamada k8s no seu repositório do github (utilizado no desafio anterior) e informe no campo abaixo.

- Executar o servidor: </br>
1 - ` kubectl apply -f k8s/backend/deploy.yml` </br>
2 - ` kubectl expose -f k8s/backend/deploy.yaml` </br>
3 - ` kubectl port-forward service/backend 3000:3000` (aplicação estará rodando na porta 3000) </br>

- Executar a aplicação React: </br>
1 - ` kubectl apply -f k8s/frontend/deploy.yml` </br>
2 - ` kubectl expose -f k8s/frontend/deploy.yml` </br>
3 - ` kubectl port-forward service/frontend 3001:3000` </br>
