# FuncoesJs 

## Function Declaration:

É a forma mais frequente de declarar uma função, sua estrutura é formada por um comando chamado de `function`, que tem o seguinte formato: function => nome da função => parâmetros => parênteses (para colocar parâmetros dentro dos parênteses) => estrutura do código que vai ser utilizado dentro da função (esses têm que estar dentro de chaves).

### Vantagens:

Esse tipo de função possui hoisting (hoisting leva o comando de declaração diretamente para o topo do algoritmo). Isso possibilita que a função consiga ser chamada em qualquer lugar do algoritmo, até mesmo antes da linha em que sua própria função foi declarada.

### Desvantagens:

Apesar do hoisting ajudar, ele também pode atrapalhar, uma vez que em um código grande existam duas váriaveis de nomes iguais, uma dentro do Scopo da função e outra fora, fica difícil saber qual que o código utilizou como resultado de saída de todo o algoritmo.

### Exemplos:
     
EX-1:      

    function boas_vindas () {
        console.log("Seja bem-vindo.")
    };
    boas_vindas();
    
 EX-2

    mult (5, 10)
    function mult (a, b){
        return a * b
    };

 EX-3

    comprimentacao("Júnior")
    function comprimentacao (nome){
        console.log("Bem vindo de volta" + nome)
    };

## Function Expression:

 Basicamente é uma função dentro de uma variável, sua estrutura (sintaxe) é a seguinte: o tipo da variável  delimitado o nome da variável pela chamada do comando function => o nome da função => parâmetros => dentro deles podem haver valores =>  chaves fechando a função => dentro dessas chaves está o corpo da função.

### Vantagens: 

Pode ser utilizada com ou sem nome, quando fazemos a função sem nome chamamos de função `anônima`, ela nem sempre vem com nomes, porém as que possuem nome podemos chamar de função `nomeada`. Mais flexível para modificações dentro de funções.

### Desvantagens:

Não possui hoisting pois o programa lê linha por linha e a linha dessa função que é lida não é a função em si mas sim a variável que ela está armazenada, não podendo ser chamada antes da linha em que a função foi criada. As funções anônimas dificultam localizar de onde vem um possível problema na compilação de um código.

### Exemplos:
EX-1

        function exibir_nome(nome){
            let mensagem = ("Iae" + nome + ", bem vindo.")
            return mensagem;
        }
        console.log(exibir_nome("Júnior"));

EX-2        

        const info = function (nome, idade){
        console.log("Opa, sou " + nome + " e tenho " + idade + " anos.");
    };
    info("Júnior", 21);

EX-3

    const num = function(a, b) {
        return a * b;
    };

    console.log(num(5, 10));


## Function Arrow:

Trata-se de um tipo de função bem mais moderna, diferente das anteriores. Essa tem como intenção deixar o código mais limpo e legível possível sem perder sua eficiência enquanto função. Sua estrutura (sintaxe) pode ser interpretada como: declara um tipo de variável => nome da função => sinal de igual => parênteses para colocar parâmetros => sinal de "=>" para iniciar a arrow => seguida pelas chaves (coleta das chaves está o conteúdo da função).

### Vantagens: 

Sintaxe simples, tornando o código mais fácil de ser compreendido. Possui this herdado, ideal para arrays e funções simples, útil como função auxiliar, em outras palavras, ótimo como uma "sub-função".

### Desvantagens:

 Menos legível e nada ideal para ser usada como função de grande porte, ela não é ideal para definir métodos ou objetos.

 ### Exemplos:


EX-1

    const saudar = nome => `bem vindo ${nome}`;
    console.log(saudar("Júnior"));



EX-2

    let somar = (a, b) => {
    return a + b;
};
console.log(somar(5, 10)); 


EX-3

    const expo = valor => valor * valor;
    console.log(expo(10));
