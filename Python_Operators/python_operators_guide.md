# Python Operatorlari - To'liq Qo'llanma

## Mundarija
1. [Arithmetic operators (Arifmetik operatorlar)](#1-arithmetic-operators-arifmetik-operatorlar)
2. [Assignment operators (Tayinlash operatorlari)](#2-assignment-operators-tayinlash-operatorlari)
3. [Comparison operators (Taqqoslash operatorlari)](#3-comparison-operators-taqqoslash-operatorlari)
4. [Logical operators (Mantiqiy operatorlar)](#4-logical-operators-mantiqiy-operatorlar)
5. [Identity operators (Identifikatsiya operatorlari)](#5-identity-operators-identifikatsiya-operatorlari)
6. [Membership operators (A'zolik operatorlari)](#6-membership-operators-azolik-operatorlari)
7. [Bitwise operators (Bitli operatorlar)](#7-bitwise-operators-bitli-operatorlar)

---

## 1. Arithmetic Operators (Arifmetik Operatorlar)

Arifmetik operatorlar matematik amallarni bajarish uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `+` | Qo'shish | Ikki qiymatni qo'shadi | `5 + 3 = 8` |
| `-` | Ayirish | Birinchi qiymatdan ikkinchisini ayiradi | `5 - 3 = 2` |
| `*` | Ko'paytirish | Ikki qiymatni ko'paytiradi | `5 * 3 = 15` |
| `/` | Bo'lish | Birinchi qiymatni ikkinchisiga bo'ladi | `5 / 3 = 1.6667` |
| `//` | Butun bo'lish | Bo'lish natijasining butun qismini qaytaradi | `5 // 3 = 1` |
| `%` | Modul | Bo'lish qoldig'ini qaytaradi | `5 % 3 = 2` |
| `**` | Daraja | Birinchi sonni ikkinchi songa ko'taradi | `5 ** 3 = 125` |

### Kodda misollar:

```python
# Arifmetik operatorlar
a = 10
b = 3

print(f"a + b = {a + b}")     # 13
print(f"a - b = {a - b}")     # 7
print(f"a * b = {a * b}")     # 30
print(f"a / b = {a / b}")     # 3.333...
print(f"a // b = {a // b}")   # 3
print(f"a % b = {a % b}")     # 1
print(f"a ** b = {a ** b}")   # 1000
```

---

## 2. Assignment Operators (Tayinlash Operatorlari)

O'zgaruvchilarga qiymat berish uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `=` | Oddiy tayinlash | O'ngdagi qiymatni chapdagiga tayinlaydi | `x = 5` |
| `+=` | Qo'shib tayinlash | O'zgaruvchiga qiymat qo'shib tayinlaydi | `x += 3` → `x = x + 3` |
| `-=` | Ayirib tayinlash | O'zgaruvchidan qiymat ayirib tayinlaydi | `x -= 3` → `x = x - 3` |
| `*=` | Ko'paytirib tayinlash | O'zgaruvchini qiymatga ko'paytirib tayinlaydi | `x *= 3` → `x = x * 3` |
| `/=` | Bo'lib tayinlash | O'zgaruvchini qiymatga bo'lib tayinlaydi | `x /= 3` → `x = x / 3` |
| `//=` | Butun bo'lib tayinlash | O'zgaruvchini qiymatga butun bo'lib tayinlaydi | `x //= 3` → `x = x // 3` |
| `%=` | Modul tayinlash | O'zgaruvchini qiymatga modul bo'lib tayinlaydi | `x %= 3` → `x = x % 3` |
| `**=` | Daraja tayinlash | O'zgaruvchini qiymatga ko'tarib tayinlaydi | `x **= 3` → `x = x ** 3` |

### Kodda misollar:

```python
# Tayinlash operatorlari
x = 10
print(f"Dastlabki x = {x}")

x += 5
print(f"x += 5 dan keyin: {x}")  # 15

x -= 3
print(f"x -= 3 dan keyin: {x}")  # 12

x *= 2
print(f"x *= 2 dan keyin: {x}")  # 24

x /= 4
print(f"x /= 4 dan keyin: {x}")  # 6.0

x //= 2
print(f"x //= 2 dan keyin: {x}") # 3.0

x %= 2
print(f"x %= 2 dan keyin: {x}")  # 1.0

x **= 3
print(f"x **= 3 dan keyin: {x}") # 1.0
```

---

## 3. Comparison Operators (Taqqoslash Operatorlari)

Ikki qiymatni taqqoslash uchun ishlatiladi va mantiqiy qiymat qaytaradi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `==` | Teng | Ikki qiymat teng bo'lsa True qaytaradi | `5 == 5` → `True` |
| `!=` | Teng emas | Ikki qiymat teng bo'lmasa True qaytaradi | `5 != 3` → `True` |
| `>` | Katta | Chap qiymat o'ng qiymatdan katta bo'lsa True | `5 > 3` → `True` |
| `<` | Kichik | Chap qiymat o'ng qiymatdan kichik bo'lsa True | `3 < 5` → `True` |
| `>=` | Katta yoki teng | Chap qiymat o'ng qiymatdan katta yoki teng bo'lsa True | `5 >= 5` → `True` |
| `<=` | Kichik yoki teng | Chap qiymat o'ng qiymatdan kichik yoki teng bo'lsa True | `3 <= 5` → `True` |

### Kodda misollar:

```python
# Taqqoslash operatorlari
a = 10
b = 5

print(f"a == b: {a == b}")   # False
print(f"a != b: {a != b}")   # True
print(f"a > b: {a > b}")     # True
print(f"a < b: {a < b}")     # False
print(f"a >= b: {a >= b}")   # True
print(f"a <= b: {a <= b}")   # False

# Stringlarni taqqoslash
name1 = "Ali"
name2 = "Vali"
print(f"'{name1}' == '{name2}': {name1 == name2}")  # False
print(f"'{name1}' < '{name2}': {name1 < name2}")    # True (alfabetik tartib)
```

---

## 4. Logical Operators (Mantiqiy Operatorlar)

Mantiqiy ifodalarni birlashtirish uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `and` | VA | Ikkala shart ham True bo'lsa True qaytaradi | `True and True` → `True` |
| `or` | YOKI | Shartlardan biri True bo'lsa True qaytaradi | `True or False` → `True` |
| `not` | EMAS | Mantiqiy qiymatni teskarisiga o'zgartiradi | `not True` → `False` |

### Haqiqat jadvali:

| A | B | A and B | A or B | not A |
|---|---|---------|--------|-------|
| True | True | True | True | False |
| True | False | False | True | False |
| False | True | False | True | True |
| False | False | False | False | True |

### Kodda misollar:

```python
# Mantiqiy operatorlar
x = 5
y = 10
z = 15

# and operatori
print(f"x < y and y < z: {x < y and y < z}")  # True
print(f"x > y and y < z: {x > y and y < z}")  # False

# or operatori
print(f"x > y or y < z: {x > y or y < z}")    # True
print(f"x > y or y > z: {x > y or y > z}")    # False

# not operatori
print(f"not (x > y): {not (x > y)}")          # True
print(f"not (x < y): {not (x < y)}")          # False

# Murakkab misollar
yosh = 25
maosh = 5000
print(f"Yosh >= 18 va maosh >= 3000: {yosh >= 18 and maosh >= 3000}")  # True
```

---

## 5. Identity Operators (Identifikatsiya Operatorlari)

Ikki o'zgaruvchi bir xil obyektga ishora qilayotganini tekshirish uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `is` | Bir xil | Ikki o'zgaruvchi bir xil obyektga ishora qilsa True | `x is y` |
| `is not` | Bir xil emas | Ikki o'zgaruvchi turli obyektlarga ishora qilsa True | `x is not y` |

### Kodda misollar:

```python
# Identity operatorlar
# Sonlar bilan
x = 5
y = 5
z = 10

print(f"x is y: {x is y}")        # True (kichik sonlar uchun)
print(f"x is not z: {x is not z}")  # True

# Ro'yxatlar bilan
list1 = [1, 2, 3]
list2 = [1, 2, 3]
list3 = list1

print(f"list1 is list2: {list1 is list2}")  # False (turli obyektlar)
print(f"list1 is list3: {list1 is list3}")  # True (bir xil obyekt)
print(f"list1 == list2: {list1 == list2}")  # True (qiymatlari bir xil)

# None bilan
a = None
b = None
print(f"a is None: {a is None}")    # True
print(f"a is b: {a is b}")          # True
```

---

## 6. Membership Operators (A'zolik Operatorlari)

Elementning to'plamda mavjudligini tekshirish uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `in` | Ichida | Element to'plamda mavjud bo'lsa True | `'a' in 'salom'` |
| `not in` | Ichida emas | Element to'plamda mavjud bo'lmasa True | `'x' not in 'salom'` |

### Kodda misollar:

```python
# Membership operatorlar
# String bilan
text = "Python dasturlash"
print(f"'Python' in text: {'Python' in text}")        # True
print(f"'Java' in text: {'Java' in text}")            # False
print(f"'Java' not in text: {'Java' not in text}")    # True

# Ro'yxat bilan
raqamlar = [1, 2, 3, 4, 5]
print(f"3 in raqamlar: {3 in raqamlar}")              # True
print(f"6 in raqamlar: {6 in raqamlar}")              # False
print(f"6 not in raqamlar: {6 not in raqamlar}")      # True

# Tuple bilan
ranglar = ('qizil', 'yashil', 'ko\'k')
print(f"'qizil' in ranglar: {'qizil' in ranglar}")    # True
print(f"'sariq' in ranglar: {'sariq' in ranglar}")    # False

# Dictionary bilan (kalitlarni tekshiradi)
talaba = {'ism': 'Ali', 'yosh': 20, 'kurs': 2}
print(f"'ism' in talaba: {'ism' in talaba}")          # True
print(f"'manzil' in talaba: {'manzil' in talaba}")    # False
```

---

## 7. Bitwise Operators (Bitli Operatorlar)

Ikkilik (binary) darajada bitlar bilan ishlash uchun ishlatiladi.

### Operatorlar ro'yxati:

| Operator | Nomi | Tavsifi | Misol |
|----------|------|---------|-------|
| `&` | AND | Har ikkala bitda 1 bo'lsa 1 qaytaradi | `5 & 3 = 1` |
| `\|` | OR | Bitlardan biri 1 bo'lsa 1 qaytaradi | `5 \| 3 = 7` |
| `^` | XOR | Bitlar turli bo'lsa 1 qaytaradi | `5 ^ 3 = 6` |
| `~` | NOT | Bitlarni teskarisiga o'zgartiradi | `~5 = -6` |
| `<<` | Chapga siljitish | Bitlarni chapga siljitadi | `5 << 1 = 10` |
| `>>` | O'ngga siljitish | Bitlarni o'ngga siljitadi | `5 >> 1 = 2` |

### Bitli operatorlar jadvali:

| A | B | A & B | A \| B | A ^ B |
|---|---|-------|--------|-------|
| 0 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 |

### Kodda misollar:

```python
# Bitwise operatorlar
a = 5   # 101 (binary)
b = 3   # 011 (binary)

print(f"a = {a} ({bin(a)})")
print(f"b = {b} ({bin(b)})")

# AND operatori
result_and = a & b
print(f"a & b = {result_and} ({bin(result_and)})")   # 1 (001)

# OR operatori
result_or = a | b
print(f"a | b = {result_or} ({bin(result_or)})")     # 7 (111)

# XOR operatori
result_xor = a ^ b
print(f"a ^ b = {result_xor} ({bin(result_xor)})")   # 6 (110)

# NOT operatori
result_not = ~a
print(f"~a = {result_not}")                          # -6

# Chapga siljitish
result_left = a << 1
print(f"a << 1 = {result_left} ({bin(result_left)})")  # 10 (1010)

# O'ngga siljitish
result_right = a >> 1
print(f"a >> 1 = {result_right} ({bin(result_right)})")  # 2 (10)
```

---

## Operatorlar Ustunligi (Operator Precedence)

Python operatorlarining ustunlik tartibi (yuqoridan pastga kamayib boradi):

1. `**` (Daraja)
2. `+x`, `-x`, `~x` (Unary operatorlar)
3. `*`, `/`, `//`, `%` (Ko'paytirish, bo'lish)
4. `+`, `-` (Qo'shish, ayirish)
5. `<<`, `>>` (Bitli siljitish)
6. `&` (Bitli AND)
7. `^` (Bitli XOR)
8. `|` (Bitli OR)
9. `==`, `!=`, `<`, `<=`, `>`, `>=`, `is`, `is not`, `in`, `not in` (Taqqoslash)
10. `not` (Mantiqiy NOT)
11. `and` (Mantiqiy AND)
12. `or` (Mantiqiy OR)

### Misol:

```python
# Operatorlar ustunligi
result = 2 + 3 * 4  # 14, (2 + 12) emas (5 * 4)
print(f"2 + 3 * 4 = {result}")

# Qavslardan foydalanish
result2 = (2 + 3) * 4  # 20
print(f"(2 + 3) * 4 = {result2}")

# Murakkab ifoda
x = 5
y = 10
z = 3
result3 = x > y or y > z and z < x
print(f"x > y or y > z and z < x = {result3}")  # True
```

---

## Xulosa

Python operatorlari dasturlashda asosiy vositalardir. Ular quyidagi kategoriyalarga bo'linadi:

- **Arifmetik operatorlar**: Matematik amallar uchun
- **Tayinlash operatorlari**: O'zgaruvchilarga qiymat berish uchun
- **Taqqoslash operatorlari**: Qiymatlarni taqqoslash uchun
- **Mantiqiy operatorlar**: Mantiqiy ifodalar uchun
- **Identifikatsiya operatorlari**: Obyektlarni identifikatsiya qilish uchun
- **A'zolik operatorlari**: Elementlarning mavjudligini tekshirish uchun
- **Bitli operatorlar**: Bitli operatsiyalar uchun

Har bir operator o'ziga xos vazifani bajaradi va to'g'ri ishlatilganda kuchli dasturlar yozishga yordam beradi. Operatorlar ustunligini bilish va qavslardan to'g'ri foydalanish muhimdir.

---

*Bu qo'llanma Python dasturlash tilida operatorlar bilan ishlash bo'yicha asosiy bilimlarni beradi. Amaliyotda ko'proq mashq qilish orqali bu bilimlarni mustahkamlash mumkin.*