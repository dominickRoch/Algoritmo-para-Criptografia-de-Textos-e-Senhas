# Algoritmo-para-Criptografia-de-Textos-e-Senhas
Projeto - 03

1.
A criptografia desempenha um papel fundamental na segurança da informação, protegendo dados sensíveis contra acessos não autorizados. O projeto visa desenvolver um algoritmo de criptografia que reconheça a importância crescente da segurança cibernética. A análise de complexidade será uma parte crucial, destacando a eficiência e o desempenho do algoritmo.

2, 3.
A análise de complexidade desempenha um papel crucial na avaliação do desempenho de algoritmos. Essa prática permite comparar algoritmos, tomar decisões de design informadas, prever o comportamento em condições futuras, identificar ineficiências no código, planejar recursos em sistemas distribuídos, adaptar-se a restrições específicas e compreender o custo computacional à medida que os conjuntos de dados aumentam. Além disso, facilita a minimização de custos de manutenção a longo prazo, guiando escolhas que impactam diretamente a eficiência de um sistema

Complexidade Temporal:
A complexidade do tempo está relacionada ao tempo de execução do algoritmo. É usada a notação "Big O" (O()) para descrever os limites superiores assintóticos do tempo de execução. Isso nos permite entender a forma que o algoritmo se comporta quando o tamanho dos dados de entrada aumenta. Por exemplo, um algoritmo de complexidade O(n) significa que o seu tempo de execução cresce de forma linear com o tamanho da entrada.
Outros símbolos incluem "Little o" (o()) para um limite superior não restritivo, "Omega" (Ω()) para um limite inferior assintótico e "Theta" (θ()) para um limite inferior assintótico. Um limite rígido que combina um limite superior e inferior.

Complexidade Espacial:
A complexidade espacial refere-se ao uso de memória pelo algoritmo. A notação "Big O" também é aplicada aqui para descrever o limite superior assintótico do espaço necessário para a execução do algoritmo. Um algoritmo com complexidade espacial O(1) indica que seu uso de memória é constante, independentemente do tamanho da entrada, enquanto O(n) implica um aumento linear na utilização de memória.


A análise assintótica é uma abordagem valiosa para compreender o comportamento de algoritmos à medida que o tamanho dos dados de entrada cresce indefinidamente. Ela se concentra em descrever a taxa de crescimento do desempenho do algoritmo, ignorando fatores constantes e termos de ordem inferior que se tornam insignificantes em grandes conjuntos de dados.
Provar cotas inferiores é uma parte essencial da análise de complexidade, pois oferece insights sobre o desempenho mínimo esperado para a resolução de um determinado problema. Algumas técnicas comuns incluem:

Prova de Adversário:
Considera um adversário inteligente que escolhe os piores casos possíveis para o algoritmo. Ao mostrar que nenhum algoritmo pode superar um determinado limite, estabelecemos uma cota inferior.
Prova de Redução:
Relaciona a complexidade de um problema desconhecido com a complexidade de um problema conhecido. Se conseguirmos mostrar que o problema conhecido é mais difícil, então estabelecemos uma cota inferior para o problema desconhecido.

4.
< -----------------------------------------------------------------------
O código é uma implementação simples da cifra de César para criptografar e descriptografar um texto usando uma chave. A medição inicial de complexidade e desempenho geralmente envolve a análise de tempo e espaço. Neste caso, a complexidade temporal é linear em relação ao tamanho do texto, pois cada caractere é processado uma vez. A complexidade espacial é constante, pois não há uso significativo de memória adicional em relação ao tamanho do texto. No entanto, é importante observar que a cifra de César é uma cifra muito fraca do ponto de vista da segurança, pois é facilmente quebrada por meio de ataques de força bruta. 

Complexidade Temporal: O loop que percorre cada caractere do texto tem uma complexidade linear O(n), onde 'n' é o tamanho do texto.
Complexidade Espacial: A complexidade espacial é O(1), pois não há alocação dinâmica de memória ou estruturas de dados que crescem com o tamanho do texto.

5.
df

