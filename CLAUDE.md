# Contexto do Design Challenge Radix

Documento vivo e fonte da verdade do projeto a partir da Etapa 2 (16/11/2026). Copiado do contexto do projeto "Design Challenge" no claude.ai, com a seção "Ambiente técnico" reescrita para o Claude Code. Todo trabalho lê este arquivo antes de começar e o atualiza ao terminar (seções "Estado atual" e "Log de decisões").

## O desafio
- Processo seletivo da Radix (consultoria brasileira de engenharia e software). Vaga de Product Designer.
- Briefing: desenhar a experiência de um assistente virtual de IA para um profissional da indústria MedTech.
- Briefing traduzido: doc "01 — Briefing do Design Challenge Radix (tradução)" — https://claude.ai/artifact/Vjud8BmbnWNyJahxhTaQpy
- Original: /Users/jonasjose/Documents/Estudos/Design Challenge/Design Challenge - Radix.pdf
- Entregáveis: (1) visão do problema e justificativa — persona, problema, valor da IA, hipóteses, riscos; (2) wireframes — tela principal, tela de interação com a IA, tela de resposta estruturada; (3) no mínimo 3 telas de alta fidelidade — interface principal, resposta da IA, uma terceira tela estratégica escolhida por nós.
- Formato: PDF consolidado (máx. 10 páginas) + link de protótipo organizado. Apresentação de 30 min depois (a agendar).
- Avaliação: clareza de raciocínio, estrutura de UX, simplificar o complexo, qualidade visual, maturidade com IA, autonomia no processo. Telas avaliadas por hierarquia visual, clareza, consistência, pensamento centrado em IA e adequação ao contexto industrial.

## Prazo
- Entrega: quarta, 18/11/2026 (prazo renegociado em 14/11; o original era 16/11). Meta interna: enviar até 18h; o fim do dia é só a margem de segurança.
- Cronograma: Seg 16/11 = Discovery/Definição (concluída às 21h, três horas depois do gate) · Ter manhã = fluxo e estrutura (gate ter 13h) · Ter tarde → Qua manhã = alta fidelidade + protótipo (gate qua 12h) · Qua tarde = PDF até 16h · Qua 18h = envio.

## O projeto em quatro frases
Cíntia inspeciona peças de seringa de madrugada e está há quatro meses na função. Quando acha um defeito, precisa decidir sozinha o que fazer, sem ter ainda a memória dos casos antigos que os veteranos têm. O assistente mostra o que a regra da fábrica manda, o que foi feito em casos parecidos, e escreve o registro junto com ela. A decisão é sempre de uma pessoa.

## Decisões já tomadas
- Recorte: lado INDUSTRIAL do MedTech, não clínico. O usuário não é médico.
- Caminho A (fábrica de descartáveis médicos, ligado à entrevista). O caminho B (serviço de campo de imagem) foi descartado: mercado já ocupado.
- Persona: Cíntia Moraes, 34, técnica de qualidade do turno da noite; dois anos na fábrica como operadora e QUATRO MESES na qualidade. Proto-persona de pesquisa de mesa, chamada assim com honestidade. Tese: "a memória da fábrica para quem ainda não tem a sua". Veteranas usam sobretudo o registro rápido.
- Problema: decisão de contenção (parar ou não a máquina, o que separar) tomada sozinha, com pressa e com responsabilidade. NÃO é um problema de busca.
- Escopo ENXUTO (decisão do Jonas: nem ele nem a IA conhecem fábrica; o briefing avalia simplificar):
  - Fica: resposta em três blocos que nunca se misturam ("o que a regra diz", "o que foi registrado", "o que a IA sugere"); caminhos de contenção lado a lado (a ideia ousada escolhida); conta simples do material (horas desde a última inspeção boa × produção por hora); IA que diz "não sei" e mostra o caminho mais seguro da regra; registro que se escreve enquanto ela age e é confirmado com o crachá; defeito novo = foto + nome.
  - Visão de futuro (uma linha cada no PDF): verificação rápida ("próximo teste"); descobrir quando o defeito começou com dados internos da máquina; aviso antes da inspeção.
- Telas: principal (mapa das máquinas em que a cor muda com o tempo sem inspeção e fica amarela com ocorrência aberta; cor sempre com ícone e palavra; sem citar pessoa ou turno) · interação (escolhas por toque, sem teclado) · resposta estruturada · terceira tela estratégica = visão do supervisor (problemas que se repetem por máquina e tipo de defeito, com suposições de causa rotuladas; nunca por pessoa). Tablet como base; desenho responsivo que também serve computador; uma única linguagem visual.
- Jornada e telas são coisas diferentes: a jornada tem 6 passos (doc 05); quantas telas ela vira é decisão da Etapa 2.
- Cinco hipóteses-chave para o PDF: estão no início da seção "Hipóteses" do doc 04.
- Persona sintética: usada só como ferramenta de estresse (doc 04, última seção), nunca como evidência.
- Processo: sem wireframe à mão. A estrutura das telas é feita direto em código com os componentes do design system em tons de cinza (isso vira o wireframe) e depois recebe o tema (isso vira a alta fidelidade). No PDF: "estrutura primeiro, direto no material".
- Design system: Astryx (Meta, open source, MIT, React + StyleX, beta), tema Neutral. Entra como dependência, sem fork. AINDA FALTA CONFIRMAR: existência do tema "Neutral" e dos componentes de chat (trava a Etapa 3).
- Sem Storybook. Hospedagem: Vercel, ligada ao GitHub. PRD não vai para o PDF.

## Regra de informação sobre o cliente (esclarecida pelo Jonas em 16/11)
- O nome do cliente NUNCA aparece em entregável, doc, repositório ou PDF. O repositório é público.
- Informação PÚBLICA sobre o cliente PODE e DEVE ser pesquisada e usada para orientar as escolhas, em termos genéricos. O que não entra é detalhe que só alguém de dentro saberia.
- O que a pesquisa pública mostrou, sem citar nome: fabrica produto acabado (seringas, agulhas, cateteres) em duas fábricas no Brasil; tem programa interno de excelência operacional que analisa problemas por tipo de causa (pessoa, máquina, método, material); investe em fábrica digital; qualidade e investigação de causa são tema caro para a empresa. Não sabemos em que área a Radix atua lá.
- Discurso da Radix (site): ampliar performance, eficiência e crescimento sustentável; "fortalecer a tomada de decisão com soluções que ganham tração no dia a dia". Usar nas métricas e na narrativa do PDF como resultado mensurável (menos material descartado, menos tempo de máquina parada), não como slogan.

## Ambiente técnico
- Repositório público: https://github.com/jonas-ux/ai-assistant (branch main). Pastas: docs/ (artefatos .md) e app/ (protótipo).
- Pasta de trabalho: /Users/jonasjose/Documents/Estudos/Design Challenge/ai-assistant, no Mac do Jonas. O Claude Code roda direto nela.
- Git: roda no Mac do Jonas, com a conta GitHub dele. Commit e push direto desta pasta. Antes de cada push, dizer em palavras simples o que vai subir.
- Protótipo: rodar localmente para o Jonas ver no navegador a cada ajuste; publicar na Vercel, ligada ao GitHub.
- Docs → repositório: docs criados no claude.ai NÃO são transcritos à mão (a cópia à mão sai diferente). O Jonas exporta cada doc pelo menu do documento (Exportar → Markdown) e salva em docs/. O Claude Code então RENOMEIA o arquivo exportado para o nome padrão (não duplica: duplicar deixa dois arquivos e confunde), faz commit e push. Explicar ao Jonas cada passo em palavras simples antes de fazer.
- Docs novos criados no Claude Code (06 em diante) nascem direto como .md em docs/, com o número de ordem no nome.
- Nomes padrão no repo: docs/03-pesquisa-dominio-panorama-competitivo.md, docs/04-definicao.md, docs/05-prd.md. Se um doc mudar depois de exportado, pedir nova exportação.
- Jonas se vê como designer, não desenvolvedor: o Claude Code escreve todo o código.

## Como trabalhar com o Jonas
- Português. Um assunto por mensagem, guiando passo a passo.
- Ele NÃO conhece o setor nem termos de programação. Explicar todo termo na hora em que aparece, como para um leigo, com exemplo ou analogia. Textos autoexplicativos.
- Crítica honesta sempre, inclusive das próprias afirmações e de fontes externas. Não atribuir a ele afirmações que são da IA.
- Ele é o líder; a IA é a assistente. Quando ele dá uma direção, executar; discordância se expressa uma vez, com motivo, e a decisão é dele.
- AVISAR ANTES de fazer qualquer coisa cujo resultado possa sair diferente do que foi criado na conversa (cópia à mão, conversão de formato, resumo, troca de palavras). Ele prefere fazer um passo manual a correr risco de erro.
- Quando estiver inseguro com a complexidade, simplificar em vez de acrescentar mecanismos.
- Separar claramente "o que eu fiz" de "o que preciso de você"; a lista final só aparece quando existe algo para ele decidir.
- Todo documento gerado leva número de ordem no início do título (01, 02, 03…), em sequência global do projeto.
- Ele comenta direto nos docs; ler os comentários antes de responder.

## Documentos
- 01 — Briefing traduzido: https://claude.ai/artifact/Vjud8BmbnWNyJahxhTaQpy
- 02 — Prompts das etapas: https://claude.ai/artifact/KjZ3DJSfd1aACzhdCKj613
- 03 — Pesquisa de domínio + panorama competitivo: https://claude.ai/artifact/9VLF5aEDuAX4i2S4f5rH7i · repo: docs/03-pesquisa-dominio-panorama-competitivo.md
- 04 — Definição (persona, problema, papel da IA, hipóteses, riscos, persona sintética): https://claude.ai/artifact/3D6Ds4K414Hor7yqoCmJdo · repo: docs/04-definicao.md
- 05 — PRD (fonte de verdade para o design): https://claude.ai/artifact/DE7m4YFUF8Jj8QqrPAUTuM · repo: docs/05-prd.md
- Os três arquivos do repo são exportações exatas dos docs, feitas pelo Jonas em 16/11.
- 06 a 09 — a criar nas etapas (ver doc 02).

## Estado atual
- Etapa 1 (Discovery + Definição) concluída em 16/11/2026 às 21h30. Docs 03, 04 e 05 aprovados pelo Jonas, no repositório e na cópia local, sem pendências de arquivo.
- Próxima: Etapa 2 — fluxo e estrutura, terça 17/11 de manhã (gate 13h). Começa pela jornada de 6 passos do doc 05.
- Pendente fora do cronograma: Jonas ia mandar 4 perguntas a um amigo desenvolvedor da Radix sobre como a consultoria trabalha (quem usa o que constroem, se o conceito soa plausível, o que preocupa em projetos com IA, o que designers erram em contexto industrial). É opinião de uma pessoa: calibra o tom, não valida a persona.

## Log de decisões
- 13/11 — Recorte industrial, cronograma, repo público, Astryx Neutral, sem Storybook, wireframe em código, proto-persona + persona sintética como ferramenta.
- 14/11 — Prazo renegociado para quarta 18/11; cronograma redistribuído entre seg e qua.
- 14/11 — Em vez de ir direto para descartáveis, a Etapa 1 compara dois caminhos (A conectado à entrevista, B independente); Jonas escolhe.
- 16/11 — Caminho A, técnica de qualidade (candidata A2 da matriz do doc 04).
- 16/11 — Problema reenquadrado de "informação espalhada" para "decisão sozinha, sob pressão, com responsabilidade".
- 16/11 — Regra de informação esclarecida: pesquisa pública sobre o cliente orienta as escolhas; o nome nunca aparece.
- 16/11 — Escopo enxuto, com "caminhos lado a lado" como a ideia ousada e a conta simples do material de volta ao projeto.
- 16/11 — Terceira tela estratégica: visão do supervisor (ideia do Jonas), agrupada por máquina e tipo de defeito, nunca por pessoa.
- 16/11 — Cíntia passa a ter quatro meses na função (antes, anos de casa).
- 16/11 — Docs vão para o repo por exportação manual do Jonas, nunca por transcrição do chat.
- 16/11 — Etapas 2 e 3 passam para o Claude Code no Mac do Jonas. Este CLAUDE.md vira a fonte da verdade do projeto.
