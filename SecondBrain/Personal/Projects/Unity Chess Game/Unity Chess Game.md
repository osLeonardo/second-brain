#### Itens
- 1 (um) dado de 6 (seis) lados;
- 1 (um) dado de 20 (vinte) lados;
- 1 (um) jogo completo  de xadrez (pecas e tabuleiro)

#### Classes
				 | Guarda | Arqueiro | Cavaleiro | Torre | Paladino | Rei
		  Ataque |   01   |    03    |     01    |   02  |    10    |  00
		    Vida |   05   |    05    |     01    |   15  |    10    |  30
		 Alcance |   01   |    03    |     01    |   02  |    01    |  00
	Movimentação |   03   |    03    |     02    |   00  |    01    |  04

#### Habilidades
- **Guarda**
>Transforma-se em qualquer outro Classe caso chegue ao outro lado do campo (pode transformar-se em Paladino apenas se o da sua equipe não estiver mais vivo).

- **Arqueiro**
>Às distâncias 2 e 3 (dois e três), seu dano é normal, mas à uma casa do inimigo, seu dano se iguala ao de um guarda, 1 (um).

- **Torre**
>Sua Bola de Fogo causa dano normalmente à casa-alvo e metade do dano causado às casas ao seu entorno;
>
>Pode transformar-se em um Arqueiro, caso não haja mais vivos na equipe.

- **Cavaleiro**
>Os Cavaleiros ganham 1 (um) ponto por cada Guarda inimigo morto, para incrementar em Ataque.

- **Rei**
>Caso não haja mais Guardas e Torres, pode dar spawn de 2 (dois) Guardas ao atravessar o campo (apenas uma vez na partida);
>
>Caso o Rei fique sozinho, o jogador pode rolar um dado de 20 (vinte) lados apenas 1 (uma) vez. Caso caia em:
>
>	- 1 (um): Recebe buff 1 (um) de Ataque ate o proximo turno;
>	- 8 (oito): Pode dar spawn de 1 (um) Paladino;
>	- 13 (treze): Pode dar spawn de 3 (três) Guardas;
>	- 20 (vinte): Ativa a Magia Armageddon (Vitória);
>	- Qualquer outro número: Derrota (sem causadores de dano).

#### Movimentação / Combate
- Só é possível movimentar na horizontal e vertical;
- Combate pode ser iniciado na horizontal, vertical e diagonal.
- Pode-se interagir o total de 2 (duas) peças iguais no mesmo turno, sendo:
>Movimentar 2 (duas) peças diferentes (da mesma Classe), podendo atacar apenas 1 (uma) vez (com uma das peças movidas);
>
>Atacar utilizando 2 (duas) peças de Classe diferentes, não podendo mover-se;
>
>A ação de mover sempre deve ser realizada antes de atacar;
>
>	- Caso o jogador ataque sem ter se movido, suas ações de movimento são automaticamente anuladas, permitindo então:
>		- que realize um segundo ataque com outra peca;
>		- finalize seu turno.
- **Paladino**
>As ações permitidas no turno são reduzidas a 1 (uma) no caso do Paladino, então:
>
>	- Apenas mover ou apenas atacar;
>	- Interagir com o Paladino impossibilita interagir com qualquer outra peça no mesmo turno;
>	- Interagir com qualquer peça impossibilita interagir com o Paladino no mesmo turno.

#### Informações adicionais
- Toda peça *spawnada* sofre efeito de zumbificação, tendo +1 (um) de Ataque (desde que não reduza o total para 0 (zero)) e -10% (dez) de Vida (arredondando sempre ao menor valor)
>Isto não se aplica às habilidades do Guarda e da Torre, por se tratarem de transformações.