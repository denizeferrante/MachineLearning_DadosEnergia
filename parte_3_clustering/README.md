# Parte 3 – Clustering de consumidores de energia (K-Means)

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `clustering_energia.ipynb` | Notebook com o exemplo resolvido e o exercício proposto implementado, executado e respondido |
| `consumidores_energia_proposto.csv` | Base de entrada (60 consumidores) |
| `imagens/` | Gráficos Elbow, Silhouette e dispersões por cluster (Python) |
| `orange/` | Fluxo `.ows`, CSV exportado com clusters e prints do Orange (**adicionar**) |

## Escolha de k

**k = 4.** A curva Elbow muda de inclinação em k = 4: a queda da inércia passa de ≈ 12,8 (3→4) para ≈ 2,9 (4→5).
O Silhouette Score também é máximo em k = 4 (≈ 0,667, contra 0,648 em k = 3 e 0,586 em k = 5).

## Perfis encontrados

| Perfil | Consumidores | Consumo médio | Demanda média | % noturno |
|---|---:|---:|---:|---:|
| Baixo consumo, uso diurno | 15 | ≈ 225 kWh | ≈ 3,1 kW | ≈ 19% |
| Intermediário, uso diurno | 15 | ≈ 473 kWh | ≈ 6,2 kW | ≈ 22% |
| Intermediário, uso noturno | 15 | ≈ 482 kWh | ≈ 6,4 kW | ≈ 72% |
| Alto consumo e alta demanda | 15 | ≈ 918 kWh | ≈ 12,2 kW | ≈ 47% |

Os dois grupos intermediários só se separam por causa do percentual noturno.

## Ações sugeridas

- **Alto consumo e alta demanda:** acompanhar a demanda máxima e orientar a distribuir o uso de equipamentos potentes para reduzir picos.
- **Intermediário noturno:** oferecer tarifa diferenciada por horário, já que ≈ 72% do consumo ocorre entre 22h e 6h.

Os grupos indicam hipóteses: não comprovam desperdício, eficiência ou tipo de estabelecimento.
