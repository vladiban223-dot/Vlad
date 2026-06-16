def calculator():
    print("--- Простой калькулятор на Python ---")
    print("Доступные операции: +, -, *, /")
    print("Для выхода введите 'выход'\n")

    while True:
        user_input = input("Введите операцию (например, 2 + 2): ").strip()
        
        if user_input.lower() == 'выход':
            print("Программа завершена. До свидания!")
            break
            
        try:
            # Разделяем ввод на части: число, оператор, число
            parts = user_input.split()
            if len(parts) != 3:
                print("Ошибка! Вводите через пробел, например: 5 * 10")
                continue
                
            num1 = float(parts[0])
            operator = parts[1]
            num2 = float(parts[2])
            
            # Выполняем расчеты
            if operator == '+':
                result = num1 + num2
            elif operator == '-':
                result = num1 - num2
            elif operator == '*':
                result = num1 * num2
            elif operator == '/':
                if num2 == 0:
                    print("Ошибка: Деление на ноль невозможно!")
                    continue
                result = num1 / num2
            else:
                print(f"Ошибка: Оператор '{operator}' не поддерж
