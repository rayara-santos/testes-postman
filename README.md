# Teste de API utilizando o Postman 
<hr>
- api pública <a href="https://gorest.co.in"> gorest.co.in </a>
<hr>

# Cenários automatizados
<hr>
Cenário de Teste: Usuário <br>
1 - Criar usuário <br>
Método: POST <br>
URL: https://gorest.co.in/public/v2/users<br>
Corpo (JSON):<br>
  code{ "name": "Mr. goku", "email": "goku@test", "gender": "male", "status":"active"}<br>
Esperado:<br>
  - Status 201 (Created)<br>
  - Resposta com o mesmo corpo enviado no json<br>

2 - Listar usuário<br>
Método: GET<br>
URL: https://gorest.co.in/public/v2/users<br>
Esperado:<br>
  - Status 200 (OK)<br>
  - Lista com todos os users cadastrados<br>

3 - Atualizar usuário<br>
Método: PUT/PATCH<br>
URL: https://gorest.co.in/public/v2/users/{id}<br>
Esperado:<br>
  - Status Status 200 (OK)<br>
  - Retorno de um get com o item atualizado no top<br>

4 - Deletar usuário<br>
Método: DELETE<br>
URL: https://gorest.co.in/public/v2/users/{id}<br>
Esperado:<br>
  - Status 204 (No Content)<br>
  - Nenhuma resposta no corpo.<br>

<br><br>
Cenário de Teste: Posts e comments <br>
1 - Criar Posts <br>
Método: POST<br>
URL: https://gorest.co.in/public/v2/users/{id}/posts<br>
Corpo (JSON):<br>
  code{ "title":"teste", "body":"i don't know"}<br>
Esperado:<br>
  - Status 201 (Created)<br>
  - Resposta com o mesmo corpo enviado no json + user_id<br>

2 - Criar Comments<br>
Método: POST<br>
URL: https://gorest.co.in/public/v2/post/{idPost}/comments<br>
Corpo (JSON):<br>
  code{ "post":"93273", "name":"Gokuzin", "email":"gokuson@test", "body":"test"}<br>
Esperado:<br>
  - Status 201 (Created)<br>
  - Resposta com o mesmo corpo enviado no json<br>

3 - Atualizar Posts<br>
Método: PUT/PATCH<br>
URL: https://gorest.co.in/public/v2/post/{idPost}<br>
Esperado:<br>
  - Status 200 (OK)<br>
  - Retorno do body com o item atualizado no top + id e user_id<br>

4 - Atualizar Comments<br>
Método: PUT/PATCH<br>
URL: https://gorest.co.in/public/v2/comments/{idComments}<br>
Esperado:<br>
  - Status Status 200 (OK)<br>
  - Retorno do body com o item atualizado no top + id e post_id<br>

5 - Deletar Posts<br>
Método: DELETE<br>
URL: https://gorest.co.in/public/v2/posts/{idPosts}<br>
Esperado:<br>
  - Status 204 (No Content)<br>
  - Nenhuma resposta no corpo.
<br>
6 -Deletar Comments<br>
Método: DELETE<br>
URL: https://gorest.co.in/public/v2/comments/{idComments}<br>
Esperado:<br>
  - Status 204 (No Content)<br>
  - Nenhuma resposta no corpo.<br>

7 - Listar Posts<br>
Método: GET<br>
URL: https://gorest.co.in/public/v2/posts<br>
Esperado:<br>
  - Status 200 (OK)<br>
  - Lista com todos os posts criados<br>

8 - Listar Comments<br>
Método: GET<br>
URL: https://gorest.co.in/public/v2/comments<br>
Esperado:<br>
  - Status 200 (OK)<br>
  - Lista com todos os comentarios criados<br>





