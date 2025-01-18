def D_to_B(num, precision=10):
    if num == 0:
        return "0"

    # Handle negative numbers
    if num < 0:
        sign = "-"
    else:
        sign = ""
    num = abs(num)

    # Split integer and fractional parts
    integer_part = int(num)
    fractional_part = num - integer_part

    # Convert integer part
    binary_integer = ""
    if integer_part == 0:
        binary_integer = "0"
    while integer_part > 0:
        binary_integer = str(integer_part % 2) + binary_integer
        integer_part //= 2

    # Convert fractional part
    binary_fraction = ""
    count = 0
    while fractional_part > 0 and count < precision:
        fractional_part *= 2
        bit = int(fractional_part)
        binary_fraction += str(bit)
        fractional_part -= bit
        count += 1

    # Combine integer and fractional parts
    if binary_fraction:
        return sign + binary_integer + "." + binary_fraction
    else:
        return sign + binary_integer


def D_to_O(num, precision=10):
    if num == 0:
        return "0"

    # Handle negative numbers
    if num < 0:
        sign = "-"
    else:
        sign = ""
    num = abs(num)

    # Split integer and fractional parts
    integer_part = int(num)
    fractional_part = num - integer_part

    # Convert integer part
    octal_integer = ""
    if integer_part == 0:
        octal_integer = "0"
    while integer_part > 0:
        octal_integer = str(integer_part % 8) + octal_integer
        integer_part //= 8

    # Convert fractional part
    octal_fraction = ""
    count = 0
    while fractional_part > 0 and count < precision:
        fractional_part *= 8
        digit = int(fractional_part)
        octal_fraction += str(digit)
        fractional_part -= digit
        count += 1

    # Combine integer and fractional parts
    if octal_fraction:
        return sign + octal_integer + "." + octal_fraction
    else:
        return sign + octal_integer


def D_to_H(num, precision=10):
    if num == 0:
        return "0"

    # Handle negative numbers
    if num < 0:
        sign = "-"
    else:
        sign = ""
    num = abs(num)

    # Hexadecimal digits mapping
    hex_map = "0123456789ABCDEF"

    # Split integer and fractional parts
    integer_part = int(num)
    fractional_part = num - integer_part

    # Convert integer part
    hex_integer = ""
    if integer_part == 0:
        hex_integer = "0"
    while integer_part > 0:
        hex_integer = hex_map[integer_part % 16] + hex_integer
        integer_part //= 16

    # Convert fractional part
    hex_fraction = ""
    count = 0
    while fractional_part > 0 and count < precision:
        fractional_part *= 16
        digit = int(fractional_part)
        hex_fraction += hex_map[digit]
        fractional_part -= digit
        count += 1

    # Combine integer and fractional parts
    if hex_fraction:
        return sign + hex_integer + "." + hex_fraction
    else:
        return sign + hex_integer


# Home Page
print("=====================")
print("> Decimal Conversion")
print("=====================")

running = True
while running:
    print("> What Base Do You Want To Convert To?")
    print("> 1) Binary [Base 2]\n"
          "> 2) Octal [Base 8]\n"
          "> 3) Hexadecimal [Base 16]\n"
          "> E To Exit")
    base = input("> Enter: ")
    if base == "E" or base == "e":
        quit()
    elif base == "1":
        try:
            number = float(input("> Enter your number: "))
            print(f"{number} is {D_to_B(number)} in Binary.")
        except Exception as e:
            print(e)
    elif base == "2":
        try:
            number = float(input("> Enter your number: "))
            print(f"{number} is {D_to_O(number)} in Octal.")
        except Exception as e:
            print(e)
    elif base == "3":
        try:
            number = float(input("> Enter your number: "))
            print(f"{number} is {D_to_H(number)} in Hexadecimal.")
        except Exception as e:
            print(e)
    else:
        running = False
