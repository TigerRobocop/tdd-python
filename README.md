## FizzBuzz TDD

*Traduzido de: http://www.blog.pythonlibrary.org/2019/09/18/python-code-kata-fizzbuzz/*

- Vamos escrever um programa que escreve números de 1 a 100, cada um numa nova linha;
- Pra cada número múltiplo de 3, escreve **Fizz** ao invés do número;
- Pra cada número múltiplo de 5, escreve 'Buzz' ao invés do número;
- Pra cada número múltiplo de ambos 3 e 5, escreve 'FizzBuzz' ao invés do número;

# Atividades (Setup)

1. Criar uma pasta FizzBuzz
2. Abrir um terminal nesta pasta
3. Iniciar um repositório git `git init`
4. Criar um arquivo `.gitignore`, incluir a extensão *.pyc 

# Atividade 1 - Fizz

1. Criar um arquivo `test_fizzbuzz.py`
2. Adicione este código no arquivo:
```python
import fizzbuzz # módulo ainda não criado
import unittest # nativo python

# utiliza a subclasse TestCase 
class TestFizzBuzz(unittest.TestCase):
 
    # criar série de funções que representam os casos de teste
    def test_multiple_of_three(self):
       self.assertEqual(fizzbuzz.process(6), 'Fizz')
 
# executa o módulo
if __name__ == '__main__':
    unittest.main()
```

3. Rodar `python test_fizzbuzz.py` e analisar o que aconteceu (falhou)
4. Criar um `fizzbuzz.py` vazio
5. Rodar teste novamente e analisar o que aconteceu (falhou)
6. Adicionar uma função `process()` em `fizzbuzz.py`
```python
def process(number):
    if number % 3 == 0:
        return 'Fizz'
```
7. Rodar teste novamente e analisar o que aconteceu (passou)



