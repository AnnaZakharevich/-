# Тема 7. 
Отчет по Теме #7 выполнил(а):
- Захаревич Анна Антоновна
- ИВТ-22-1

| Задание | Лаб_раб | Сам_раб |
| ------ | ------ | ------ |
| Задание 1 | + | + |
| Задание 2 | + | + |
| Задание 3 | + | + |
| Задание 4 | + | + |
| Задание 5 | + | + |
| Задание 6 | + |   |
| Задание 7 | + |   |
| Задание 8 | + |   |
| Задание 9 | + |   |
| Задание 10 | + |   |

знак "+" - задание выполнено; знак "-" - задание не выполнено;

Работу проверили:
- к.э.н., доцент Панов М.А.

## Лабораторная работа №1
### Составьте текстовый файл и положите его в одну директорию с программой на Python. Текстовый файл должен состоять минимум из двух строк.


```python

f = open ('input.txt')
print (f. readline ())
f.close()



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l1.png)

## Выводы

В данном коде выводятся три строки с использованием функции `print()`. Каждая строка содержит разные значения

## Лабораторная работа №2
### Напишите программу, которая выведет только первую строку из вашего файла, при этом используйте конструкцию open(/close).


```python

f = open ('input.txt', 'r')
print (f. readline ())
f.close()


```




```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l2.1.png)

## Выводы

В данном коде производится вычисление и вывод значений внутри операции print

## Лабораторная работа №3
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию open/close).

```python

f = open (' input.txt', 'r')
print (f. readlines () )
f.close ()



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l3.png)


## Выводы

В этом коде выводится сообщение "Привет, Мир!" тремя различными способами.
  
## Лабораторная работа №4
### Напишите программу, которая выведет все строки из вашего файла в массиве, при этом используйте конструкцию with open).


```python

with open('input.txt') as f:
print (1. readlines ())


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l4.png)


## Выводы

В данном коде наглядно показана трансформация типов перменных из одного типа в другой.

## Лабораторная работа №5
### Напишите программу, которая выведет каждую строку из вашего файла отдельно, при этом используйте конструкцию with open).


```python

with open ('input.txt') as 1:
for line in f:
print (line)



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l5.png)


## Выводы

Этот код выводит на экран значения трех переменных, заданных пользователем с клавиатурыэл

## Лабораторная работа №6
### Напишите программу, которая будет добавлять новую строку в ваш файл, а потом выведет полученный файл в консоль. Вывод можно осуществлять любым способом. Обязательно проверьте сам файл, чтобы изменения в нем тоже отображались.

```python

with open('input.txt',|'a+') as f:
f.write ('\nIm additional line')
with open('input.txt', 'r') as f:
result = f. readlines ()
print (result)


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l6.png)


## Выводы

В этом коде показана работа основных математических операций

## Лабораторная работа №7
### Напишите программу, которая перепишет всю информацию, которая была у вас в файле до этого, например напишет любые данные из произвольно вами составленного списка. Также не забудьте проверить что измененная вами информация сохранилась в файле.



```python

lines = ['one', 'two', 'three']
with open ('input.txt', 'w') as f:
for line in lines:
f.write ('\nCycle run ' + line)
print ('Done! ' )


```


### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l7.png)


## Выводы

В данном коде демонстрируется работа математических операций со строковыми переменными

## Лабораторная работа №8
### Выберите любую папку на своем компьютере, имеющую вложенные директории. Выведите на печать в терминал ее содержимое, как и всех подкаталогов при помощи функции print_docs(directory).
 


```python

import os
def print docs (directory) :
all
_files = os.walk(directory)
for printie tanka Teatalog 101) содержит:")
print (1'Директории: |", "-join([folder for folder in catalog(1]])|')
print (1'файлы: [", "-join([tile for file in catalog(2]])|*)
print ('-'*40)
print
_docs ("/Users/1/OneDrive/Рабочий стол/3 курс/Пи Панов/Лаба 7*)



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l8.png)


## Выводы

Этот код демонстрирует работы функции sentence 

## Лабораторная работа №9
### Документ «input. txt» содержит следующий текст:
Приветствие
Спасибо
Извините
Пожалуйста
До свидания
Ты готов?
Как дела?
С днем рождения!
Удача!
Я тебя люблю.
Требуется реализовать функцию, которая выводит слово, имеющее максимальную длину (или список слов, если таковых несколько).
Проверьте работоспособность программы на своем наборе данных




```python

Def longest_words (file) :
with open (file, encoding='utf-8') as f:
words = f.read() split()
max_length = len (max (words, key=len) )
for
word in words:
if len (word) == max_length:
sought_words - word
it
len (sought
_words) = 1:
return sought_words[0]
return sought
words
print (longest_words (' input.txt') )


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l9.png)


## Выводы

В данном коде показана возможность деления вывода на подстроки

## Лабораторная работа №10
### Требуется создать csv-файл «rows_300.csv» со следующими столбцами:
• Nº - номер по порядку (от 1 до 300);
• Секунда - текущая секунда на вашем ПК;
• Микросекунда - текущая миллисекунда на часах.
Ди наняв на калой итерии цикла искусственно



```python

import csv 
import datetime 
import time
with open ('rows_300.csv', *w', encoding='utf-8', newline
1:
writer = csv.writer (1)
writer.writerow(['p'
• 'Секунда" , 'Микросекунда' ] )
for line in range (1,
301):
writer.writerow([line, datetime.datetime.now()-second, datetime.datetime time.sleep (0.01)



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/l10.png)


## Выводы

Этот код демонстрирует работы функции sentence 

## Самостоятельная работа №1
### Найдите в интернете любую статью (объем статьи не менее 200 слов), скопируйте ее содержимое в файл и напишите программу, которая считает количество слов в текстовом файле и определит самое часто встречающееся слово. Результатом выполнения задачи будет: скриншот файла со статьей, листинг кода, и вывод в консоль, в котором будет указана вся необходимая информация.

```python

from collections import Counter
import string

# Открываем файл и читаем содержимое
with open('article.txt', 'r', encoding='utf-8') as file:
    text = file.read()

# Удаляем пунктуацию и переводим текст в нижний регистр
translator = str.maketrans('', '', string.punctuation)
cleaned_text = text.translate(translator).lower()

# Разбиваем текст на слова
words = cleaned_text.split()

# Считаем количество слов
word_count = len(words)

# Находим самое часто встречающееся слово
word_frequency = Counter(words)
most_common_word, most_common_count = word_frequency.most_common(1)[0]

# Выводим результаты
print(f'Общее количество слов: {word_count}')
print(f'Самое часто встречающееся слово: "{most_common_word}" (встречается {most_common_count} раз)')



```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/s1.png)


## Выводы

В этом коде используется функция bool, для вывода булевого значения из числа
  
## Самостоятельная работа №2
### У вас появилась необходимость в ведении книги расходов, посмотрев все существующие варианты вы пришли к выводу что ничего не устраивает и нужно делать самому. Напишите программу для учета расходов. Программа должна позволять вводить информацию о расходах, сохранять ее в файл и выводить существующие данные в консоль. Ввод информации происходит через консоль. Результатом выполнения задачи будет: скриншот файла с учетом расходов, листинг кода, и вывод в консоль, с демонстрацией работоспособности программы.


```python

import json
import os

# Имя файла для хранения данных о расходах
FILENAME = 'expenses.json'

# Функция для добавления расхода
def add_expense(expense):
    if os.path.exists(FILENAME):
        with open(FILENAME, 'r', encoding='utf-8') as file:
            data = json.load(file)
    else:
        data = []

    data.append(expense)

    with open(FILENAME, 'w', encoding='utf-8') as file:
        json.dump(data, file, ensure_ascii=False, indent=4)

# Функция для отображения всех расходов
def show_expenses():
    if os.path.exists(FILENAME):
        with open(FILENAME, 'r', encoding='utf-8') as file:
            data = json.load(file)
            for i, expense in enumerate(data, start=1):
                print(f"{i}. Дата: {expense['date']}, Сумма: {expense['amount']}, Описание: {expense['description']}")
    else:
        print("Нет записей о расходах.")

def main():
    while True:
        print("\n1. Добавить расход")
        print("2. Показать все расходы")
        print("3. Выход")
        
        choice = input("Выберите действие: ")
        
        if choice == '1':
            date = input("Введите дату (YYYY-MM-DD): ")
            amount = float(input("Введите сумму: "))
            description = input("Введите описание: ")
            expense = {
                'date': date,
                'amount': amount,
                'description': description
            }
            add_expense(expense)
            print("Расход добавлен!")
        
        elif choice == '2':
            print("\nСписок расходов:")
            show_expenses()
        
        elif choice == '3':
            break
        
        else:
            print("Неверный выбор. Пожалуйста, выберите снова.")

if __name__ == "__main__":
    main()


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/s2.png)

## Выводы

В данном коде реализована возможность присвоения значений нескольким переменным в одной строке
  
## Самостоятельная работа №3
### Имеется файл input.txt с текстом на латинице. Напишите программу, которая выводит следующую статистику по тексту: количество букв латинского алфавита; число слов; число строк.
• Текст в файле:
Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
• Ожидаемый результат:
Input file contains:
108 letters
20 words
4 lines



```python

def get_text_statistics(filename):
    try:
        with open(filename, 'r', encoding='utf-8') as file:
            text = file.readlines()

        # Инициализация счетчиков
        letter_count = 0
        word_count = 0
        line_count = len(text)

        # Обработка строк
        for line in text:
            # Удаление лишних пробелов и специального символа новой строки
            line = line.strip()
            letters_in_line = sum(c.isalpha() for c in line)  # Подсчет литер
            words_in_line = len(line.split())  # Подсчет слов

            letter_count += letters_in_line
            word_count += words_in_line

        # Возврат статистики в виде словаря
        return {
            'letters': letter_count,
            'words': word_count,
            'lines': line_count
        }

def main():
    filename = 'input.txt'
    statistics = get_text_statistics(filename)
    
    print(f"Input file contains:")
    print(f"{statistics['letters']} letters")
    print(f"{statistics['words']} words")
    print(f"{statistics['lines']} lines")

if __name__ == "__main__":
    main()


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/s3.png)

## Выводы

В данном коде показана возможность присвоения значения переменной с клавиатуры
  
## Самостоятельная работа №4
### Напиши программу на python. 4) Напишите программу, которая получает на вход предложение, выводит его в терминал, заменяя все запрещенные слова звездочками * (количество звездочек равно количеству букв в слове). Запрещенные слова, разделенные символом пробела, хранятся в текстовом файле input.txt. Все слова в этом файле записаны в нижнем регистре. Программа должна заменить запрещенные слова, где бы они ни встречались, даже в середине другого слова. Замена производится независимо от регистра: если файл input.txt содержит запрещенное слово ехат, то слова ехат, Exam, ЕхаМ, ЕХАМ и ехАт должны быть заменены на ****.
• Запрещенные слова:
hello email python the exam wor is
• Предложение для проверки:
Hello, world! Python IS the programming language of thE future. My
EMAIL is....
PYTHON is awesome!!!!
• Ожидаемый результат:
*****, ***ld! *********** programming language of *** future. My
*******
******** awesome!!!!



```python

def load_banned_words(filename):
    """Загружает запрещенные слова из файла и возвращает их в виде множества."""
    with open(filename, 'r', encoding='utf-8') as file:
        banned_words = set(file.read().strip().split())
    return banned_words

def replace_banned_words(sentence, banned_words):
    """Заменяет запрещенные слова на звездочки в предложении."""
    import re
    
    def replace_word(match):
        word = match.group(0)
        return '*' * len(word)  # Заменяем слово на звездочки
    
    # Создаём регулярное выражение для поиска запрещенных слов (независимо от регистра)
    regex_pattern = r'\b(' + '|'.join(re.escape(word) for word in banned_words) + r')\b'
    # Используем re.IGNORECASE для игнорирования регистра
    replaced_sentence = re.sub(regex_pattern, replace_word, sentence, flags=re.IGNORECASE)
    
    return replaced_sentence

def main():
    # Загружаем запрещенные слова
    banned_words = load_banned_words('input.txt')
    
    # Предложение для проверки
    test_sentence = "Hello, world! Python IS the programming language of thE future. My EMAIL is.... PYTHON is awesome!!!!"
    
    print("Исходное предложение:")
    print(test_sentence)
    
    # Заменяем запрещенные слова
    result = replace_banned_words(test_sentence, banned_words)
    
    print("\nРезультат:")
    print(result)

if __name__ == "__main__":
    main()


```
### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/s4.png)

## Выводы

В этом коде продемонстрирована возможность исполнения математических операций над строковыми переменными
  
## Самостоятельная работа №5
### Самостоятельно придумайте и решите задачу на python, которая будет взаимодействовать с текстовым файлом.



```python

import re
from collections import Counter

def load_text(filename):
    """Загружает текст из файла."""
    with open(filename, 'r', encoding='utf-8') as file:
        return file.read().strip()

def count_words(text):
    """Подсчитывает частоту слов в тексте."""
    # Приводим текст к нижнему регистру и заменяем знаки препинания на пробелы
    cleaned_text = re.sub(r'[^\w\s]', ' ', text.lower())
    words = cleaned_text.split()
    
    # Подсчитываем частоту появления каждого слова
    word_count = Counter(words)
    return word_count

def save_word_count(word_count, filename):
    """Сохраняет результаты подсчета слов в файл."""
    with open(filename, 'w', encoding='utf-8') as file:
        for word, count in word_count.items():
            file.write(f'{word}: {count}\n')

def main():
    # Загружаем текст из файла
    text = load_text('input.txt')

    # Считаем слова
    word_count = count_words(text)

    # Сохраняем результаты в файл
    save_word_count(word_count, 'output.txt')

    print("Частота слов успешно подсчитана и сохранена в output.txt.")

if __name__ == "__main__":
    main()


```


### Результат.
![Меню](https://github.com/AnnaZakharevich/-/blob/main/laba%205/pic/s5.png)

## Выводы

В данном коде показывается вывод коментариев совместно с переменными
  


## Общие выводы по теме
### Выполняя данную работу я вспомнила основные функции Python, синтаксис этого языка. В задачах этой работы используются простейшие операции, необходимые для присваивания значений, вывода этих значений и их изменения.
