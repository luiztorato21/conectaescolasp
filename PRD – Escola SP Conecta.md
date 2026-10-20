# PRD – Escola SP Conecta

Oct 13, 2026 · @Luiz Torato

## Visão geral

A Escola SP Conecta substitui a entrevista e a atribuição em nível de diretoria por uma conexão em duas etapas: o professor monta um perfil e escolhe de 1 a 20 escolas de toda a rede; cada diretor pode conectar os professores que escolheram sua escola; ao encerrar o prazo dos diretores, o sistema o distribui automaticamente para a escola de maior prioridade entre as que o conectaram.

**Objetivo:** dar autonomia ao diretor na composição da equipe e ampliar as opções do professor para além da própria diretoria.

**Público participante**

- Professores com farol vermelho
- Professores com farol amarelo indicados à não permanência
- Categoria O
- Novíssimos
- Efetivos adidos
- OFA adidos

**Fora de escopo nesta versão:** entrevista presencial, atribuição em nível de diretoria, justificativa de não escolha e a regra para professor sem conexão (ponto em aberto).

**Padrão visual:** listas e grids seguem o padrão da SED. O mini currículo usa layout moderno, no estilo de perfil do LinkedIn.

## Visão Professor

O professor completa o perfil, ordena de 1 a 20 escolas por prioridade e acompanha o resultado. Depois do envio, voltar à visão do professor abre o acompanhamento, sem reiniciar o cadastro.

**Fluxo**

1. **Acesso:** entra pela SED e vê o aviso de participação no processo.
2. **Dados automáticos:** confere os dados que vêm da SED (somente leitura).
3. **Disciplinas de interesse:** escolhe ao menos uma disciplina que deseja lecionar entre as habilitadas e correlatas da sua formação. Não pode adicionar uma disciplina fora dessa lista.
4. **Foto:** envia a foto de perfil (JPG/PNG, recorte quadrado, até 5 MB).
5. **Comentário:** escreve uma apresentação livre (sugestão: até 500 caracteres).
6. **Vídeo:** informa o link de um vídeo não listado no YouTube e sua duração em mm:ss. O envio aceita de 00:01 a 05:00. Neste protótipo, a duração é declarada pelo professor; a verificação automática do vídeo e da privacidade depende de integração com o YouTube.
7. **Escolha de escolas:** seleciona de 1 a 20 escolas de qualquer diretoria e define a ordem de prioridade.
8. **Revisão e envio:** vê a prévia do mini currículo, as disciplinas escolhidas e a duração informada do vídeo antes de confirmar o envio.
9. **Acompanhamento:** após o envio, vê o status **Em análise** até o encerramento do prazo dos diretores. Nesse momento, o sistema encontra a primeira escola da sua ordem de prioridade que marcou **Conectar** e mostra a escola definida e a posição de prioridade. O professor não escolhe nem confirma a escola.

**Tela: escolha de escolas**

- Filtros: diretoria, município, escola, PEI (sim/não) e etapa de ensino (anos finais do Ensino Fundamental, Ensino Médio e EJA no protótipo)
- Grid padrão SED com: código, escola, diretoria, município, PEI (sim/não), etapas de ensino e ação Adicionar
- Lista "Minhas escolas" numerada por prioridade, com ações **Subir**, **Descer** e **Remover**; a posição 1 é a maior prioridade
- Contador "X de 20 escolas"
- Aviso visível: "Os diretores das escolas escolhidas verão o seu perfil. Ao fim do prazo dos diretores, o sistema definirá automaticamente a primeira escola da sua lista de prioridades que também conectou com você."
- Escolas PEI só aparecem habilitadas se o professor for credenciado para PEI
- O diretor não vê a lista completa de escolas escolhidas nem a ordem de prioridade do professor

**Status visíveis ao professor**

| Status | Quando aparece |
| --- | --- |
| Perfil incompleto | Faltam foto, uma disciplina de interesse, vídeo de até 5 minutos ou ao menos uma escola |
| Em análise | Perfil enviado; prazo dos diretores em andamento |
| Escola definida | Prazo dos diretores encerrado; o sistema encontrou a escola conectada de maior prioridade |
| Sem conexão | Prazo encerrado sem nenhuma escola da lista que tenha conectado o professor; regra posterior a definir |


**Regras da visão professor**

- O professor não vê quais diretores clicaram em Não conectar
- Durante o prazo, pode editar foto, comentário, vídeo e escolas
- Pode alterar as disciplinas de interesse somente entre as compatíveis com sua formação
- Pode reordenar as escolas escolhidas; essa prioridade é privada para o professor
- Após o fim do prazo do professor, o perfil fica bloqueado
- Após enviar o perfil, **Continuar** e a troca para a visão do professor levam ao acompanhamento, sem reabrir o cadastro
- No acompanhamento, antes do encerramento do prazo vê **Em análise**; depois vê a escola definida automaticamente e a posição dela na sua lista de prioridades
- A distribuição automática ocorre uma vez ao encerrar o prazo dos diretores; depois disso, as decisões dos diretores ficam bloqueadas no protótipo

## Visão Diretor

O diretor vê em lista todos os professores que escolheram a sua escola, abre o mini currículo e decide entre Conectar e Não conectar.

**Fluxo**

1. **Acesso:** entra pela SED e vê um painel da sua escola com o total de candidatos, quantos já foram conectados ou não conectados e quantos estão pendentes. No protótipo, seleciona a escola do diretor para simular mais de uma escola.
2. **Lista de candidatos:** grid padrão SED.
3. **Detalhe:** abre o mini currículo estilo LinkedIn.
4. **Decisão:** clica em Conectar ou Não conectar, confirma a escolha antes do registro e não precisa informar justificativa.
5. **Resultado:** após o encerramento do prazo, vê se o sistema distribuiu o professor para sua escola, para outra escola ou se não houve distribuição.

**Grid de candidatos (padrão SED)**

| Coluna | Observação |
| --- | --- |
| Foto (miniatura) | Avatar circular |
| Nome | Link para o mini currículo |
| Cargo |  |
| Categoria | O, Efetivo, OFA etc. |
| Disciplinas de interesse | Escolhidas pelo professor entre as habilitadas e correlatas da sua formação |
| Farol | Ícone vermelho / amarelo / verde |
| PEI | Credenciado sim/não |
| Nota final |  |
| Decisão | Pendente / Conectado / Não conectado |

- Filtros: categoria, disciplina, farol, PEI, decisão
- Ordenação por qualquer coluna
- Ações rápidas na linha: **Conectar** em verde com joinha para cima (👍) e **Não conectar** em vermelho com joinha para baixo (👎)

**Regras da visão diretor**

- Pode conectar mais professores do que vagas (ponto a validar)
- Pode alterar a decisão até o fim do seu prazo; depois, a decisão fica definitiva
- Não há campo de justificativa
- O professor só aparece como candidato da escola que selecionou depois de enviar o perfil
- A decisão do diretor é registrada por escola; mais de uma escola pode conectar o mesmo professor
- O diretor vê as disciplinas que o professor quer lecionar, mas não vê a ordem de prioridade das escolas
- O sistema faz a distribuição após o encerramento do prazo: o diretor vê "Distribuído automaticamente para sua escola", "Distribuído para outra escola" ou "Sem distribuição"

## Mini currículo estilo LinkedIn

O mini currículo é um card de perfil em blocos. O professor vê a lista das escolas que escolheu; o diretor vê, adicionalmente, o gráfico de Avaliação Diagnóstica - Farol. A ordem de prioridade das escolas não aparece para o diretor.

**Estrutura de cima para baixo**

1. **Header (capa):** faixa colorida no topo, foto circular sobreposta, nome em destaque e cargo logo abaixo. Ao lado, os badges Farol (cor), PEI credenciado e Indicação de não permanência, quando houver.
2. **Linha de dados rápidos:** chips com Categoria, DI, Idade, Data de exercício e CPF mascarado (\***.123.456-**).
3. **Indicadores:** cards numéricos lado a lado com Nota final de confirmação e Nota PSS (novo).
4. **Avaliação Diagnóstica - Farol (somente diretor):** gráfico com quatro barras para Parcial 2025, Final 2025, Parcial 2026 e Final 2026. Uma linha liga os pontos no topo das barras para mostrar a evolução. Cada barra e seu ponto usam a cor da faixa qualitativa vermelho, amarelo ou verde, sem nota numérica. No protótipo, o histórico é demonstrativo e a última faixa coincide com o farol atual do professor.
5. **Sobre:** o comentário do professor, com "ver mais" quando longo.
6. **Vídeo:** player do YouTube incorporado, no padrão 16:9, com a duração informada (até 5 minutos).
7. **Formação:** disciplinas habilitadas como tags de destaque; correlatas como tags secundárias. Selo "aderente à vaga" nas que batem com a necessidade da escola.
8. **Disciplinas de interesse:** seleção feita pelo professor entre as opções da sua formação, visível ao diretor.
9. **Escolas escolhidas:** lista em ordem de prioridade, só na visão do professor.
10. **Barra de ação fixa (visão diretor):** botões **Conectar** em verde com 👍 e **Não conectar** em vermelho com 👎, com setas para ir ao próximo/anterior candidato sem voltar à lista.

**Diretrizes visuais**

- Cards com cantos arredondados, sombra leve e bastante espaço em branco
- Ícones de linha para cada campo (calendário, diploma, escola)
- Responsivo: no celular, os blocos empilham e a barra de ação fica no rodapé
- Cores do farol usadas só em badges, nunca no card inteiro
- Avaliar com o jurídico: exibir Idade e foto pode gerar questionamento por viés; alternativa é mostrar só tempo de exercício

## Regras de negócio e pontos em aberto

O diretor marca **Conectar** ou **Não conectar** para cada professor. O sistema pede confirmação antes de gravar a decisão; se ele cancelar, a decisão anterior permanece. Ao encerrar o prazo dos diretores, o sistema percorre a lista de escolas do professor em ordem de prioridade e define a primeira que marcou **Conectar**. Se a primeira não o conectou, tenta a segunda e assim por diante. Antes do encerramento, o professor vê **Em análise**. Se nenhuma escola o conectou, mostra **Sem conexão**; o encaminhamento posterior permanece em aberto.

| # | Regra |
| --- | --- |
| RN01 | Participam: farol vermelho, farol amarelo indicado à não permanência, Categoria O, novíssimos, efetivos adidos e OFA adidos |
| RN02 | Não há entrevista nem atribuição em nível de diretoria |
| RN03 | Todo participante escolhe de 1 a 20 escolas, de qualquer diretoria |
| RN05 | Vídeo obrigatório via link do YouTube não listado, com duração de 00:01 a 05:00; no protótipo, a duração é informada pelo professor |
| RN06 | O diretor decide entre Conectar e Não conectar, sem justificativa |
| RN07 | Antes do encerramento do prazo dos diretores, o professor vê apenas **Em análise**; após o encerramento, vê a escola definida ou **Sem conexão**, sem reiniciar o cadastro |
| RN08 | Ao encerrar o prazo dos diretores, o sistema define automaticamente a primeira escola da ordem de prioridade do professor que marcou **Conectar**; o professor não escolhe nem confirma |
| RN09 | Escolas PEI só podem ser escolhidas por professores credenciados |
| RN10 | CPF exibido sempre mascarado |
| RN11 | O envio exige foto, ao menos uma disciplina de interesse, vídeo válido de até 5 minutos e ao menos uma escola |
| RN12 | Cada decisão do diretor pertence à escola correspondente; o encerramento do prazo executa a distribuição automática e bloqueia novas decisões no protótipo |
| RN13 | As disciplinas de interesse devem pertencer às disciplinas habilitadas ou correlatas da formação do professor |
| RN14 | O professor define e pode alterar a ordem de prioridade das escolas escolhidas; o diretor não vê essa lista nem sua ordem |
| RN15 | A busca de escolas pode ser filtrada por PEI e etapa de ensino; a lista mostra esses atributos em cada escola |
| RN16 | O gráfico de Avaliação Diagnóstica - Farol aparece somente no mini currículo do diretor, com quatro barras e uma linha ligando os pontos no topo; cada barra e ponto usam a cor da faixa vermelho, amarelo ou verde, e o histórico usado no protótipo é demonstrativo |

**Pontos em aberto**

- [ ] Regra posterior para professor sem distribuição automática
- [ ] Limite de conexões por diretor (igual ao nº de vagas ou acima)
- [ ] Rodadas: haverá segunda rodada para vagas que sobrarem após as conexões finais?
- [ ] Prioridade legal entre categorias (efetivo antes de OFA/O)
- [ ] Validação jurídica: sem justificativa para farol vermelho/amarelo, exibição de idade e foto
- [ ] Termo de consentimento de uso de imagem e vídeo (LGPD)
- [ ] Calendário: prazo do professor, prazo dos diretores, execução da distribuição automática e divulgação do resultado
- [ ] Integração com o YouTube para verificar automaticamente duração de até 5 minutos e privacidade não listada
- [ ] Fonte oficial e atualização das etapas de ensino oferecidas por cada escola
