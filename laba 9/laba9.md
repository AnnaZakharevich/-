# Тема 8. 
Отчет по Теме #8 выполнил(а):
- Захаревич Анна Антоновна
- ИВТ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + |   |
| Задание 3 | + |   |
| Задание 4 | + |   |
| Задание 5 | + |   |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Допустим, что вы решили ординально и немного странно познакомиться с человеком. Для этого у вас должен быть написан свой класс на Python, который будет проверять удача вам имя человека или нет. Для этого создайте класс, указав в свойствах только имя. Далее создайте функцию init (), а в ней сделайте проверку на то удалял человек ваше имя или нет. Также можете проверить что будет, если в этой функции указали атрбиут, который не указан в вашем классе, например, попробуйте вызывать фамилию.


```python

class Ivan:
    __slots__ = ['name']

    def __init__(self, name):
        if name == 'Иван':
            self.name = f"Да, я {name}"
        else:
            self.name = f"Я не {name} , а Иван"

person1 = Ivan('Алексей')
person2 = Ivan('Иван')
print(person1.name)
print(person2.name)

person2.surname = 'Петров'



```
### Результат.

![image](https://github.com/user-attachments/assets/68a8bd78-85ec-4ed2-b5be-94fc8d568361)

## Выводы
В этой задаче с помощью функции и проверки через если программа проверяет, угадали ли мы имя человека


## Лабораторная работа №2
### Вам дали важное задание, написать программу морожного прогамму, которая будет писать добавилы ли топпинги в мороженое и цену после возможного изменения. Для этого вам нужно написать класс, в котором будет определяться изменении ли состав мороженного или нет. В этом классе реализуйте метод, выводящий на печать «Мороженное с {ТОППИНГ}» в случае наличия добавки, а иначе отобразится следующая фраза: «Обычное мороженое». При этом программа должна воспринимать как топпинг только аргументы типа string.


```python


class Icecream:
    def __init__(self, ingredient=None):
        if isinstance(ingredient, str):
            self.ingredient = ingredient
        else:
            self.ingredient = None

    def composition(self):
        if self.ingredient:
            print(f"Мороженое с {self.ingredient}")
        else:
            print('Обычное мороженое')

icecream = Icecream()
icecream.composition()
icecream = Icecream('шоколадом')
icecream.composition()
icecream = Icecream(5)
icecream.composition()


```
### Результат.

![image](https://github.com/user-attachments/assets/4781ffb3-b860-444b-9fbd-5c80ededde27)

## Выводы
в данной программе с помощью функции реализуется определение наличия/отсутсвия топпинга в мороженом


## Лабораторная работа №3
### Петя – начинающий программист и на занятиях ему сказали реализовать пакет...что-то. А вы хороший друг Пети и ко всему прочему прекрасно знаете, что пакет... что-то – это никакусица, поэтому решаете помочь вашему другу с написанием класса с никакусицей. Ваш класс будет не просто никакусией, а классом с сеттером, гейтером и деструктором. После написания класса вам необходимо промодестрировать что все написанные вами функции работают. Также вас необходимо объяснить Пете почему на скриншоте ниже в консоли выводится ошибка.


```python

class MyClass:
    def __init__(self, value):
        self._value = value

    def get_value(self):
        return self._value

    def set_value(self, value):
        self._value = value

    def del_value(self):
        del self._value

    value = property(get_value, set_value, del_value, "Свойство value")

# Тестовый пример использования
if __name__ == '__main__':
    obj = MyClass(42)
    print(obj.get_value())
    obj.set_value(45)
    print(obj.get_value())
    obj.set_value(100)
    print(obj.get_value())
    obj.del_value()
    print(obj.get_value())


```
### Результат.

![image](https://github.com/user-attachments/assets/029ea753-5d4d-4a98-b7d1-2a9ae8c674a8)

## Выводы
1. Метод класса, который служит конструктором, должен называться __init__. Здесь он назван просто init, что является ошибкой.
2. Опечатка в методе get_value. В данном методе вместо _value должно быть value, так как именно это имя используется в сигнатуре свойства.

  
## Лабораторная работа №4
### Вам прекрасно известно, что кошки и собаки являются млекопитающими, но компьютер этого не понимает, поэтому вам нужно написать три класса: Кошки, Собаки, Млекопитающие. И при помощи этих классов создать класс Петровской-Любы со всеми её питомцами.


```python

class Mammal:
    className = 'Mammal'
class Dog(Mammal):
    species = 'canine'
    sounds = 'wow'
class Cat(Mammal):
    species = 'feline'
    sounds = 'meow'

dog = Dog()
print(f"Dog is {dog.className}, but they say {dog.sounds}")
cat = Cat()
print(f"Cat is {cat.className}, but they say {dog.sounds}")



```
### Результат.

![image](https://github.com/user-attachments/assets/590f878d-d4c7-4552-98d8-6eb9bf922197)

## Выводы
В данной задаче наглядно показан пример наследования классов


## Лабораторная работа №5
### На разных языках здороваются по-разному, но суть остаётся одинаковой, люди друг с другом здороваются. Давай вместе с вами реализуем программу с полиморфизмом, которая будет описывать всю суть первого предложения задачи. Для этого мы можем выбрать языка, например, русский и английский и написать для них отдельные классы, в которых будет в виде артикля слово, которым здороваются на этих языках. А также напишем функцию, которая будет выводить информацию о том, как на этих языках здороваются. Заметьте, что для решения поставленной задачи мы использовали декоратор @staticmethod, поскольку нам не нужны обязательные параметры-ссылки вовсе.


```python

Class Russian:
@staticmethod def greeting():
print ("Привет")
cLass English:
@staticmethod def greeting():
print ("Hello")
def greet(language):
language. greeting)
ivan = Russian©
greet (ivan)
john = EnglishO
greet john)


```
### Результат.

![image](https://github.com/user-attachments/assets/591295a0-2d7d-424a-bf01-975ee43bcb47)

## Выводы
В данной задаче наглядно показан пример полиморфизма 



## Самостоятельная работа №1
### Задание садовник и помидоры


```python


class Gardener:
    def __init__(self, name, plant):
        self.name = name
        self._plant = plant

    def work(self):
        if self._plant.tomatoes:
            self._plant.grow_all()

    def harvest(self):
        if self._plant.all_are_ripe():
            self._plant.give_away_all()
            print(f"Садовник {self.name} собрал урожай!")
        else:
            print(f"Садовник {self.name} пока не может собирать урожай, не все томаты созрели.")

    @staticmethod
    def knowledge_base():
        print("Справка по садоводству:")
        print("- Для ухода за томатами необходимо регулярно поливать куст и удалять сорняки.")
        print("- Томаты готовы к сбору урожая, когда они полностью краснеют.")
        print("- Собирайте томаты аккуратно, не повреждая куст.")


class Tomato:
    states = {0: 'Отсутствует', 1: 'Цветение', 2: 'Зеленый', 3: 'Красный'}

    def __init__(self, index):
        self._index = index
        self._state = 0

    def grow(self):
        if self._state < 3:
            self._state += 1

    def is_ripe(self):
        if self._state == 3:
            return True
        return False


class TomatoBush:
    def __init__(self, num):
        self.tomatoes = [Tomato(i) for i in range(num)]

    def grow_all(self):
        for tomato in self.tomatoes:
            tomato.grow()

    def all_are_ripe(self):
        return all(tomato.is_ripe() for tomato in self.tomatoes)

    def give_away_all(self):
        self.tomatoes = []


Gardener.knowledge_base()

bush = TomatoBush(10)
gardener = Gardener("Иван", bush)

for _ in range(3):
    gardener.work()

gardener.harvest()

while not bush.all_are_ripe():
    gardener.work()
    gardener.harvest()

gardener.harvest()



```
### Результат.

![image](https://github.com/user-attachments/assets/a71e1a13-e54d-41da-b3bb-ed2088a9ba36)

## Выводы
Я рассмотрела основы создания классов и объектов в Python, а также работу с методами класса и конструкторами. Практическое применение принципов ООП позволило лучше понять их значимость при разработке программных систем.
  

  


## Общие выводы по теме
### В ходе выполнения данной лабораторной работы были изучены ключевые концепции объектно-ориентированного программирования, такие как инкапсуляция, наследование и полиморфизм. Эти принципы позволяют создавать гибкий и расширяемый код, который легко поддерживать и модифицировать.
