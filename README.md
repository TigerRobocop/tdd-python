# BoraDale TDD

Executar Teste
`python test_boradale.py`

Executar 
`python boradale.py`

## Etapa 1 - BORA

```python
# test_boradale.py

import boradale
import unittest

class TestBoraDale(unittest.TestCase):

    def test_multiple_of_three(self):
       self.assertEqual(boradale.process(6), 'Bora')

if __name__ == '__main__':
    unittest.main()
```
```python
# boradale.py

def process(number):
    if number % 3 == 0:
        return 'Bora'
```

## Etapa 2 - DALE

```python
# test_boradale.py

import boradale
import unittest

class TestBoraDale(unittest.TestCase):

    def test_multiple_of_three(self):
        self.assertEqual(boradale.process(6), 'Bora')

    def test_multiple_of_five(self):
        self.assertEqual(boradale.process(20), 'Dale')
if __name__ == '__main__':
    unittest.main()
```

```python
# boradale.py

def process(number):
    if number % 3 == 0:
        return 'Bora'
    elif number % 5 == 0:
        return 'Dale'
```

## Etapa 3 - BORADALE

```python
# test_boradale.py

import boradale
import unittest

class TestBoraDale(unittest.TestCase):

    def test_multiple_of_three(self):
        self.assertEqual(boradale.process(6), 'Bora')

    def test_multiple_of_five(self):
        self.assertEqual(boradale.process(20), 'Dale')

    def test_boradale(self):
        self.assertEqual(boradale.process(15), 'BoraDale')

if __name__ == '__main__':
    unittest.main()
```

```python
# boradale.py

def process(number):
    if number % 3 == 0 and number % 5 == 0:
        return 'BoraDale'
    elif number % 3 == 0:
        return 'Bora'
    elif number % 5 == 0:
        return 'Dale'
```

## Etapa Final - Refactor

```python
# test_boradale.py

import boradale
import unittest
class TestBoraDale(unittest.TestCase):

    def test_multiple_of_three(self):
        self.assertEqual(boradale.process(6), 'Bora')

    def test_multiple_of_five(self):
        self.assertEqual(boradale.process(20), 'Dale')

    def test_boradale(self):
        self.assertEqual(boradale.process(15), 'BoraDale')

    def test_regular_numbers(self):
        self.assertEqual(boradale.process(2), 2)
        self.assertEqual(boradale.process(98), 98)

if __name__ == '__main__':
    unittest.main()
```

```python
# boradale.py

def process(number):
    if number % 3 == 0 and number % 5 == 0:
        return 'BoraDale'
    elif number % 3 == 0:
        return 'Bora'
    elif number % 5 == 0:
        return 'Dale'
    else:
        return number

if __name__ == '__main__':
    for i in range(1, 101):
        print(process(i))
```








