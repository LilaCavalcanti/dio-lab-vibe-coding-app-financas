# 💸 App de Organização de Finanças Pessoais com Vibe Coding

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
* Feedback sobre: clareza do design, acessibilidade, utilidade do app, facilidade de uso e exibição dos dados. Considerar notas em escala de 1 a 10, em que 1 é péssimo e 10 é ótimo.
* Percentual de transações corretamente vinculadas às categorias.

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

### 2. Explorando o Lovable na Prática

Com seu PRD pronto e revisado, é hora de colocar a IA em ação. Abra o Lovable, cole seu prompt completo e peça o plano inicial do MVP do seu aplicativo. Como o plano gratuito limita você a 5 interações por dia, seja estratégico:
- Faça perguntas diretas e construtivas, como “crie o fluxo de telas com base nas funcionalidades listadas” ou “gere uma versão resumida do plano de MVP”;
- Priorize clareza nas instruções para aproveitar ao máximo cada resposta;

Durante essa etapa, você pode orientar a IA para três entregas principais:
1. Agente Financeiro: defina o comportamento e o tom de voz de um consultor financeiro pessoal, alinhado ao público e objetivo do app.
2. Fluxo de Telas: peça à IA para gerar o fluxo conceitual de telas com base nas funcionalidades descritas no PRD, simulando a interação por conversa.
3. Plano de MVP: solicite um resumo das 5 funcionalidades principais, dos recursos necessários e um plano de validação inicial (como medir se o app cumpre seu propósito).

> [!TIP]
> Se preferir, você pode fazer tudo com o **Copilot**. O importante é exercitar a habilidade de transformar intenções em instruções claras e testar os limites da IA como parceira criativa.

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
