# Conilon
Repositório contendo arquivos utilizados no desenvolvimento do modelo de IA referente a defesa do mestrado no PPGMCS - Programa de Pós graduação em Modelagem Computacional e Sistemas


O Conilon Dataset foi desenvolvido exclusivamente para este projeto com o objetivo de suprir a ausência de bases públicas dedicadas ao café Coffea canephora (conilon). Após consultas diretas a instituições de referência nacional — Embrapa Café, Emater e Epamig — constatou-se que não havia, até então, um conjunto de imagens estruturado, público e rotulado contendo doenças e pragas específicas dessa variedade.

Diante dessa lacuna, o Conilon Dataset emerge como uma contribuição inédita e estratégica para pesquisas de visão computacional aplicadas à cafeicultura, especialmente no segmento do conilon, ainda sub-representado na literatura.

# 📸 Estrutura do Dataset

O dataset foi organizado considerando consistência visual, diversidade e representatividade, garantindo condições adequadas para treinamento robusto de modelos de aprendizado profundo.

Características principais

Imagens capturadas em campo real, contemplando:

- Diferentes condições de iluminação

- Múltiplos ângulos de captura

- Variações fenológicas das plantas

- Distintos níveis de severidade das doenças/pragas

Rotulagem realizada com base em critérios técnicos, reduzindo ambiguidades sem comprometer a variabilidade natural.

Organização seguindo boas práticas da literatura:

train/

val/

test/



O dataset também se diferencia de bases consolidadas como ROCOLE e LiCoLe, que são voltadas majoritariamente para Coffea arabica, não refletindo adequadamente as particularidades fisiológicas e fitossanitárias do café conilon.

# 🧠 Pipeline de Treinamento

O pipeline de treinamento adotado neste projeto segue um fluxo padronizado e replicável, desde o pré-processamento das imagens até a avaliação dos modelos.

1. Pré-processamento das imagens

- Redimensionamento para tamanho compatível com as arquiteturas utilizadas

- Normalização por canal

Aumento de dados (data augmentation):

- Rotação

- Flips horizontais/verticais

- Variação de brilho e contraste


2. Organização dos conjuntos

Treinamento: 70% das imagens

Validação: 15%

Teste: 15%

(Proporções definidas para garantir avaliação confiável e não enviesada.)

3. Estratégia de treinamento

- Frameworks utilizados: PyTorch

- Otimizador: Adam e SGD

- Critério de custo: Cross-Entropy

- Early stopping para evitar sobreajuste


# 🤖 Modelos Treinados

Diferentes arquiteturas de redes neurais profundas foram avaliadas a fim de identificar o melhor equilíbrio entre desempenho, custo computacional e aplicabilidade prática.

Modelos avaliados: 

- MobileNetV2 

Focada no baixo custo computacional
Ideal para aplicações em dispositivos embarcados

- ResNet50

Modelo mais profundo, com maior capacidade de extração de características
Utilizado como referência comparativa de desempenho


# Resultados gerais

Ambos os modelos alcançaram alta acurácia no conjunto de teste.

A MobileNetV2 demonstrou excelente relação entre eficiência e desempenho, sendo adequada para implementações em campo.
A ResNet50 apresentou métricas superiores em cenários com maior complexidade visual, servindo como baseline robusto.




# 🚀 Potencial de Expansão

O Conilon Dataset foi projetado para ser expandido, permitindo:

inclusão de novas classes de doenças e pragas

ampliação do número de imagens por classe

uso em novas tarefas, como detecção em tempo real e segmentação

Assim, além de atender aos objetivos do estudo original, o dataset se consolida como uma base aberta, em evolução, capaz de impulsionar pesquisas futuras em visão computacional aplicada à cafeicultura.
