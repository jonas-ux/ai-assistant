# 05 — PRD: assistente de IA para a técnica de qualidade

Nov 16, 2026 · @Jonas José

## Resumo

Cíntia inspeciona peças de seringa de madrugada e está há quatro meses na função. Quando acha um defeito, precisa decidir sozinha o que fazer, sem ter ainda a memória dos casos antigos que os veteranos têm. O assistente mostra o que a regra da fábrica manda, o que foi feito em casos parecidos, e escreve o registro junto com ela. A decisão é sempre de uma pessoa.

PRD é a sigla em inglês para "documento de requisitos do produto": um resumo curto do que vamos construir e por quê. Este serve de base para o design e para o protótipo; não vai para o PDF. O raciocínio completo está nos docs 03 e 04.

## Problema

Quando a técnica de qualidade encontra um defeito durante a produção, ela decide a contenção (parar ou não a máquina, quanto material separar) sozinha e com pressa, e no dia seguinte responde por essa decisão. As regras existem e os casos antigos também, mas estão em lugares diferentes e não chegam a ela na hora. O registro é escrito depois, de memória, e passa incompleto para o turno seguinte.

Isto é uma hipótese de pesquisa de mesa. Nenhuma pessoa real foi ouvida.

## Para quem

| Quem | Papel no produto |
| --- | --- |
| **Cíntia, técnica de qualidade do turno da noite** | Usuária principal. Quatro meses na qualidade, no primeiro semestre do turno da noite. Usa um tablet da fábrica, de luva e máscara, em pé entre as máquinas. O assistente é a memória da fábrica para quem ainda não tem a sua. Veteranas usam sobretudo o registro rápido |
| **Quem assina a decisão final, de manhã** | Lê o registro que Cíntia deixou e decide o destino do material |
| **Supervisor de qualidade** | Vê o resumo dos problemas que se repetem. É o leitor da terceira tela |

## Objetivos

1. Cíntia vê a regra aplicável e os casos parecidos sem precisar procurar nem digitar.
2. Ela compara as opções de contenção lado a lado e escolhe com segurança. Cada opção mostra quanto material foi produzido desde a última inspeção boa.
3. O registro fica pronto enquanto ela age, e serve para o turno seguinte e para quem assina.
4. O supervisor enxerga os problemas que se repetem, sem depender de ler relatório por relatório.

## O que este produto não faz

| Não faz | Por quê |
| --- | --- |
| Decidir o destino do material ou liberar lote | São decisões assinadas por uma pessoa |
| Sugerir ajuste na máquina | Mexer no processo é de outra função e tem regra própria |
| Avisar antes de a inspeção achar o defeito | Depende de dados internos da máquina, que não sabemos se existem; fica como visão de futuro |
| Medir desempenho de pessoas | O resumo do supervisor agrupa por máquina e por tipo de defeito, nunca por pessoa |

## Como saber se deu certo

Sem dados reais, não há metas numéricas. Estas são as medidas que um piloto acompanharia.

| Medida | O que mostra | Aparece em |
| --- | --- | --- |
| Parte dos defeitos registrada pelo assistente | Se ela usa de verdade | Dias |
| Tempo entre achar o defeito e ter o registro completo | Se agir e registrar viraram a mesma coisa | Dias |
| Vezes em que quem decide de manhã precisou pedir mais informação a Cíntia | Se o registro chega completo | Semanas |
| Vezes em que a IA disse "não sei" e isso estava certo | Se a IA sabe o próprio limite | Semanas |
| Tempo até a decisão final sobre o material separado | Eficiência: material parado é custo | Meses |
| Material descartado por ocorrência | Desperdício, que também é uma medida de sustentabilidade | Meses |
| Problemas que voltam a acontecer | Se as investigações de causa melhoraram | Meses |

## A jornada da Cíntia

Jornada e telas são coisas diferentes: a jornada é o caminho que Cíntia percorre, e cada passo pode usar uma tela, várias ou nenhuma. Abaixo está a jornada; quantas telas ela vira é decisão da Etapa 2. As marcações em itálico só apontam onde entram as telas que o briefing exige.

1. **Começo do turno.** O tablet é da fábrica e passa de mão em mão. Cíntia encosta o crachá nele para o sistema saber quem está usando, do mesmo jeito que se abre uma catraca. Ela vê o mapa das máquinas do setor. *Tela principal.*
2. **Ronda sem problema.** Ela inspeciona uma máquina, está tudo certo, e registra com um toque. Isso provavelmente já existe hoje em algum sistema e não é novidade nossa. Importa porque a hora da última inspeção boa alimenta a conta do passo 4.
3. **Achou um defeito.** Ela toca na máquina e escolhe o tipo de defeito numa lista. Não digita. Se o defeito não estiver na lista, ela fotografa e dá um nome; o novo tipo entra no catálogo depois que alguém da qualidade revisar. *Tela de interação.*
4. **O assistente responde.** Ele mostra o que a regra manda, os casos parecidos, quanto material foi produzido desde a última inspeção boa e os caminhos possíveis lado a lado. Se não achar caso parecido, diz isso e mostra o caminho mais seguro previsto na regra. *Tela de resposta estruturada.*
5. **Ela toma a decisão imediata.** Parar ou não a máquina, e o que separar. O registro se monta com o que ela viu e fez. Ela lê um resumo de três linhas e confirma encostando o crachá de novo. Em indústria regulada, essa confirmação identificada é o que vale como assinatura; não há papel.
6. **Na manhã seguinte.** A decisão de Cíntia foi a imediata. Sobra uma segunda decisão, que não é dela: o que fazer com o material separado (descartar, inspecionar de novo ou aproveitar). Quem decide isso encontra o caso pronto. O supervisor vê o resumo dos problemas que se repetem. *Terceira tela.*

## As telas

| Tela | O que mostra | Entregável | Aparelho |
| --- | --- | --- | --- |
| **Principal** | Mapa das máquinas do setor, com o estado de cada uma | Estrutura em cinza e alta fidelidade | Tablet |
| **Interação** | Escolha da máquina e do tipo de defeito, por toques | Estrutura em cinza | Tablet |
| **Resposta estruturada** | Regra, casos parecidos e os caminhos lado a lado, com a fonte de cada informação | Estrutura em cinza e alta fidelidade | Tablet |
| **Visão do supervisor** | Problemas que se repetem, por máquina e tipo de defeito, com suposições de causa marcadas como suposições | Alta fidelidade; é a terceira tela estratégica | Tablet e computador, num desenho que se adapta aos dois |

"Estrutura em cinza" é o que o briefing chama de wireframe: a tela só com a organização da informação, sem cores nem acabamento.

### O que cada tela precisa ter

- **Principal**
  - Um mapa das máquinas em que a cor conta a história: cada máquina vai mudando de cor conforme passa o tempo desde a última inspeção, e fica em amarelo quando tem uma ocorrência em aberto. Ideia de Jonas.
  - A cor nunca vem sozinha: cada estado também tem um ícone e uma palavra, para quem não distingue cores e para a luz da fábrica.
  - As ocorrências em aberto aparecem na própria máquina, sem dizer quem registrou nem de qual turno vieram. O foco é a máquina, não o colega.
  - Um caminho rápido para defeito já conhecido: registrar em dois toques.
- **Interação**
  - Nenhum teclado no caminho principal.
  - Máquina e lote já preenchidos.
  - Para defeito novo: foto e nome.
- **Resposta estruturada**
  - Três blocos com nomes simples, que nunca se misturam (ver a tabela abaixo).
  - Os caminhos lado a lado. Cada um mostra o que a regra diz, o que aconteceu em casos parecidos e quanto material foi produzido desde a última inspeção boa.
  - O trecho da regra em uma ou duas linhas, na própria tela. Cíntia não vai parar para ler um documento no meio da produção; o documento completo fica guardado no registro, para quem decide de manhã e para auditoria.
  - Um estado de "não sei": mostra o caminho mais seguro previsto na regra e deixa o caso sinalizado para a manhã. Chamar alguém é uma opção, não uma obrigação.
  - O aviso do que é decisão de outra pessoa.
- **Visão do supervisor**
  - Os problemas que mais se repetem, agrupados por máquina e tipo de defeito.
  - Suposições de causa marcadas como suposições, com os casos em que se baseiam.
  - Nenhuma contagem por pessoa.

As quatro telas usam uma única linguagem visual.

### Os três blocos da resposta

| Bloco | O que é | Exemplo |
| --- | --- | --- |
| **O que a regra diz** | Um trecho copiado do documento oficial da fábrica. A IA não muda as palavras | "Risco visível na peça: separar todo o material produzido desde a última inspeção aprovada." |
| **O que foi registrado** | Fatos que já estão no sistema | "Última inspeção boa: 1h10. Esta máquina faz cerca de 9.600 peças por hora. Em 12 de setembro houve um caso igual nesta máquina." |
| **O que a IA sugere** | O que ela concluiu a partir dos dois blocos acima. Pode estar errada | "Foram produzidas cerca de 19.000 peças desde a última inspeção boa. Nos 3 casos parecidos, a máquina foi parada." |

A conta do material é simples de propósito: horas desde a última inspeção boa vezes a produção por hora da máquina. Usa só o que o próprio assistente já registrou, sem depender de dados internos da máquina.

## Como a IA se comporta

1. **Ela não escreve pergunta.** Cíntia toca na máquina e no tipo de defeito, e o assistente já responde.
2. **Três blocos que nunca se misturam.** O que a regra diz, o que foi registrado e o que a IA sugere.
3. **A regra cabe em duas linhas.** O trecho aparece na tela; o documento completo fica guardado no registro.
4. **"Não sei" é uma resposta.** Sem caso parecido, a IA diz isso, mostra o caminho mais seguro da regra e sinaliza o caso para a manhã.
5. **A IA organiza a decisão; não a toma.** A decisão imediata é de Cíntia. A decisão final sobre o material é de outra pessoa.
6. **Agir e registrar são a mesma coisa.** O registro que Cíntia confirma com o crachá tem só fatos: o que viu, o que fez e a que horas.
7. **Pouco texto e nenhum teclado.** Escolhas e botões grandes, para uso em pé e de luva.

## Riscos principais

| Risco | O que o desenho faz |
| --- | --- |
| A IA inventar uma regra ou um caso | Regra só aparece como trecho literal, com fonte; sem fonte, não aparece |
| Cíntia confiar sem conferir | Rótulo de sugestão, fonte a um toque, e ela escolhe o caminho em vez de aceitar um veredito |
| Ela sentir que está sendo vigiada | O registro é dela, revisado por ela; o resumo do supervisor nunca mostra pessoas |
| Exigência de provar que o software é confiável, comum em indústria regulada | O assistente apoia; o registro oficial e a decisão continuam no processo da fábrica |

A lista completa está no doc 04.

## Visão de futuro

Ideias que ficaram fora de propósito, para manter o projeto simples. Entram no PDF em uma linha cada.

- **Verificação rápida:** a IA sugere uma checagem que reduz a dúvida antes da decisão.
- **Quando o defeito começou:** a IA usa os dados internos da máquina para descobrir o momento em que algo mudou e reduzir o material a separar. A conta simples, desde a última inspeção boa, já está no projeto.
- **Aviso antecipado:** a IA acompanha a máquina e avisa antes de a inspeção achar o defeito.

## Perguntas em aberto

| Pergunta | Quem responde | Trava o trabalho? |
| --- | --- | --- |
| Quantos estados intermediários o protótipo mostra, além das telas obrigatórias? | Design, na Etapa 2 | Não |
| O design system escolhido tem tema neutro e componentes de conversa? | Verificação técnica, antes da Etapa 3 | Sim, para a Etapa 3 |
| Existe plantão da qualidade à noite nessas fábricas? | Usuários reais | Não; fica como hipótese |
| Os registros da máquina podem ser lidos por um assistente? | Engenharia da fábrica | Não; só afeta a visão de futuro |
