<?php

class A {
    public function getNome() {
        echo "Meu nome é A\n";
    }
}

class B extends A {
    public function getNome() {
        echo "Meu nome é B\n";
    }
}

function imprimeNome(A $objeto) {
    $objeto->getNome();
}

$a = new A();
$b = new B();

imprimeNome($a);
imprimeNome($b);

//Reference: https://blog.casadodesenvolvedor.com.br/solid-na-pratica/

//O princípio da substituição de Liskov declara que as subclasses devem ser substituíveis por suas classes de base.

// Isso quer dizer que, se a classe B for uma subclasse da classe A, devemos poder passar um objeto da classe B para qualquer método que espere um objeto da classe A e o método não deverá produzir resultados estranhos, nesse caso. No exemplo acima, como a classe B herda o comportamento da classe A, ao utilizar a função imprimeNome() o código funcionará da mesma forma.