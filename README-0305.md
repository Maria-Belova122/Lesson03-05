# ЗАДАНИЕ ПО ТЕМЕ "Рекурсия"

def get_multiplied_digits(number):
    # Представим число в виде строки, оставив только цыфры, отличные от нуля
    str_number = str(number).replace('0', '')
    length = len(str_number)
    first = int(str_number[0])
    if length == 1:
        return first
    else:
        return first * get_multiplied_digits(int(str_number[1:]))


result1 = get_multiplied_digits(40203)  # result1 = 4 * 2 * 3
result2 = get_multiplied_digits(9)  # result2 = 9
result3 = get_multiplied_digits(7780905)  # result3 = 7 * 7 * 8 * 9 * 5
result4 = get_multiplied_digits(6000)  # result4 = 6
print(result1)
print(result2)
print(result3)
print(result4)