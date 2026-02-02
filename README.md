# 💸 Cont.AI - Seu novo App de Organização Financeira com Vibe Coding

O objetivo deste projeto foi criar um **App de Organização de Finanças Pessoais** com o apoio da IA através de ferramentas como o **Copilot** e o **Lovable**. A ideia era utilizar uma comunicação simples e natural através de **Vibe Coding**, de modo que eu pudesse guiar a IA descrevendo minhas ideias de forma simples, clara e objetiva.


## Problema

Muitas pessoas não conseguem manter um **controle financeiro via aplicativo** porque são exigidas muitas entradas de dados de forma manual, de modo que esse trabalho organização é visto como **tedioso** e até memso **difícil**. 

Sendo assim, quero criar uma solução que permita controlar as finanças por meio de uma **conversa simples com agentes de IA**, semelhante a mensagens de WhatsApp, por exemplo. Ou seja, você conta como tem gastado seu dinheiro no dia-a-dia para o seu **agente de IA** através de um chat e ele **organiza as informações pra você**!


## Etapas do Desafio

### 1. Criar o Prompt

Criei um **PRD (Product Requirements Document)** inicial simplificado, e utilizei o **Copilot** para **refinar** este requerimento. 

O PRD é uma especificação que serve como **_briefing_** para a IA entender a ideia do produto, contendo os **principais pontos** como um contexto, a descrição do problema, o público-alvo, as principais funcionalidades desejadas e o entregável que espero obter da IA.

```txt

# Contexto
Quero criar um aplicativo de Organização de Finanças Pessoais que funcione por meio de conversas com o usuário, utilizando linguagem natural em português.
A ideia é facilitar o controle financeiro de forma simples e natural, sem formulários manuais ou planilhas complexas.

# Problema
Muitas pessoas desistem de controlar seus gastos porque os apps atuais exigem muita entrada manual e pouca personalização. Além disso, em muitos casos as interfaces não são intuitivas, causando dúvidas em iniciantes.
Quero resolver isso com uma experiência de conversa, recomendações automáticas de economia personalizadas, telas e botões intuitivos, e gráficos que consigam sintetizar de forma simples a análise financeira apresentada.

# Público-Alvo
Pessoas ou famílias que querem começar a organizar suas finanças de forma prática e sem complicação, principalmente iniciantes.

# Funcionalidades-Chave

1. Tela de cadastro e login segura

- Acesso mediante e-mail ou telefone (DDD + número).
- Senha forte com pelo menos 8 caracteres, incluindo letras maiúsculas, minúsculas, números e um caractere especial.
- Dois tipos de perfil de acesso possíveis: usuário único ou grupo (família).

2. Registro de transações financeiras via chat

- Entrada dos dados em linguagem natural.
- Data automática no formato dd/mm/aaaa.
- Valor monetário em reais (BRL) acompanhado do símbolo padrão R$.
- Histórico completo das conversas.
- Possibilidade de edição, exclusão ou confirmação do registro informado.

3. Classificação das transações financeiras

- Opção de editar, incluir e excluir categorias.
- Opção de personalizar as cores das categorias (ex.: verde para receita, vermelho para despesa fixa, amarelo para despesa variável, azul para investimentos).
- Categoria de Receita: ex.: salário, aposentadoria, mesada, bônus, transferências bancárias recebidas de terceiros (Pix, TED, dentre outros), rendimento de investimentos, recebimento de aluguéis.
- Categoria de Despesa Fixa: ex.: aluguel, condomínio, plano de saúde, prestação de financiamento, conta de energia, conta de água, conta de internet, conta de gás, taxas do imóvel (IPTU, bombeiros, dentre outros), educação (escola, faculdade, curso, mestrado, dentre outros), doações.
- Categoria de Despesa Variável: ex.: cartão de crédito, compras pela internet (ex.: Amazon, Mercado Pago, Magalu, Shein, Shopee, AliExpress, dentre outros), restaurante, supermercado, padaria, gasolina, estacionamento, roupas e calçados, consertos e manutenções, procedimentos estéticos (ex.: salão de beleza, manicure, depilação, plásticas, botox, dentre outros), lazer (cinema, show, praia, dentre outros).
- Categoria de Investimento: ex.: aplicação no Tesouro Direto, CDB, Ações, Fundos Imobiliários, ETFs, Criptomoedas, Poupança.

4. Gestão familiar

- Funcionalidade válida apenas para o perfil de acesso de grupo (família).
- Mais de um avatar pode ser criado (um para cada pessoa da família).
- Para o perfil de acesso em grupo (família), a classificação das transações financeiras deve conter a identificação do avatar responsável pela transação.

5. Metas financeiras

- Opção de criar, editar e excluir metas.
- Opção de personalizar metas por cores.
- As metas devem ter obrigatoriamente um nome (ex.: "Comprar apartamento"), uma data-alvo no formato dd/mm/aaaa (ex.: 01/12/2028) e um valor-alvo acompanhado do R$ (ex.: "R$ 100.000,00").
- Relatórios mensais e anuais.

6. Agente Financeiro (IA)

- Recomendações educativas e acessíveis.
- Atualização diária, de forma resumida e pontual, sobre os principais índices da economia (ex.: IPCA, SELIC, valor do Dólar e do Euro).

7. Relatórios Simples e Familiares

- Para o perfil de acesso em grupo (família), a exibição dos resultados pode ser segmentada por usuário (avatar) ou consolidada para o grupo.
- Possibilidade de edição do formato de exibição dos gráficos em forma de pizza ou barra.
- Gráficos básicos, com 4 cores principais:

  > Verde → Receitas
  > Vermelho → Despesas fixas
  > Amarelo → Despesas variáveis
  > Azul → Investimentos


# Entregável da IA

Plano de MVP (Produto Mínimo Viável), considerando:

1. Principais Telas

- Tela de Perfil: informações de cadastro e login do usuário (nome, e-mail ou telefone, senha, avatar). Habilitar possibilidade de edição dos dados sensíveis (e-mail, telefone e senha) mediante entrada da senha de acesso do app.
- Tela de Configurações: preferências de layout do app, cores e acessibilidade.
- Tela de Conversa: registro das transações financeiras via chat.
- Tela de Categorias: lista das categorias de transações financeiras já em uso, possibilitando a edição e criação de novas categorias.
- Tela de Metas: exibição gráfica das metas estabelecidas com o nome da meta, a data-alvo, o valor-alvo e o valor parcial arrecadado (exibir tanto o valor monetário parcial arrecadado quanto a representação percentual em relação ao valor-alvo). Possibilidade de edição das metas e criação de novas.
- Tela de Relatórios: visão gráfica consolidada com as 4 cores utilizadas para receitas, despesas fixas, despesas variáveis e investimentos.

2. Validação Inicial

- Teste com usuários de perfis diversos (iniciante, avançado, pessoas com necessidades de acessibilidade).
- Teste com grupo (família) de 3 a 5 membros.
- Métricas:
  > Feedback sobre: clareza do design, acessibilidade, utilidade do app, facilidade de uso e exibição dos dados. Considerar notas em escala de 1 a 10, em que 1 é péssimo e 10 é ótimo.
  > Percentual de transações corretamente vinculadas às categorias.

3. Recursos e características principais do app

- Design Universal.
- NLP (Processamento de Linguagem Natural).
- Flexibilidade no Uso: suporte a texto e voz.
- Interface Intuitiva: linguagem simples e ícones familiares.
- Informação Perceptível: contraste adequado, gráficos coloridos e textos alternativos para leitores de tela.
- Tolerância ao Erro: fácil edição de transações e categorias.
- Baixo Esforço Físico: poucos cliques para acessar relatórios.
- Ar Familiar: design acolhedor, com cores suaves e elementos visuais que remetem à vida doméstica.
- Tom educativo: linguagem acessível, sem jargões financeiros.

```

### 2. Construir com o Lovable

Realizei as seguintes interações com o Lovable:

> Crie um app de finanças pessoais com base no PRD (Product Requirements Document).

> Ative o chat inteligente com IA para classificar transações automaticamente quando o usuário digitar no chat.

> Criar uma nova tela de "Extrato" para armazenar as informações das transações financeiras informadas no chat inteligente. O extrato deve permitir a exibição mensal, trimestral ou por período definido pelo usuário sendo o intervalo máximo de 90 dias. Considere a classificação inteligente das transações financeiras pra identificar corretamente o que é receita (entrada de valor) e o que é despesa (saída de valor).

> Adicionar funcionalidade de editar transações no chat inteligente antes de efetivamente registrar a transação. Apenas após o ok do usuário a transação deve ser devidamente registrada. Além disso, integre o chat inteligente com a funcionalidade de metas, de forma que seja possível criar ou alimentar valores de uma meta através de comandos simples no chat.

> Alterar cor do ícone e da fonte do valor do saldo nas abas "relatorio" e "extrato" para preto. Além disso, na aba "relatório",  subtrair o valor do investimento do montante do saldo, assim como é feito na aba de extrato.
> 
> Por exemplo: se na aba "relatórios" o saldo é de 3000 reais e é registrado um investimento no valor de 500, o saldo deve apresentar o valor de 2500.

> Para o perfil de acesso em grupo (família), a classificação das transações financeiras deve conter a identificação do avatar responsável pela transação. Na aba "extrato" deve ser incluída uma nova coluna "Membro" para identificar o membro da família que realizou a transação informada no chat.
>
> Por exemplo: se no chat inteligente for inserida a frase "supermercado 50 mae", na aba de extrato o registro de 50 reais gastos na categoria supermercado deve ser atribuído ao membro "Mãe", conforme identificação do avatar.

> Ajuste o chat inteligente para que ele seja capaz de processar mais de uma ação através de uma única frase de comando. Por exemplo, se eu escrever no chat "adicione 200 na meta de viagem e lance esse valor como uma despesa de lazer no balanço do mês", duas ações devem acontecer:
> 1. A meta "Viagem de férias" deve ter o seu valor arrecadado ajustado com o acréscimo de 200 reais
> 2. O valor de 200 reais deve ser lançado como uma transação financeira de acordo com sua classificação automática (nesse caso, categoria "Lazer" do tipo "Despesa Variável")

> Possibilitar a edição dos tipos de categoria existentes na aba "Categorias". Isto é, ajuste os tipos de categoria para que seja possível criar nova categoria, editar ou excluir as categorias já existentes de cada tipo de categoria.
>
> Além disso, estabeleça cores fixas para cada categoria segundo as informações abaixo. Essas cores devem ser aplicadas tanto para as novas categorias a serem criadas quanto para as que já existem.
> 
> - Despesa fixa: #DC2626
> - Despesa variável: #FACC15
> - Receita: #16A34A
> - Investimento: #2563EB

> Na aba "Categorias", não está sendo possível excluir as categorias criadas nos tipos de categoria. Sendo assim, ajuste o processo para que seja possível editar os tipos de categoria existentes. Isto é, reordenar as categorias já existentes para cada tipo, criar nova categoria, editar as categorias, ou excluir as categorias já existentes de cada tipo de categoria.

> Para o perfil de acesso em grupo (família), na aba "Extrato", mantenha a identificação do avatar responsável pela transação financeira apenas na coluna "Membro". Não é necessário repetir essa informação entre parêntesis na descrição da transação como está sendo feito agora.
>
> Por exemplo: se for inserida a frase "salário 3000 pai" no chat inteligente, ao gravar essa informação na aba Extrato, a descrição da transação deve ficar apenas "Recebimento de salário" ao invés de "Recebimento de salário (Pai)" como está ficando atualmente.

> Mude o nome do app de "FinançasFácil" para "Cont.AI" e altere a logo do app de "F" para "C".


### 3. Principais funcionalidades do Cont.AI

**1. Login/cadastro seguro**

- Possibilidade de criação de conta através de email e senha forte (8 caracteres, com maiúsculas, minúsculas, números e caractere especial)
- Possibilidade de dois tipos de perfis diferentes: 
  - Perfil de usuário individual
  - Perfil de grupo (família)

**2. Chat inteligente**

- Chat integrado com IA para classificação automática de transações, bem como criação e atualização de metas financeiras através de linguagem natural

**3. Extrato financeiro**

- Exibição individual dos lançamentos financeiros, apresentando data, descrição, categoria do lançamento, membro responsável pelo lançamento (funcionalidade exclusiva do perfil de grupo) e valor lançado. 
- Exibição dos valores consolidados de entradas, saídas, investimento e saldo final
- Possibilidade de filtro de transações registradas por período mensal, trimestral ou período customizado

**4. Categorização de transações financeiras**

- Criação de tipos de categoria macro, ex: receita, investimento, despesa fixa e despesa variável
- Criação de subcategorias, ex: salário (atribuído ao tipo "receita"), aluguel (atribuído ao tipo "despesa fixa)
- Possibilidade de edição/exclusão dos tipos de categoria e seus subtipos

**5. Metas financeiras**

- Criação, edição e exclusão de metas financeiras personalizadas
- Exibição visual do percentual já arrecadado para cada meta 

**6. Exibição de relatório**

- Exibição consolidada em gráficos de visualização amigável (pizza ou barra) das transações financeiras
- Possibilidade de filtro por período mensal, trimestral ou período customizado
- Exibição dos valores consolidados de receitas, despesas, investimentos e saldo final


### 4. Resultado obtido

Acesso ao app: https://contai-finapp.lovable.app


### 3. Entregando o Desafio na DIO



Finalize seu projeto criando um **repositório no GitHub** (pode ser um **fork** deste).  
No README do seu repositório, inclua:

- Seu **prompt final** (PRD);  
- Prints ou pequenos vídeos das interações com a IA;  
- Um resumo do que o seu **App de Finanças Pessoais** faz;  
- Uma breve **reflexão sobre o processo**:
  - O que funcionou bem?  
  - O que não funcionou como o esperado?  
  - O que aprendeu sobre conversar com IAs?

> [!TIP]
> Publique seu repositório e compartilhe o link na plataforma da DIO! Sua entrega é a prova de que você domina o raciocínio de Vibe Coding, mesmo sem escrever uma única linha de código.

## 💬 Conclusão

Vibe Coding é sobre clareza, curiosidade e criatividade, não sobre perfeição técnica. O verdadeiro objetivo aqui é aprender a pensar junto com a IA, transformando ideias em conceitos reais e enxergando a tecnologia como uma extensão do seu raciocínio criativo. Cada interação é um experimento, quanto mais clara for sua intenção, mais surpreendente será o resultado.
