<div> 
<p><a href="https://github.com/JosiTubaroski/WEB-API-com-.NET-8-e-SQL-Server">Home</a></p>
</div> 

<img src="https://github.com/JosiTubaroski/Controllers_Services/blob/main/img/01_Fx_Controller_Interface_Service_2.jpg"/>

# Listar Autor Por ID

### Incluir o Método no AutorService.cs

<img src="https://github.com/JosiTubaroski/Listar_Autor_Por_ID/blob/main/img/AutorService_BuscarID.png"/>

O código define um método assíncrono em C# chamado BuscarAutorPorId, que busca um autor no banco de dados com base no ID informado (idAutor).

#### Explicação do código

- O método <b>retorna</b> um objeto do tipo ResponseModel<AutorModel>.
- Ele usa o <b>Entity Framework</b> para acessar _context.Autores, que deve ser um DbSet<AutorModel>, representando a tabela de autores no banco de dados.
- A busca é feita com FirstOrDefaultAsync, que retorna o primeiro autor com o ID fornecido ou null caso não encontre.
- Se o autor não for encontrado, a resposta contém a mensagem "Nenhum registro localizado!".
- Se o autor for encontrado, os dados dele são armazenados no resposta.Dados e a mensagem "Autor Localizado!" é retornada.
- Se ocorrer alguma exceção, a mensagem de erro será armazenada e Status será definido como false.

#### Fluxo do código

1. Tenta buscar um autor no banco de dados pelo idAutor.
2. Se encontrar → Retorna o autor e uma mensagem de sucesso.
3. Se não encontrar → Retorna uma mensagem informando que não há registros.
4. Se der erro → Captura a exceção e retorna a mensagem de erro.

### Incluir o metodo buscar por iD no AutorControler.cs

<img src="https://github.com/JosiTubaroski/Listar_Autor_Por_ID/blob/main/img/02_AutorController_BuscarId.png"/>


