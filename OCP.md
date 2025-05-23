<?python

from abc import ABC, abstractmethod

class Desconto(ABC):
    @abstractmethod
    def calcular(self, valor):
        pass

class DescontoNatal(Desconto):
    def calcular(self, valor):
        return valor * 0.9  # 10% de desconto

class DescontoAniversario(Desconto):
    def calcular(self, valor):
        return valor * 0.85  # 15% de desconto

class CalculadoraDescontos:
    def aplicar_desconto(self, desconto: Desconto, valor):
        return desconto.calcular(valor)

//Reference: https://chatgpt.com/

// Princípio Aberto-Fechado — Objetos ou entidades devem estar abertos para extensão, mas fechados para modificação, ou seja, quando novos comportamentos e recursos precisam ser adicionados no software, devemos estender e não alterar o código fonte original. Aberto para extensão: Podemos adicionar novas classes de desconto (DescontoBlackFriday, DescontoEstudante, etc.) sem alterar nenhuma linha da classe CalculadoraDescontos.
Fechado para modificação: A classe CalculadoraDescontos não precisa ser modificada quando adicionamos novos tipos de desconto. Basta que eles implementem a interface Desconto, possibilitando a extensabilidade. Juntamente com a manutenção facilitada: você não mexe em código que já funciona, e o baixo acoplamento: CalculadoraDescontos não depende dos detalhes dos tipos de desconto.
