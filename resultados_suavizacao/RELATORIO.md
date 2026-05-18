# Relatório Final — Suavização e Detecção de Bordas

## 1. Introdução

Imagens reais frequentemente apresentam degradações como ruído do sensor, granulação, pequenas variações aleatórias de intensidade e artefatos de compressão. Essas degradações podem prejudicar etapas posteriores, como segmentação e classificação.

## 2. Dataset Utilizado

- **Dispositivo:** Samsung A12 (camera traseira, modo automático)
- **Iluminação:** Noturna (luz artificial)
- **Distância:** 10–25 cm
- **Classes:** A (rosa) e B (não rosa)

## 3. Filtros de Suavização Aplicados

### 3.1 Filtro da Média
- Substitui cada pixel pela média dos vizinhos
- Simples mas borra bordas

### 3.2 Filtro da Mediana
- Substitui cada pixel pela mediana dos vizinhos
- Eficaz contra ruído sal e pimenta

### 3.3 Filtro Gaussiano
- Usa função Gaussiana para ponderar vizinhos
- Preserva melhor bordas que a média

### 3.4 Filtro Bilateral
- Considera proximidade espacial e similaridade de intensidade
- Preserva bordas enquanto suaviza

## 4. Operadores de Detecção de Bordas

### 4.1 Sobel
- Calcula gradiente nas direções X e Y
- Robusto a ruído

### 4.2 Laplacian
- Detecta bordas em todas as direções
- Sensível a ruído (requer pré-suavização)

### 4.3 Canny
- Multi-etapa: Sobel + supressão de não-máximos + histerese
- Bordas finas e precisas

## 5. Resultados e Conclusão

- O filtro bilateral apresentou os melhores resultados para preservação de bordas
- O operador Canny com thresholds (50, 150) apresentou os melhores resultados para detecção de bordas
- O pré-processamento com filtro Gaussiano foi essencial para reduzir falsas detecções
- A escolha do filtro e operador depende da aplicação específica