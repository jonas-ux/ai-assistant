# 04 — Definição: proto-persona, problema, valor da IA, hipóteses e riscos

Nov 16, 2026 · @Jonas José

## Escopo final

Em 16/11, Jonas decidiu simplificar: o projeto fica com a Cíntia e com uma solução enxuta. Este doc guarda todo o raciocínio, inclusive as ideias que saíram; o que vale para o design está no doc 05 (PRD).

| Fica no projeto | Foi para "visão de futuro" |
| --- | --- |
| Resposta com regra, dado e sugestão separados | A verificação rápida ("o próximo teste") |
| Os caminhos lado a lado, como formato da resposta | Descobrir quando o defeito começou, com dados internos da máquina (a conta simples, desde a última inspeção boa, voltou ao projeto) |
| A IA dizer "não sei" e indicar quem chamar | A IA avisar antes da inspeção |
| O registro que se escreve enquanto ela age | A mudança de tese sobre liberar material de manhã |
| A visão do supervisor, como terceira tela estratégica |  |

Motivo: nem Jonas nem a IA conhecem fábrica por dentro, e o briefing avalia a capacidade de simplificar. As seções abaixo que tratam das ideias retiradas continuam aqui como registro do processo.

## Escolha do caminho e da persona

**Decisão (16/11, Jonas): caminho A, candidata A2, a técnica de qualidade do chão de fábrica.** Ela ficou em primeiro em todas as formas de somar a matriz, por margem pequena quando saem os dois critérios que eu acrescentei. O restante desta seção registra como a escolha foi feita.

### Os quatro candidatos

Cada um descrito por uma cena, para ficar concreto.

|  | Quem é | A cena |
| --- | --- | --- |
| A1 | **Preparador de processo.** Cuida das máquinas injetoras: troca molde, dá partida, ajusta. | A peça começa a sair com rebarba. Ele precisa saber até onde pode mexer na temperatura sem sair do que foi aprovado, e se isso já aconteceu nesse molde. |
| A2 | **Técnica de qualidade do chão de fábrica.** Inspeciona peças durante a produção e decide o que fazer quando acha defeito. | Na ronda das 3h ela acha um risco nas peças de uma máquina. Precisa saber: o procedimento manda parar a linha? Separar quanto material? Isso já aconteceu, e o que resolveram? |
| B1 | **Engenheiro de serviço de campo.** Conserta ressonâncias e tomógrafos dentro de hospitais. | O tomógrafo parou com um código de erro. Ele está sozinho, o hospital pergunta quando volta, e ele precisa decidir o próximo teste e que peça pedir. |
| B2 | **Engenheiro de suporte remoto.** Atende por telefone e tela, analisando os registros da máquina à distância. | Recebe o chamado, lê os registros de erro e tenta resolver sem mandar ninguém, ou decide quem mandar e com que peça. |

### A matriz

Notas de 1 a 5, onde 5 é melhor. Os quatro primeiros critérios são os que você pediu; os dois últimos eu acrescentei e estão marcados.

| Critério | O que mede | A1 Preparador | A2 Téc. qualidade | B1 Eng. de campo | B2 Suporte remoto |
| --- | --- | --- | --- | --- | --- |
| Intensidade da dor | Quão urgente e custoso é o momento | 4 | 4 | 5 | 3 |
| Quanto a IA ajuda de verdade | Se ela faz algo que uma busca comum não faz | 5 | 5 | 4 | 4 |
| Cabe em 3 telas | Se a história se conta em principal, resposta e uma terceira | 4 | 5 | 4 | 5 |
| Cara de indústria | Se o avaliador reconhece contexto industrial na hora | 5 | 5 | 4 | 2 |
| **Soma dos 4 critérios pedidos** |  | **18** | **19** | **17** | **14** |
| Espaço para se diferenciar (meu) | O quanto o mercado já ocupa esse lugar | 4 | 5 | 2 | 2 |
| Dá para defender na apresentação (meu) | Se você consegue explicar sem ser da área e sem informação de dentro | 3 | 4 | 3 | 3 |
| **Soma dos 6 critérios** |  | **25** | **28** | **22** | **19** |

### Por que cada nota

- **Dor.** B1 leva 5 porque tem o melhor número da pesquisa (cerca de 60% de resolução na primeira visita) e um equipamento parado. A1 e A2 levam 4: o momento é tenso, com lote em risco, mas a evidência é indireta.
- **IA ajuda.** Em A, a resposta exige cruzar três coisas que estão em lugares diferentes: o procedimento, o limite aprovado e o que aconteceu em casos passados. Busca comum não faz isso. Em B a IA também ajuda, mas perde um ponto porque não há conexão dentro da sala de ressonância.
- **3 telas.** A2 e B2 levam 5 porque a história fecha sozinha: situação, pergunta, resposta estruturada, próximo passo.
- **Indústria.** B2 leva 2 porque é um trabalho de mesa. B1 leva 4 porque acontece em hospital, e o avaliador pode ler como clínico.
- **Diferenciar.** B já tem um especialista com clientes do setor. A2 ocupa o vão entre as duas famílias de produto do doc 03.
- **Defender.** A2 leva 4 porque os conceitos de qualidade (procedimento, defeito, lote, decisão assinada) se explicam em linguagem comum. A1 exige falar de parâmetros de máquina; B1, de eletrônica de equipamento.

### O argumento contra a minha recomendação

- **A dor de A2 é menos provada.** Não achei número que meça o tempo que ela perde. Se o avaliador perguntar "como você sabe que isso dói?", a resposta honesta é "por inferência, e eis como eu validaria".
- **A ligação com a entrevista corta dos dois lados.** Mostra que você ouviu; mas pode parecer que você sabe mais do que deveria. A regra de só usar o que foi dito na entrevista resolve, desde que apareça escrita no PDF.
- **As notas são julgamento meu.** Um ponto a mais ou a menos em dois critérios inverte A2 e B1 na soma dos quatro pedidos.
- **B1 conta uma história mais fácil.** "Máquina parada, engenheiro sozinho" se entende em cinco segundos. A2 precisa de uma frase a mais de contexto.

### O que muda se você escolher cada um

| Se escolher | A tese do projeto vira | Maior risco |
| --- | --- | --- |
| A2 | "A IA junta procedimento e precedente na hora do desvio, e devolve a decisão para quem assina." | Dor sem número direto |
| A1 | "A IA diz até onde dá para ajustar sem sair do aprovado." | Exige domínio técnico de injeção |
| B1 | "A IA leva o conhecimento do veterano para quem está sozinho em campo." | Parecer algo que já existe |
| B2 | "A IA faz a triagem antes de mandar alguém." | Pouca cara de indústria |

## Proto-persona

Cíntia é técnica de qualidade no turno da noite de uma fábrica de descartáveis médicos de plástico. Ela é uma proto-persona: foi montada a partir de pesquisa de mesa, sem entrevista com nenhuma pessoa real. Tudo abaixo é suposição a validar.

|  |  |
| --- | --- |
| Nome | Cíntia Moraes, 34 anos |
| Cargo | Técnica de qualidade, turno da noite |
| Onde trabalha | Fábrica de descartáveis médicos, como seringas: molda as peças plásticas em sala limpa, monta, embala e esteriliza o produto acabado |
| Formação e tempo de casa | Curso técnico; dois anos na empresa como operadora e quatro meses na qualidade, no primeiro semestre do turno da noite. Conhece o básico, mas ainda não tem a memória dos casos antigos que os veteranos têm. Mudança decidida por Jonas em 16/11: uma técnica com anos de casa precisaria pouco do assistente |
| O que faz | Inspeciona peças durante a produção, libera a linha no início de cada lote, registra medições e abre o relatório quando acha um defeito |
| O que decide sozinha | A contenção imediata: parar ou não a máquina, quanto material separar |
| O que não decide | O destino final do material e a liberação do lote, que são da garantia da qualidade, no horário comercial |
| Com quem fala | Operadores, preparador de processo, líder de turno; de manhã, a técnica do turno seguinte e a analista de qualidade |

### O que a fábrica dela produz

A fábrica faz produtos médicos descartáveis do começo ao fim: molda as partes plásticas, monta, embala e esteriliza. Cíntia atua na etapa de moldagem. O exemplo que veio da entrevista é a parte plástica das seringas. O que segue é conhecimento geral sobre esse tipo de fábrica, não informação de nenhuma empresa.

| Peça | O que é |
| --- | --- |
| Corpo da seringa | O cilindro transparente com a escala de medida |
| Haste do êmbolo | A peça que se empurra com o polegar |
| Protetor da agulha | A capinha que cobre a agulha |
| Canhão da agulha | A base plástica colorida onde a agulha de metal é fixada |

Um único molde faz dezenas de peças iguais a cada poucos segundos, e a máquina roda dia e noite. Por isso um defeito que passa uma hora sem ser visto já contaminou milhares de peças.

Os defeitos que Cíntia procura:

- **Rebarba:** sobra de plástico na emenda do molde. Pode soltar partícula ou atrapalhar o encaixe.
- **Falha de preenchimento:** a peça saiu incompleta.
- **Ponto preto:** sujeira ou plástico queimado dentro da peça.
- **Risco ou marca:** dano na superfície; no corpo da seringa, pode atrapalhar a leitura da escala ou o deslizar do êmbolo.
- **Deformação ou medida fora:** a peça não encaixa ou vaza.

Numa seringa, um defeito pequeno pode virar vazamento, dose errada ou contaminação. É isso que faz a decisão dela pesar.

### Um turno dela

Ela percorre as máquinas em rondas, de touca, máscara e luva. Em cada uma, pega amostras, olha, mede e anota. Na maior parte das vezes está tudo certo. Quando não está, o relógio começa a correr: cada minuto de máquina rodando com defeito é mais material suspeito para separar depois.

De madrugada, quem assina as decisões maiores não está na fábrica. Ela resolve o imediato com o que tem à mão e deixa o resto registrado para a manhã.

### O que ela usa hoje

- Um terminal compartilhado com a pasta de procedimentos, em arquivos longos.
- O sistema da qualidade, onde ficam os relatórios de defeitos antigos, com busca por palavra exata.
- O caderno ou a planilha de passagem de turno.
- O telefone do líder ou do supervisor, quando a dúvida é grande.
- A memória dos colegas mais antigos.

### O que ela quer

- Tomar a ação certa sem ter de acordar ninguém.
- Não parar a linha à toa, nem deixar passar o que devia ter parado.
- Deixar um registro que se sustente quando alguém perguntar "por que você fez isso?".

### O que a frustra

- Saber que a resposta existe em algum procedimento e não achar o trecho a tempo.
- Descobrir de manhã que o mesmo defeito já tinha acontecido em outro turno e ninguém sabia.
- Reescrever no relatório o que já tinha explicado de boca na passagem de turno.

### Restrições de uso

- Luva e máscara o turno todo dentro da sala; em pé, entre máquinas.
- Aparelho da fábrica, compartilhado; nada de celular pessoal.
- Ruído das máquinas.
- Fora da sala, uma mesa com computador comum para escrever relatórios.

## Problema

Quando Cíntia acha um defeito, ela decide sozinha, com a máquina rodando, quanto parar e quanto separar, e de manhã responde por isso. O problema é de decisão sob pressão, com responsabilidade; não é de busca.

Esta é a segunda versão do enquadramento. A primeira dizia "a informação está espalhada", o que só admitia uma solução: juntar a informação, um caminho óbvio. Quem apontou isso foi Jonas, em 16/11. A afirmação de que o mercado já oferece essa solução é minha, tirada do panorama competitivo do doc 03.

### O trabalho que ela precisa fazer (job to be done)

> Quando encontro um defeito durante a produção, quero decidir a contenção sabendo o tamanho provável do estrago e o que a regra e os casos passados dizem, para proteger o paciente sem desperdiçar material bom e conseguir explicar depois por que fiz o que fiz.

Por trás do trabalho prático há um emocional: sentir-se segura de que agiu certo, sozinha, de madrugada.

### Declaração do problema

A técnica de qualidade toma, sozinha e em minutos, uma decisão que custa caro nos dois sentidos: separar material de menos deixa peça ruim seguir; separar de mais joga material bom fora e para a máquina sem necessidade. Ela decide sem saber quando o defeito começou, registra depois e de memória, e o que aprendeu não chega inteiro ao próximo turno nem a quem vai investigar a causa.

| O que pesa | Por quê | O que acontece hoje |
| --- | --- | --- |
| O relógio | A máquina faz milhares de peças por hora; cada minuto aumenta o material suspeito | Ela age antes de ter certeza |
| O tamanho do estrago | Ninguém sabe quando o defeito começou; só quando foi a última inspeção boa | Separa a mais, por segurança, ou a menos, por pressão de produção |
| A responsabilidade | De manhã alguém pergunta "por que parou?" ou "por que não parou?" | O registro é escrito depois, de memória, e defende mal a decisão |
| A continuidade | O que ela viu e tentou fica na cabeça dela | O turno seguinte recebe a passagem de turno, mas só com o que coube na anotação, e a investigação da causa começa com informação pobre |

O que o problema não é:

- **Não é falta de procedimento.** As regras existem.
- **Não é falta de competência.** Ela sabe inspecionar.
- **Não é um problema de busca.** Achar o documento mais rápido ajuda, mas não tira dela o peso de decidir sem saber o tamanho do estrago.

### Por que isso importa para o negócio

A mesma decisão aparece em três números que uma fábrica acompanha: material descartado, tempo de máquina parada e qualidade das investigações de causa. Os dois primeiros são eficiência e desperdício. O terceiro é o ponto em que os reguladores mais reprovam fábricas de dispositivos médicos, como mostra o doc 03.

### Projeção ilustrativa

Os números abaixo são inventados para mostrar a ordem de grandeza do ganho. São plausíveis para esse tipo de máquina, por conhecimento geral, mas não vêm de nenhuma fábrica real. No PDF, entram com o rótulo "cenário ilustrativo".

| Suposição | Valor |
| --- | --- |
| Peças por ciclo da máquina | 32 |
| Duração de um ciclo | 12 segundos |
| Produção por hora | 9.600 peças |
| Intervalo entre rondas de inspeção | 2 horas |

|  | Hoje | Com o assistente |
| --- | --- | --- |
| O que se sabe sobre o início do defeito | Só que a última inspeção estava boa | Os registros da máquina mostram uma mudança 20 minutos antes |
| Material suspeito a separar | Até 19.200 peças | Cerca de 3.200 peças |
| Tempo até decidir a contenção | 15 minutos | 5 minutos, ou 1.600 peças a menos |

Neste cenário, cada ocorrência teria cerca de 80% menos material suspeito. Material suspeito não é o mesmo que material descartado: parte dele é reinspecionada e aproveitada. A projeção só vale se a máquina registrar seus parâmetros ao longo do tempo.

### Ideia registrada: a visão do gestor

Ideia de Jonas, em 16/11. Os registros que Cíntia e as colegas geram ao agir alimentam uma visão para quem responde pelo turno ou pela qualidade: tempo de máquina parada, material separado, alertas quando um indicador sai do esperado e um relatório dos problemas que se repetem, com hipóteses de causa.

- **Onde entra:** é candidata à terceira tela estratégica e mostra o valor para o negócio, não só para a pessoa.
- **O que a torna centrada em IA:** a síntese dos problemas recorrentes com hipóteses de causa. Os gráficos de indicadores, sozinhos, são um painel comum.
- **Cuidado:** o briefing pede uma persona simples. O gestor aparece como quem recebe o resultado do trabalho da Cíntia, não como segunda persona.
- **Decisão:** fica para a Etapa 2, junto com as outras candidatas à terceira tela.

### Perguntas "como poderíamos"

1. Como poderíamos mostrar a ela o tamanho provável do estrago antes que ela precise perguntar?
2. Como poderíamos fazer com que agir e registrar fossem a mesma coisa, de modo que a passagem de turno e a investigação já nasçam prontas?
3. Como poderíamos dar a ela a segurança de saber quando decidir sozinha e quando chamar alguém?

### Crítica do próprio enquadramento

- **A pergunta 1 depende de dados que talvez não existam.** Estimar o estrago exige saber a hora da última inspeção boa e quanto a máquina produziu desde então. Se isso ainda estiver em papel, a ideia cai. Vira hipótese de viabilidade técnica.
- **A pergunta 1 chega perto da linha.** Uma IA que estima "quanto separar" está a um passo de decidir por ela. O desenho precisa mostrar a conta e deixar a decisão com a pessoa.
- **"Minutos" e "milhares por hora" são ordens de grandeza minhas,** não medições.
- **A solidão da madrugada é suposição.** Se houver plantão da qualidade à noite, a dor diminui.
- **Continua sem número direto de dor.** O briefing não pede evidência; pede hipóteses. Esta entra como a primeira delas, com a forma de validar.

## Papel da IA

A IA é a colega que chega à cena já sabendo o contexto, faz a conta do estrago, lembra o que aconteceu antes e escreve o registro enquanto Cíntia age. Ela nunca decide o que tem assinatura.

### O que ela faz que uma busca comum não faz

|  | Busca comum | Este assistente |
| --- | --- | --- |
| Ponto de partida | Ela digita palavras | Ela aponta a máquina e o defeito; lote, molde e hora da última inspeção boa já estão lá |
| O que usa | Textos de documentos | Documentos, registros da máquina, inspeções anteriores e casos passados |
| O que devolve | Uma lista de documentos para ela ler | Uma resposta montada: o que a regra manda, o tamanho provável do estrago, o que foi feito em casos parecidos |
| Quando não acha | Nada, ou algo que não serve | Diz que não sabe e indica quem chamar |
| Depois da resposta | Nada | O registro e a passagem de turno já estão escritos |

### Os cinco papéis

1. **Chega sabendo.** Parte da situação, não de uma pergunta. Cíntia não precisa descrever onde está nem o que está rodando.
2. **Faz a conta e mostra.** Estima quanto material pode estar afetado e exibe de onde tirou a estimativa: última inspeção boa, produção desde então, mudança registrada pela máquina.
3. **Lembra por ela.** Traz casos parecidos, inclusive de outros turnos, e organiza as causas possíveis em quatro grupos que toda fábrica conhece: pessoa, máquina, método e material.
4. **Escreve enquanto ela age.** Cada passo vira o relatório do defeito, a passagem de turno e o ponto de partida da investigação. Ela revisa e confirma; não redige.
5. **Sabe quando não basta.** No caso sem precedente ou sem dado, diz que é hora de chamar alguém e entrega o resumo pronto para enviar.

### Apostas mais ousadas

Jonas avaliou os cinco papéis como "o básico bem feito" (16/11). Estas três apostas vão além. Cada uma muda o trabalho da Cíntia, e não só a velocidade com que ela o faz.

| Aposta | O que muda | Exemplo na tela | Risco |
| --- | --- | --- | --- |
| **O próximo teste** | Em vez de só estimar o estrago, a IA indica a verificação mais barata que mais reduz a dúvida | "Meça 5 peças da cavidade 12 do molde. Se estiverem boas, o defeito está em 1 das 32 cavidades e o material suspeito cai de 3.200 para 100 peças." | Sugerir um teste errado e dar falsa segurança |
| **A IA fala primeiro** | Ela não espera a ronda: acompanha os registros da máquina e chama a Cíntia quando algo muda | "Máquina 7 mudou há 6 minutos. Em 2 casos parecidos, isso veio antes de rebarba. Vale inspecionar agora." | Alertas demais, que ela aprende a ignorar; exige mais dados e mais validação |
| **Os caminhos lado a lado** | A resposta estruturada deixa de ser um texto e vira a comparação das opções, cada uma com sua consequência | "Parar agora: 3.200 peças suspeitas, 40 min de máquina parada. Seguir e reinspecionar: 9.600 peças a mais por hora em risco." | Parecer que a IA está empurrando uma opção |

Minha recomendação:

- **Adotar "o próximo teste" como o coração da resposta estruturada.** É o que mais foge do padrão de mercado, mantém a decisão com a pessoa e usa a IA para raciocinar, não para buscar.
- **Usar "os caminhos lado a lado" como formato da resposta.** Combina com a anterior e resolve a tela de resposta estruturada do briefing.
- **Deixar "a IA fala primeiro" como visão de futuro,** citada no PDF. É a mais ousada, mas a que mais depende de dados e de validação.

**Decisão (16/11, Jonas):** "o próximo teste" e "os caminhos lado a lado" entram no escopo. "A IA fala primeiro" fica como visão de futuro, porque depende de os registros da máquina serem automáticos.

### Onde a IA não age

| Decisão | Quem decide | O que a IA faz no lugar |
| --- | --- | --- |
| Parar a máquina | Cíntia, com o líder de turno | Mostra o que o procedimento diz e a conta do estrago |
| Quanto material separar | Cíntia | Propõe uma faixa e mostra a base; ela confirma ou ajusta |
| Destino do material: descartar, reinspecionar ou aproveitar | Garantia da qualidade | Prepara o resumo do caso e sugere um destino, com base na regra e em casos parecidos, rotulado como sugestão. Quem decide registra o próprio motivo e assina |
| Liberação do lote | Garantia da qualidade, com assinatura | Reúne os registros; não opina |
| Causa do defeito | Quem conduz a investigação | Oferece hipóteses, rotuladas como hipóteses |
| Ajuste na máquina | Preparador de processo e engenharia | Não sugere ajuste; aponta o responsável |
| Mudança em procedimento | Qualidade, por processo formal | Nunca altera; pode sinalizar que um trecho gerou dúvida |

A regra por trás da tabela: a IA propõe, a pessoa decide e assina, e o registro guarda quem decidiu o quê.

### Como ela mostra fonte, confiança e incerteza

- **Três tipos de conteúdo que nunca se misturam.** Cada parte da resposta tem um rótulo visível:
  - **Regra:** trecho do procedimento, citado como está escrito, com documento, versão e data.
  - **Dado:** o que a máquina e as inspeções registraram.
  - **Sugestão da IA:** estimativa ou hipótese, sempre com a base ao lado.
- **Fonte a um toque.** Tocar numa regra ou num dado abre o original no ponto exato.
- **Confiança em palavras, não em porcentagem.** "87% de confiança" parece exato e não é. No lugar: "baseado em 3 casos parecidos nos últimos 12 meses" ou "entre 2.800 e 3.600 peças, porque...".
- **Diz o que falta.** "Não há registro da máquina entre 1h10 e 1h40" ou "nenhum caso parecido encontrado". A falta muda a recomendação: sem base, o caminho é chamar alguém.
- **Mostra o conflito.** Se um caso antigo foi resolvido de um jeito e o procedimento atual manda outro, mostra os dois e deixa claro que a regra vale.
- **Avisa quando o documento mudou.** Se o procedimento foi revisado depois do caso antigo, isso aparece.
- **Aceita correção.** Ela pode marcar "isto não se aplica", e a marcação entra no registro.

### Princípios de comportamento

1. Situação antes da pergunta.
2. Regra, dado e sugestão nunca se misturam.
3. Toda estimativa mostra a conta.
4. "Não sei" é uma resposta válida e útil.
5. O que tem assinatura é decidido por gente.
6. Agir e registrar são a mesma coisa.
7. Curto, e com quase nada para digitar: escolhas e botões grandes no lugar do teclado. Se o toque funciona com a luva é questão do aparelho; o que cabe ao design é não exigir gesto fino.

### Crítica desta seção

- **Nenhuma peça é nova sozinha.** Assistente com contexto, citação de fonte e rascunho automático existem no mercado. A tese está na combinação e, sobretudo, na fronteira explícita do que a IA não decide.
- **Rótulo não impede que ela siga a máquina sem pensar.** Mesmo marcada como sugestão, a estimativa tende a virar a decisão. Por isso o desenho pede que ela confirme ou ajuste o número, em vez de só aceitar.
- **Mostrar a conta ocupa espaço.** Isso briga com uma tela curta, para luva. Mas a conta é o que sustenta a decisão, então fica sempre visível. O que vai para um toque de distância é o resto: o texto integral do procedimento e os detalhes dos casos antigos.
- **O papel 2 depende de a máquina registrar seus dados ao longo do tempo.** Sem isso, a estimativa encolhe para "tudo desde a última inspeção boa", que ela já sabe.

## Hipóteses

O projeto se apoia em quinze suposições, e duas delas derrubam tudo se estiverem erradas: que Cíntia decide sozinha sob pressão (D1) e que a máquina guarda seus registros num lugar que o assistente consiga ler (T1). Nenhuma foi validada; cada uma traz a forma de testar com gente real.

### As cinco hipóteses-chave

Estas são as que vão para o PDF. Foram escolhidas por três perguntas: se estiver errada, o projeto cai? Um avaliador perguntaria sobre ela? Dá para explicar em uma frase? As demais ficam nas tabelas abaixo, como apoio.

|  | A hipótese, em uma frase | Como verificaríamos |
| --- | --- | --- |
| 1 | Cíntia decide a contenção sozinha, com pressa, e isso pesa para ela | Acompanhando dois turnos da noite |
| 2 | Quando a IA sugere uma verificação rápida para descobrir o tamanho real do problema, Cíntia a faz antes de decidir, em vez de pular por pressa | Protótipo no tablet com cenários simulados |
| 3 | Separar regra, dado e sugestão faz ela confiar na medida certa | Mostrando duas versões da resposta e perguntando "o que aqui é regra?" |
| 4 | A máquina guarda registros que o assistente consegue ler | Conversando com a engenharia e a TI da fábrica |
| 5 | Separar menos material por ocorrência paga o investimento | Medindo três meses de como é hoje |

### Desejabilidade: ela quer isso?

|  | Hipótese | Como validaríamos com usuários reais | O que a derrubaria |
| --- | --- | --- | --- |
| D1 | A contenção é decidida por uma pessoa só, sob pressão de tempo, e isso pesa | Acompanhar 2 turnos da noite; entrevistar de 5 a 8 técnicas de turnos diferentes | Existir plantão da qualidade à noite, ou a decisão ser sempre em dupla |
| D2 | Ela separaria menos material se soubesse quando o defeito começou | Rever 20 relatórios antigos: quanto foi separado e quanto estava de fato ruim | O material separado já ser próximo do realmente afetado |
| D3 | Ela faria o teste sugerido antes de decidir | Protótipo no tablet com 3 cenários simulados; observar se ela testa ou pula | Ela pular o teste por pressa na maioria das vezes |
| D4 | Separar regra, dado e sugestão aumenta a confiança certa | Mostrar duas versões da resposta, texto corrido e rotulada, e perguntar "o que aqui é regra?" | Ela não distinguir os três, ou ignorar os rótulos |
| D5 | Ela revisa de verdade o registro que a IA escreveu | Colocar um erro de propósito no rascunho e ver se ela percebe | Ela confirmar sem ler |

### Viabilidade técnica: dá para construir?

|  | Hipótese | Como validaríamos | O que a derrubaria |
| --- | --- | --- | --- |
| T1 | A máquina registra seus números ao longo do tempo e a fábrica os guarda em lugar acessível | Conversa com engenharia de processo e TI; inventário das fontes de dados | Os dados existirem só na tela da máquina, ou em papel |
| T2 | Procedimentos e relatórios antigos estão em formato digital legível | Amostra de 30 documentos | Boa parte ser papel digitalizado como imagem |
| T3 | Os casos antigos estão descritos bem o bastante para achar "parecidos" | Buscar 20 casos reais e pedir que alguém da qualidade avalie os resultados | Descrições curtas demais, como "peça com defeito" |
| T4 | A IA sugere um próximo teste útil na maioria dos casos e sabe se calar nos outros | Casos históricos avaliados às cegas por especialistas | Sugestões genéricas, ou erradas com aparência de certas |
| T5 | O assistente pode ser validado como software de ambiente regulado | Conversa com a garantia da qualidade para classificar o risco e separar apoio de registro oficial | A exigência de validação tornar o piloto inviável |
| T6 | Um tablet funciona na sala limpa: toque com luva, rede, limpeza | Um dia de teste de campo | Luva ou rede impedirem o uso |

### Viabilidade de negócio: vale a pena?

|  | Hipótese | Como validaríamos | O que a derrubaria |
| --- | --- | --- | --- |
| N1 | A redução de material suspeito por ocorrência paga o investimento | Medir 3 meses de linha de base: ocorrências, material separado, quanto foi descartado | Ocorrências raras, ou pouco material descartado |
| N2 | Registros mais ricos melhoram as investigações de causa | Comparar tempo de fechamento e repetição de problemas antes e depois de um piloto | Nenhuma diferença perceptível |
| N3 | A fábrica aceita IA num ponto de decisão de qualidade | Oficina com qualidade, produção e área regulatória | Veto por política interna ou por risco regulatório |
| N4 | Dá para começar pequeno: uma linha e um tipo de defeito | Desenhar o piloto com a fábrica | Só fazer sentido com a fábrica inteira conectada |

### Perguntas para usuários reais

Estas vieram do rascunho inicial do bônus e pertencem a quem conhece fábrica por dentro:

1. Existe alguém da qualidade no chão de fábrica durante a madrugada?
2. Quando acha um defeito, o que você consulta primeiro: um procedimento, um sistema ou um colega?
3. Dentro da área controlada, vocês usam tablet, terminal fixo ou papel?
4. Como a informação passa de um turno para o outro?

## Riscos e limitações

O maior risco não é a IA errar; é a pessoa confiar quando ela erra. O desenho reduz esse risco, mas não o elimina.

| Risco | O que pode dar errado | Como o desenho reduz | O que sobra |
| --- | --- | --- | --- |
| A IA inventar | Citar uma regra que não existe ou um caso que não aconteceu | Regra só aparece como trecho literal, com documento e versão; sem fonte, não aparece | Citar o trecho certo de um documento desatualizado |
| Confiança em excesso | Ela seguir a sugestão sem pensar | Confirmar ou ajustar o número; rótulo de sugestão; registrar o próprio motivo | Hábito e pressa vencem rótulos com o tempo |
| Teste errado | O "próximo teste" dar falsa segurança e ela separar de menos | Mostrar em que casos a sugestão se baseia; manter sempre visível o caminho conservador da regra | Um defeito novo, sem caso parecido, que pareça conhecido |
| Validação do software | Indústria regulada precisa provar que cada software faz o que promete, e uma IA não responde sempre igual | O registro oficial continua no sistema da qualidade; o assistente é apoio; versão do modelo travada; tudo fica rastreável | Custo e prazo de validação, que podem atrasar até um piloto |
| Acesso a dados | Registros da máquina presos no equipamento; histórico em papel | Começar por uma linha que já tenha dados; funcionar, com menos precisão, só com casos antigos | Sem dado da máquina, a conta do estrago perde o valor |
| Adoção | Ela sentir que a IA a vigia, ou que o registro será usado contra ela | O registro é a defesa dela: ela revê e edita antes de enviar | Desconfiança que só se resolve com tempo e com a postura da gestão |
| Autoria do registro | Se a IA escreveu, quem responde pelo que está escrito? | Ela revisa e assina; o que foi gerado fica marcado como gerado | Revisão apressada, que a hipótese D5 testa |
| Chão de fábrica | Luva, rede, aparelho compartilhado, limpeza do tablet | Pouca digitação, botões grandes, entrada por crachá | Depende de aparelho e infraestrutura que o design não controla |
| Sigilo | Dados de processo saírem da empresa | Rodar em ambiente controlado pela empresa | Decisão de arquitetura, fora do alcance deste conceito |

### Sobre a validação do software

A indústria usa um guia chamado GAMP 5 para decidir quanto de prova cada software exige, conforme o risco. Pelo que sei, a edição mais recente já trata de inteligência artificial, e a FDA publicou orientação própria sobre garantia de software. Não verifiquei essas duas afirmações nesta etapa. O que importa para o conceito é o princípio: quanto mais perto de uma decisão de qualidade, mais prova se exige. Por isso o assistente apoia e a pessoa decide.

### Limitações deste trabalho

- **Nenhum usuário real foi ouvido.** A persona é uma proto-persona de pesquisa de mesa.
- **Os números da projeção são ilustrativos.**
- **A pesquisa sobre rotina vem quase toda de fontes dos Estados Unidos.**
- **O panorama competitivo se baseia em material de venda,** não em uso dos produtos.

## Aprendizados da persona sintética

O teste com a Cíntia simulada mudou seis pontos do projeto, e o mais importante foi a tese: o valor da conta do estrago aparece mais na manhã seguinte do que na madrugada. Nada aqui é evidência.

### O que é isto e o que não é

Uma persona sintética é um personagem que a IA interpreta. Eu recebo uma ficha com o jeito de pensar da Cíntia e respondo às perguntas como ela provavelmente responderia. A ideia vem de empresas que testam seus assistentes contra clientes simulados antes de mostrá-los a clientes reais.

- **Serve para:** achar furos baratos, antes de gastar tempo de gente real.
- **Não serve para:** provar que algo é verdade. Quem escreveu as hipóteses e quem interpretou a Cíntia fui eu. É uma discussão comigo mesmo, com um ponto de vista forçado.

### A ficha usada na simulação

> Você é Cíntia, técnica de qualidade há dois anos, no turno da noite de uma fábrica de descartáveis médicos. Responda em primeira pessoa, com frases curtas e sem termos de tecnologia. Você tem pressa. Seu maior medo é levar a culpa por um lote ruim que passou. Você desconfia de novidade que vem "de cima" e confia nos colegas antigos. Você já viu sistema novo que só deu mais trabalho. Seja honesta sobre quando ignoraria uma ferramenta.

### As perguntas, as respostas e o que mudou

| Pergunta | O que a Cíntia simulada respondeu | O que mudou no projeto |
| --- | --- | --- |
| Em que situação você ignoraria o assistente? | "Quando eu já sei o que é. Rebarba naquela máquina eu vejo toda semana. Não vou parar para ler tablet." | **Modo rápido.** Para defeito conhecido, ela registra em dois toques, sem passar pela resposta completa. O valor aí é o registro, não o conselho |
| A IA sugere olhar seis peças de uma cavidade. Você olha? | "Se for um minuto, olho. Mas as peças caem todas juntas na caixa. Só sei de onde veio cada uma se tiver o número gravado nela." | **O teste mostra quanto custa.** A sugestão passa a dizer o tempo estimado, só aparece se for possível com o que ela tem à mão, e pode ser pulada com um motivo |
| Você confiaria no número de peças suspeitas? | "Eu separaria um pouco a mais do que ele diz. Se der problema, a culpa é minha. Ninguém é punido por separar demais." | **A tese muda.** De madrugada ela separa com folga, e está certa. A conta serve para a garantia da qualidade liberar de manhã, com segurança, a parte que estava boa |
| O registro se escreve sozinho. Você assina? | "Assino se estiver do jeito que eu falo. Se afirmar causa que eu não afirmei, apago. E tenho medo de assinar às 5h sem ler direito." | **O registro assinado só tem fatos:** o que ela viu, o que fez e a que horas. As hipóteses de causa ficam à parte, marcadas como da IA. Antes de assinar, um resumo de três linhas |
| E se o supervisor vir um painel com as suas ocorrências? | "Se for para ver máquina com problema, ótimo. Se for para contar quantas vezes eu parei a linha, vou parar menos." | **A visão do gestor agrupa por máquina, molde e tipo de defeito.** Nunca por pessoa |
| A IA diz "não achei caso parecido, chame alguém", às 3h. Você liga? | "Ligar para o supervisor de madrugada tem custo. Só ligo se for grave. Senão paro a máquina, separo tudo e deixo para a manhã." | **Dois níveis de escalonamento.** "Pode esperar a manhã", com o resumo pronto, e "chame agora", com o critério tirado do procedimento, não inventado pela IA |

### O que isso fez com as hipóteses

- **A hipótese-chave 2 ficou mais fraca.** A verificação rápida só funciona se a peça puder ser ligada à cavidade de onde saiu. Isso vira uma hipótese técnica nova: as peças têm o número da cavidade gravado.
- **A hipótese-chave 5 mudou de lugar.** O ganho não está em separar menos à noite, e sim em liberar mais rápido, de manhã, o que estava bom. A projeção ilustrativa precisa ser lida assim.
- **Surgiu uma hipótese nova de comportamento.** Ela separa com folga, não importa o que a IA diga, porque o custo de errar é dela.
- **A hipótese-chave 1 saiu reforçada no raciocínio, não na prova.** O medo de levar a culpa explica quase todas as respostas.

### Limites deste teste

- **As respostas refletem o que eu acho plausível.** Uma Cíntia real pode responder o oposto.
- **A ficha puxa para a desconfiança de propósito.** O objetivo era derrubar ideias, não confirmá-las.
- **Detalhes de fábrica nas respostas,** como as peças caírem juntas na caixa, são conhecimento geral meu, sem fonte.
