# Módulo 1. Soluções Elementares de Escoamento Plano Irrotacional

Este tópico apresento um estudo introdutório detalhado dos escoamentos incompressíveis não viscosos, especialmente aqueles que possuem ambas as funções, corrente e potencial de velocidades. Muitas soluções empregam o princípio da superposição, de modo que destaquei esse tipo de solução em um único módulo para melhor detalhe. Aqui vamos começar com os três escoamentos elementares, ilustrados na figura abaixo: (a) uma corrente uniforme em certa direção, (b) uma linha de fonte / sumidouro na origem e (c) uma linha de vórtice na origem.

![Linhas de correntes elementares](C:\MECANICA_DE_FLUIDOS_python\Script_Prof_Edith\FluidoPython\Tres_Escoamento_Elementares.PNG)

## *1. Corrente uniforme em certa direção*

O escoamento elementar mais simples em que podemos pensar é uma corrente uniforme
$$
V = iU,
$$
como o primeiro esquema da figura acima, movendo-se com velocidade constante U na direção $(x)$ (da esquerda para direita). E que tem tanto uma função corrente como uma função potencial de velocidades, as quais podem ser encontradas da seguinte maneira:

$$
u = U = \frac{\partial \phi}{\partial x} = \frac{\partial \psi}{\partial y} \>\>\>\>\>
v = 0 = \frac{\partial \phi}{\partial y} = -\frac{\partial \psi}{\partial x}
$$
Integrando a primeira dessas equações com relação a $(x)$ e depois diferenciando o resultado em relação a $(y)$, geramos uma expressão para a função potencial de velocidade para uma corrente uniforme:

$$
\phi = Ux + f(y) \>\>\> --> \>\>\> v = \frac{\partial \phi}{\partial y} = f^{'}(y) = 0 \>\>\> --> \>\>\> f(y) = constante
$$
A constante é arbitrária, já que as componentes da velocidade são sempre derivadas de $\psi$. Fazemos a constante igual a zero, sabendo que podemos sempre adicionar uma constante arbitrária mais tarde se desejarmos. Portanto:

*Função potencial de velocidade para uma corrente uniforme:* 	$\phi = Ux$

De maneira similar geramos uma expressão para a função de corrente para esse escoamento irrotacional planar elementar:

Função de corrente para uma corrente uniforme:* 	$\psi = Uy$

As linhas de corrente são linhas retas horizontais $(y = const)$, e as linhas equipotenciais são verticais $(x = const)$, ou seja, ortogonais às linhas de corrente, como se esperava.

Muitas vezes é conveniente expressar a função de corrente e a função potencial de velocidade em coordenadas cilíndricas em vez de coordenadas cartesianas, particularmente quando formos sobrepor uma corrente uniforme a algum outro escoamento irrotacional planar. As relações de conversão são obtidas da geometria da figura abaixo:

figura çengel

equação çengel

Com as equações acima e um pouco de trigonometria, deduzimos relações para $u$ e $v$ em termos de coordenadas cilíndricas:

equação çengel

Em coordenadas cilíndricas, a função $\psi$ e $\phi$ tornam-se:

equação çengel

## *2. Linha de fonte ou sumidouro na origem*

Nosso segundo escoamento elementar é uma linha de fonte localizada na origem do plano xy, com a própria linha coincidindo com o eixo z. Suponha que o eixo z seja uma espécie de tubo distribuidor bem fino, por meio do qual o fluido seria emitido uniformemente a uma vazão total Q ao longo de seu comprimento b. Observando o plano xy, veríamos um escoamento radial cilíndrico para
fora, ou fonte, como esboça a Figura 8.3b. As coordenadas polares no plano são adequadas
(ver Figura 4.2), não havendo velocidade circunferencial. A qualquer distância radial *r* da linha de fonte, a componente radial da velocidade, *ur* pode ser determinada aplicando-se o princípio da conservação da massa. Isto é, toda a vazão em volume por unidade de profundidade da linha de fonte deve passar atráves do círculo definido pelo raio *r*. Assim:

equação çengel

Usando coordenadas cilíndricas no termo da velocidade radial, e também reconhecendo que *uo* é zero em todos os pontos. Integrando e descartando outra vez as constantes de integração, obtemos as funções apropriadas para esse escoamento radial simples:

equação

em que m 5 Q/(2pb) é uma constante, positiva para uma fonte, negativa para um sumidouro.
Como mostrado na Figura 8.3b, as linhas de corrente são raios (u constante),
e as linhas equipotenciais são círculos (r constante). As linhas de corrente e linhas equipotenciais são mutuamente ortogonais em todos os pontos exceto na origem, que é um ponto singular.

Em situações nas quais gostaríamos de colocar uma linha de fonte ou sumidouro em algum outro lugar que não seja na origem, devemos transformar as equações ~~perigosamente~~, rsrsrs, na verdade, cuidadosamente. Para entender essa transformação com mais detalhes recomendo a leitura do livro Mecânica dos Fluidos Fundamentos e Aplicações, Çengel e Cimbala. É necessário um pouco de trigonometria para transformar as equações, e assim obtemos as funções em coordenadas cartesianas de uma fonte que está na localização absoluta (a,b):

equação çengel

## *3. Linha de vórtice irrotacional*

Nosso terceiro é uma linha de vórtice (bidimensional) e de caso simples no qual a linha está localizada na origem, tendo um movimento permanente puramente circulatório, e mais uma usamos coordenadas cilíndricos por conveniência, yu 5 f(r) apenas, e yr 5 0, que são:

equação çengel

onde T é chamado de **circulação** ou **intensidade do vórtice**. Seguindo a convenção padrão da matemática, T positivo representaum vórtice no sentido anti-horário, enquanto T negativo representa um vórtice no sentido hórario. 

Novamente, podemos integrar e determinar as funções apropriadas:

equação çengel

Como mostra a Figura 8.3c, as linhas de corrente são círculos (r constante) e as linhas equipotenciais são linhas radiais (u constante). Observe a similaridade entre as Equações (8.13) e (8.14). O vórtice livre é uma espécie de imagem reversa de uma fonte. O “vórtice de ralo”, que
se forma quando água é drenada por um orifício no fundo de um tanque, é uma boa
aproximação para o padrão de vórtice livre.

Em situações na quais gostaríamos de colocar o vórtice em algum outro lugar que não seja na origem, devemos transformar as equações conforme foi feita para uma linha de fonte. E assim obtemos as funções em coordenadas cartesianas de uma linha de vórtice que está na localização absoluta (a,b):

equação çengel



**Conteúdo fornecido sob licença MIT. (c) 2018 Batystuta Rocha. Obrigado: Prof. Edith Beatriz pelo apoio ao conhecimento, muito obrigado.**

**Versão 1.0 novembro 2018**