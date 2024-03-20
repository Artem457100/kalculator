```python
class Car:
    def __init__(self, mark, age, model, name, cusov):
        self.__mark = mark  # устанавливаем имя
        self.__age = age  # устанавливаем возраст
        self.__model = model
        self.__name = name
        self.__cusov = cusov

    # сеттер для установки возраста
    def set_age(self, age):
        if 2004 <= age <= 2024:
            self.__age = age
        else:
            print("Недопустимый год производства")

    # геттер для получения возраста
    def get_age(self):
        return self.__age

    # геттер для получения имени
    def get_mark(self):
        return self.__mark

    def get_model(self):
        return self.__model

    def get_name(self):
        return self.__name

    def get_cusov(self):
        return self.__cusov

    def print_car(self):
        print(f"Марка: {self.__mark}\tВозраст: {self.__age}\tМодель: {self.__model}\tНазвание: {self.__name}\tМодель кузова: {self.__name}")
login = input()
password = input()
log = 1
pas = 2
if login == log and password == pas:
    print("Заказывайте")
else:
    print('Error')
mark_ = input('Введите марку машины: ')
age_ = int(input('Введите возраст машины: '))
model_ = input('Введите модель машины: ')
name_ = input('Введите название машины: ')
cusov_ = input('Введите модель кузова машины: ')
cars = Car(mark_, age_, model_, name_, cusov_)
cars.print_car()  # Имя: Tom  Возраст: 39
cars.set_age(2025)  # Недопустимый возраст
cars.set_age(2023)
cars.print_car()  # Имя: Tom  Возраст: 25
```
