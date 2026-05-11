Objetivo:
Construir um mini dataset com 2 classes e 10 imagens no total, aplicando na prática os
fundamentos discutidos em aula:
 Resolução e profundidade de cor
 Conversões de espaço de cor (RGB, HSV, escala de cinza)
 Aquisição (condições de captura)
 Armazenamento e formatos (RAW/JPEG/PNG)
 Análise de impacto visual e funcional das escolhas
 Resposta no google Colab em markdown um relatório em conjunto com os códigos
respostas.
Esta atividade simula etapas reais de um projeto profissional:
 Construção de dataset próprio.
 Controle de aquisição.
 Decisão sobre formato e resolução.
 Análise de impacto técnico antes de treinar modelos.
Em aplicações industriais, médicas ou científicas, essas decisões definem o sucesso ou fracasso
do sistema. O objetivo é que o aluno desenvolva mentalidade de engenharia, não apenas execução
técnica.

Enunciado:
Você deverá capturar 10 imagens originais (feitas por você, com câmera do celular), que possam
ser separadas em duas classes (5 imagens por classe). Em seguida, você deverá aplicar
transformações e decisões de armazenamento com base nos fundamentos de Processamento de
Imagens Digitais vistos em aula, organizando ao final um mini dataset estruturado, pronto para
ser usado em tarefas de Visão Computacional.

Instruções:
Parte 1: Definiçio das classes
Escolha um tema simples, com boa distinção visual e fácil coleta:
Sugestões:
 Classe A: “Folha” | Classe B: “Flor”
 Classe A: “Copo” | Classe B: “Garrafa”
 Classe A: “Teclado” | Classe B: “Mouse”
 Classe A: “Porta” | Classe B: “Janela”
 Classe A: “Objeto com cor dominante vermelha” | Classe B: “Objeto com cor dominante
azul”
obs: Você pode escolher outro exemplo de imagem, acima sio sugestões opcionais.

 (Minha escolha) Classe A: “Objeto com cor dominante rosa” | Classe B: “Objeto com cor dominante não rosa”

Regras:
 As duas classes devem ser coerentes e claramente definidas.
 As imagens precisam ser capturadas por você , não baixar da internet.
Parte 2: Aquisiçio de imagens
Capture 5 imagens por classe, totalizando 10.
Requisitos mínimos de captura:
 Pelo menos 2 cenários de iluminação no conjunto total, por exemplo com luz natural,
sombra e luz artificial.
 Pelo menos 2 distâncias/ângulos diferentes para cada classe.
 Evitar filtros automáticos, desativar embelezamento.
Você deverá registrar em texto em markdown:
 Dispositivo usado: smartphone modelo X (foi Samsung A12)
 Condição de iluminação (pela noite)
 Distância aproximada (foi próxima da imagem)
 Observação de ruído, desfoque se houver.
Parte 3: Transformações de Imagens
Para 1 exemplo de cada classe, você deverá gerar versões derivadas.
A. Anilise de Resoluçio:
 1 versão em resolução original
 1 versão com redução em 50% da resolução
 1 versão com redução em 20% da resolução
obs: Realize comentário no colab sobre perda de detalhe percebida e possível impacto em visão
computacional
B. Espaço de cor
Gerar 1 exemplo de cada classe visualização em:
 RGB
 HSV.
 Escala de cinza

Registro textual:
Quais diferenças visuais aparecem ao converter ?
Em que tipo de tarefa você usaria cada uma?
C. Quantizaçio
Escolha uma imagem de cada classe e gere versões em:
 256 níveis de cinza
 64 níveis de cinza
 32 níveis de cinza
 2 níveis de cinza
Registrar:
O que muda visualmente?
Qual versão ainda seria mais útil para o seu dataset? e para qual aplicação ?
D. Formato de arquivo
Salvar versões em formatos diferentes:
 JPEG com compressão
 PNG sem perdas
Registrar:
 Tamanho do arquivo (KB/MB)
 Diferença visual percebida
 Hipótese sobre impacto em tarefas de PDI
Parte 4: Estrutura do mini dataset
Você deverá organizar o dataset em pastas com padrão de ML:

Estrutura sugerida:
dataset/
classe_A/
img001_original.įpg
img002_original.įpg
img003_original.įpg
img004_original.įpg
img005_original.įpg
classe_B/
img006_original.įpg
img007_original.įpg
img008_original.įpg
img009_original.įpg
img010_original.įpg

RUBRICA DE AVALIAÇÃO:
1. Aquisiçio das Imagens (20 pontos)
Avalia a qualidade da captura e coerência das classes.
Nível Descrição Pontos
Excelente 10 imagens próprias, classes bem definidas, variação controlada de
iluminação e ângulo, registro técnico claro
18–20
Bom 10 imagens próprias, classes coerentes, pouca variação de cenário ou
registro parcial
14–17
Regular Classes pouco distintas ou variação insuficiente 8–13
Insuficiente Uso de imagens da internet ou ausência de critérios de captura 0–7
2. Aplicaçio Correta dos Fundamentos (30 pontos)
Avalia se os conceitos foram corretamente aplicados.
Nível Descrição Pontos
Excelente Todas as transformações aplicadas corretamente e justificadas
tecnicamente
27–30
Bom Transformações aplicadas, mas justificativas superficiais 21–26
Regular Aplicações incompletas ou com erros conceituais 11–20
Insuficiente Transformações ausentes ou incorretas 0–10
Prazo: Semana 03 em 03/04/2026
3. Anilise Técnica e Reflexio Crítica (25 pontos)
Avalia profundidade conceitual e capacidade analítica.
Nível Descrição Pontos
Excelente Relaciona claramente resolução, cor, formato e aquisição com impacto
em Visão Computacional
22–25
Bom Responde às perguntas, mas com pouca conexão sistêmica 16–21
Regular Respostas descritivas, sem análise técnica 8–15
Insuficiente Respostas superficiais ou ausentes 0–7
4. Estruturaçio do Mini Dataset (15 pontos)
Avalia organização e padronização.
Nível Descrição Pontos
Excelente Estrutura clara de pastas, nomes padronizados, metadados organizados 13–15
Bom Estrutura organizada, mas com pequenas inconsistências 10–12
Regular Organização confusa ou incompleta 5–9
Insuficiente Dataset desorganizado ou incompleto 0–4
5. Organizaçio e Clareza do Notebook (10 pontos)
Avalia formatação, explicações e apresentação.
Nível Descrição Pontos
Excelente Notebook organizado, explicações claras, boa visualização das imagens 9–10
Bom Organização adequada, mas pouco detalhamento 7–8
Regular Apresentação confusa 4–6
Insuficiente Notebook desestruturado 0–3