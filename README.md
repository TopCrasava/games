import array as arr
import random
import time
import sys

def орел_решка():
    money = input('Можливо, хочете поставити щось на кон (гроші)? ')
    print()

    time.sleep(1)

    monet = input("Оберіть 'орел' чи 'решка': ")
    time.sleep(2.5)

    print("Загрузка⌛⌛⌛")
    time.sleep(0.5)
    print('\n⌛\n')
    time.sleep(0.5)
    print('\n⌛\n')
    time.sleep(0.5)
    print('\n⌛\n')
    time.sleep(2.5)

    choices = {'орел': 1, 'решка': 2}

    try:
        monetValue = random.randint(1, 2)
        monet = choices[monet]
    except KeyError:
        print("Помилка: невірний вибір.")
        sys.exit()

    if monetValue == monet:
        print('Правильно, ви виграли!')
    else:
        print('Ви програли')

    time.sleep(1)

    if money != '0':
        if monetValue == monet:
            print(f'Ваш виграш: {money}')
        else:
            print(f'Ваш програш: {money}')
    elif monetValue == monet and int(money) > 99:
        print(f'Ви зіграли куш!!! Ваш куш: {money}')

def приклади():
    print('Оберіть режим:')
    print('1. Віднімання')
    print('2. Додавання')
    print('3. Множення')
    print('4. Ділення')

    choice = int(input("Ваш вибір: "))

    if choice == 1:
        режим_віднімання()
    elif choice == 2:
        режим_додавання()
    elif choice == 3:
        режим_множення()
    elif choice == 4:
        режим_ділення()
    else:
        print('Невірний вибір.')

# віднімання
def режим_віднімання():
    # логіка віднімання
    # вибір складності
        print('виберіть складність')
        print()
        print('вибір:легка, нормальна, важка')
        print()
        choise = input()
    # легка
        if choise == 'легка':
          one = 0
          two = 0
          result = 0

          one = random.randint(1, 10)
          two = random.randint(1, 10)
          result = two - one
          print(f"{two} - {one}")

          try:
              resurd = int(input("Введіть відповідь: "))
          except ValueError:
              print("Будь ласка, введіть число.")
              exit()

          print()

          Time = time.time()
          timer = time.time()
          AllTime = timer - Time

          if result == resurd and AllTime <= 0.1:
              print("Правильно, ви виграли!!!")
              print(f"Час виконання операції: {AllTime} секунд")
          elif 0.1 > AllTime:
              print("ви не встигли.")
          else:
              print("Не правильно, ви програли.")
    # нормальна
        elif choise == 'нормальна':
         oneo = random.randint(1, 50)
         twot = random.randint(1, 50)
         resultl = twot - oneo
         print(f"{twot} - {oneo}")

         try:
             resurdd = int(input("Введіть відповідь: "))
         except ValueError:
             print("Будь ласка, введіть число.")
             exit()

         print()

         Timet = time.time()

         timert = time.time()
         AllTimet = timert - Timet

         if resultl == resurdd and AllTimet <= 0.1:
           print("Правильно, ви виграли!!!")
           print(f"Час виконання операції: {AllTimet} секунд")
         elif 0.1 > AllTimet:
           print("ви не встигли.")
         else:
           print("Не правильно, ви програли.")
    # важка
        elif choise == 'важка':
         onen = random.randint(1, 100)
         twow = random.randint(1, 100)
         resultl = twow - onen
         print(f"{twow} - {onen}")
         try:
             resurdd = int(input("Введіть відповідь: "))
         except ValueError:
             print("Будь ласка, введіть число.")
             exit()
         print()

         Timetr = time.time()
         timertt = time.time()
         AllTimetd = timertt - Timetr

         if resultl == resurdd and AllTimetd <= 0.1:
           print("Правильно, ви виграли!!!")
           print(f"Час виконання операції: {AllTimetd} секунд")
         elif 0.1 > AllTimetd:
           print("ви не встигли.")
         else:
           print("Не правильно, ви програли.")

# додавання
def режим_додавання():
    # Логіка додавання
    # Вибір Складності 
       print('виберіть складність')
       print()
       print('вибір:легка, нормальна, важка')
       print()
       choise = input()
    # легка
       if choise == 'легка':
        one = random.randint(1, 10)
        two = random.randint(1, 10)
        result = one + two

        print(f'{one} + {two}')
        print()
        print('скільки буде?')
        print()
        resul = int(input())
        print()

        if result == resul:
            print('правильно!!!')
        else:
            print('неправильно')

    # нормальна
       elif choise == 'нормальна':
         one = random.randint(1, 50)
         two = random.randint(1, 50)
         result = one + two

         print(f'{one} + {two}')
         print()
         print('скільки буде?')
         print()
         resul = int(input())
         print()

         if result == resul:
             print('правильно!!!')
         else:
             print('неправильно')

    # важка
       elif choise == 'важка':
         one = random.randint(1, 100)
         two = random.randint(1, 100)
         result = one + two

         print(f'{one} + {two}')
         print()
         print('скільки буде?')
         print()
         resul = int(input())
         print()

         if result == resul:
             print('правильно!!!')
         else:
             print('неправильно')

       else:
          print('складності не знайдено')

# множення
def режим_множення():
    # Логіка множення
    #вибір складності
       print('виберіть складність')
       print()
       print('вибір:легка, нормальна, важка')
       print()
       choise = input()

    # легка
       if choise == 'легка':
        one = random.randint(1, 10)
        two = random.randint(1, 10)
        result = one*two

        print(f'{one} * {two}')
        print()
        print('скільки буде?')
        print()
        resul = int(input())
        print()

        if result == resul:
            print('правильно!!!')
        else:
            print('неправильно')

    # нормальна
       elif choise == 'нормальна':
         one = random.randint(1, 20)
         two = random.randint(1, 20)
         result = one*two

         print(f'{one} * {two}')
         print()
         print('скільки буде?')
         print()
         resul = int(input())
         print()

         if result == resul:
             print('правильно!!!')
         else:
             print('неправильно')

    # важка
       elif choise == 'важка':
         one = random.randint(1, 50)
         two = random.randint(1, 50)
         result = one*two

         print(f'{one}*{two}')
         print()
         print('скільки буде?')
         print()
         resul = int(input())
         print()

         if result == resul:
             print('правильно!!!')
         else:
             print('неправильно')

       else:
          print('складності не знайдено')

# ділення
def режим_ділення():
    # Логіка ділення
    # вибір складності
       print('виберіть складність:')  
       print()
       print('вибір:', end="")
       print('легка, нормальна, важка')
       print()
       choise = input()

    # легка
       if choise == 'легка':
         two = 2
         even_number = random.randrange(2, 21, 2)
         result = even_number / two

         print('Ось числа:')
         print()
         print(f'{even_number} / {two}')
         print()
         resul = float(input())

         print()

         if result == resul:
             print('Правильно!!!')
         else:
             print('Неправильно')

    # нормальна
       elif choise == 'нормальна':
        two = 2
        four = 4
        even_number = random.randrange(2, 51, 2)
        four_even_number = random.randrange(4, 52, 4)
        four_or_two = random.randint(1, 2)
        if four_or_two == 1:
         result = even_number / two

         print('Ось числа:')
         print()
         print(f'{even_number} / {two}')
         print()
         resul = float(input())

         print()

         if result == resul:
            print('Правильно!!!')
         else:
            print('Неправильно')
        else:
          result = four_even_number / four

          print('Ось числа:')
          print()
          print(f'{four_even_number} / {four}')
          print()
          resul = float(input())

          print()

          if result == resul:
             print('Правильно!!!')
          else:
             print('Неправильно')

    # важка    
       elif choise == 'важка':
         four = 4
         eight = 8
         four_even_number = random.randrange(4, 100, 4)
         eight_even_number = random.randrange(8, 104, 8)
         eight_or_four = random.randint(1, 2)
         if eight_or_four == 1:
          result = four_even_number / four

          print('Ось числа:')
          print()
          print(f'{four_even_number} / {four}')
          print()
          resul = float(input())

          print()

          if result == resul:
             print('Правильно!!!')
          else:
             print('Неправильно')
         else:
           result = eight_even_number / eight

           print('Ось числа:')
           print()
           print(f'{eight_even_number} / {eight}')
           print()
           resul = float(input())

           print()

           if result == resul:
              print('Правильно!!!')
           else:
              print('Неправильно')

# середнье арифметичне
def середнє_арифметичне():
    масив = arr.array('i', [random.randint(1, 10) for _ in range(3)])

    suma = sum(масив)
    resulllt = round(suma / len(масив), 0)

    print(масив)
    print()
    print("Яке середнє арифметичне тут?")
    print()

    res = int(input(""))

    time_start = time.time()
    time.sleep(0.1)
    time_end = time.time()

    if res == resulllt and (time_end - time_start) < 0.1:
        print("\nАбсолютно рівно!!!")
    else:
        print('\nНеправильно')

def main():
    print("В що ви хочете зіграти?")
    print('\n1. Орел чи решка\n2. Приклади\n3. Середнє арифметичне')
    game = input("Ваш вибір: ")

    if game.lower() in ['орел чи решка', '1']:
        орел_решка()
    elif game.lower() in ['приклади', '2']:
        приклади()
    elif game.lower() in ['середнє арифметичне', '3']:
        середнє_арифметичне()
    else:
        print('Гри не знайдено.')

if __name__ == "__main__":
    main()
