## Diagrama do banco de dados

### Filme
- Id (PK)
- Titulo
- DuracaoMinutos
- Genero

### Sala
- Id (PK)
- Nome
- CapacidadeTotal

### Sessao
- Id (PK)
- DataHoraInicio
- DataHoraFim
- FilmeId (FK)
- SalaId (FK)

### Ingresso
- Id (PK)
- SessaoId (FK)
- Preco


### Meu comando para criar o serviço do SQL no docker

sudo docker run -d \
  --name sqlserver \
  -e 'ACCEPT_EULA=Y' \
  -e 'MSSQL_SA_PASSWORD=SUASENHA' \
  -p 1433:1433 \
  -v sqlserver_data:/var/opt/mssql \
  mcr.microsoft.com/mssql/server:2022-latest

### Atualize:

- appsettings.json
- appsettings.Development.json

Para conter uma chave da API do Gemini
"Gemini": {
    "ApiKey": "SUA_CHAVE_GEMIN"
  }

E para conter sua string de conexão
"ConnectionStrings": {
    "DefaultConnection": "Server=127.0.0.1,1433;Database=CinemaDb;User Id=sa;Password=SUASENHA;Encrypt=False;"
  },
