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
Medir empiricamente o desempenho de um algoritmo ou sistema é crucial para entender como ele se comporta na prática, especialmente em condições do mundo real. A importância dessas medidas vai além da análise teórica e fornece informações valiosas que podem impactar diretamente o desenvolvimento, otimização e manutenção de software. Como:

Validação das Análises Teóricas:
As análises teóricas de complexidade fornecem estimativas, mas as medidas empíricas validam essas estimativas na prática. Elas ajudam a confirmar se as previsões teóricas se alinham com o desempenho real do algoritmo ou sistema.
Adaptação a Cenários Reais:
O desempenho de um algoritmo pode variar em diferentes ambientes e condições de entrada. Medidas empíricas ajudam a entender como o algoritmo se comporta sob diversas circunstâncias, permitindo adaptações e otimizações específicas.
Identificação de Gargalos:
Permitem a identificação de gargalos de desempenho. Ao analisar os resultados, é possível identificar partes específicas do código que consomem mais tempo ou recursos, orientando esforços de otimização.
Aprimoramento Contínuo:
A medição contínua de desempenho é crucial durante o desenvolvimento contínuo de software. Ela permite que a equipe de desenvolvimento identifique áreas que podem ser aprimoradas à medida que o software evolui.

< ----------------------------------------------------------------------------------------

6.
As relações de recorrência são ferramentas matemáticas poderosas para analisar algoritmos recursivos. Elas descrevem a relação entre um problema de tamanho [n] e o mesmo problema com tamanho menor. No contexto da análise de algoritmos, as relações de recorrência são frequentemente usadas para modelar o tempo ou espaço de execução em termos da entrada do algoritmo. No caso de algoritmos de criptografia, onde a recursividade pode não ser uma característica comum, podemos explorar uma aplicação mais tangencial das relações de recorrência na otimização do desempenho.
Exemplo:

void criptografia(char *texto, int chave) {
    int tam = strlen(texto);

    for (int i = 0; i < tam; i++) {
        if (texto[i] >= 'A' && texto[i] <= 'Z') {
            texto[i] = (texto[i] - 'A' + chave) % TAMANHO_ALFBT + 'A';
        } else if (texto[i] >= 'a' && texto[i] <= 'z') {
            texto[i] = (texto[i] - 'a' + chave) % TAMANHO_ALFBT + 'a';
        }
    }
}

7.
A comparação de desempenho entre algoritmos iterativos e recursivos é fundamental para escolher a abordagem mais eficiente, especialmente em contextos como a criptografia.
Algoritmo Recursivo:
void criptografiaRecursiva(char *texto, int chave) {
    if (*texto != '\0') {
        if (*texto >= 'A' && *texto <= 'Z') {
            *texto = (*texto - 'A' + chave) % 26 + 'A';
        } else if (*texto >= 'a' && *texto <= 'z') {
            *texto = (*texto - 'a' + chave) % 26 + 'a';
        }
        criptografiaRecursiva(texto + 1, chave);
    }
}

Algoritmo Iterativo:
void criptografiaIterativa(char *texto, int chave) {
    int tam = strlen(text);

    for (int i = 0; i < tam; i++) {
        if (texto[i] >= 'A' && texto[i] <= 'Z') {
            texto[i] = (texto[i] - 'A' + chave) % 26 + 'A';
        } else if (texto[i] >= 'a' && texto[i] <= 'z') {
            texto[i] = (texto[i] - 'a' + chave) % 26 + 'a';
        }
    }
}

Recursivo:

Prós: Pode ser mais fácil de entender e implementar para alguns.
Contras: Pode ter um custo de desempenho maior devido à sobrecarga de chamadas recursivas.

Iterativo:
Prós: Tendência a ser mais eficiente em termos de desempenho devido a ausência de sobrecarga de chamadas recursivas.
Contras: Pode ser considerado menos elegante por alguns programadores.

8.
O projeto eficiente de algoritmos é fundamental para desenvolver soluções que sejam rápidas, eficazes e que usem de forma otimizada os recursos disponíveis.

Recursão:
A recursão é uma técnica na qual uma função chama a si mesma para resolver instâncias menores do mesmo problema. Útil para problemas que podem ser divididos em subproblemas idênticos ou semelhantes. Pode simplificar a implementação e tornar o código mais legível.

Dividir para Conquistar:
Divide-se um problema complexo em subproblemas menores, resolve cada subproblema de forma independente e, em seguida, combina as soluções para obter a solução do problema original. Útil para problemas complexos que podem ser decompostos em partes mais simples e independentes.

Programação Dinâmica:
Solução de problemas por meio da combinação de soluções de subproblemas já resolvidos, armazenando as soluções intermediárias para evitar recálculos. Útil quando um problema pode ser dividido em subproblemas sobrepostos e a solução de um subproblema é reutilizada.

Programação Gulosa:
Abordagem que faz escolhas locais ótimas em cada estágio, na esperança de atingir uma solução global ótima. Útil quando uma escolha ótima local leva a uma solução global ótima.

Backtracking:
Solução de problemas por tentativa e erro, gerando todas as possíveis soluções e retrocedendo quando uma solução parcial não pode ser completada para uma solução válida. Útil para problemas de decisão que podem ser estruturados como uma árvore de escolhas.




