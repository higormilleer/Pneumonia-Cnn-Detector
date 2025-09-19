---

## 📊 Resultados

O modelo foi treinado e avaliado utilizando a base de dados **Chest X-Ray Pneumonia**.  
Os principais resultados foram obtidos em termos de **accuracy**, **precision**, **recall** e **f1-score**.

### Classification Report

O relatório de classificação apresenta o desempenho em cada classe:  

- **Pneumonia (Class 0)**: alta precisão (0.94) e bom recall (0.85).  
- **Normal (Class 1)**: desempenho equilibrado, com recall de 0.91, mostrando boa capacidade de identificar exames normais.  

<img src="Resultado/classification_report.png" width="600"/>

---

### Matriz de Confusão

A matriz de confusão permite visualizar os acertos e erros por classe:  

- 332 radiografias de pneumonia foram corretamente identificadas.  
- 212 radiografias normais foram corretamente classificadas.  
- Alguns falsos negativos e falsos positivos ocorreram, mas em baixa quantidade.  

<img src="Resultado/confusion_matrix.png" width="500"/>

---

### Teste com imagens externas

Para validar a robustez, foram utilizadas **10 imagens externas** (5 Pneumonia + 5 Normal), salvas na pasta `Imagens/`.  
O modelo conseguiu distinguir corretamente a maioria dos casos, como mostrado no grid abaixo:  

<img src="Resultado/grid_custom.png" width="900"/>

Legenda:  
- **True** = classe real.  
- **Pred** = classe prevista.  
- **P(pneumonia)** = probabilidade estimada pelo modelo.  
- ✓ = acerto, ✗ = erro.

---

## 📌 Conclusão

O modelo apresentou **87% de acurácia geral**, com bom equilíbrio entre as métricas de precisão e recall.  
Apesar de alguns erros em casos limítrofes, os resultados indicam que a CNN pode ser utilizada como uma ferramenta auxiliar em triagens médicas, especialmente em cenários com grande volume de exames.
