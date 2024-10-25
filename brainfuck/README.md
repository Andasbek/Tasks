### Инструкции для Python версии задачи

1. Реализуйте функцию `brainfuck_interpreter`, которая будет интерпретировать код на языке Brainfuck.
2. Функция принимает строку, содержащую код Brainfuck, и выполняет его, используя массив байтов (размером 2048), который изначально заполнен нулями.
3. Указатель начинается на первой ячейке массива.

### Операции в Brainfuck:
- `>`: Переместить указатель вправо.
- `<`: Переместить указатель влево.
- `+`: Увеличить значение текущей ячейки на 1.
- `-`: Уменьшить значение текущей ячейки на 1.
- `.`: Напечатать символ, соответствующий текущему значению ячейки.
- `[`: Если значение текущей ячейки равно 0, перейти к команде после соответствующей `]`.
- `]`: Если значение текущей ячейки не равно 0, перейти к команде после соответствующей `[`.
- Любые другие символы являются комментариями и должны игнорироваться.

### Ожидаемая функция:
```python
def brainfuck_interpreter(code: str) -> None:
    # Реализация функции
    pass
```

### Пример использования:
```python
brainfuck_interpreter("++++++++++[>+++++++>++++++++++>+++>+<<<<-]>++.>+.+++++++..+++.>++.<<+++++++++++++++.>.+++.------.--------.>+.>.")
# Должно вывести: Hello World!

brainfuck_interpreter("+++++[>++++[>++++H>+++++i<<-]>>>++<<<<-]>>--------.>+++++.>.")
# Должно вывести: Hi

brainfuck_interpreter("++++++++++[>++++++++++>++++++++++>++++++++++<<<-]>---.>--.>-.>++++++++++.")
# Должно вывести: abc
```

### Условия:
1. Размер кода не превышает 4096 операций.
2. Массив состоит из 2048 байтов, и все байты изначально равны 0.
3. Задачу необходимо решить без использования библиотек для обработки Brainfuck кода.

### Подсказка:
Студенту рекомендуется реализовать ручное управление указателем, а также отслеживание циклов `[ ]`, учитывая вложенные структуры.