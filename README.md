# Blog

Projeto "Blog com CRUD Completo".

### **Requisitos Funcionais**

1. **Gerenciamento de Usuários:**
   - O sistema deve permitir que usuários se cadastrem, façam login e gerenciem suas contas.
   - O sistema deve permitir que um usuário crie, edite e delete seu próprio perfil.

2. **Autenticação e Autorização:**
   - O sistema deve autenticar usuários utilizando JWT.
   - Usuários autenticados devem ter diferentes níveis de permissão (e.g., administrador, usuário regular).
   - Somente usuários autenticados devem poder criar, editar ou deletar posts.

3. **Gerenciamento de Posts:**
   - O sistema deve permitir que usuários criem, editem e deletem posts de blog.
   - Os posts devem ter título, corpo, tags, categoria e data de publicação.
   - O sistema deve permitir que usuários visualizem uma lista de posts e os detalhes de um post específico.
   - Posts devem ser associados a categorias e tags para facilitar a organização e a busca.

4. **Sistema de Comentários:**
   - O sistema deve permitir que usuários comentem em posts.
   - Usuários devem poder editar e deletar seus próprios comentários.
   - O sistema deve exibir uma lista de comentários para cada post.

5. **Categorias e Tags:**
   - O sistema deve permitir que administradores criem, editem e deletem categorias.
   - Os posts podem ser associados a múltiplas tags.
   - O sistema deve permitir a visualização de posts por categorias e tags.

6. **Sistema de Busca:**
   - O sistema deve permitir que usuários busquem por posts usando palavras-chave.
   - A busca deve incluir títulos, conteúdos, tags e categorias dos posts.

7. **Gerenciamento de Arquivos (opcional):**
   - O sistema deve permitir que usuários façam upload de imagens para ilustrar os posts.
   - As imagens devem ser armazenadas e associadas aos respectivos posts.

### **Requisitos Não Funcionais**

1. **Desempenho:**
   - O sistema deve ser capaz de lidar com um grande número de usuários simultâneos sem degradação significativa de performance.

2. **Segurança:**
   - O sistema deve garantir que dados sensíveis, como senhas, sejam devidamente criptografados.
   - Implementar validação e sanitização de dados para evitar ataques de injeção de SQL e XSS.

3. **Usabilidade:**
   - A API deve seguir os princípios RESTful, tornando-a fácil de integrar com front-ends diversos.
   - O sistema deve fornecer respostas claras e detalhadas para erros e exceções.

4. **Escalabilidade:**
   - O sistema deve ser projetado para fácil escalabilidade horizontal e vertical.

5. **Manutenção:**
   - O código deve ser modular e bem documentado para facilitar a manutenção e adição de novas funcionalidades.

### **Casos de Uso**

1. **Cadastro de Usuário:**
   - **Ator:** Visitante
   - **Descrição:** Um visitante cria uma nova conta fornecendo um nome de usuário, email e senha.
   - **Pré-condição:** O visitante deve fornecer um email único.
   - **Pós-condição:** O usuário está registrado e pode fazer login.

2. **Login de Usuário:**
   - **Ator:** Usuário
   - **Descrição:** Um usuário faz login fornecendo seu email e senha.
   - **Pré-condição:** O usuário deve ter uma conta existente.
   - **Pós-condição:** O usuário está autenticado e recebe um token JWT.

3. **Criar Post:**
   - **Ator:** Usuário autenticado
   - **Descrição:** O usuário cria um novo post fornecendo título, conteúdo, categoria e tags.
   - **Pré-condição:** O usuário deve estar autenticado.
   - **Pós-condição:** O post é salvo no banco de dados e fica visível para outros usuários.

4. **Editar Post:**
   - **Ator:** Usuário autenticado
   - **Descrição:** O usuário edita um post existente que ele criou.
   - **Pré-condição:** O usuário deve estar autenticado e ser o autor do post.
   - **Pós-condição:** O post é atualizado no banco de dados.

5. **Deletar Post:**
   - **Ator:** Usuário autenticado
   - **Descrição:** O usuário deleta um post que ele criou.
   - **Pré-condição:** O usuário deve estar autenticado e ser o autor do post.
   - **Pós-condição:** O post é removido do banco de dados.

6. **Visualizar Post:**
   - **Ator:** Usuário ou Visitante
   - **Descrição:** Um usuário ou visitante visualiza a lista de posts ou os detalhes de um post específico.
   - **Pré-condição:** O post deve existir.
   - **Pós-condição:** O post é exibido ao usuário ou visitante.

7. **Comentar em Post:**
   - **Ator:** Usuário autenticado
   - **Descrição:** Um usuário comenta em um post existente.
   - **Pré-condição:** O usuário deve estar autenticado.
   - **Pós-condição:** O comentário é salvo e exibido no post.

8. **Buscar Posts:**
   - **Ator:** Usuário ou Visitante
   - **Descrição:** O usuário ou visitante busca posts por palavras-chave, categoria ou tag.
   - **Pré-condição:** O sistema deve ter posts armazenados.
   - **Pós-condição:** Uma lista de posts correspondentes é exibida.

9. **Gerenciar Categorias (Admin):**
   - **Ator:** Administrador
   - **Descrição:** O administrador cria, edita ou deleta categorias.
   - **Pré-condição:** O usuário deve ter permissão de administrador.
   - **Pós-condição:** As categorias são gerenciadas e atualizadas no sistema.

Esses requisitos e casos de uso são um bom ponto de partida para definir o escopo do projeto e ajudar no desenvolvimento do sistema de blog.
