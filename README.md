## Questão 4 — Diagrama de bifurcação do mapa logístico
 
Construção do diagrama de bifurcação do mapa logístico dado por
 
$$G(x) = r\,x\,(1 - x)$$
 
onde `r` é um parâmetro. O código foi modificado para gerar o diagrama nos
intervalos pedidos no item (a): `r ∈ [2.5, 4.0]` e `r ∈ [3.73, 3.75]`.
 
O código completo está no notebook [`listaE_questao4.ipynb`](listaE_questao4.ipynb).
Ele roda direto no Google Colab, sem instalar bibliotecas adicionais (usa apenas
`numpy` e `matplotlib`).
 
### Método numérico
 
A iteração do mapa foi implementada em uma função separada dos valores numéricos
e das condições iniciais:
 
```python
def mapa_logistico(x, r):
    x = r*x*(1 - x)
    return x
```
 
Para cada valor de `r`, as primeiras 500 iterações são descartadas (transiente)
e as 100 seguintes são guardadas, revelando o comportamento estável do sistema.
 
### (a.1) Intervalo r ∈ [2.5, 4.0]
 
O diagrama clássico: à medida que `r` cresce, o sistema passa de ponto fixo para
duplicações de período e, por fim, para o regime caótico.
 
![Diagrama para r em [2.5, 4.0]](diagrama_2.5_4.0.png)
 
### (a.2) Zoom no intervalo r ∈ [3.73, 3.75]
 
Ampliação de uma janela periódica que aparece dentro do regime caótico.
 
![Diagrama para r em [3.73, 3.75]](diagrama_3.73_3.75.png)
