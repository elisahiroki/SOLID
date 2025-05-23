<?php

class Order
{
    public function calculateTotalSum(){/*...*/}
    public function getItems(){/*...*/}
    public function getItemCount(){/*...*/}
    public function addItem($item){/*...*/}
    public function deleteItem($item){/*...*/}
}

class OrderRepository
{
    public function load($orderID){/*...*/}
    public function save($order){/*...*/}
    public function update($order){/*...*/}
    public function delete($order){/*...*/}
}

class OrderViewer
{
    public function printOrder($order){/*...*/}
    public function showOrder($order){/*...*/}
}

//Reference: https://www.apphp.com/tutorials/index.php?page=solid-principles-in-php-examples
https://medium.com/desenvolvendo-com-paixao/o-que-%C3%A9-solid-o-guia-completo-para-voc%C3%AA-entender-os-5-princ%C3%ADpios-da-poo-2b937b3fc530

//Princípio da Responsabilidade Única — Uma classe deve ter um, e somente um, motivo para mudar.

//Esse princípio declara que uma classe deve ser especializada em um único assunto e possuir apenas uma responsabilidade dentro do software, ou seja, a classe deve ter uma única tarefa ou ação para executar. Perceba no exemplo acima que temos 3 classes, cada uma cuidando da sua função: class Order cuidando da lógica de negócios, class OrderRepository cuidando da persistência de dados e a class OrderViewer cuidando da apresentação visual.
