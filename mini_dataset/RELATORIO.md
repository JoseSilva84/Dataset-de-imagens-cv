# Relatorio Final — Mini Dataset de Processamento de Imagens Digitais

## 1. Aquisicao de Imagens
- **Dispositivo:** Samsung A12 (camera traseira, modo automatico)
- **Iluminacao:** Noturna (luz artificial)
- **Distancia:** 10–25 cm
- **Angulos:** Frontal, ~30 graus, ~45 graus zenital
- **Observacao:** Ruido visivel em ISO alto; leve desfoque periferico

## 2. Classes
| Classe | Descricao | Imagens Originais |
|--------|-----------|-------------------|
| A | Objetos com cor dominante rosa | 5 |
| B | Objetos com cor dominante nao rosa | 5 |

## 3. Transformacoes Aplicadas
| Transformacao | Classe A | Classe B |
|---------------|----------|----------|
| Original | sim | sim |
| 50pct Resolucao | sim | sim |
| 20pct Resolucao | sim | sim |
| HSV | sim | sim |
| Escala de Cinza | sim | sim |
| Quantizacao 256 | sim | sim |
| Quantizacao 64 | sim | sim |
| Quantizacao 32 | sim | sim |
| Quantizacao 2 (binario) | sim | sim |
| JPEG comprimido | sim | sim |
| PNG sem perdas | sim | sim |

## 4. Analise Tecnica

### 4.1 Resolucao
A reducao de resolucao impacta diretamente a quantidade de informacao espacial. A 20pct, detalhes finos sao perdidos.

### 4.2 Espaco de Cor
- RGB: padrao para redes neurais
- HSV: melhor para segmentacao por cor
- Cinza: economico e eficaz para tarefas baseadas em forma

### 4.3 Quantizacao
Niveis abaixo de 32 introduzem posterizacao visivel. Recomenda-se >=64 niveis.

### 4.4 Formato
JPEG 30pct qualidade gera artefatos perceptiveis. PNG e preferivel quando fidelidade e prioridade.

## 5. Conclusao
O dataset gerado cobre os fundamentos de aquisicao, resolucao, cor, quantizacao e formatos de arquivo. A estrutura segue o padrao de diretorios para ML, pronto para uso com ferramentas como ImageDataGenerator, torchvision.datasets.ImageFolder ou tf.keras.utils.image_dataset_from_directory.