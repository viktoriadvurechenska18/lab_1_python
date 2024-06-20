# завдання 1
def calculate_area(length, width):
    return length * width

# Введення даних для трьох прямокутників
length1 = float(input("Введіть довжину першого прямокутника: "))
width1 = float(input("Введіть ширину першого прямокутника: "))
length2 = float(input("Введіть довжину другого прямокутника: "))
width2 = float(input("Введіть ширину другого прямокутника: "))
length3 = float(input("Введіть довжину третього прямокутника: "))
width3 = float(input("Введіть ширину третього прямокутника: "))

# Розрахунок площі для кожного прямокутника
area1 = calculate_area(length1, width1)
area2 = calculate_area(length2, width2)
area3 = calculate_area(length3, width3)

# Виведення площі
print("Площа першого прямокутника:", area1)
print("Площа другого прямокутника:", area2)
print("Площа третього прямокутника:", area3)


#завдання 2
import math

def calculate_hypotenuse(leg1, leg2):
    return math.sqrt(leg1**2 + leg2**2)

def compare_hypotenuses(leg1_1, leg2_1, leg1_2, leg2_2):
    hypotenuse1 = calculate_hypotenuse(leg1_1, leg2_1)
    hypotenuse2 = calculate_hypotenuse(leg1_2, leg2_2)
    
    if hypotenuse1 > hypotenuse2:
        print("Перший трикутник має більшу гіпотенузу.")
    elif hypotenuse1 < hypotenuse2:
        print("Другий трикутник має більшу гіпотенузу.")
    else:
        print("Гіпотенузи обох трикутників рівні між собою.")
        
    print("Довжина гіпотенузи першого трикутника:", hypotenuse1)
    print("Довжина гіпотенузи другого трикутника:", hypotenuse2)

# Введення даних для двох трикутників
leg1_1 = float(input("Введіть перший катет першого трикутника: "))
leg2_1 = float(input("Введіть другий катет першого трикутника: "))
leg1_2 = float(input("Введіть перший катет другого трикутника: "))
leg2_2 = float(input("Введіть другий катет другого трикутника: "))

# Порівняння гіпотенуз
compare_hypotenuses(leg1_1, leg2_1, leg1_2, leg2_2)


#завдання 3
def point_inside_circle(x, y, a, b, R):
    distance_squared = (x - a)**2 + (y - b)**2
    return distance_squared <= R**2

def count_points_inside_circle(points, a, b, R):
    count = 0
    for point in points:
        if point_inside_circle(point[0], point[1], a, b, R):
            count += 1
    return count

# Введення параметрів кола
a = float(input("Введіть координату a центра кола: "))
b = float(input("Введіть координату b центра кола: "))
R = float(input("Введіть радіус кола: "))

# Введення координат трьох точок
P = tuple(map(float, input("Введіть координати точки P (p1, p2): ").split()))
F = tuple(map(float, input("Введіть координати точки F (f1, f2): ").split()))
L = tuple(map(float, input("Введіть координати точки L (l1, l2): ").split()))

# Розрахунок кількості точок всередині кола
points = [P, F, L]
points_inside = count_points_inside_circle(points, a, b, R)

# Виведення результату
print("Кількість точок, які лежать всередині кола:", points_inside)

#завдання 4
def calculate_area_rectangle(x, y):
    return x * y

# Введення довжин сторін двох прямокутників
X = float(input("Введіть довжину сторони X: "))
Y = float(input("Введіть довжину сторони Y: "))
Z = float(input("Введіть довжину сторони Z: "))
T = float(input("Введіть довжину сторони T: "))

# Розрахунок площі кожного прямокутника та загальної площі
area1 = calculate_area_rectangle(X, Y)
area2 = calculate_area_rectangle(Z, T)
total_area = area1 + area2

# Виведення загальної площі
print("Загальна площа двох прямокутників:", total_area)


#завдання 5
def find_numbers_divisible_by_all(n, divisors):
    result = []
    for i in range(1, n + 1):
        if all(i % divisor == 0 for divisor in divisors):
            result.append(i)
    return result

# Введення числа n та списку дільників
n = int(input("Введіть число n: "))
divisors = list(map(int, input("Введіть числа, на які потрібно ділити (через пробіл): ").split()))

# Знаходження чисел, які діляться на всі введені числа
result = find_numbers_divisible_by_all(n, divisors)

# Виведення результату
print("Натуральні числа, що діляться на кожне з введених чисел:")
print(result)



