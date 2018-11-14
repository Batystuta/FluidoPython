# Módulo 0. Introdução e Revisão

Este é o primeiro notebook do material FluidoPython, para Escoamento Potencial. Se você não estiver familiarizado com a computação numérica usando o Python, primeiro estude as ferramentas científica em Python, recomendada como "lição zero" deste material.

Você pode ler e acompanhar este caderno on-line, enquanto digita o código em seu próprio bloco de anotações Jupyter limpo ou em um arquivo ".py" no seu editor Python favorito. De qualquer maneira, certifique-se de experimentar os códigos e escrever suas próprias versões e assim ampliando o seu conhecimento!

## *1. Introdução rápida*

A mecânica dos fluidos é um tema excitante e fascinante, com aplicações práticas ilimitadas que variam de sistema biológicos microscópicos a automóveis, aviões e propulsão de aeronaves. Contudo, ela é também, historicamente, um dos assuntos mais desafiadores para os estudantes universitários. Dessa maneira, é importantíssimo o uso extensivo de imagens como um instrumento de aprendizagem que ajuda o aluno a entender a matéria.

## *2. Conceitos sobre campo potencial de velocidades*

Lembre-se que, se os efeitos viscosos são desprezados, os escoamentos a baixas velocidades são irrotacionais, $\bigtriangledown \times V = 0$, existindo o potencial de velocidades $\phi$ tal que

$$
\mathrm{V} = \bigtriangledown \phi
$$

$$
\mathit{u} = \frac{\partial \phi }{\partial x} \>\>\>\>
\mathit{v} = \frac{\partial \phi }{\partial y} \>\>\>\>
\mathit{w} = \frac{\partial \phi }{\partial z}
$$

A equação da continuidade, $\bigtriangledown V = 0$, reduz-se à equação de Laplace para $\phi$:
$$
\bigtriangledown ^{2} \phi = \frac{\partial^2 \phi}{\partial x^2} + \frac{\partial^2 \phi}{\partial y^2} + \frac{\partial^2 \phi}{\partial z^2} = 0
$$

## *3. Conceitos sobre função corrente* 

Relembre que, se um escoamento é descrito por apenas duas coordenadas, também existe a função corrente $\psi$ como uma opção de abordagem. Para escoamentos incompressíveis planos, em coordenadas $\mathit{xy}$, a forma correta é:

$$
\mathit{u} = \frac{\partial \psi }{\partial x} \mathit{v} = - \frac{\partial \psi }{\partial y}
$$
A condição de irrotacionalidade também reduz-se à equação de Laplace para $\psi$:

$$
2\omega _{z} = 0 = \frac{\partial v}{\partial x} - \frac{\partial u}{\partial y} = \frac{\partial }{\partial x}\left ( -\frac{\partial \psi}{\partial x} \right ) - \frac{\partial }{\partial y}\left ( \frac{\partial \psi}{\partial y} \right )
$$

$$
\frac{\partial^2 \psi}{\partial x^2} + \frac{\partial^2 \psi}{\partial y^2} = 0
$$

Para as aplicações deste material, podemos calcular tanto o $\phi$ como $\psi$, ou ambas, e a solução correspondente será uma *rede de escoamento ortogonal*, como na figura abaixo.

![](C:\MECANICA_DE_FLUIDOS_python\Script_Prof_Edith\FluidoPython\Linhas_Correntes_Equipotenciais.jpg)

Muitas soluções são convenientemente expressas em coordenadas polares $(r,\theta)$. Os componentes de velocidade e as relações diferenciais para as funções $\phi$ e $\psi$ são alterados para as seguintes formas:

$$
v_{r} = \frac{\partial \phi}{\partial r} = \frac{1}{r} \frac{\partial \psi}{\partial \theta} \>\>\>\>\> 
v_{\theta} = \frac{1}{r} \frac{\partial \phi}{\partial \theta} = - \frac{\partial \psi}{\partial r}
$$
A equação de Laplace assume a seguinte forma:

$$
\frac{1}{r} \frac{\partial }{\partial r} \left ( r \frac{\partial \phi}{\partial r} \right ) + \frac{1}{r^{2}} \frac{\partial^2 \phi}{\partial \theta^{2}} = 0
$$
Para $\psi(r,\theta)$, a mesma equação vale exatamente em termos de coordenadas polares:

$$
\frac{1}{r} \frac{\partial }{\partial r} \left ( r \frac{\partial \psi}{\partial r} \right ) + \frac{1}{r^{2}} \frac{\partial^2 \psi}{\partial \theta^{2}} = 0
$$
Um aspecto intrigante do escoamento potencial sem superfície livre é que tanto as equações governantes, equação de Laplace para $\psi​$ e $\phi​$ não contêm parâmetros. Logo, as soluções são puramente geométricas, dependendo apenas do formato do corpo, da orientação da corrente livre e - surpreendentemente - da posição do ponto de estagnação traseiro. Não há número de Reynolds, Froude ou Mach para complicar a semelhança dinâmica. Os escoamentos não viscosos são cinematicamente semelhantes sem parâmetros adicionais.



**Conteúdo fornecido sob licença MIT. (c) 2018 Batystuta Rocha. Obrigado: Profa. Edith Beatriz pelo apoio ao conhecimento, muito obrigado.**

**Versão 1.0 novembro 2018**