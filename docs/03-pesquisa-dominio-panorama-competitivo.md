# 03 — Pesquisa de domínio + panorama competitivo

14 de novembro de 2026 · Jonas José

## Como ler este doc

Este doc descreve dois contextos de trabalho do MedTech industrial, na mesma profundidade, para apoiar a escolha entre os caminhos A e B. Ele não escolhe o caminho: a matriz e a recomendação ficam no doc 04.

- **Método:** pesquisa de mesa em fontes públicas (normas, reguladores, fabricantes, associações, vagas de emprego). Nenhum usuário real foi ouvido.
- **Limite:** o que está aqui é o que a indústria publica sobre si mesma. O dia a dia real pode ser diferente; cada lacuna está marcada na seção de crítica das fontes.
- **Regra de informação:** o caminho A é descrito como uma fábrica genérica do setor. Nada aqui vem de informação interna de qualquer empresa.

## Glossário para quem não é da área

Os termos abaixo aparecem no doc inteiro. Cada um está explicado como se explicaria a alguém de fora da indústria.

| Termo | O que é, em linguagem comum |
| --- | --- |
| Lote | Um conjunto de peças feitas juntas, na mesma máquina, com a mesma matéria-prima. Se uma peça tem problema, suspeita-se do lote inteiro. |
| Registro de lote (registro histórico do produto) | O "diário" daquele lote: quem fez, quando, com que material, o que foi medido. É a prova de que tudo correu como devia. |
| Não conformidade (NC) | Qualquer coisa que saiu diferente do combinado: peça fora da medida, etapa pulada, registro incompleto. Abre-se um relatório para cada uma. |
| Desvio | Parecido com NC, mas no processo: a máquina ou a pessoa fez algo fora do procedimento. |
| CAPA | Sigla em inglês para "ação corretiva e preventiva". É a investigação formal aberta quando um problema é grave ou se repete: descobrir a causa de verdade, corrigir e provar que não volta. A NC trata o sintoma; a CAPA trata a causa. |
| POP / SOP | Procedimento operacional padrão. O documento oficial que diz como uma tarefa deve ser feita. |
| Instrução de trabalho | Versão mais detalhada do procedimento, passo a passo, para uma máquina ou produto específico. |
| Validação de processo | Bateria de testes que prova, antes de produzir para valer, que a máquina faz peça boa de forma repetível. |
| IQ, OQ, PQ | As três etapas da validação: a máquina foi instalada certo (IQ), funciona em toda a faixa de ajustes (OQ) e produz peça boa por vários dias seguidos (PQ). |
| Janela validada | A faixa de ajustes da máquina que já foi testada e aprovada. Dentro dela pode-se mexer; fora dela, não sem autorização. |
| Sala limpa | Sala com ar filtrado e controle de poeira, onde se entra de touca, máscara, luva e avental. As classes ISO 7 e ISO 8 dizem o quanto de partícula é tolerado. |
| Moldagem por injeção | Plástico derretido é injetado sob pressão dentro de um molde de metal e sai como peça pronta. A máquina chama-se injetora. |
| Rastreabilidade | Conseguir dizer, para qualquer peça, de que lote veio, com que material e em que dia. |
| Liberação de lote | A assinatura final da qualidade dizendo que o lote pode ser vendido. |
| ISO 13485 | Norma internacional que define como uma empresa de dispositivos médicos deve organizar sua qualidade. |
| FDA / QMSR | FDA é o órgão regulador dos Estados Unidos, equivalente à ANVISA. QMSR é a regra de qualidade dela para dispositivos médicos. |
| Citação da FDA (formulário 483) | Lista de falhas que o inspetor da FDA entrega à fábrica ao fim de uma inspeção. |
| RDC | Resolução da ANVISA. A RDC 665 trata de fabricação; a RDC 509, de como hospitais cuidam de seus equipamentos. |
| Engenheiro de serviço de campo | Técnico do fabricante que vai ao hospital instalar, revisar e consertar o equipamento. |
| Resolução na primeira visita | Percentual de chamados resolvidos sem precisar voltar outro dia. |
| Manutenção preventiva | Revisão programada, como a do carro, feita antes de quebrar. |
| Gantry | O "anel" do tomógrafo ou da ressonância por onde o paciente passa. |
| Zona IV | A sala onde fica o ímã da ressonância. É a área de acesso mais restrito, porque o ímã nunca desliga. |
| Gaiola de Faraday | Revestimento metálico nas paredes da sala de ressonância que barra ondas de rádio. Por isso celular e Wi-Fi não funcionam lá dentro. |

## Caminho A — fábrica de descartáveis médicos

Uma fábrica de descartáveis médicos produz milhões de peças plásticas iguais, e o trabalho das pessoas é provar, lote a lote, que cada uma saiu dentro do processo validado. O conhecimento que o assistente teria de alcançar está espalhado em procedimentos, registros de lote e histórico de desvios.

### Como funciona

1. A resina entra, é inspecionada e liberada com rastreabilidade de lote.
2. A injetora molda as peças dentro de uma sala limpa, em geral ISO classe 7 ou 8 ([Rosti](https://www.rosti.com/resources/blogs/cleanroom-injection-moulding-class-7-vs-class-8-what-is-the-difference/)). A classe 8 admite até 3.520.000 partículas ≥ 0,5 µm por m³; a classe 7, dez vezes menos ([RapidDirect](https://www.rapiddirect.com/blog/medical-device-injection-molding/)).
3. O processo roda dentro de uma janela validada (IQ, OQ, PQ). Ajustar dentro da janela é operação normal; sair dela é uma mudança que exige avaliação formal ou revalidação ([SG Systems](https://sgsystemsglobal.com/?p=42236)).
4. A qualidade inspeciona durante o processo, por amostragem, e registra tudo no registro do lote.
5. Peça fora de especificação vira não conformidade (NC): o lote é segregado, investigado e, se o problema for sistêmico, abre-se uma CAPA.
6. A garantia da qualidade revisa o registro do lote e decide a liberação. Essa decisão é humana e assinada.

### Papéis

| Papel | O que faz | Onde trabalha |
| --- | --- | --- |
| Operador de injetora | Alimenta, acompanha a máquina, inspeciona visualmente, preenche o registro | Sala limpa, em pé, o turno todo |
| Preparador / técnico de processo | Troca molde, dá partida, ajusta parâmetros dentro da janela validada, resolve defeitos | Sala limpa, entre várias máquinas |
| Inspetor / técnico de qualidade | Liberação de linha, inspeção em processo, medições, abre NC, revisa registros de lote | Sala limpa e laboratório de metrologia |
| Engenheiro de processo | Define parâmetros e janelas, conduz validações, investiga causa raiz | Escritório e chão de fábrica |
| Analista / engenheiro de garantia da qualidade | Dono de NC e CAPA, controle de mudanças, liberação de lote, auditorias | Escritório |
| Líder de turno | Distribui pessoas, responde por meta e passagem de turno | Chão de fábrica |

As atribuições do inspetor e do técnico de qualidade vêm de vagas reais ([Nordson Medical](https://talents.vaia.com/companies/nordson-medical/parker/cqc-tech-i-107807827/), [Cretex Medical](https://jofdav.com/jobs/52157421-quality-technician-molding-assembly-1st-shift), [Randstad](https://www.randstadusa.com/jobs/309/ab_4971986/quality-control-inspector_ontario/)). Os nomes em português são a tradução usual no Brasil, sem fonte dedicada.

### Documentos que consultam

| Documento | Para que serve | Quem mais usa |
| --- | --- | --- |
| POP / SOP | Regra geral de como fazer (paramentação, limpeza, tratamento de NC) | Todos |
| Instrução de trabalho | Passo a passo de uma operação ou produto | Operador, preparador |
| Ficha de processo / folha de parâmetros | Valores e limites validados da máquina para aquele molde | Preparador, engenheiro |
| Plano de inspeção e desenho | O que medir, com que frequência e tolerância | Inspetor |
| Registro histórico do produto (registro de lote) | Prova do que aconteceu naquele lote | Operador preenche, qualidade revisa |
| Relatório de não conformidade | Descrição, contenção e destino do material fora de especificação | Inspetor, garantia da qualidade |
| CAPA | Causa raiz, ação corretiva e verificação de eficácia | Garantia da qualidade, engenharia |
| Protocolos e relatórios de validação | Evidência da janela de processo | Engenheiro, auditor |
| Manual da máquina e lista de alarmes | Diagnóstico de falha do equipamento | Preparador, manutenção |

### Normas que pesam

| Norma | O que exige, em uma linha |
| --- | --- |
| ISO 13485:2016 | Sistema de gestão da qualidade para dispositivos médicos: processo validado, registros, rastreabilidade |
| FDA QMSR (21 CFR 820) | Em vigor desde 2 de fevereiro de 2026; incorpora a ISO 13485 por referência ([UL](https://www.ul.com/resources/us-fda-harmonization-21-cfr-part-820-iso-134852016)) |
| ANVISA RDC 665/2022 | Boas Práticas de Fabricação no Brasil; define registro histórico do produto e registro mestre do produto ([texto da RDC](https://saude.campinas.sp.gov.br/saude/lista_legislacoes/legis_2022/U_RS-MS-ANVISA-RDC-665_300322.pdf)) |
| ISO 14644-1 | Classificação da sala limpa por contagem de partículas |
| ISO 14971 | Gerenciamento de risco do produto |

Com o QMSR, os termos americanos DMR, DHR e DHF saíram do regulamento e deram lugar ao vocabulário da ISO; o conteúdo exigido continua ([UL](https://www.ul.com/resources/us-fda-harmonization-21-cfr-part-820-iso-134852016)). Para o produto, isso significa usar "registro do lote" e não "DHR" na interface.

### Restrições físicas

- **Paramentação:** touca, máscara, luvas, avental e propés o turno todo ([vaga Jabil](https://expoint.co/job/430526532)). Luva atrapalha toque fino em tela; máscara atrapalha voz e reconhecimento facial.
- **Sem objetos pessoais:** celular próprio não entra em sala limpa. O acesso é por terminal fixo ou tablet da fábrica, quase sempre compartilhado.
- **Ruído:** injetoras e periféricos são barulhentos ([vaga Jabil](https://expoint.co/job/84794120)), o que enfraquece interface por voz.
- **Turnos:** operação 24 horas, com turnos de 12 horas em escala rotativa em parte das fábricas ([vaga Jabil](https://expoint.co/job/430526532)). A passagem de turno é o ponto onde o contexto se perde.
- **Em pé e em movimento:** consulta precisa caber em segundos, com leitura a um braço de distância.
- **Papel ainda existe:** muitas fábricas preenchem registro de lote à mão. Não achei número confiável sobre a proporção.

### Onde dói

- **CAPA é a falha mais citada pela FDA há dez anos.** No ano fiscal de 2025 foram 342 citações de CAPA em 2.660, ou 12,8%; controle de processo teve 155 e validação de processo, 153 ([Pure Global, sobre dados da FDA](https://www.pureglobal.com/blog-posts/fda-inspection-readiness-checklist-for-medical-device-manufacturers)).
- **Decidir na hora se um desvio é ajuste ou mudança.** O preparador precisa saber o limite validado daquele parâmetro, naquele molde, e o que já foi tentado antes.
- **Achar o precedente.** A resposta para "isso já aconteceu?" está em NCs e CAPAs antigas, escritas por outras pessoas em outros turnos.

Ressalva importante: os dados de inspeção da FDA valem para fabricantes de dispositivo acabado. Quem faz só o componente plástico costuma ser cobrado pelo cliente, por auditoria de fornecedor, e não diretamente pela FDA. Isso muda quem é o "auditor" na história, e esse ponto não foi confirmado em fonte primária.

## Caminho B — serviço de campo de equipamentos de imagem

O engenheiro de serviço de campo trabalha sozinho, dentro do hospital de outra pessoa, com um equipamento de milhões parado e pacientes esperando. O conhecimento que o assistente teria de alcançar está em manuais de serviço, logs de erro da máquina e histórico de atendimentos.

### Como funciona

1. O hospital abre um chamado, ou o monitoramento remoto do fabricante detecta a falha antes ([Siemens Healthineers](https://www.siemens-healthineers.com/en-ie/services/customer-services/upspeed-services/smart-remote-services)).
2. O suporte remoto tenta resolver à distância. A Philips declara resolver cerca de 30% dos casos assim ([Philips](https://www.documents.philips.com/assets/20211223/1c68294bf853419781dbae0700c31b7b.pdf)).
3. Se não resolve, o engenheiro vai ao local com a hipótese e as peças que achou que precisaria.
4. No local, ele lê os logs de erro, que são o ponto de partida mais útil segundo um engenheiro da área ([Zone3 Podcast](https://share.transistor.fm/s/9180890a)), consulta manual e esquemas, testa e troca componentes.
5. Depois do reparo, calibra, testa e documenta. O hospital só volta a usar o equipamento após essa liberação.
6. Ele registra o atendimento, pede peças e segue para o próximo local.

A maior parte do tempo é reativa, não planejada ([Zone3 Podcast](https://share.transistor.fm/s/9180890a)). A manutenção preventiva ocupa o resto.

### Papéis

| Papel | O que faz | Onde trabalha |
| --- | --- | --- |
| Engenheiro de serviço de campo do fabricante | Instala, faz preventiva, diagnostica e repara; registra atendimentos e pede peças | Vários hospitais por semana, sozinho |
| Engenheiro de suporte remoto | Analisa logs à distância, orienta o colega em campo, escala para a fábrica | Central de atendimento |
| Engenheiro de empresa multimarcas | Mesmo trabalho, em equipamentos de vários fabricantes, com menos acesso a documentação | Campo |
| Engenheiro clínico do hospital | Dono do parque de equipamentos, contrata e fiscaliza o serviço, guarda o histórico | Hospital |
| Gestor de serviço / despacho | Prioriza chamados, aloca engenheiros, responde por prazo de contrato | Escritório |
| Tecnólogo ou técnico de radiologia | Opera o equipamento, relata o sintoma, cobra o retorno | Sala de exame |

As atribuições do engenheiro de campo vêm de vagas reais ([GE Healthcare](https://www.ihireengineering.com/jobs/view/487799435), [SimonMed](https://www.monster.com/job-openings/field-service-engineer-orlando-fl--ed822e53-1d9d-4f8d-9721-378018eaf0a8), [Symmetrio](https://remotejobs.jobboardly.com/jobs/senior-field-service-engineer-imaging-mri-ct-69bfce8a)). Treinamento do fabricante, em geral Siemens ou GE, aparece como requisito ou forte preferência em quase todas.

### Documentos que consultam

| Documento | Para que serve |
| --- | --- |
| Manual de serviço | Procedimentos de diagnóstico, desmontagem, calibração |
| Esquemas elétricos e diagramas | Seguir o sinal até o componente com falha |
| Logs de erro e eventos da máquina | O que a máquina registrou antes e durante a falha |
| Boletins técnicos e ações de campo | Falhas conhecidas e correções obrigatórias daquele modelo |
| Histórico de atendimentos do equipamento | O que já foi trocado e o que voltou a falhar |
| Roteiro de manutenção preventiva | Lista de verificações por modelo e intervalo |
| Catálogo de peças | Código, compatibilidade e disponibilidade |
| Procedimentos de segurança do local | Regras da sala de ressonância, proteção radiológica |
| Relatório de serviço | Registro do que foi feito, exigido pelo fabricante e pelo hospital |

### Normas que pesam

| Norma | O que exige, em uma linha |
| --- | --- |
| ISO 13485 e FDA QMSR | O fabricante precisa registrar e analisar os atendimentos de assistência técnica |
| IEC 62353 (ABNT NBR IEC 62353) | Ensaios de segurança elétrica recorrentes e após reparo ([catálogo da norma](https://genorma.com/en/standards/iec-62353-2014-ed2/amp)) |
| ANVISA RDC 509/2021 | O hospital deve ter plano de gerenciamento dos equipamentos, com rastreabilidade ([texto da RDC](https://fitoterapiabrasil.com.br/sites/default/files/legislacao/rdc_509_2021_comp.pdf)) |
| Diretrizes de segurança em ressonância do ACR | Quatro zonas de acesso; a sala do magneto é a zona IV, a mais restrita ([artigo no PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC10657250)) |
| Regras de proteção radiológica | Controle de exposição em tomografia; no Brasil, norma da ANVISA para radiologia diagnóstica, não verificada nesta rodada |

### Restrições físicas

- **Nada ferromagnético perto do magneto.** O campo está sempre ligado e objetos de ferro viram projéteis ([OpenAnesthesia](https://www.openanesthesia.org/keywords/magnetic-resonance-imaging-safety/)). Notebook e celular comuns ficam fora da sala.
- **Sem sinal dentro da sala.** A sala de ressonância é construída como gaiola de Faraday para bloquear radiofrequência externa ([Radiopaedia](https://radiopaedia.org/articles/radiofrequency-shielding)). Wi-Fi e celular não entram; isso é inferência a partir da física, não um relato de engenheiro.
- **Rede do hospital não é dele.** Conexão depende da rede de visitantes ou do próprio celular, fora da sala.
- **Mãos ocupadas e postura ruim.** Trabalho dentro do gantry e atrás de gabinetes, com ferramenta na mão.
- **Sozinho e sob pressão.** As vagas pedem trabalho independente, sem supervisão ([Symmetrio](https://remotejobs.jobboardly.com/jobs/senior-field-service-engineer-imaging-mri-ct-69bfce8a)), com a equipe do hospital perguntando quando volta.
- **Plantão e deslocamento.** Segundo turno e sobreaviso são comuns ([GE Healthcare](https://www.ihireengineering.com/jobs/view/487799435)).

### Onde dói

- **Quase metade das visitas não resolve na primeira vez.** Em imagem, a taxa de resolução na primeira visita fica em torno de 60%; uma visita falha aumenta o custo em 87% e adiciona 12 dias ao reparo ([AuntMinnie, sobre relatório da Aquant](https://auntminnie.com/practice-management/service/equipment/article/15742637/ai-for-medical-imaging-service-technicians-speeds-fixit-resolution-time)). A Philips declara 88% para si ([Philips](https://www.philips.co.id/healthcare/service/remote-maintenance)).
- **Distância entre o melhor e o pior.** As melhores equipes resolvem na primeira visita 83% das vezes; as piores, 56% ([Aquant](https://discover.aquant.ai/medical-device-service-benchmarks)). Isso sugere que o conhecimento está na cabeça de poucos veteranos.
- **Acesso a documentação é disputado.** Empresas multimarcas reclamam de dificuldade para obter manuais e especificações dos fabricantes; a FDA analisou o tema em 2018 e não impôs novas regras ([FDA](https://www.fda.gov/media/113431/download?attachment)).
- **Equipamento parado custa caro, mas não se sabe quanto.** As cifras publicadas vão de 7.900 dólares por hora a 50.000 dólares por hora, todas de fornecedores de software. Nenhuma deve ir para o PDF.

## A e B lado a lado

Os dois caminhos sustentam um assistente de IA; a diferença está em quem consulta, com que urgência e em que aparelho. Esta tabela compara só o que a pesquisa de domínio mostrou. A matriz de decisão, com critérios e nota, fica no doc 04.

| Dimensão | A — fábrica de descartáveis | B — serviço de campo de imagem |
| --- | --- | --- |
| Momento da consulta | Desvio com a linha rodando; lote em risco | Equipamento parado; hospital esperando |
| Pergunta típica | "Isso está dentro do validado? Já aconteceu antes? O que o procedimento manda fazer?" | "O que esse erro significa? Qual o próximo teste? Que peça levar?" |
| Onde está a resposta | Procedimentos internos, registros de lote, NCs e CAPAs antigas | Manual do fabricante, logs da máquina, histórico de atendimentos |
| Decisão que fica com o humano | Destino do material e liberação do lote | Devolver o equipamento para uso em pacientes |
| Aparelho provável | Terminal ou tablet compartilhado, com luva | Notebook e celular próprios, fora da sala do magneto |
| Conexão | Rede da fábrica, estável | Instável; nenhuma dentro da sala de ressonância |
| Trabalha | Em equipe, por turno | Sozinho |
| Melhor número de dor encontrado | CAPA é 12,8% das citações da FDA; mede a empresa, não a pessoa | 60% de resolução na primeira visita; mede a pessoa, mas vem de fornecedor |
| Contexto de uso no briefing | "Escritório ou híbrido" | "Campo" |

Duas observações que já pesam na escolha da persona:

- **No caminho A, quem sofre com documento provavelmente não é o operador.** O operador segue uma instrução fixa. Quem precisa cruzar parâmetro validado, procedimento e precedente é o preparador de processo ou o técnico de qualidade.
- **No caminho B, o fabricante já é dono dos dados e do canal.** Se os grandes fabricantes já entregam um assistente desses aos próprios engenheiros, sobra menos espaço para diferenciar. Isso se confirma ou cai no panorama competitivo.

## Crítica das fontes

A base regulatória é sólida; a descrição do dia a dia é fraca e quase toda americana. Nenhuma fonte mede o que mais importa para o desafio: quanto tempo essas pessoas perdem procurando informação.

| Confiança | Fontes | Por quê |
| --- | --- | --- |
| Alta | Textos da ANVISA (RDC 665, RDC 509), relatório da FDA de 2018, data do QMSR, limites da ISO 14644 | Fonte primária, ou fato repetido de forma idêntica por muitas fontes independentes |
| Média | Vagas de emprego; citações da FDA analisadas por terceiros; artigo sobre zonas de ressonância | Dados reais, mas vagas descrevem o cargo ideal, não o dia real |
| Baixa | Blogs de fabricantes de peças (Rosti, RapidDirect, SG Systems); relatório da Aquant; números da Philips sobre si mesma; custo de equipamento parado; um episódio de podcast | Material de venda, autodeclaração ou relato de uma pessoa só |

Problemas específicos encontrados:

- **O número de CAPA muda conforme a conta.** Uma análise dá 342 citações e 12,8%; outra dá 279 e 10,5%. A primeira soma todo o artigo 820.100; a segunda conta só a alínea (a). Foi usada a primeira, e a ordem de grandeza é a mesma.
- **A taxa de 60% vem de quem vende a solução.** A Aquant vende IA para serviço de campo. O número é plausível, mas tem interesse embutido.
- **Uma fonte errou a unidade.** Um site de consultoria descreve a classe da sala limpa em partículas "por pé quadrado"; a norma mede por volume de ar. Essa fonte foi descartada.
- **Viés de país.** Papéis, turnos e rotina vêm de vagas dos Estados Unidos. Do Brasil, só as normas.

O que ficou sem resposta:

- Quanto tempo se perde procurando informação, em qualquer dos dois caminhos.
- Que proporção das fábricas ainda usa registro de lote em papel.
- Que aparelho o pessoal realmente usa dentro da sala limpa.
- Se o fabricante só do componente plástico é inspecionado pelo regulador ou apenas auditado pelo cliente.
- Como é a conexão real do engenheiro de campo dentro de hospitais brasileiros.
- Qual norma brasileira rege os testes após manutenção em tomógrafos.

Essas lacunas viram hipóteses no doc 04, cada uma com a forma de validar com usuários reais.

## Panorama competitivo

Conversar com os documentos da empresa já é o básico que todo fornecedor oferece; não dá para se diferenciar por aí. O espaço aberto está em como a resposta mostra fonte e dúvida, em onde a IA para e devolve a decisão à pessoa, e em quem fica entre o chão de fábrica e o escritório da qualidade.

### Quem já está no mercado

São três famílias de produto. Nenhuma é concorrente de verdade num exercício de conceito; servem para mostrar o que o avaliador já viu.

| Família | O que é, em linguagem comum | Exemplos | Para quem a IA trabalha |
| --- | --- | --- | --- |
| Copiloto do chão de fábrica | Aplicativo no tablet do operador, com instruções passo a passo e um chat para tirar dúvida | [Tulip](https://tulip.co/blog/introducing-ai-copilot-for-manufacturers-in-the-life-sciences-industry/), [Poka](https://www.poka.io/en/industrial-ai/), [Augmentir](https://augmentir.com/), [Siemens Industrial Copilot](https://news.siemens.com/en-us/ai-agents-manufacturing) | Operador, manutenção |
| IA dentro do sistema da qualidade | O software onde a fábrica guarda procedimentos, NCs e CAPAs ganhou um assistente | [MasterControl](https://briefglance.com/companies/mastercontrol-solutions-inc/pulses/32346), [Veeva](https://clarkstonconsulting.com/insights/veeva-ai-agents/), [Dot Compliance](https://intuitionlabs.ai/articles/gxp-compliance-software-eqms-comparison-2026) | Analista de qualidade, no escritório |
| Copiloto de serviço de campo | Assistente que lê manuais e histórico de atendimentos e sugere o diagnóstico | [Aquant](https://aquant.ai/industries/medical-devices), monitoramento preditivo da [GE HealthCare](https://www.trimedx.com/resource/how-ai-is-powering-smarter-medical-equipment-service) | Engenheiro de campo, suporte remoto |

### Padrões de mercado

1. **Chat sobre os documentos da casa virou item de série.** A Tulip responde a partir da instrução de trabalho ou do registro ([Tulip](https://tulip.co/digital-guidance/)); a Aquant ingere os manuais de serviço ([Aquant](https://appsource.microsoft.com/en-us/product/web-apps/aquant.aquant)); a Poka promete respostas ancoradas no conhecimento operacional ([Poka](https://www.poka.io/en/industrial-ai/)).
2. **O assistente mora dentro da ferramenta que a pessoa já usa.** Ninguém vende um aplicativo de chat separado. Isso bate com a leitura de "pensamento centrado em IA" do briefing.
3. **A corrida é de "responde" para "faz".** A Siemens diz que quer ir além do modelo de pergunta e resposta e executar fluxos inteiros ([Plant Automation](https://www.plantautomation-technology.com/technology-exclusives/press-releases/siemens-introduces-ai-agents-for-industrial-automation)). A Veeva planeja agentes para novembro de 2026 ([Clarkston](https://clarkstonconsulting.com/insights/veeva-ai-agents/)). A Poka mantém a aprovação do operador antes de agir ([Poka](https://www.poka.io/en/industrial-ai/)).
4. **A IA da qualidade olha para o escritório.** O lançamento da MasterControl em abril de 2026 resume eventos de qualidade para quem os analisa ([BriefGlance](https://briefglance.com/companies/mastercontrol-solutions-inc/pulses/32346)). Não foi encontrado nada desenhado para quem está de luva ao lado da máquina.
5. **Serviço de campo em dispositivos médicos já tem especialista.** A Aquant lista Stryker, Hologic, Cytiva, Elekta e Fresenius como clientes ([Aquant](https://aquant.ai/industries/medical-devices)) e tem assistente por voz para o técnico.
6. **Promessa em número grande, prova pequena.** "Até 50% de produtividade" na Siemens ([Siemens](https://news.siemens.com/en-us/ai-agents-manufacturing)); "39% mais rápido" na Aquant ([Aquant](https://www.aquant.ai/platform)). São números do próprio vendedor.

### Onde dá para se diferenciar

| Oportunidade | Por que está aberta | O que isso pede do design |
| --- | --- | --- |
| Fonte e dúvida como parte central da resposta | Todos dizem "resposta ancorada"; nenhum material mostra como a incerteza aparece na tela | Resposta estruturada com trecho citado, versão do documento e sinal claro de "não sei" |
| Fronteira explícita do que a IA não decide | O mercado corre para a autonomia; em indústria regulada, a decisão assinada é humana | Mostrar onde a IA para e a quem ela entrega a decisão |
| A pessoa entre o chão e a qualidade | Uma família serve o operador, outra serve o analista no escritório | Persona que precisa de procedimento e de precedente ao mesmo tempo, em pé |
| Continuidade entre turnos | Aparece só de passagem, como análise de padrões | O assistente carrega o contexto do que já foi tentado |
| Uso com restrição física | Os materiais mostram telas de chat comuns | Alvos grandes, pouca digitação, leitura à distância |

### O que isso diz sobre A e B

- **O caminho B é o mais ocupado.** Já existe um especialista com clientes de dispositivos médicos, e os fabricantes de equipamento têm os dados e o canal. Um conceito ali tende a parecer algo que já existe.
- **O caminho A tem um vão entre duas categorias.** Isso dá mais espaço para uma tese própria, mas exige explicar bem a persona, que é menos óbvia.

### Limites desta análise

- **Tudo aqui é material de venda.** Nenhum desses produtos foi usado, e as telas reais não foram vistas. "Não aparece no site" não significa "não existe no produto".
- **Não há dado de uso.** Nenhuma fonte diz se os operadores usam o chat de fato.
- **A lista não é completa.** Foram escolhidos exemplos representativos de cada família.

## Fontes

Páginas consultadas em 14 de novembro de 2026.

**Reguladores e normas**

- [ANVISA — RDC 665/2022, Boas Práticas de Fabricação](https://saude.campinas.sp.gov.br/saude/lista_legislacoes/legis_2022/U_RS-MS-ANVISA-RDC-665_300322.pdf)
- [ANVISA — classificação de impacto dos itens da RDC 665](https://www.gov.br/anvisa/pt-br/centraisdeconteudo/publicacoes/certificacao-e-fiscalizacao/compilado-procedimentos-SNVS/0016-pop-o-snvs-016/anexo-i-pop-o-snvs-016-classificacao-de-impacto-dos-itens-da-resolucao-rdc-665-rev-02-1-2.pdf)
- [ANVISA — RDC 509/2021, gerenciamento de tecnologias em saúde](https://fitoterapiabrasil.com.br/sites/default/files/legislacao/rdc_509_2021_comp.pdf)
- [FDA — relatório sobre assistência técnica de dispositivos médicos, 2018](https://www.fda.gov/media/113431/download?attachment)
- [UL — harmonização do 21 CFR 820 com a ISO 13485](https://www.ul.com/resources/us-fda-harmonization-21-cfr-part-820-iso-134852016)
- [IEC 62353:2014 — ficha da norma](https://genorma.com/en/standards/iec-62353-2014-ed2/amp)

**Caminho A**

- [Rosti — sala limpa classe 7 e classe 8](https://www.rosti.com/resources/blogs/cleanroom-injection-moulding-class-7-vs-class-8-what-is-the-difference/)
- [RapidDirect — moldagem por injeção para dispositivos médicos](https://www.rapiddirect.com/blog/medical-device-injection-molding/)
- [SG Systems — janelas de parâmetros de moldagem](https://sgsystemsglobal.com/?p=42236)
- [Pure Global — citações da FDA em dispositivos, ano fiscal 2025](https://www.pureglobal.com/blog-posts/fda-inspection-readiness-checklist-for-medical-device-manufacturers)
- [GMP Insiders — observações de inspeção da FDA, ano fiscal 2025](https://gmpinsiders.com/fy-2025-fda-inspection-observations/)
- Vagas: [Nordson Medical](https://talents.vaia.com/companies/nordson-medical/parker/cqc-tech-i-107807827/), [Cretex Medical](https://jofdav.com/jobs/52157421-quality-technician-molding-assembly-1st-shift), [Randstad](https://www.randstadusa.com/jobs/309/ab_4971986/quality-control-inspector_ontario/), [Jabil, operador](https://expoint.co/job/84794120), [Jabil, turnos](https://expoint.co/job/430526532)

**Caminho B**

- [AuntMinnie — quase metade dos chamados de imagem exige segunda visita](https://auntminnie.com/practice-management/service/equipment/article/15742637/ai-for-medical-imaging-service-technicians-speeds-fixit-resolution-time)
- [Aquant — benchmark de serviço em dispositivos médicos, 2025](https://discover.aquant.ai/medical-device-service-benchmarks)
- [Philips — serviços remotos](https://www.philips.co.id/healthcare/service/remote-maintenance) e [documento sobre gestão de equipamentos](https://www.documents.philips.com/assets/20211223/1c68294bf853419781dbae0700c31b7b.pdf)
- [Siemens Healthineers — Smart Remote Services](https://www.siemens-healthineers.com/en-ie/services/customer-services/upspeed-services/smart-remote-services)
- [Zone3 Podcast — o que faz um engenheiro de serviço de campo](https://share.transistor.fm/s/9180890a)
- [PMC — zonas de segurança em ressonância](https://pmc.ncbi.nlm.nih.gov/articles/PMC10657250)
- [OpenAnesthesia — segurança em ressonância](https://www.openanesthesia.org/keywords/magnetic-resonance-imaging-safety/)
- [Radiopaedia — blindagem de radiofrequência](https://radiopaedia.org/articles/radiofrequency-shielding)
- Vagas: [GE Healthcare](https://www.ihireengineering.com/jobs/view/487799435), [SimonMed](https://www.monster.com/job-openings/field-service-engineer-orlando-fl--ed822e53-1d9d-4f8d-9721-378018eaf0a8), [Symmetrio](https://remotejobs.jobboardly.com/jobs/senior-field-service-engineer-imaging-mri-ct-69bfce8a)

**Panorama competitivo** (consultadas em 16 de novembro de 2026)

- [Siemens — agentes de IA industriais](https://news.siemens.com/en-us/ai-agents-manufacturing) e [cobertura da Plant Automation](https://www.plantautomation-technology.com/technology-exclusives/press-releases/siemens-introduces-ai-agents-for-industrial-automation)
- [Tulip — Frontline Copilot](https://tulip.co/blog/introducing-ai-copilot-for-manufacturers-in-the-life-sciences-industry/) e [orientação digital](https://tulip.co/digital-guidance/)
- [Poka — IA industrial](https://www.poka.io/en/industrial-ai/)
- [Augmentir](https://augmentir.com/)
- [MasterControl — Event Summarizer](https://briefglance.com/companies/mastercontrol-solutions-inc/pulses/32346)
- [Clarkston — agentes de IA da Veeva](https://clarkstonconsulting.com/insights/veeva-ai-agents/)
- [IntuitionLabs — comparação de sistemas de qualidade, 2026](https://intuitionlabs.ai/articles/gxp-compliance-software-eqms-comparison-2026)
- [Aquant — dispositivos médicos](https://aquant.ai/industries/medical-devices), [plataforma](https://www.aquant.ai/platform) e [ficha na Microsoft](https://appsource.microsoft.com/en-us/product/web-apps/aquant.aquant)
- [TRIMEDX — IA no serviço de equipamentos médicos](https://www.trimedx.com/resource/how-ai-is-powering-smarter-medical-equipment-service)
