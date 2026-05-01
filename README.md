# decimal
Групповой проект по реализации библиотеки decimal для работы со 128-битным числом с плавающей запятой.

Библиотека s21_decimal.h на языке C, групповой проект для Школы21. 

### **Что делает**
Реализует 128-битное число с плавающей запятой в диапазоне от +79,228,162,514,264,337,593,543,950,335 до -79,228,162,514,264,337,593,543,950,335. Использует массив из четырёх int32.

**Арифметические операции**
Сложение	int s21_add(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)
Вычитание	int s21_sub(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)
Умножение	int s21_mul(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)
Деление		int s21_div(s21_decimal value_1, s21_decimal value_2, s21_decimal *result)

**Операции сравнения**
Меньше	 	        int s21_is_less(s21_decimal, s21_decimal)
Меньше или равно	int s21_is_less_or_equal(s21_decimal, s21_decimal)
Больше		        int s21_is_greater(s21_decimal, s21_decimal)
Больше или равно	int s21_is_greater_or_equal(s21_decimal, s21_decimal)
Равно		        int s21_is_equal(s21_decimal, s21_decimal)
Не равно		    int s21_is_not_equal(s21_decimal, s21_decimal)

**Преобразования**
Из int  	int s21_from_int_to_decimal(int src, s21_decimal *dst)
Из float	int s21_from_float_to_decimal(float src, s21_decimal *dst)
В int	    int s21_from_decimal_to_int(s21_decimal src, int *dst)
В float	    int s21_from_decimal_to_float(s21_decimal src, float *dst)

**Дополнительные функции**
Округление вниз             int s21_floor(s21_decimal value, s21_decimal *result)
Математическое округление	int s21_round(s21_decimal value, s21_decimal *result)
Отбросить дробную часть     int s21_truncate(s21_decimal value, s21_decimal *result)
Инвертировать знак          int s21_negate(s21_decimal value, s21_decimal *result)

### **Команды для локального запуска**
git clone
install_deps - *установить библиотеки check, lcov*  
make all - *собрать библиотеку*     
make test - *запустить тесты*   
make gcov_report - *запустить анализ тестового покрытия*   

### **Над чем я работала**
В команде было 5 человек, 2 занимались операциями, 1 функциями сравнения, 2 тестированием.

Я работала над реализацией математических операций и внутренних вспомогательных функций: алгоритмы сложения и вычитания, деления и умножения, разделение числа на целую и дробную часть, (внутренние вспомогательные) сложение и деление целых положительных без учета точки. Работа совместная.

### **Чем запомнилось**
- Командной работой (очные обсуждения + активное использование Git)
- Глубже изучила побитовые операции и работу с типами данных, влияние сложности алгоритма на скорость работы программы
- Интересно постепенно выстраивать базу вспомогательных функций, когда путь к требуемому результату не очевиден изначально