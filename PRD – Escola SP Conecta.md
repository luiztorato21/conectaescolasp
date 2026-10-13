# PRD – Escola SP Conecta

Oct 13, 2026 · @Luiz Torato

## Visão geral

A Escola SP Conecta substitui a entrevista e a atribuição em nível de diretoria por uma conexão em duas etapas: o professor monta um perfil e escolhe de 1 a 20 escolas de toda a rede; cada diretor pode conectar os professores que escolheram sua escola; por fim, o professor usa **Conectar** para finalizar com uma única escola entre as que o conectaram.

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

O professor completa o perfil, escolhe de 1 a 20 escolas e acompanha as conexões recebidas. Depois do envio, voltar à visão do professor abre o acompanhamento, sem reiniciar o cadastro.

**Fluxo**

1. **Acesso:** entra pela SED e vê o aviso de participação no processo.
2. **Dados automáticos:** confere os dados que vêm da SED (somente leitura).
3. **Foto:** envia a foto de perfil (JPG/PNG, recorte quadrado, até 5 MB).
4. **Fit cultural:** responde 10 perguntas. O rascunho é salvo durante o preenchimento; as respostas completas são registradas ao clicar em **Registrar respostas** ou ao avançar. Depois do registro, não podem ser editadas.
5. **Comentário:** escreve uma apresentação livre (sugestão: até 500 caracteres).
6. **Vídeo:** informa o link do YouTube (não listado), com validação do link e duração máxima de 5 minutos.
7. **Escolha de escolas:** seleciona de 1 a 20 escolas de qualquer diretoria.
8. **Revisão e envio:** vê a prévia do mini currículo, o total de respostas de fit preenchidas e confirma o envio. Se as 10 respostas estiverem completas no rascunho, o envio as registra. Se faltar alguma, o usuário pode voltar por **Editar fit cultural**.
9. **Acompanhamento:** após o envio, vê o status e as escolas que o conectaram. No protótipo, as conexões aparecem assim que o diretor decide. O professor clica em **Conectar** em uma única escola para finalizar.

**Tela: escolha de escolas**

- Filtros: diretoria, município, nome/código da escola, tipo (PEI/regular)
- Grid padrão SED com: código, escola, diretoria, município, PEI (sim/não), ação Adicionar
- Lista "Minhas escolas" com opção de remover
- Contador "X de 20 escolas"
- Aviso visível: "Os diretores das escolas escolhidas verão o seu perfil. Se mais de uma escola conectar com você, a decisão final é sua."
- Escolas PEI só aparecem habilitadas se o professor for credenciado para PEI

**Status visíveis ao professor**

| Status | Quando aparece |
| --- | --- |
| Perfil incompleto | Faltam foto, 10 respostas de fit registradas, vídeo ou ao menos uma escola |
| Em análise | Prazo dos diretores em andamento |
| Escolha pendente | Uma ou mais escolas conectaram; o professor precisa finalizar com uma |
| Conexão finalizada | Professor conectou com uma escola |
| Sem conexão | Nenhuma escola conectou (regra a definir) |

**Regras da visão professor**

- O professor não vê quais diretores clicaram em Passar
- Durante o prazo, pode editar foto, comentário, vídeo e escolas; as respostas de fit ficam bloqueadas após o registro das 10 perguntas
- Após o fim do prazo do professor, o perfil fica bloqueado
- Após enviar o perfil, **Continuar** e a troca para a visão do professor levam ao acompanhamento, sem reabrir o cadastro
- No acompanhamento, vê somente as escolas que o conectaram e pode usar **Conectar** em apenas uma
- A conexão final é definitiva; depois dela, as demais escolas ficam indisponíveis e as decisões dos diretores são bloqueadas no protótipo

## Visão Diretor

O diretor vê em lista todos os professores que escolheram a sua escola, abre o mini currículo e decide entre Conectar e Passar.

**Fluxo**

1. **Acesso:** entra pela SED e vê um painel da sua escola com o total de candidatos, quantos já foram conectados ou passados e quantos estão pendentes. No protótipo, seleciona a escola do diretor para simular mais de uma escola.
2. **Lista de candidatos:** grid padrão SED.
3. **Detalhe:** abre o mini currículo estilo LinkedIn.
4. **Decisão:** clica em Conectar ou Passar, sem justificativa.
5. **Acompanhamento:** vê se o professor finalizou a conexão com sua escola, escolheu outra ou ainda não concluiu.

**Grid de candidatos (padrão SED)**

| Coluna | Observação |
| --- | --- |
| Foto (miniatura) | Avatar circular |
| Nome | Link para o mini currículo |
| Cargo |  |
| Categoria | O, Efetivo, OFA etc. |
| Disciplinas habilitadas | Destacar as aderentes à necessidade da escola |
| Farol | Ícone vermelho / amarelo / verde |
| PEI | Credenciado sim/não |
| Nota final |  |
| Decisão | Pendente / Conectado / Passado |

- Filtros: categoria, disciplina, farol, PEI, decisão
- Ordenação por qualquer coluna
- Ações rápidas Conectar e Passar direto na linha

**Regras da visão diretor**

- Pode conectar mais professores do que vagas (ponto a validar)
- Pode alterar a decisão até o fim do seu prazo; depois, a decisão fica definitiva
- Não há campo de justificativa
- O professor só aparece como candidato da escola que selecionou depois de enviar o perfil
- A decisão do diretor é registrada por escola; mais de uma escola pode conectar o mesmo professor
- A decisão final é do professor: após a conexão dele, o diretor vê "Conexão finalizada com sua escola" ou "Escolheu outra escola"

## Mini currículo estilo LinkedIn

O mini currículo é um card de perfil em blocos, com o mesmo layout na prévia do professor e no detalhe do diretor. A diferença é que só o professor vê a lista das escolas que escolheu.

**Estrutura de cima para baixo**

1. **Header (capa):** faixa colorida no topo, foto circular sobreposta, nome em destaque e cargo logo abaixo. Ao lado, os badges Farol (cor), PEI credenciado e Indicação de não permanência, quando houver.
2. **Linha de dados rápidos:** chips com Categoria, DI, Idade, Data de exercício e CPF mascarado (\***.123.456-**).
3. **Indicadores:** cards numéricos lado a lado com Nota final de confirmação e Nota PSS (novo).
4. **Sobre:** o comentário do professor, com "ver mais" quando longo.
5. **Vídeo:** player do YouTube incorporado, no padrão 16:9, com até 5 minutos.
6. **Formação:** disciplinas habilitadas como tags de destaque; correlatas como tags secundárias. Selo "aderente à vaga" nas que batem com a necessidade da escola.
7. **Fit cultural:** as 10 perguntas com as respostas do professor, em acordeão ou cards.
8. **Escolas escolhidas:** só na visão do professor.
9. **Barra de ação fixa (visão diretor):** botões **Conectar** (primário) e **Passar** (secundário), com setas para ir ao próximo/anterior candidato sem voltar à lista.

**Diretrizes visuais**

- Cards com cantos arredondados, sombra leve e bastante espaço em branco
- Ícones de linha para cada campo (calendário, diploma, escola)
- Responsivo: no celular, os blocos empilham e a barra de ação fica no rodapé
- Cores do farol usadas só em badges, nunca no card inteiro
- Avaliar com o jurídico: exibir Idade e foto pode gerar questionamento por viés; alternativa é mostrar só tempo de exercício

## Regras de negócio e pontos em aberto

O diretor conecta primeiro; depois o professor finaliza a conexão com uma das escolas que o conectaram. No protótipo, essa lista aparece imediatamente após a decisão do diretor; o calendário oficial de liberação continua em aberto.

| # | Regra |
| --- | --- |
| RN01 | Participam: farol vermelho, farol amarelo indicado à não permanência, Categoria O, novíssimos, efetivos adidos e OFA adidos |
| RN02 | Não há entrevista nem atribuição em nível de diretoria |
| RN03 | Todo participante escolhe de 1 a 20 escolas, de qualquer diretoria |
| RN04 | As 10 perguntas de fit cultural têm rascunho persistente; depois de registradas, as respostas não podem ser editadas |
| RN05 | Vídeo obrigatório via link do YouTube não listado, com até 5 minutos |
| RN06 | O diretor decide entre Conectar e Passar, sem justificativa |
| RN07 | No protótipo, o professor vê no acompanhamento as escolas que o conectaram assim que há decisão do diretor, sem reiniciar o cadastro |
| RN08 | O professor usa **Conectar** para finalizar com uma única escola; a conexão é definitiva e libera as demais escolas |
| RN09 | Escolas PEI só podem ser escolhidas por professores credenciados |
| RN10 | CPF exibido sempre mascarado |
| RN11 | O envio exige foto, 10 respostas completas de fit cultural, vídeo válido e ao menos uma escola; respostas completas no rascunho são registradas no envio |
| RN12 | Cada decisão do diretor pertence à escola correspondente; a conexão final do professor bloqueia novas decisões no protótipo |

**Pontos em aberto**

- [ ] Regra para professor sem nenhuma conexão
- [ ] Prazo do professor para conectar e regra se ele não conectar
- [ ] Limite de conexões por diretor (igual ao nº de vagas ou acima)
- [ ] Rodadas: haverá segunda rodada para vagas que sobrarem após as conexões finais?
- [ ] Prioridade legal entre categorias (efetivo antes de OFA/O)
- [ ] Validação jurídica: sem justificativa para farol vermelho/amarelo, exibição de idade e foto
- [ ] Termo de consentimento de uso de imagem e vídeo (LGPD)
- [ ] Definição das 10 perguntas de fit cultural
- [ ] Calendário: prazo do professor, prazo do diretor, liberação das conexões recebidas, prazo da conexão final e divulgação do resultado
