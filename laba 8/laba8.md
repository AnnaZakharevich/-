# Тема 8. 
Отчет по Теме #8 выполнил(а):
- Захаревич Анна Антоновна
- ИВТ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |


знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Создайте класс 'Car' с атрибутами производитель и модель. Создайте объект этого класса. Напишите компоненты для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями.


```python

class Car:
    def __init__ (self, make, model):
        self.make = make
        self.model = model

my_car = Car("Toyota", "Corolla")



```
### Результат.

![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%208/pic/image.png)

## Выводы

В данном коде выводятся три строки с использованием функции `print()`. Каждая строка содержит разные значения

## Лабораторная работа №2
### Дополните код из первого задания, добавив в него аттрибуты и методы класса, заставьте машину "поехать". Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.


```python

class Car:

    def __init__(self, make, model):
        self.make = make
        self.model = model

    def drive(self):
        print(f"Driving the {self.make} {self.model}")

mycar = Car("Toyota", "Corolla")
mycar.drive()



```
### Результат.



## Выводы

В данном коде производится вычисление и вывод значений внутри операции print

## Лабораторная работа №3
###  Создайте новый класс «ElectricCar» с методом «charge» и атрибутом емкость батарей. Реализуйте его наследовние от класса, созданного в первом задании. Заставьте машину ехать, а потом заряжаться.

Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.


```python

class ElectricCar(Car) :
    def __init__(self, make, model, battery_capacity) :
        super().__init__(make, model)
        self.battery_capacity = battery_capacity
    def charge(self):
        print(f"Charging the {self.make} {self.model} with {self.battery_capacity} kWh")

my_electric_car = ElectricCar("Tesla", "Model S", 75)
my_electric_car.drive()
my_electric_car.charge()



```
### Результат.




## Выводы

В этом коде выводится сообщение "Привет, Мир!" тремя различными способами.
  
## Лабораторная работа №4
### Реализуйте инкапсуляцию для класса, созданного в первом задании. Создайте защищенный атрибут производителя и приватный атрибут модели. Вызовите защищенный атрибут и заставьте машину поедать. Напишите комментарии для кода, объясняющие его работу. Результатом выполнения задания будет листинг кода с комментариями и получившийся вывод в консоль.


```python

class Car:
    def __init__(self, make, model):
        self.make = make # Защищенный атрибут
        self.model = model # Приватный атрибут
    def drive(self):
        print(f"Driving the {self._make} {self.__model}")

my_car = Car('Toyota', 'Corolla')
print(my_car) # Доступ к защищенному аттрибуту"
# print(my_car._make) Ошибка! Защищенный аттрибт не доступен
my_car.drive()



```
### Результат.




## Выводы

В данном коде наглядно показана трансформация типов перменных из одного типа в другой.

## Лабораторная работа №5
### Реализуйте полиморфизм создания основной (общий) класс "Shape", а также еще два класса "Rectangle" и "Circle". Внутри последних двух классов реализуйте методы для подсчета площади фигуры. После этого создайте массив с фигурами, поместите туда круг и прямоугольник, затем при помощи цикла выведите их площади. Напишите комментарии к коду, объясняющие его работу. Результатом выполнения задания будет список кода с комментариями и получившийся вывод в консоль.


```python

class Shape:
    def area(self):
        pass


class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height


class Circle(Shape) :
    def __init__(self, radius):
        self.radius = radius


    def area(self):
        return 3.14 * self.radius * self.radius



```
### Результат.




## Выводы

Этот код выводит на экран значения трех переменных, заданных пользователем с клавиатурыэл



## Самостоятельная работа №1
### Самостоятельно создайте класс и его объект. Они должны отличаться, от тех, что указаны в теоретическом материале (методичке) и лабораторных заданиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.

```python

class Car:
    def __init__(self, model, color, max_speed):
        self.model = model
        self.color = color
        self.max_speed = max_speed
    
    def info(self):
        return f"Модель: {self.model}, Цвет: {self.color}, Максимальная скорость: {self.max_speed} км/ч"

    def accelerate(self, increase):
        self.max_speed += increase
        return f"Максимальная скорость увеличена до: {self.max_speed} км/ч"

if __name__ == "__main__":
    # Создание объекта класса Car
    my_car = Car("Tesla Model 3", "Красный", 250)

    # Вывод информации об автомобиле
    print(my_car.info())

    # Увеличение максимальной скорости
    print(my_car.accelerate(20))

    # Вывод обновленной информации
    print(my_car.info())


```
### Результат.



## Выводы

В этом коде используется функция bool, для вывода булевого значения из числа
  
## Самостоятельная работа №2
### Самостоятельно создавайте атрбуты и методы для ранее созданного класса. Они должны отличаться, от того, что указано в теоретическом материале (методике) и лабораторных занятиях. Результатом выполнения задания будет листинг кода и получившийся вывод консоли.


```python

class Car:
    def __init__(self, model, color, fuel_type, year):
        self.model = model
        self.color = color
        self.fuel_type = fuel_type
        self.year = year
        self.mileage = 0  # атрибут для отслеживания пробега

    def drive(self, distance):
        self.mileage += distance
        return f"{self.model} проехал {distance} км. Текущий пробег: {self.mileage} км."

    def refuel(self, amount):
        return f"{self.model} заправлен на {amount} литров {self.fuel_type}."

    def car_age(self, current_year):
        age = current_year - self.year
        return f"{self.model} - возраст: {age} лет."

    def info(self):
        return (f"Модель: {self.model}, Цвет: {self.color}, "
                f"Тип топлива: {self.fuel_type}, Год выпуска: {self.year}, "
                f"Пробег: {self.mileage} км.")

if __name__ == "__main__":
    # Создание объекта класса Car
    my_car = Car("Ford Mustang", "Синий", "Бензин", 2018)

    # Вывод информации об автомобиле
    print(my_car.info())

    # Вождение автомобиля
    print(my_car.drive(150))
    
    # Заправка автомобиля
    print(my_car.refuel(50))
    
    # Получение возраста автомобиля
    print(my_car.car_age(2024))

    # Вывод обновленной информации
    print(my_car.info())



```
### Результат.


## Выводы

В данном коде реализована возможность присвоения значений нескольким переменным в одной строке
  
## Самостоятельная работа №3
### Самостоятельно реализуйте наследование, продолжая работать с ранее созданным классом. Оно должно отличаться, от того, что указано в теоретическом материалале (методишке) и лабораторных задания. Результатам выполнения задания будет листинги кода и получившейся вывод консоли.


```python

class Book:
    def __init__(self, title, author, year, genre=None, rating=None, available=True):
        self.title = title
        self.author = author
        self.year = year
        self.genre = genre
        self.rating = rating
        self.available = available

    def set_genre(self, genre):
        self.genre = genre
        return f"Жанр книги '{self.title}' установлен на '{self.genre}'."
    
    def set_rating(self, rating):
        if 0 <= rating <= 10:
            self.rating = rating
            return f"Оценка книги '{self.title}' изменена на {self.rating}."
        else:
            return "Оценка должна быть в пределах от 0 до 10."
    
    def check_availability(self):
        return self.available
    
    def borrow(self):
        if self.available:
            self.available = False
            return f"Вы взяли книгу '{self.title}'."
        else:
            return f"Книга '{self.title}' недоступна."
    
    def return_book(self):
        self.available = True
        return f"Вы вернули книгу '{self.title}'."

    def book_info(self):
        availability = "доступна" if self.available else "недоступна"
        return f"Книга: '{self.title}', Автор: '{self.author}', Год: {self.year}, Жанр: {self.genre}, Оценка: {self.rating}, Статус: {availability}"

# Подкласс для университетских книг
class UniversityBook(Book):
    def __init__(self, title, author, year, subject, edition, genre=None, rating=None, available=True):
        super().__init__(title, author, year, genre, rating, available)
        self.subject = subject
        self.edition = edition

    def book_info(self):
        base_info = super().book_info()
        return f"{base_info}, Предмет: {self.subject}, Издание: {self.edition}"

# Подкласс для художественных книг
class FictionBook(Book):
    def __init__(self, title, author, year, fiction_type, genre=None, rating=None, available=True):
        super().__init__(title, author, year, genre, rating, available)
        self.fiction_type = fiction_type

    def book_info(self):
        base_info = super().book_info()
        return f"{base_info}, Тип художественной литературы: {self.fiction_type}"

# Примеры использования
if __name__ == "__main__":
    # Создаем экземпляры книг
    uni_book = UniversityBook("Основы программирования", "Иванов И.И.", 2020, "Информатика", "2-е")
    fiction_book = FictionBook("Война и мир", "Лев Толстой", 1869, "Роман")

    # Вывод информации о книгах
    print(uni_book.book_info())
    print(fiction_book.book_info())
    
    # Тестируем методы
    print(uni_book.borrow())
    print(uni_book.book_info())
    print(uni_book.return_book())
    print(uni_book.book_info())

    print(fiction_book.set_rating(8))
    print(fiction_book.book_info())



```
### Результат.



## Выводы

В данном коде показана возможность присвоения значения переменной с клавиатуры
  
## Самостоятельная работа №4
### Самостоятельно реализируйте инкапсуляцию, продолжая работать с раннее созданный класс. Она должна отличаться, оттого, что указнана в теоретисеском материале (методие) и лабороторных занятий. Результатами выполнения задания будут листинги кода и получения вывода консоли.


```python

class Book:
    def __init__(self, title, author, year, genre=None, rating=None, available=True):
        self.__title = title        # Приватный атрибут
        self.__author = author      # Приватный атрибут
        self.__year = year          # Приватный атрибут
        self.__genre = genre        # Приватный атрибут
        self.__rating = rating      # Приватный атрибут
        self.__available = available # Приватный атрибут

    # Геттеры
    def get_title(self):
        return self.__title
    
    def get_author(self):
        return self.__author
    
    def get_year(self):
        return self.__year
    
    def get_genre(self):
        return self.__genre
    
    def get_rating(self):
        return self.__rating
    
    def is_available(self):
        return self.__available
    
    # Сеттеры
    def set_genre(self, genre):
        self.__genre = genre
        return f"Жанр книги '{self.get_title()}' установлен на '{self.__genre}'."
    
    def set_rating(self, rating):
        if 0 <= rating <= 10:
            self.__rating = rating
            return f"Оценка книги '{self.get_title()}' изменена на {self.__rating}."
        else:
            return "Оценка должна быть в пределах от 0 до 10."
    
    def borrow(self):
        if self.__available:
            self.__available = False
            return f"Вы взяли книгу '{self.get_title()}'."
        else:
            return f"Книга '{self.get_title()}' недоступна."
    
    def return_book(self):
        self.__available = True
        return f"Вы вернули книгу '{self.get_title()}'."

    def book_info(self):
        availability = "доступна" if self.__available else "недоступна"
        return f"Книга: '{self.get_title()}', Автор: '{self.get_author()}', Год: {self.get_year()}, Жанр: {self.__genre}, Оценка: {self.__rating}, Статус: {availability}"

# Подкласс для университетских книг
class UniversityBook(Book):
    def __init__(self, title, author, year, subject, isbn, available=True):
        super().__init__(title, author, year, genre='Academic', available=available)
        self.__subject = subject  # Приватный атрибут
        self.__isbn = isbn        # Приватный атрибут

    def get_subject(self):
        return self.__subject

    def get_isbn(self):
        return self.__isbn

    def book_info(self):
        base_info = super().book_info()
        return f"{base_info}, Предмет: {self.get_subject()}, ISBN: {self.get_isbn()}"

# Пример использования
if __name__ == "__main__":
    book1 = Book("1984", "Джордж Оруэлл", 1949)
    print(book1.book_info())
    print(book1.set_genre("Дистопия"))
    print(book1.set_rating(9))
    print(book1.borrow())
    print(book1.book_info())
    print(book1.return_book())

    uni_book = UniversityBook("Математика", "Иванов И.И.", 2020, "Математика", "978-3-16-148410-0")
    print(uni_book.book_info())
    print(uni_book.borrow())
    print(uni_book.book_info())



```
### Результат.



## Выводы

В этом коде продемонстрирована возможность исполнения математических операций над строковыми переменными
  
## Самостоятельная работа №5
### Самостоятельно реализовайте полиморфизм. Он должен отличаться от того что указан в теоретическийм материале (методиике)и лабораторних задания. Результом выполнения задание будет линтинг кода и получилшися вывод консол


```python

class Shape:
    def area(self):
        raise NotImplementedError("Метод area() должен быть реализован в подклассах.")
    
    def description(self):
        return "Это фигура."

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14159 * (self.radius ** 2)
    
    def description(self):
        return f"Круг с радиусом {self.radius}."

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height

    def area(self):
        return self.width * self.height
    
    def description(self):
        return f"Прямоугольник шириной {self.width} и высотой {self.height}."

class Triangle(Shape):
    def __init__(self, base, height):
        self.base = base
        self.height = height

    def area(self):
        return 0.5 * self.base * self.height
    
    def description(self):
        return f"Треугольник с основанием {self.base} и высотой {self.height}."

def print_shape_info(shape):
    print(shape.description())
    print(f"Площадь: {shape.area()}")

if __name__ == "__main__":
    shapes = [
        Circle(5),
        Rectangle(4, 6),
        Triangle(3, 7),
    ]

    for shape in shapes:
        print_shape_info(shape)



```
### Результат.



## Выводы

В данном коде показывается вывод коментариев совместно с переменными
  


## Общие выводы по теме
### Выполняя данную работу я вспомнила основные функции Python, синтаксис этого языка. В задачах этой работы используются простейшие операции, необходимые для присваивания значений, вывода этих значений и их изменения.
