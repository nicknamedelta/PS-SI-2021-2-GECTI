# Descrição dos Casos de Uso: GErenciador de Chamados de TI - GECTI

## Descrição dos Atores

- `Usuário`: Aquele que se beneficia de forma direta do sistema, assim, cadastrando os chamados para que os técnicos os atendam;
- `Técnico`: É quem recebe e atende os chamados que foram cadastrados pelo Usuário;
- `Administrador`: É o responsável pela manutenção e gerenciamento do sistema;

## Lista e descrição dos Casos de Uso

### CdU 01: Cadastrar um novo chamado
   - **descrição**: O sistema deve permitir o usuário cadastrar um chamado com informações necessárias;
   - **pré-condição**: o usuário deve estar logado ao sistema;
   - **pós-condição**: o chamado será armazenado no sistema e ficará disponível aos demais atores;
   - **fluxo padrão**: o usuário irá clicar em um botão com a ação de cadastrar um novo chamado e irá abrir um formulário para preenchimento dos dados de um novo chamado;
   - **exceção**: o usuário irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 02: Preencher os dados de um novo chamado
   - **descrição**: O sistema deve permitir o usuário preencher o novo chamado com as informações necessárias;
   - **pré-condição**: o usuário deve estar o formulário de novo chamado aberto;
   - **pós-condição**: os dados preenchidos no formulário serão incorporados ao chamado aberto;
   - **fluxo padrão**: o usuário preencherá o título, descrição e atribui as categorias pré-cadastradas que identificaram nesse chamado. Não obstante, o sistema irá vincular os dados do usuário ao chamado; 
   - **exceção**: o usuário irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 03: Listar histórico de chamados
   - **descrição**: O sistema deve permitir o usuário de visualizar em formato de lista os seus chamados anteriores;
   - **pré-condição**: o usuário deve estar logado ao sistema;
   - **pós-condição**: todos os chamados do usuários serão exibidos em uma lista;
   - **fluxo padrão**: é exibida uma lista com todos os chamados do usuário, exibindo todos os dados e possibilitando a edição daqueles chamados que não foram atendidos;
   - **exceção**: caso o usuário não possua chamados será exibido uma mensagem de "Histórico vazio." senão irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 04: Receber identificador de acompanhamento
   - **descrição**: O sistema deve permitir o usuário de receber um identificador para fácil recuperação cada um de seus chamados anteriores;
   - **pré-condição**: o usuário deve ter cadastrado o chamado;
   - **pós-condição**: será informado o identificador;
   - **fluxo padrão**: após cadastrar um novo chamado, será exibido na tela o identificador do chamado;
   - **exceção**: o usuário irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 05: Alterar chamado
   - **descrição**: O sistema deve permitir o usuário de alterar dados de seus chamados;
   - **pré-condição**: o usuário deve ter cadastrado o chamado;
   - **pós-condição**: o chamado terá seus dados alterados;
   - **fluxo padrão**: o usuário irá clicar e alterar os dados que forem permitidos alteração, sendo estes: título, descrição e categorias. Ademais, não é permitido que o usuário altere o estado do seu chamado;
   - **exceção**: o usuário irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 06: Listar chamados de uma empresa
   - **descrição**: O sistema deve permitir o administrador e/ou técnico listar os chamados da uma empresa a qual está responsável;
   - **pré-condição**: o administrador/técnico deve estar logado ao sistema;
   - **pós-condição**: será exibida uma lista ordenada de forma cronológica dos chamados cadastrados;
   - **fluxo padrão**: o administrador/técnico recebe 3 listas de chamados(pendentes, em andamento e concluídos);
   - **exceção**: o administrador/técnico irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 07: Notificar chamados pendentes
   - **descrição**: O sistema deve permitir o técnico de receber uma notificação quando um existir um chamado que ainda não foi concluído;
   - **pré-condição**: o técnico deve estar com um ou mais chamados pendentes;
   - **pós-condição**: o chamado em que o prazo esteja no final será informado;
   - **fluxo padrão**: o chamado pendente ficará em destaque e será notificado caso o prazo final esteja próximo;
   - **exceção**: o técnico irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 08: Atender chamados
   - **descrição**: O sistema deve permitir o técnico atender um chamado, alterando o seu estado;
   - **pré-condição**: o técnico deve estar logado ao sistema e disponível;
   - **pós-condição**: o chamado terá seu estado e/ou prazo alterado;
   - **fluxo padrão**: o técnico altera o estado do chamado para "em andamento";
   - **exceção**: o técnico irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 09: Alterar estado de um chamado
   - **descrição**: O sistema deve permitir o administrador, técnico ou uma ação do sistema alterar o estado de um chamado;
   - **pré-condição**: o administrador deve estar logado ao sistema e o técnico com o chamado "pendente";
   - **pós-condição**: o chamado terá seu estado alterado;
   - **fluxo padrão**: o administrador/técnico clica no chamado e altera o campo com o seu estado;
   - **exceção**: o administrador/técnico irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 10: Gerar relatório de atendimento
   - **descrição**: O sistema deve permitir o administrador gerar relatórios dos atendimentos e a natureza dos chamados;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá gerar o relatório com as informações necessárias e irá disponibilizá-las ao administrador;
   - **fluxo padrão**: o administrador clica em "Gerar Relatório", apresentando as informações necessárias referentes aos chamados atendidos;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 11: Cadastrar empresa
   - **descrição**: O sistema deve permitir o administrador de cadastrar sua empresa, sendo este ambiente o qual os seus funcionários(técnicos e usuários) estarão vinculados;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá armazenar os dados da empresa cadastrada;
   - **fluxo padrão**: o administrador clica em "Cadastrar empresa", assim informando o cnpj, nome fantasia e telefone comercial;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 12: Cadastrar departamentos de uma empresa
   - **descrição**:  O sistema deve permitir o administrador cadastrar departamentos da empresa, assim, definindo também informações inerentes ao departamento;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá armazenar os departamentos cadastrados;
   - **fluxo padrão**: o administrador irá clicar em "Cadastrar departamento" e preencherá um formulário com dados necessários e após validado será cadastrado;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 13: Cadastrar usuários e técnicos de uma empresa
   - **descrição**: O sistema deve permitir o administrador de vincular e gerenciar os usuários da sua empresa e delimitar os técnicos que irão receber os chamados;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá armazenar os dados dos usuários e técnicos da empresa cadastrada;
   - **fluxo padrão**: o administrador clica em "Cadastrar usuários/técnicos", assim informando o nome, email, função e telefone;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 14: Cadastrar tipos e categorias de chamados
   - **descrição**: O sistema deve permitir o administrador de cadastrar os tipos dos chamados e suas categorias;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá armazenar a nova categoria/tipo cadastrado;
   - **fluxo padrão**: o administrador irá cadastrar as categorias e tipos disponíveis para aquela categoria, preenchendo somente o nome ambos;
   - **exceção**: caso já exista a categoria o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 15: Definir prioriade para as categorias de chamados
   - **descrição**: O sistema deve permitir o administrador de definir a prioridade de uma categoria, assim informando ao técnico um prazo esperado para esta categoria;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá armazenar a prioridade da categoria cadastrada;
   - **fluxo padrão**: o administrador irá definir a prioridade para a categoria disponível, preenchendo somente o tempo(em horas) disponível para atender a categoria e o sistema definirá, por meio de uma regra interna, a prioridade("alta, média e baixa");
   - **exceção**: caso não seja validado o valor, o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 16: Gerenciar chamados de uma empresa
   - **descrição**: O sistema deve permitir o administrador de gerenciar os chamados, assim, podendo alterar o seus dados e estados;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o administrador poderá alterar os dados e estados do chamado;
   - **fluxo padrão**: o administrador irá selecionar o chamado, alterar os dados e/ou estado e irá salvar as alterações;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 17: Apresentar estatísticas dos chamados atentidos
   - **descrição**: O sistema deve permitir o administrador de gerar relatórios referentes a estatísticas dos chamados atendidos(e.g. total de chamados de uma categoria);
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá exibir os relatórios gerados;
   - **fluxo padrão**: o administrador irá clicar em "Gerar Relatório" e será gerado um relatório com informações pertinentes ao administrador a respeito dos chamados;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 18: Apresentar frequência dos chamados de uma categoria
   - **descrição**:  O sistema deve permitir o administrador de gerar relatórios referentes a frequência de chamados em uma determinada categoria;
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá exibir os relatórios gerados;
   - **fluxo padrão**: o administrador irá clicar em "Gerar Relatório" e será gerado um relatório com informações pertinentes ao administrador a respeito da frequência dos chamados de uma categoria;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;

### CdU 19: Apresentar tempo médio de atendimento dos chamados
   - **descrição**:  O sistema deve permitir o administrador de gerar relatórios referentes a média de tempo de chamados semelhantes(e.g. média de tempo dos chamados da categoria X);
   - **pré-condição**: o administrador deve estar logado ao sistema;
   - **pós-condição**: o sistema irá exibir os relatórios gerados;
   - **fluxo padrão**: o administrador irá clicar em "Gerar Relatório" e será gerado um relatório com informações pertinentes ao administrador a respeito do tempo médio dos chamados de uma categoria;
   - **exceção**: o administrador irá receber uma mensagem de erro na tela informando a falha do sistema ao realizar a ação;
