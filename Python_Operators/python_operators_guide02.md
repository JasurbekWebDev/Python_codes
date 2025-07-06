# Python Operatorlari - To'liq Qo'llanma

## Mundarija
1. [Arithmetic operators (Arifmetik operatorlar)](#1-arithmetic-operators)
2. [Assignment operators (Tayinlash operatorlari)](#2-assignment-operators)
3. [Comparison operators (Taqqoslash operatorlari)](#3-comparison-operators)
4. [Logical operators (Mantiqiy operatorlar)](#4-logical-operators)
5. [Identity operators (Identifikatsiya operatorlari)](#5-identity-operators)
6. [Membership operators (A'zolik operatorlari)](#6-membership-operators)
7. [Bitwise operators (Bitli operatorlar)](#7-bitwise-operators)

---

## 1. Arithmetic Operators

Arifmetik operatorlar matematik amallarni bajarish uchun ishlatiladi.

### Operatorlar ro'yxati:
- **`+`** - Qo'shish
- **`-`** - Ayirish
- **`*`** - Ko'paytirish
- **`/`** - Bo'lish (natija float)
- **`//`** - Butun bo'lish (floor division)
- **`%`** - Qoldiq (modulo)
- **`**`** - Daraja (exponentiation)

### Misollar:
```python
a = 10
b = 3

print(a + b)    # 13
print(a - b)    # 7
print(a * b)    # 30
print(a / b)    # 3.3333333333333335
print(a // b)   # 3
print(a % b)    # 1
print(a ** b)   # 1000
```

### Amaliy qo'llanish:
```python
# Aylananing yuzini hisoblash
import math
radius = 5
area = math.pi * radius ** 2
print(f"Aylana yuzi: {area:.2f}")

# Vaqtni soat, minut, soniyaga ajratish
total_seconds = 3661
hours = total_seconds // 3600
minutes = (total_seconds % 3600) // 60
seconds = total_seconds % 60
print(f"{hours}:{minutes:02d}:{seconds:02d}")
```

---

## 2. Assignment Operators

Tayinlash operatorlari o'zgaruvchilarga qiymat berish uchun ishlatiladi.

### Operatorlar ro'yxati:
- **`=`** - Oddiy tayinlash
- **`+=`** - Qo'shib tayinlash
- **`-=`** - Ayirib tayinlash
- **`*=`** - Ko'paytirib tayinlash
- **`/=`** - Bo'lib tayinlash
- **`//=`** - Butun bo'lib tayinlash
- **`%=`** - Qoldiq bilan tayinlash
- **`**=`** - Darajaga ko'tarib tayinlash

### Misollar:
```python
x = 10
print(f"Boshlang'ich qiymat: {x}")

x += 5      # x = x + 5
print(f"x += 5: {x}")

x -= 3      # x = x - 3
print(f"x -= 3: {x}")

x *= 2      # x = x * 2
print(f"x *= 2: {x}")

x /= 4      # x = x / 4
print(f"x /= 4: {x}")

x //= 2     # x = x // 2
print(f"x //= 2: {x}")

x %= 3      # x = x % 3
print(f"x %= 3: {x}")

x **= 3     # x = x ** 3
print(f"x **= 3: {x}")
```

### Amaliy qo'llanish:
```python
# Hisoblagich
counter = 0
counter += 1  # Increment
print(f"Counter: {counter}")

# Compound interest calculator
principal = 1000
rate = 0.05
principal *= (1 + rate)
print(f"Bir yildan keyin: ${principal:.2f}")
```

---

## 3. Comparison Operators

Taqqoslash operatorlari ikki qiymatni taqqoslash uchun ishlatiladi va natija sifatida Boolean qiymat qaytaradi.

### Operatorlar ro'yxati:
- **`==`** - Teng
- **`!=`** - Teng emas
- **`>`** - Katta
- **`<`** - Kichik
- **`>=`** - Katta yoki teng
- **`<=`** - Kichik yoki teng

### Misollar:
```python
a = 10
b = 5
c = 10

print(f"a == b: {a == b}")    # False
print(f"a != b: {a != b}")    # True
print(f"a > b: {a > b}")      # True
print(f"a < b: {a < b}")      # False
print(f"a >= c: {a >= c}")    # True
print(f"b <= a: {b <= a}")    # True
```

### Amaliy qo'llanish:
```python
# Yosh tekshirish
age = 18
if age >= 18:
    print("Kattalar uchun")
else:
    print("Bolalar uchun")

# Parol kuchi tekshirish
password = "mypassword123"
if len(password) >= 8:
    print("Parol yetarlicha kuchli")
else:
    print("Parol kamida 8 ta belgidan iborat bo'lishi kerak")
```

---

## 4. Logical Operators

Mantiqiy operatorlar shartli ifodalarni birlashtirish uchun ishlatiladi.

### Operatorlar ro'yxati:
- **`and`** - Ikkala shart ham to'g'ri bo'lsa True
- **`or`** - Kamida bitta shart to'g'ri bo'lsa True
- **`not`** - Shartni teskarisiga o'giradi

### Misollar:
```python
x = 5
y = 10
z = 15

print(f"x < y and y < z: {x < y and y < z}")    # True
print(f"x > y or y < z: {x > y or y < z}")      # True
print(f"not x > y: {not x > y}")                # True
```

### Amaliy qo'llanish:
```python
# Foydalanuvchi autentifikatsiyasi
username = "admin"
password = "secret123"
is_admin = True

if username == "admin" and password == "secret123":
    print("Kirish muvaffaqiyatli")
    if is_admin:
        print("Admin huquqlari berildi")
else:
    print("Noto'g'ri foydalanuvchi nomi yoki parol")

# Yosh va litsenziya tekshirish
age = 20
has_license = True

if age >= 18 and has_license:
    print("Haydash mumkin")
elif age >= 18 and not has_license:
    print("Litsenziya olish kerak")
else:
    print("Yosh yetarli emas")
```

---

## 5. Identity Operators

Identifikatsiya operatorlari ob'ektlarning xotiradan bir xil joyda joylashganligini tekshiradi.

### Operatorlar ro'yxati:
- **`is`** - Bir xil ob'ekt
- **`is not`** - Har xil ob'ekt

### Misollar:
```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(f"a is b: {a is b}")          # False
print(f"a is c: {a is c}")          # True
print(f"a is not b: {a is not b}")  # True

# None bilan taqqoslash
value = None
print(f"value is None: {value is None}")        # True
print(f"value is not None: {value is not None}")# False
```

### Amaliy qo'llanish:
```python
# Singleton pattern
class Database:
    _instance = None
    
    def __new__(cls):
        if cls._instance is None:
            cls._instance = super().__new__(cls)
        return cls._instance

db1 = Database()
db2 = Database()
print(f"db1 is db2: {db1 is db2}")  # True

# None tekshirish
def process_data(data=None):
    if data is None:
        print("Ma'lumot berilmagan")
        return []
    return data
```

---

## 6. Membership Operators

A'zolik operatorlari elementning ketma-ketlikda mavjudligini tekshiradi.

### Operatorlar ro'yxati:
- **`in`** - Element mavjud
- **`not in`** - Element mavjud emas

### Misollar:
```python
fruits = ["apple", "banana", "orange"]
text = "Hello World"
numbers = {1, 2, 3, 4, 5}

print(f"'apple' in fruits: {'apple' in fruits}")          # True
print(f"'grape' not in fruits: {'grape' not in fruits}")  # True
print(f"'World' in text: {'World' in text}")              # True
print(f"3 in numbers: {3 in numbers}")                    # True
```

### Amaliy qo'llanish:
```python
# Email validatsiya
email = "user@example.com"
if "@" in email and "." in email:
    print("Email formati to'g'ri")
else:
    print("Noto'g'ri email format")

# Ruxsat etilgan foydalanuvchilar
allowed_users = ["admin", "user1", "user2"]
current_user = "user1"

if current_user in allowed_users:
    print("Kirish ruxsat etilgan")
else:
    print("Kirish rad etilgan")

# Kalit so'zlar filtri
forbidden_words = ["spam", "virus", "hack"]
message = "This is a normal message"

if any(word in message.lower() for word in forbidden_words):
    print("Xabar bloklangan")
else:
    print("Xabar yuborildi")
```

---

## 7. Bitwise Operators

Bitli operatorlar ikkilik (binary) darajada amallar bajaradi.

### Operatorlar ro'yxati:
- **`&`** - Bitli AND
- **`|`** - Bitli OR
- **`^`** - Bitli XOR
- **`~`** - Bitli NOT (complement)
- **`<<`** - Chapga siljitish
- **`>>`** - O'ngga siljitish

### Misollar:
```python
a = 12  # 1100 (binary)
b = 7   # 0111 (binary)

print(f"a & b: {a & b}")    # 4 (0100)
print(f"a | b: {a | b}")    # 15 (1111)
print(f"a ^ b: {a ^ b}")    # 11 (1011)
print(f"~a: {~a}")          # -13
print(f"a << 2: {a << 2}")  # 48 (110000)
print(f"a >> 2: {a >> 2}")  # 3 (0011)
```

### Amaliy qo'llanish:
```python
# Ruxsatnomalar tizimi
READ = 1    # 001
WRITE = 2   # 010
EXECUTE = 4 # 100

# Ruxsatnomalarni birlashtirish
permissions = READ | WRITE  # 011
print(f"Permissions: {permissions}")

# Ruxsatnoma tekshirish
if permissions & READ:
    print("O'qish ruxsati bor")
if permissions & WRITE:
    print("Yozish ruxsati bor")
if permissions & EXECUTE:
    print("Ijro etish ruxsati bor")
else:
    print("Ijro etish ruxsati yo'q")

# Effektiv matematik amallar
def is_even(n):
    return n & 1 == 0

def multiply_by_power_of_2(n, power):
    return n << power

def divide_by_power_of_2(n, power):
    return n >> power

print(f"8 juft son: {is_even(8)}")
print(f"5 * 2^3: {multiply_by_power_of_2(5, 3)}")
print(f"20 / 2^2: {divide_by_power_of_2(20, 2)}")
```

---

## Operatorlar Ustuvorligi

Python operatorlari quyidagi tartibda bajariladi (yuqoridan pastga):

1. **`()`** - Qavslar
2. **`**`** - Daraja
3. **`+x, -x, ~x`** - Unary operatorlar
4. **`*, /, //, %`** - Ko'paytirish, bo'lish
5. **`+, -`** - Qo'shish, ayirish
6. **`<<, >>`** - Siljitish
7. **`&`** - Bitli AND
8. **`^`** - Bitli XOR
9. **`|`** - Bitli OR
10. **`==, !=, <, <=, >, >=, is, is not, in, not in`** - Taqqoslash
11. **`not`** - Mantiqiy NOT
12. **`and`** - Mantiqiy AND
13. **`or`** - Mantiqiy OR

### Misol:
```python
result = 2 + 3 * 4 ** 2 and True or False
# Bu quyidagicha hisoblanadi:
# 4 ** 2 = 16
# 3 * 16 = 48
# 2 + 48 = 50
# 50 and True = True
# True or False = True
print(result)  # True
```

---

## Xulosa

Python operatorlari dasturlashda muhim rol o'ynaydi. Ularni to'g'ri tushunish va qo'llash samarali kod yozish uchun zarur. Har bir operator turining o'ziga xos xususiyatlari va qo'llanish sohalari mavjud.

**Muhim eslatmalar:**
- Arifmetik operatorlar matematik hisoblar uchun
- Taqqoslash operatorlari shartli ifodalar uchun
- Mantiqiy operatorlar murakkab shartlar uchun
- Identity operatorlar ob'ekt identifikatsiyasi uchun
- Membership operatorlar ketma-ketlik tekshirish uchun
- Bitwise operatorlar past darajadagi amallar uchun

Bu operatorlarni amalda qo'llab, Python dasturlashda malakangizni oshiring!

---

**Sana:** 2025-yil
**Til:** Python
**Maqsad:** Ta'lim va amaliy qo'llanish