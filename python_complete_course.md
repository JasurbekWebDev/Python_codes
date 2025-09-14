# TO'LIQ PYTHON DASTURLASH KURSI

## Mundarija
1. [Python bilan tanishuv](#1-python-bilan-tanishuv)
2. [O'zgaruvchilar va ma'lumot turlari](#2-ozgaruvchilar-va-malumot-turlari)
3. [Amallar va ifodalar](#3-amallar-va-ifodalar)
4. [Kiritish va chiqarish](#4-kiritish-va-chiqarish)
5. [Shartli operatorlar](#5-shartli-operatorlar)
6. [Tsikllar](#6-tsikllar)
7. [Ro'yxatlar (Lists)](#7-royxatlar-lists)
8. [Kortejlar (Tuples)](#8-kortejlar-tuples)
9. [Lug'atlar (Dictionaries)](#9-lugatlar-dictionaries)
10. [To'plamlar (Sets)](#10-toplamlar-sets)
11. [Satrlar bilan ishlash](#11-satrlar-bilan-ishlash)
12. [Funksiyalar](#12-funksiyalar)
13. [Fayllar bilan ishlash](#13-fayllar-bilan-ishlash)
14. [Xatoliklar va istisnolar](#14-xatoliklar-va-istisnolar)
15. [Obyektga yo'naltirilgan dasturlash](#15-obyektga-yonaltirilgan-dasturlash)
16. [Modullar va paketlar](#16-modullar-va-paketlar)
17. [Ilg'or mavzular](#17-ilgor-mavzular)

---

# 1. Python bilan tanishuv

Python - bu sodda, o'qish va yozish oson, kuchli dasturlash tili.

### Python tarixi va xususiyatlari
- 1991-yilda Guido van Rossum tomonidan yaratilgan
- Interpretatsiya qilinadigan til
- Katta kutubxonalar majmuasi
- Cross-platform (turli operatsion tizimlarda ishlaydi)

### Birinchi dastur

```python
# Bu sizning birinchi Python dasturingiz
print("Salom, dunyo!")
print("Python dasturlashni boshlayapmiz!")

# Izohlar uchun # belgisi ishlatiladi
# Bu satr bajarilmaydi
```

**Natija:**
```
Salom, dunyo!
Python dasturlashni boshlayapmiz!
```

---

## 2. O'zgaruvchilar va ma'lumot turlari

### O'zgaruvchilar yaratish

```python
# O'zgaruvchilar yaratish
ism = "Ahmad"
yosh = 25
bo'y = 1.75
talaba_mi = True

print(f"Ism: {ism}")
print(f"Yosh: {yosh}")
print(f"Bo'y: {bo'y} metr")
print(f"Talaba: {talaba_mi}")
```

### Asosiy ma'lumot turlari

```python
# 1. Butun sonlar (int)
son1 = 42
son2 = -15
print(f"Butun son: {son1}, turi: {type(son1)}")

# 2. O'nlik sonlar (float)
narx = 15.99
pi = 3.14159
print(f"O'nlik son: {narx}, turi: {type(narx)}")

# 3. Satrlar (string)
shahar = "Toshkent"
matn = 'Python juda zo\'r!'
print(f"Satr: {shahar}, turi: {type(shahar)}")

# 4. Mantiqiy qiymatlar (boolean)
rost = True
yolg'on = False
print(f"Mantiqiy: {rost}, turi: {type(rost)}")

# 5. Hech narsa (None)
bo'sh = None
print(f"Bo'sh qiymat: {bo'sh}, turi: {type(bo'sh)}")
```

### Ma'lumot turini tekshirish va o'zgartirish

```python
# Turni tekshirish
raqam = 123
print(type(raqam))  # <class 'int'>

# Turni o'zgartirish (Type casting)
satr_raqam = "456"
butun_raqam = int(satr_raqam)
print(f"Satr: {satr_raqam}, Butun son: {butun_raqam}")

# Turlararo o'tish
a = 10
b = float(a)    # 10.0
c = str(a)      # "10"
d = bool(a)     # True (0 dan boshqa barcha sonlar True)

print(f"int: {a}, float: {b}, str: {c}, bool: {d}")
```

---

## 3. Amallar va ifodalar

### Arifmetik amallar

```python
# Asosiy arifmetik amallar
a = 20
b = 3

qo'shish = a + b      # 23
ayirish = a - b       # 17
ko'paytirish = a * b  # 60
bo'lish = a / b       # 6.666...
butun_bo'lish = a // b  # 6
qoldiq = a % b        # 2
daraja = a ** b       # 8000 (20 ning 3-darajasi)

print(f"Qo'shish: {a} + {b} = {qo'shish}")
print(f"Ayirish: {a} - {b} = {ayirish}")
print(f"Ko'paytirish: {a} * {b} = {ko'paytirish}")
print(f"Bo'lish: {a} / {b} = {bo'lish}")
print(f"Butun bo'lish: {a} // {b} = {butun_bo'lish}")
print(f"Qoldiq: {a} % {b} = {qoldiq}")
print(f"Daraja: {a} ** {b} = {daraja}")
```

### Taqqoslash amallar

```python
x = 10
y = 5

print(f"{x} == {y}: {x == y}")  # False
print(f"{x} != {y}: {x != y}")  # True
print(f"{x} > {y}: {x > y}")    # True
print(f"{x} < {y}: {x < y}")    # False
print(f"{x} >= {y}: {x >= y}")  # True
print(f"{x} <= {y}: {x <= y}")  # False
```

### Mantiqiy amallar

```python
# Mantiqiy operatorlar
a = True
b = False

print(f"a and b: {a and b}")  # False
print(f"a or b: {a or b}")    # True
print(f"not a: {not a}")      # False

# Amaliy misol
yosh = 22
maktabni_bitirgan = True

universitetga_kirish = yosh >= 18 and maktabni_bitirgan
print(f"Universitetga kira oladi: {universitetga_kirish}")
```

---

## 4. Kiritish va chiqarish

### Ma'lumot kiritish

```python
# Foydalanuvchidan ma'lumot olish
ism = input("Ismingizni kiriting: ")
yosh = int(input("Yoshingizni kiriting: "))
bo'y = float(input("Bo'yingizni kiriting (metr): "))

print(f"Salom {ism}!")
print(f"Siz {yosh} yoshda ekansiz")
print(f"Bo'yingiz {bo'y} metr")

# Xavfsiz kiritish
try:
    ball = int(input("Balingizni kiriting (0-100): "))
    if 0 <= ball <= 100:
        print(f"Sizning balingiz: {ball}")
    else:
        print("Baho 0 dan 100 gacha bo'lishi kerak!")
except ValueError:
    print("Iltimos, son kiriting!")
```

### Chiroyli chiqarish

```python
# f-string ishlatish (tavsiya etiladi)
ism = "Ali"
yosh = 20
print(f"Mening ismim {ism}, men {yosh} yoshdaman")

# format() metodi
print("Mening ismim {}, men {} yoshdaman".format(ism, yosh))
print("Mening ismim {name}, men {age} yoshdaman".format(name=ism, age=yosh))

# % formatlaash (eski usul)
print("Mening ismim %s, men %d yoshdaman" % (ism, yosh))

# Raqamlarni formatlash
narx = 1500.789
print(f"Narx: {narx:.2f} so'm")  # 1500.79 so'm

foiz = 0.85
print(f"Foiz: {foiz:.1%}")  # 85.0%
```

---

## 5. Shartli operatorlar

### if-elif-else strukturasi

```python
# Oddiy if operatori
yosh = 18

if yosh >= 18:
    print("Siz kattasiz")
else:
    print("Siz hali bolasiz")

# Ko'p shartli if-elif-else
baho = 85

if baho >= 90:
    harfli_baho = "A"
elif baho >= 80:
    harfli_baho = "B"
elif baho >= 70:
    harfli_baho = "C"
elif baho >= 60:
    harfli_baho = "D"
else:
    harfli_baho = "F"

print(f"Sizning bahongiz: {harfli_baho}")
```

### Murakkab shartlar

```python
# Bir nechta shartlarni birlashtirish
yosh = 25
ish_bor = True
oylik = 5000000

kredit_olish = yosh >= 21 and ish_bor and oylik >= 3000000

if kredit_olish:
    print("Kredit olishingiz mumkin!")
else:
    print("Kredit olish shartlarini qondirmayapsiz")
    
# Ichma-ich if operatorlari
ob_havo = "quyoshli"
harorat = 25

if ob_havo == "quyoshli":
    if harorat > 20:
        print("Sayrga chiqish uchun ajoyib kun!")
    else:
        print("Quyoshli, lekin sovuq")
else:
    print("Ichkarida qoling")
```

### Qisqa if operatori (ternary)

```python
# Qisqa if operatori
yosh = 20
status = "katta" if yosh >= 18 else "kichik"
print(f"Siz {status}siz")

# Amaliy misol
a = 10
b = 5
katta = a if a > b else b
print(f"Eng katta son: {katta}")
```

---

## 6. Tsikllar

### for tsikli

```python
# Oddiy for tsikli
print("1 dan 5 gacha sonlar:")
for i in range(1, 6):
    print(i)

# Ro'yxat bo'ylab iteratsiya
mevalar = ["olma", "banan", "apelsin", "uzum"]
print("\nMevalar ro'yxati:")
for meva in mevalar:
    print(f"- {meva}")

# Indeks bilan birga
print("\nIndeks va qiymat:")
for indeks, meva in enumerate(mevalar):
    print(f"{indeks}: {meva}")

# range() funksiyasi turli ko'rinishlari
print("\n0 dan 9 gacha:")
for i in range(10):
    print(i, end=" ")

print("\n\n2 dan 10 gacha 2 qadam bilan:")
for i in range(2, 11, 2):
    print(i, end=" ")
```

### while tsikli

```python
# Oddiy while tsikli
hisoblagich = 1
print("\n\n1 dan 5 gacha (while):")
while hisoblagich <= 5:
    print(hisoblagich)
    hisoblagich += 1

# Foydalanuvchi kiritguncha davom etish
print("\nSonlarni kiriting (0 kiritsangiz to'xtaydi):")
while True:
    son = int(input("Son: "))
    if son == 0:
        break
    print(f"Siz {son} sonini kiritdingiz")

# Shartli while
javob = ""
while javob.lower() != "ha":
    javob = input("Dasturni tugatmoqchimisiz? (ha/yo'q): ")
print("Dastur tugadi!")
```

### break va continue

```python
# break - tsiklni to'xtatish
print("1 dan 10 gacha, lekin 5 da to'xtash:")
for i in range(1, 11):
    if i == 5:
        break
    print(i)

print("\n")

# continue - keyingi iteratsiyaga o'tish
print("1 dan 10 gacha, juft sonlarsiz:")
for i in range(1, 11):
    if i % 2 == 0:  # juft son bo'lsa
        continue
    print(i)

# Amaliy misol
sonlar = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
toq_sonlar_yigindisi = 0

for son in sonlar:
    if son % 2 == 0:  # juft son bo'lsa, o'tkazib yuborish
        continue
    toq_sonlar_yigindisi += son

print(f"\nToq sonlar yig'indisi: {toq_sonlar_yigindisi}")
```

---

## 7. Ro'yxatlar (Lists)

### Ro'yxat yaratish va asosiy amallar

```python
# Ro'yxat yaratish
bo'sh_royxat = []
sonlar = [1, 2, 3, 4, 5]
mevalar = ["olma", "banan", "apelsin"]
aralash = [1, "matn", 3.14, True]

print("Sonlar ro'yxati:", sonlar)
print("Mevalar ro'yxati:", mevalar)
print("Aralash ro'yxat:", aralash)

# Ro'yxat elementlariga murojaat
print(f"\nBirinchi meva: {mevalar[0]}")
print(f"Oxirgi meva: {mevalar[-1]}")
print(f"Ikkinchi meva: {mevalar[1]}")

# Ro'yxat uzunligi
print(f"Mevalar soni: {len(mevalar)}")
```

### Ro'yxat metodlari

```python
# Element qo'shish
mevalar = ["olma", "banan"]
mevalar.append("apelsin")  # oxiriga qo'shish
print("append dan keyin:", mevalar)

mevalar.insert(1, "uzum")  # 1-indeksga qo'shish
print("insert dan keyin:", mevalar)

# Element o'chirish
mevalar.remove("banan")  # qiymat bo'yicha o'chirish
print("remove dan keyin:", mevalar)

oxirgi_meva = mevalar.pop()  # oxirgisini o'chirish va qaytarish
print(f"O'chirilgan meva: {oxirgi_meva}")
print("pop dan keyin:", mevalar)

del mevalar[0]  # indeks bo'yicha o'chirish
print("del dan keyin:", mevalar)

# Boshqa foydali metodlar
sonlar = [3, 1, 4, 1, 5, 9, 2, 6]
print(f"\nAsl ro'yxat: {sonlar}")

sonlar.sort()  # tartiblash
print(f"Tartiblangan: {sonlar}")

sonlar.reverse()  # teskari tartiblash
print(f"Teskari: {sonlar}")

print(f"1 soni necha marta uchraydi: {sonlar.count(1)}")
print(f"5 sonining indeksi: {sonlar.index(5)}")
```

### Ro'yxat bilan ishlash

```python
# Ro'yxatni birlashtirish
ro'yxat1 = [1, 2, 3]
ro'yxat2 = [4, 5, 6]
birlashgan = ro'yxat1 + ro'yxat2
print("Birlashgan ro'yxat:", birlashgan)

# Ro'yxatni ko'paytirish
takroriy = [0] * 5
print("Takroriy ro'yxat:", takroriy)

# Kesim (slicing)
sonlar = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
print(f"Asl ro'yxat: {sonlar}")
print(f"Birinchi 5 ta: {sonlar[:5]}")
print(f"Oxirgi 3 ta: {sonlar[-3:]}")
print(f"2 dan 7 gacha: {sonlar[2:7]}")
print(f"2 qadam bilan: {sonlar[::2]}")

# Ro'yxat ichida qidirish
if "apelsin" in mevalar:
    print("Apelsin bor!")
else:
    print("Apelsin yo'q")

# List comprehension
kvadratlar = [x**2 for x in range(10)]
print("Kvadratlar:", kvadratlar)

juft_sonlar = [x for x in range(20) if x % 2 == 0]
print("Juft sonlar:", juft_sonlar)
```

---

## 8. Kortejlar (Tuples)

### Kortej yaratish va xususiyatlari

```python
# Kortej yaratish
bo'sh_kortej = ()
koordinata = (3, 5)
rgb_rang = (255, 128, 0)
aralash_kortej = (1, "matn", 3.14, True)

print("Koordinata:", koordinata)
print("RGB rang:", rgb_rang)
print("Aralash kortej:", aralash_kortej)

# Bir elementli kortej
bir_elementli = (42,)  # vergul muhim!
print("Bir elementli kortej:", bir_elementli)

# Kortej elementlariga murojaat
print(f"X koordinata: {koordinata[0]}")
print(f"Y koordinata: {koordinata[1]}")

# Kortejni ochish (unpacking)
x, y = koordinata
print(f"x = {x}, y = {y}")

r, g, b = rgb_rang
print(f"Qizil: {r}, Yashil: {g}, Ko'k: {b}")
```

### Kortej bilan ishlash

```python
# Kortejlar o'zgarmas (immutable)
try:
    koordinata[0] = 10  # Xatolik beradi!
except TypeError as e:
    print(f"Xatolik: {e}")

# Kortej metodlari
sonlar = (1, 2, 3, 2, 4, 2, 5)
print(f"2 soni necha marta: {sonlar.count(2)}")
print(f"3 sonining indeksi: {sonlar.index(3)}")

# Kortejni ro'yxatga aylantirish
ro'yxat = list(sonlar)
ro'yxat[0] = 10
yangi_kortej = tuple(ro'yxat)
print(f"Asl kortej: {sonlar}")
print(f"Yangi kortej: {yangi_kortej}")

# Kortejlarni birlashtirish
kortej1 = (1, 2, 3)
kortej2 = (4, 5, 6)
birlashgan = kortej1 + kortej2
print("Birlashgan kortej:", birlashgan)

# Kortejda qidirish
if 3 in sonlar:
    print("3 soni mavjud")

# Nesting (ichma-ich kortejlar)
nuqtalar = ((0, 0), (1, 1), (2, 4))
for i, (x, y) in enumerate(nuqtalar):
    print(f"Nuqta {i+1}: ({x}, {y})")
```

---

## 9. Lug'atlar (Dictionaries)

### Lug'at yaratish va asosiy amallar

```python
# Lug'at yaratish
bo'sh_lugat = {}
talaba = {
    "ism": "Ahmad",
    "yosh": 20,
    "fakultet": "IT",
    "kurs": 2
}

print("Talaba ma'lumotlari:", talaba)

# Elementlarga murojat qilish.
print(f"Ism: {talaba['ism']}")
print(f"Yosh: {talaba['yosh']}")

# Xavfsiz murojaat (get metodi)
print(f"Fakultet: {talaba.get('fakultet', 'Noma\'lum')}")
print(f"Telefon: {talaba.get('telefon', 'Noma\'lum')}")

# Yangi element qo'shish va o'zgartirish
talaba["telefon"] = "+998901234567"
talaba["yosh"] = 21  # mavjud qiymatni o'zgartirish

print("Yangilangan ma'lumotlar:", talaba)
```

### Lug'at metodlari

```python
# Lug'at metodlari
kitob = {
    "nomi": "Python dasturlash",
    "muallif": "Ahmad",
    "sahifalar": 300,
    "yil": 2023
}

# Kalitlar, qiymatlar va juftliklar
print("Kalitlar:", list(kitob.keys()))
print("Qiymatlar:", list(kitob.values()))
print("Juftliklar:", list(kitob.items()))

# Lug'at bo'ylab iteratsiya
print("\nKitob haqida ma'lumot:")
for kalit, qiymat in kitob.items():
    print(f"{kalit}: {qiymat}")

# Element o'chirish
del kitob["yil"]
print("\n'yil' o'chirilgandan keyin:", kitob)

ochirgan = kitob.pop("sahifalar", "Topilmadi")
print(f"O'chirilgan qiymat: {ochirgan}")

# Lug'atni tozalash
nusxa = kitob.copy()  # nusxa olish
kitob.clear()  # tozalash
print("Tozalangandan keyin:", kitob)
print("Nusxa:", nusxa)
```

### Murakkab lug'atlar

```python
# Ichma-ich lug'atlar
maktab = {
    "nom": "1-son maktab",
    "o'quvchilar": {
        "10A": ["Ali", "Vali", "Guli"],
        "10B": ["Sami", "Nuri", "Doni"],
        "11A": ["Karim", "Halim", "Salim"]
    },
    "o'qituvchilar": {
        "matematika": "Aziz Azizov",
        "fizika": "Vali Valiyev",
        "kimyo": "Guli Guliyeva"
    }
}

print("Maktab nomi:", maktab["nom"])
print("10A sinf o'quvchilari:", maktab["o'quvchilar"]["10A"])
print("Matematika o'qituvchisi:", maktab["o'qituvchilar"]["matematika"])

# Ro'yxat ichidagi lug'atlar
talabalar = [
    {"ism": "Ali", "yosh": 20, "baho": 85},
    {"ism": "Vali", "yosh": 19, "baho": 92},
    {"ism": "Guli", "yosh": 21, "baho": 78}
]

print("\nTalabalar ro'yxati:")
for talaba in talabalar:
    print(f"{talaba['ism']} ({talaba['yosh']} yosh): {talaba['baho']} ball")

# Eng yuqori bahoni topish
eng_yuqori = max(talabalar, key=lambda x: x['baho'])
print(f"Eng yuqori baho: {eng_yuqori['ism']} - {eng_yuqori['baho']} ball")
```

---

## 10. To'plamlar (Sets)

### To'plam yaratish va asosiy amallar

```python
# To'plam yaratish
bo'sh_toplam = set()
raqamlar = {1, 2, 3, 4, 5}
mevalar = {"olma", "banan", "apelsin", "olma"}  # takroriy elementlar o'chadi
print("Raqamlar to'plami:", raqamlar)
print("Mevalar to'plami:", mevalar)  # faqat unikal elementlar qoladi

# Ro'yxatdan to'plam yaratish
ro'yxat = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]
unikal = set(ro'yxat)
print("Asl ro'yxat:", ro'yxat)
print("Unikal elementlar:", unikal)

# Element qo'shish va o'chirish
hayvonlar = {"mushuk", "it", "qush"}
hayvonlar.add("baliq")
print("Baliq qo'shilgandan keyin:", hayvonlar)

hayvonlar.remove("it")  # element bo'lmasa xatolik beradi
print("It o'chirilgandan keyin:", hayvonlar)

hayvonlar.discard("sher")  # element bo'lmasa xatolik bermaydi
print("Sher o'chirilgandan keyin:", hayvonlar)
```

### To'plamlar bilan amallar

```python
# To'plamlar ustida matematik amallar
A = {1, 2, 3, 4, 5}
B = {4, 5, 6, 7, 8}

print(f"A to'plam: {A}")
print(f"B to'plam: {B}")

# Birlashtirish (Union)
birlashma = A | B  # yoki A.union(B)
print(f"Birlashma (A ∪ B): {birlashma}")

# Kesishma (Intersection)
kesishma = A & B  # yoki A.intersection(B)
print(f"Kesishma (A ∩ B): {kesishma}")

# Ayirma (Difference)
ayirma = A - B  # yoki A.difference(B)
print(f"Ayirma (A - B): {ayirma}")

# Simmetrik ayirma
sim_ayirma = A ^ B  # yoki A.symmetric_difference(B)
print(f"Simmetrik ayirma (A △ B): {sim_ayirma}")

# Ichiga olish (Subset/Superset)
C = {1, 2, 3}
print(f"C {C} A ning qismi: {C.issubset(A)}")
print(f"A C ni o'z ichiga oladi: {A.issuperset(C)}")

# Ajralganlik
D = {10, 11, 12}
print(f"A va D ajralgan: {A.isdisjoint(D)}")
```

### Amaliy misollar

```python
# So'zda takrorlanmagan harflar topish
soz = "dasturlash"
unikal_harflar = set(soz)
print(f"'{soz}' so'zidagi unikal harflar: {unikal_harflar}")
print(f"Unikal harflar soni: {len(unikal_harflar)}")

# Ikkita ro'yxatdagi umumiy elementlar
ro'yxat1 = ["olma", "banan", "apelsin", "uzum"]
ro'yxat2 = ["banan", "kivi", "apelsin", "shaftoli"]

umumiy = set(ro'yxat1) & set(ro'yxat2)
print(f"Umumiy mevalar: {umumiy}")

# Takrorlanmagan elementlarni saqlash
def unikal_qilish(ro'yxat):
    return list(set(ro'yxat))

asl_ro'yxat = [1, 2, 2, 3, 4, 4, 5, 5, 5]
unikal_ro'yxat = unikal_qilish(asl_ro'yxat)
print(f"Asl: {asl_ro'yxat}")
print(f"Unikal: {unikal_ro'yxat}")
```

---

## 11. Satrlar bilan ishlash

### Satr yaratish va asosiy xususiyatlar

```python
# Satr yaratish usullari
oddiy_satr = "Bu oddiy satr"
qo'shtirnoqli = 'Bu ham satr'
ko'p_qatorli = """Bu
ko'p qatorli
satr"""

print(oddiy_satr)
print(qo'shtirnoqli)
print(ko'p_qatorli)

# Maxsus belgilar (escape characters)
maxsus = "Bu satr\nyangi qatorda\tva tab bilan"
print(maxsus)

# Raw string (r belgisi bilan)
fayl_yo'li = r"C:\Users\Ahmad\Desktop\fayl.txt"
print(fayl_yo'li)

# Satr uzunligi va indekslash
matn = "Python dasturlash"
print(f"Satr uzunligi: {len(matn)}")
print(f"Birinchi harf: {matn[0]}")
print(f"Oxirgi harf: {matn[-1]}")
print(f"5-indeksdagi harf: {matn[5]}")
```

### Satr metodlari

```python
# Satr metodlari
matn = "  Python Dasturlash Tili  "
print(f"Asl matn: '{matn}'")

# Bo'sh joylarni tozalash
print(f"strip(): '{matn.strip()}'")
print(f"lstrip(): '{matn.lstrip()}'")
print(f"rstrip(): '{matn.rstrip()}'")

# Katta va kichik harflarga aylantirish
print(f"upper(): '{matn.upper()}'")
print(f"lower(): '{matn.lower()}'")
print(f"title(): '{matn.title()}'")
print(f"capitalize(): '{matn.capitalize()}'")

# Satr tekshirish metodlari
satr1 = "Python123"
satr2 = "12345"
satr3 = "python"

print(f"'{satr1}' raqam va harflardan: {satr1.isalnum()}")
print(f"'{satr2}' faqat raqamlar: {satr2.isdigit()}")
print(f"'{satr3}' kichik harflar: {satr3.islower()}")

# Satrni bo'lish va birlashtirish
gap = "Python dasturlash juda qiziqarli"
so'zlar = gap.split()
print(f"So'zlar: {so'zlar}")

yangi_gap = " - ".join(so'zlar)
print(f"Birlashtirish: {yangi_gap}")

# Almashtirish
eski_matn = "Java dasturlash tili"
yangi_matn = eski_matn.replace("Java", "Python")
print(f"Almashtirilgan: {yangi_matn}")
```

### Satr formatlash

```python
# f-string (eng yaxshi usul)
ism = "Ahmad"
yosh = 25
maosh = 1500.50

# Oddiy f-string
print(f"Mening ismim {ism}, men {yosh} yoshdaman")

# Raqamlarni formatlash
print(f"Maosh: {maosh:.2f} million")
print(f"Foiz: {0.85:.1%}")
print(f"Katta raqam: {1234567:,}")

# Hizalash
print(f"{'O\'ng':>10}")  # o'ngga
print(f"{'Chap':<10}")   # chapga
print(f"{'Markazga':^15}")  # markazga

# format() metodi
shablon = "Ism: {name}, Yosh: {age}, Shahar: {city}"
print(shablon.format(name="Vali", age=30, city="Toshkent"))

# % formatlash (eski usul)
print("Ism: %s, Yosh: %d, Maosh: %.2f" % (ism, yosh, maosh))
```

### Satrlar bilan ilg'or ishlash

```python
# Satrda qidirish
matn = "Python dasturlash tilini o'rganamiz"

print(f"'dasturlash' bor: {'dasturlash' in matn}")
print(f"'Java' yo'q: {'Java' not in matn}")
print(f"'Python' joylashuvi: {matn.find('Python')}")
print(f"'tili' joylashuvi: {matn.index('tili')}")

# Satrni kesish (slicing)
print(f"Birinchi 6 harf: {matn[:6]}")
print(f"7-harfdan oxirigacha: {matn[7:]}")
print(f"7 dan 17 gacha: {matn[7:17]}")
print(f"Teskari: {matn[::-1]}")

# Satr takrorlash
chiziq = "-" * 30
print(chiziq)
print("SARLAVHA")
print(chiziq)

# Maxsus belgilarni encode/decode qilish
matn_utf8 = "Salom dunyo! 🌍"
encoded = matn_utf8.encode('utf-8')
decoded = encoded.decode('utf-8')
print(f"Asl: {matn_utf8}")
print(f"Encoded: {encoded}")
print(f"Decoded: {decoded}")

# Regex bilan ishlash (import kerak)
import re

matn = "Telefon: +998-90-123-45-67"
raqam = re.findall(r'\d+', matn)
print(f"Topilgan raqamlar: {raqam}")
```

---

## 12. Funksiyalar

### Oddiy funksiyalar

```python
# Oddiy funksiya
def salomlash():
    print("Assalomu alaykum!")

# Funksiyani chaqirish
salomlash()

# Parametrli funksiya
def shaxsiy_salomlash(ism):
    print(f"Salom, {ism}!")

shaxsiy_salomlash("Ahmad")
shaxsiy_salomlash("Fotima")

# Qiymat qaytaruvchi funksiya
def qo'shish(a, b):
    natija = a + b
    return natija

yig'indi = qo'shish(5, 3)
print(f"5 + 3 = {yig'indi}")

# Bir nechta qiymat qaytarish
def matematik_amallar(a, b):
    qo'shish = a + b
    ayirish = a - b
    ko'paytirish = a * b
    bo'lish = a / b if b != 0 else None
    return qo'shish, ayirish, ko'paytirish, bo'lish

q, a, k, b = matematik_amallar(10, 3)
print(f"10 va 3: qo'shish={q}, ayirish={a}, ko'paytirish={k}, bo'lish={b:.2f}")
```

### Parametrlarning turli ko'rinishlari

```python
# Standart qiymatli parametrlar
def tanishtiruv(ism, yosh, shahar="Toshkent"):
    print(f"Mening ismim {ism}, {yosh} yoshdaman, {shahar}da yashayman")

tanishtiruv("Ali", 25)  # shahar standart qiymatni oladi
tanishtiruv("Vali", 30, "Samarqand")  # barcha parametrlar berildi

# Kalit so'z argumentlari
def buyurtma(taom, miqdor=1, narx=0, chegirma=0):
    summa = narx * miqdor * (1 - chegirma/100)
    print(f"Taom: {taom}, Miqdor: {miqdor}, Summa: {summa} so'm")

buyurtma("Osh", miqdor=2, narx=15000, chegirma=10)
buyurtma(taom="Lag'mon", narx=12000)

# O'zgaruvchan miqdordagi argumentlar (*args)
def yigindi(*raqamlar):
    return sum(raqamlar)

print(f"Yig'indi: {yigindi(1, 2, 3, 4, 5)}")
print(f"Yig'indi: {yigindi(10, 20)}")

# Kalit so'zli o'zgaruvchan argumentlar (**kwargs)
def ma'lumot_chiqar(**malumotlar):
    for kalit, qiymat in malumotlar.items():
        print(f"{kalit}: {qiymat}")

print("Talaba ma'lumotlari:")
ma'lumot_chiqar(ism="Sardor", yosh=22, fakultet="IT", kurs=3)
```

### Ilg'or funksiya mavzulari

```python
# Lambda funksiyalari
kvadrat = lambda x: x ** 2
print(f"5 ning kvadrati: {kvadrat(5)}")

yig'indi = lambda a, b: a + b
print(f"Lambda yig'indi: {yig'indi(10, 5)}")

# Higher-order functions
sonlar = [1, 2, 3, 4, 5]

# map() funksiyasi
kvadratlar = list(map(lambda x: x**2, sonlar))
print(f"Kvadratlar: {kvadratlar}")

# filter() funksiyasi
juft_sonlar = list(filter(lambda x: x % 2 == 0, sonlar))
print(f"Juft sonlar: {juft_sonlar}")

# Ichki funksiyalar (Nested functions)
def tashqi_funksiya(x):
    def ichki_funksiya(y):
        return x + y
    return ichki_funksiya

qo'shuvchi = tashqi_funksiya(10)
natija = qo'shuvchi(5)  # 10 + 5 = 15
print(f"Ichki funksiya natijasi: {natija}")

# Dekorator misoli
def vaqt_o'lchash(func):
    import time
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"{func.__name__} {end_time - start_time:.4f} soniyada bajarildi")
        return result
    return wrapper

@vaqt_o'lchash
def katta_hisobla():
    return sum(range(1000000))

natija = katta_hisobla()
print(f"Yig'indi: {natija}")
```

### Rekursiv funksiyalar

```python
# Faktorial hisoblash
def faktorial(n):
    if n <= 1:
        return 1
    else:
        return n * faktorial(n - 1)

print(f"5! = {faktorial(5)}")

# Fibonachchi ketma-ketligi
def fibonachchi(n):
    if n <= 1:
        return n
    else:
        return fibonachchi(n-1) + fibonachchi(n-2)

print("Fibonachchi ketma-ketligi:")
for i in range(10):
    print(fibonachchi(i), end=" ")
print()

# Optimallashtirilgan Fibonachchi (memoization)
def fib_memo(n, memo={}):
    if n in memo:
        return memo[n]
    if n <= 1:
        return n
    memo[n] = fib_memo(n-1, memo) + fib_memo(n-2, memo)
    return memo[n]

print(f"\nOptimal Fibonachchi F(50) = {fib_memo(50)}")
```

---

## 13. Fayllar bilan ishlash

### Asosiy fayl amallari

```python
# Faylga yozish
def fayl_yaratish():
    with open("test.txt", "w", encoding="utf-8") as fayl:
        fayl.write("Bu birinchi qator\n")
        fayl.write("Bu ikkinchi qator\n")
        fayl.write("Bu uchinchi qator\n")
    print("Fayl yaratildi va yozildi")

fayl_yaratish()

# Fayldan o'qish
def fayl_o'qish():
    try:
        with open("test.txt", "r", encoding="utf-8") as fayl:
            mazmun = fayl.read()
            print("Faylning to'liq mazmuni:")
            print(mazmun)
    except FileNotFoundError:
        print("Fayl topilmadi!")

fayl_o'qish()

# Qator bo'yicha o'qish
def qatorlar_o'qish():
    try:
        with open("test.txt", "r", encoding="utf-8") as fayl:
            print("Qator bo'yicha:")
            for i, qator in enumerate(fayl, 1):
                print(f"{i}: {qator.strip()}")
    except FileNotFoundError:
        print("Fayl topilmadi!")

qatorlar_o'qish()

# Faylga qo'shimcha yozish
def fayl_qo'shimcha():
    with open("test.txt", "a", encoding="utf-8") as fayl:
        fayl.write("Bu qo'shimcha qator\n")
        fayl.write("Yana bir qator\n")
    print("Fayl yangilandi")

fayl_qo'shimcha()
```

### Murakkab fayl amallari

```python
import os
import json
import csv

# JSON fayllar bilan ishlash
def json_misol():
    # Ma'lumotlarni JSON faylga yozish
    ma'lumot = {
        "talabalar": [
            {"ism": "Ali", "yosh": 20, "baho": 85},
            {"ism": "Vali", "yosh": 19, "baho": 92},
            {"ism": "Guli", "yosh": 21, "baho": 78}
        ],
        "sana": "2023-12-01"
    }
    
    with open("talabalar.json", "w", encoding="utf-8") as fayl:
        json.dump(ma'lumot, fayl, ensure_ascii=False, indent=2)
    print("JSON fayl yaratildi")
    
    # JSON fayldan o'qish
    with open("talabalar.json", "r", encoding="utf-8") as fayl:
        yuklangan = json.load(fayl)
        print("JSON fayldan o'qilgan ma'lumot:")
        for talaba in yuklangan["talabalar"]:
            print(f"  {talaba['ism']}: {talaba['baho']} ball")

json_misol()

# CSV fayllar bilan ishlash
def csv_misol():
    # CSV fayl yaratish
    with open("mahsulotlar.csv", "w", newline="", encoding="utf-8") as fayl:
        yozuvchi = csv.writer(fayl)
        yozuvchi.writerow(["Mahsulot", "Narx", "Miqdor"])  # sarlavha
        yozuvchi.writerow(["Olma", 5000, 50])
        yozuvchi.writerow(["Banan", 8000, 30])
        yozuvchi.writerow(["Apelsin", 6000, 40])
    print("CSV fayl yaratildi")
    
    # CSV fayldan o'qish
    with open("mahsulotlar.csv", "r", encoding="utf-8") as fayl:
        o'quvchi = csv.reader(fayl)
        print("CSV fayldan o'qilgan ma'lumot:")
        for qator in o'quvchi:
            print("  ", " | ".join(qator))

csv_misol()

# Fayl va papka bilan ishlash
def fayl_tizimi():
    # Fayl mavjudligini tekshirish
    if os.path.exists("test.txt"):
        print("test.txt fayl mavjud")
        
        # Fayl ma'lumotlari
        stat = os.stat("test.txt")
        print(f"Fayl hajmi: {stat.st_size} bayt")
        
    # Papka yaratish
    if not os.path.exists("yangi_papka"):
        os.mkdir("yangi_papka")
        print("Yangi papka yaratildi")
    
    # Papka mazmuninii ko'rish
    print("Hozirgi papka mazmuni:")
    for element in os.listdir("."):
        if os.path.isfile(element):
            print(f"  📄 {element}")
        elif os.path.isdir(element):
            print(f"  📁 {element}")

fayl_tizimi()
```

### Xatoliklarni boshqarish

```python
# Fayl bilan ishlashda xatoliklarni boshqarish
def xavfsiz_fayl_o'qish(fayl_nomi):
    try:
        with open(fayl_nomi, "r", encoding="utf-8") as fayl:
            return fayl.read()
    except FileNotFoundError:
        print(f"Xatolik: '{fayl_nomi}' fayl topilmadi")
        return None
    except PermissionError:
        print(f"Xatolik: '{fayl_nomi}' faylga kirish ruxsati yo'q")
        return None
    except Exception as e:
        print(f"Kutilmagan xatolik: {e}")
        return None

# Test qilish
mazmun = xavfsiz_fayl_o'qish("mavjud_emas.txt")
if mazmun:
    print("Fayl muvaffaqiyatli o'qildi")

# Context manager yaratish
class FaylBoshqaruvchi:
    def __init__(self, fayl_nomi, rejim):
        self.fayl_nomi = fayl_nomi
        self.rejim = rejim
        self.fayl = None
    
    def __enter__(self):
        print(f"Fayl ochilmoqda: {self.fayl_nomi}")
        self.fayl = open(self.fayl_nomi, self.rejim, encoding="utf-8")
        return self.fayl
    
    def __exit__(self, exc_type, exc_val, exc_tb):
        print(f"Fayl yopilmoqda: {self.fayl_nomi}")
        if self.fayl:
            self.fayl.close()

# Maxsus context manager dan foydalanish
with FaylBoshqaruvchi("test2.txt", "w") as fayl:
    fayl.write("Context manager orqali yozilgan matn")
```

---

## 14. Xatoliklar va istisnolar

### Asosiy istisno turlari

```python
# Turli xil xatoliklar misollari
def xatolik_misollari():
    # SyntaxError - sintaksis xatoligi (kod yozishda)
    # print("Salom"  # qavs yopilmagan
    
    # NameError - noma'lum o'zgaruvchi
    try:
        print(mavjud_emas_ozgaruvchi)
    except NameError as e:
        print(f"NameError: {e}")
    
    # TypeError - noto'g'ri ma'lumot turi
    try:
        natija = "5" + 3
    except TypeError as e:
        print(f"TypeError: {e}")
    
    # ValueError - noto'g'ri qiymat
    try:
        raqam = int("abc")
    except ValueError as e:
        print(f"ValueError: {e}")
    
    # ZeroDivisionError - nolga bo'lish
    try:
        natija = 10 / 0
    except ZeroDivisionError as e:
        print(f"ZeroDivisionError: {e}")
    
    # IndexError - indeks xatoligi
    try:
        ro'yxat = [1, 2, 3]
        print(ro'yxat[5])
    except IndexError as e:
        print(f"IndexError: {e}")
    
    # KeyError - kalit xatoligi
    try:
        lugat = {"a": 1, "b": 2}
        print(lugat["c"])
    except KeyError as e:
        print(f"KeyError: {e}")

xatolik_misollari()
```

### Try-except-else-finally

```python
# To'liq try-except strukturasi
def xavfsiz_bo'lish(a, b):
    try:
        natija = a / b
    except ZeroDivisionError:
        print("Xatolik: Nolga bo'lib bo'lmaydi!")
        return None
    except TypeError:
        print("Xatolik: Faqat raqamlar bilan ishlaydi!")
        return None
    else:
        print("Bo'lish muvaffaqiyatli amalga oshirildi")
        return natija
    finally:
        print("Bu kod har doim bajariladi")

print("Test 1:")
print(xavfsiz_bo'lish(10, 2))

print("\nTest 2:")
print(xavfsiz_bo'lish(10, 0))

print("\nTest 3:")
print(xavfsiz_bo'lish("10", "2"))

# Bir nechta xatolikni birdaniga tutish
def murakkab_amal(ro'yxat, indeks):
    try:
        qiymat = int(ro'yxat[indeks])
        natija = 100 / qiymat
        return natija
    except (IndexError, ValueError, ZeroDivisionError) as e:
        print(f"Xatolik yuz berdi: {type(e).__name__}: {e}")
        return None

# Test
ro'yxat = ["10", "0", "abc", "5"]
for i in range(6):
    print(f"Indeks {i}: {murakkab_amal(ro'yxat, i)}")
```

### Maxsus xatoliklar yaratish

```python
# Maxsus istisno sinfi yaratish
class YoshXatoligi(Exception):
    """Yosh bilan bog'liq xatoliklar uchun"""
    def __init__(self, yosh, xabar="Noto'g'ri yosh"):
        self.yosh = yosh
        self.xabar = xabar
        super().__init__(self.xabar)

class HaydovchilikGuvohnomasiXatoligi(Exception):
    """Haydovchilik guvohnomasi bilan bog'liq xatoliklar"""
    pass

def haydovchilik_tekshirish(yosh, guvohnoma_bor):
    if yosh < 18:
        raise YoshXatoligi(yosh, "Haydovchilik uchun kamida 18 yosh bo'lishi kerak")
    
    if not guvohnoma_bor:
        raise HaydovchilikGuvohnomasiXatoligi("Haydovchilik guvohnomasi yo'q!")
    
    print("Haydovchilik uchun ruxsat berildi!")

# Maxsus xatoliklarni sinash
test_hollari = [
    (16, True),    # Yosh kam
    (20, False),   # Guvohnoma yo'q
    (25, True),    # Hammasi joyida
]

for yosh, guvohnoma in test_hollari:
    try:
        haydovchilik_tekshirish(yosh, guvohnoma)
    except YoshXatoligi as e:
        print(f"Yosh xatoligi: {e} (Yosh: {e.yosh})")
    except HaydovchilikGuvohnomasiXatoligi as e:
        print(f"Guvohnoma xatoligi: {e}")
    except Exception as e:
        print(f"Kutilmagan xatolik: {e}")
    print("---")

# Xatolikni qayta ko'tarish (re-raising)
def hisobla_va_log(a, b):
    try:
        natija = a / b
        print(f"Hisoblash muvaffaqiyatli: {a} / {b} = {natija}")
        return natija
    except Exception as e:
        print(f"Xatolik yuzaga keldi: {e}")
        print("Xatolik log fayliga yozilmoqda...")
        raise  # Xatolikni qayta ko'tarish

try:
    hisobla_va_log(10, 0)
except ZeroDivisionError:
    print("Dasturning yuqori darajasida xatolik tutildi")
```

### Xatoliklarni monitoring qilish

```python
import traceback
import logging
from datetime import datetime

# Logging sozlash
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s',
    handlers=[
        logging.FileHandler('xatoliklar.log', encoding='utf-8'),
        logging.StreamHandler()
    ]
)

def xatolikni_log_qilish():
    try:
        # Xatolik yuzaga keltirish
        ro'yxat = [1, 2, 3]
        print(ro'yxat[10])
    except Exception as e:
        # Batafsil xatolik ma'lumotini log qilish
        error_info = {
            'xatolik_turi': type(e).__name__,
            'xabar': str(e),
            'vaqt': datetime.now().strftime('%Y-%m-%d %H:%M:%S'),
            'traceback': traceback.format_exc()
        }
        
        logging.error(f"Xatolik yuz berdi: {error_info['xatolik_turi']}")
        logging.error(f"Xabar: {error_info['xabar']}")
        logging.error(f"Traceback:\n{error_info['traceback']}")
        
        print("Xatolik log fayliga yozildi")

xatolikni_log_qilish()

# Assert operatori
def yosh_tekshirish(yosh):
    assert yosh >= 0, "Yosh manfiy bo'lishi mumkin emas"
    assert yosh <= 150, "Yosh haddan tashqari katta"
    assert isinstance(yosh, int), "Yosh butun son bo'lishi kerak"
    
    return f"Yosh to'g'ri: {yosh}"

# Assert test qilish
test_yoshlar = [25, -5, 200, 30.5]
for yosh in test_yoshlar:
    try:
        natija = yosh_tekshirish(yosh)
        print(natija)
    except AssertionError as e:
        print(f"Assert xatoligi: {e}")
    except Exception as e:
        print(f"Boshqa xatolik: {e}")
```

---

## 15. Obyektga yo'naltirilgan dasturlash

### Sinflar va obyektlar

```python
# Oddiy sinf yaratish
class Avtomobil:
    def __init__(self, marka, model, yil, rang="oq"):
        self.marka = marka
        self.model = model
        self.yil = yil
        self.rang = rang
        self.kilometraj = 0
        self.yoqilg'i_tank = 50  # litr
    
    def ma'lumot(self):
        return f"{self.yil} yil {self.marka} {self.model} ({self.rang})"
    
    def haydash(self, masofa):
        yoqilg'i_sarfi = masofa / 10  # 10 km/litr
        if self.yoqilg'i_tank >= yoqilg'i_sarfi:
            self.kilometraj += masofa
            self.yoqilg'i_tank -= yoqilg'i_sarfi
            print(f"{masofa} km yo'l bosildi. Kilometraj: {self.kilometraj}")
        else:
            print("Yoqilg'i yetmaydi!")
    
    def yoqilg'i_quyish(self, miqdor):
        self.yoqilg'i_tank = min(self.yoqilg'i_tank + miqdor, 50)
        print(f"Yoqilg'i quqildi. Hozirgi miqdor: {self.yoqilg'i_tank} litr")

# Obyektlar yaratish va ishlatish
avtomobil1 = Avtomobil("Toyota", "Camry", 2020, "qora")
avtomobil2 = Avtomobil("BMW", "X5", 2019)

print(avtomobil1.ma'lumot())
print(avtomobil2.ma'lumot())

avtomobil1.haydash(100)
avtomobil1.yoqilg'i_quyish(20)
avtomobil1.haydash(200)
```

### Voraslik (Inheritance)

```python
# Asosiy (ota) sinf
class Hayvon:
    def __init__(self, tur, yosh):
        self.tur = tur
        self.yosh = yosh
        self.sog'liq = 100
    
    def ovqatlanish(self):
        print(f"{self.tur} ovqatlanmoqda")
        self.sog'liq = min(self.sog'liq + 10, 100)
    
    def uxlash(self):
        print(f"{self.tur} uxlamoqda")
        self.sog'liq = min(self.sog'liq + 5, 100)
    
    def holat(self):
        return f"{self.tur} ({self.yosh} yosh) - Sog'liq: {self.sog'liq}%"

# Voris sinflar
class It(Hayvon):
    def __init__(self, ism, yosh, zot):
        super().__init__("It", yosh)  # Ota sinfning __init__ metodini chaqirish
        self.ism = ism
        self.zot = zot
        self.sadoqat = 100
    
    def vovullash(self):
        print(f"{self.ism} vov-vov qilmoqda!")
        self.sadoqat += 5
    
    def o'ynash(self):
        print(f"{self.ism} o'ynashni yaxshi ko'radi")
        self.sog'liq -= 5
        self.sadoqat += 10
    
    def holat(self):  # Metodning qayta aniqlanishi (override)
        return f"It {self.ism} ({self.zot}, {self.yosh} yosh) - Sog'liq: {self.sog'liq}%, Sadoqat: {self.sadoqat}%"

class Mushuk(Hayvon):
    def __init__(self, ism, yosh, rang):
        super().__init__("Mushuk", yosh)
        self.ism = ism
        self.rang = rang
        self.mustaqillik = 80
    
    def miyovlash(self):
        print(f"{self.ism} miyov-miyov qilmoqda")
    
    def tirmolash(self):
        print(f"{self.ism} tirmolayapti")
        self.mustaqillik += 5
    
    def holat(self):
        return f"Mushuk {self.ism} ({self.rang}, {self.yosh} yosh) - Sog'liq: {self.sog'liq}%, Mustaqillik: {self.mustaqillik}%"

# Voris sinflardan obyektlar yaratish
it = It("Bobik", 3, "Nemis cho'poni")
mushuk = Mushuk("Mursik", 2, "oq")

print(it.holat())
print(mushuk.holat())

it.vovullash()
it.o'ynash()
it.ovqatlanish()

mushuk.miyovlash()
mushuk.tirmolash()
mushuk.uxlash()

print("\nYangilangan holatlar:")
print(it.holat())
print(mushuk.holat())
```

### Maxfiylik va xususiyatlar

```python
# Private va protected o'zgaruvchilar
class BankHisobi:
    def __init__(self, egasi, boshlang'ich_balans=0):
        self.egasi = egasi  # public
        self._hisob_raqami = self._hisob_raqam_yaratish()  # protected
        self.__balans = boshlang'ich_balans  # private
        self.__pin_kod = "1234"  # private
    
    def _hisob_raqam_yaratish(self):  # protected method
        import random
        return f"UZ{''.join([str(random.randint(0, 9)) for _ in range(10)])}"
    
    def __pin_tekshirish(self, pin):  # private method
        return pin == self.__pin_kod
    
    def balansni_korish(self, pin):
        if self.__pin_tekshirish(pin):
            return self.__balans
        else:
            return "Noto'g'ri PIN kod!"
    
    def pul_qo'yish(self, miqdor, pin):
        if self.__pin_tekshirish(pin):
            if miqdor > 0:
                self.__balans += miqdor
                return f"{miqdor} so'm qo'yildi. Yangi balans: {self.__balans}"
            else:
                return "Miqdor musbat bo'lishi kerak!"
        else:
            return "Noto'g'ri PIN kod!"
    
    def pul_yechish(self, miqdor, pin):
        if self.__pin_tekshirish(pin):
            if 0 < miqdor <= self.__balans:
                self.__balans -= miqdor
                return f"{miqdor} so'm yechildi. Qolgan balans: {self.__balans}"
            else:
                return "Yetarli mablag' yo'q yoki noto'g'ri miqdor!"
        else:
            return "Noto'g'ri PIN kod!"
    
    def pin_o'zgartirish(self, eski_pin, yangi_pin):
        if self.__pin_tekshirish(eski_pin):
            self.__pin_kod = yangi_pin
            return "PIN kod muvaffaqiyatli o'zgartirildi!"
        else:
            return "Eski PIN kod noto'g'ri!"

# Bank hisobi bilan ishlash
hisob = BankHisobi("Ahmad Ahmadov", 1000000)

print(f"Hisob egasi: {hisob.egasi}")
print(f"Hisob raqami: {hisob._hisob_raqami}")  # protected ga kirish mumkin (tavsiya etilmaydi)

# Private o'zgaruvchiga to'g'ridan-to'g'ri kirish mumkin emas
# print(hisob.__balans)  # AttributeError beradi

print(hisob.balansni_korish("1234"))
print(hisob.pul_qo'yish(500000, "1234"))
print(hisob.pul_yechish(200000, "1234"))
print(hisob.pin_o'zgartirish("1234", "5678"))
print(hisob.balansni_korish("5678"))
```

### Property va getter/setter

```python
# Property dekoratori bilan ishlash
class Harorat:
    def __init__(self, selsiy=0):
        self._selsiy = selsiy
    
    @property
    def selsiy(self):
        return self._selsiy
    
    @selsiy.setter
    def selsiy(self, qiymat):
        if qiymat < -273.15:
            raise ValueError("Harorat mutlaq noldan past bo'lishi mumkin emas")
        self._selsiy = qiymat
    
    @property
    def fahrenheyt(self):
        return self._selsiy * 9/5 + 32
    
    @fahrenheyt.setter
    def fahrenheyt(self, qiymat):
        self.selsiy = (qiymat - 32) * 5/9
    
    @property
    def kelvin(self):
        return self._selsiy + 273.15
    
    @kelvin.setter
    def kelvin(self, qiymat):
        self.selsiy = qiymat - 273.15

# Harorat bilan ishlash
harorat = Harorat(25)

print(f"Selsiy: {harorat.selsiy}°C")
print(f"Fahrenheyt: {harorat.fahrenheyt}°F")
print(f"Kelvin: {harorat.kelvin}K")

# Fahrenheyt orqali o'zgartirish
harorat.fahrenheyt = 100
print(f"\n100°F ga o'zgartirildi:")
print(f"Selsiy: {harorat.selsiy:.2f}°C")
print(f"Kelvin: {harorat.kelvin:.2f}K")

# Noto'g'ri qiymat kiritish
try:
    harorat.selsiy = -300
except ValueError as e:
    print(f"Xatolik: {e}")
```

### Polimorfizm va abstrakt sinflar

```python
from abc import ABC, abstractmethod
import math

# Abstrakt sinf yaratish
class Shakl(ABC):
    def __init__(self, rang="oq"):
        self.rang = rang
    
    @abstractmethod
    def yuza_hisoblash(self):
        pass
    
    @abstractmethod
    def perimetr_hisoblash(self):
        pass
    
    def ma'lumot(self):
        return f"{self.__class__.__name__} - Rang: {self.rang}"

# Konkret sinflar yaratish
class To'rtburchak(Shakl):
    def __init__(self, uzunlik, kenglik, rang="oq"):
        super().__init__(rang)
        self.uzunlik = uzunlik
        self.kenglik = kenglik
    
    def yuza_hisoblash(self):
        return self.uzunlik * self.kenglik
    
    def perimetr_hisoblash(self):
        return 2 * (self.uzunlik + self.kenglik)

class Aylana(Shakl):
    def __init__(self, radius, rang="oq"):
        super().__init__(rang)
        self.radius = radius
    
    def yuza_hisoblash(self):
        return math.pi * self.radius ** 2
    
    def perimetr_hisoblash(self):
        return 2 * math.pi * self.radius

class Uchburchak(Shakl):
    def __init__(self, a, b, c, rang="oq"):
        super().__init__(rang)
        self.a, self.b, self.c = a, b, c
    
    def yuza_hisoblash(self):
        # Heron formulasi
        s = self.perimetr_hisoblash() / 2
        return math.sqrt(s * (s - self.a) * (s - self.b) * (s - self.c))
    
    def perimetr_hisoblash(self):
        return self.a + self.b + self.c

# Polimorfizm namoyishi
shakllar = [
    To'rtburchak(5, 3, "qizil"),
    Aylana(4, "ko'k"),
    Uchburchak(3, 4, 5, "yashil")
]

print("Shakllar ro'yxati:")
for shakl in shakllar:
    print(f"{shakl.ma'lumot()}")
    print(f"  Yuza: {shakl.yuza_hisoblash():.2f}")
    print(f"  Perimetr: {shakl.perimetr_hisoblash():.2f}")
    print()

# Umumiy yuza hisoblash
umumiy_yuza = sum(shakl.yuza_hisoblash() for shakl in shakllar)
print(f"Barcha shakllarning umumiy yuzasi: {umumiy_yuza:.2f}")
```

---

## 16. Modullar va paketlar

### Modullar bilan ishlash

```python
# matematik_amallar.py moduli yaratish
"""
Bu fayl matematik_amallar.py deb nomlanishi kerak
"""

# matematik_amallar.py fayl mazmuni:
PI = 3.14159

def qo'shish(a, b):
    """Ikkita sonni qo'shish"""
    return a + b

def ayirish(a, b):
    """Ikkita sonni ayirish"""
    return a - b

def ko'paytirish(a, b):
    """Ikkita sonni ko'paytirish"""
    return a * b

def bo'lish(a, b):
    """Ikkita sonni bo'lish"""
    if b != 0:
        return a / b
    else:
        raise ValueError("Nolga bo'lib bo'lmaydi")

def aylana_yuza(radius):
    """Aylana yuzasini hisoblash"""
    return PI * radius ** 2

def faktorial(n):
    """Faktorial hisoblash"""
    if n < 0:
        raise ValueError("Manfiy son uchun faktorial hisoblanmaydi")
    if n <= 1:
        return 1
    result = 1
    for i in range(2, n + 1):
        result *= i
    return result

class Kalkulyator:
    """Oddiy kalkulyator sinfi"""
    
    @staticmethod
    def hisoblash(ifoda):
        """Matn ko'rinishidagi ifodani hisoblash"""
        try:
            return eval(ifoda)
        except:
            return "Noto'g'ri ifoda"

# Agar modul to'g'ridan-to'g'ri ishga tushirilsa
if __name__ == "__main__":
    print("Matematik amallar moduli test qilinmoqda...")
    print(f"5 + 3 = {qo'shish(5, 3)}")
    print(f"10 - 4 = {ayirish(10, 4)}")
    print(f"6 * 7 = {ko'paytirish(6, 7)}")
    print(f"15 / 3 = {bo'lish(15, 3)}")
    print(f"Radius 5 bo'lgan aylana yuza: {aylana_yuza(5)}")
    print(f"5! = {faktorial(5)}")

# Modullarni import qilishning turli usullari
import math
print(f"math.pi = {math.pi}")
print(f"math.sqrt(16) = {math.sqrt(16)}")

from math import sin, cos, tan
print(f"sin(30°) = {sin(math.radians(30))}")

from math import *  # Barcha funksiyalarni import qilish (tavsiya etilmaydi)
print(f"e ning qiymati: {e}")

import math as m  # Alias bilan import qilish
print(f"m.factorial(5) = {m.factorial(5)}")

# datetime moduli bilan ishlash
from datetime import datetime, date, timedelta

hozir = datetime.now()
print(f"Hozirgi sana va vaqt: {hozir}")
print(f"Faqat sana: {date.today()}")

# Sana bilan hisoblash
bir_hafta_keyin = hozir + timedelta(days=7)
print(f"Bir hafta keyin: {bir_hafta_keyin}")

# Sanani formatlash
formatli_sana = hozir.strftime("%Y-yil %B oyining %d-kuni, %H:%M")
print(f"Formatli sana: {formatli_sana}")
```

### Paketlar yaratish

```python
# Paket strukturasi:
# mening_paketim/
# ├── __init__.py
# ├── matematik.py
# ├── matn.py
# └── yordamchi/
#     ├── __init__.py
#     └── utillar.py

# mening_paketim/__init__.py fayl mazmuni:
"""
Mening paketim - turli xil foydali funksiyalar to'plami
"""

__version__ = "1.0.0"
__author__ = "Sizning ismingiz"

# Paketdan import qilinishi kerak bo'lgan asosiy elementlar
from .matematik import *
from .matn import *

# mening_paketim/matematik.py fayl mazmuni:
def katta_topish(*sonlar):
    """Berilgan sonlar ichidan eng kattasini topish"""
    return max(sonlar)

def o'rtacha_hisobla(sonlar):
    """Sonlar ro'yxatining o'rtacha qiymatini hisoblash"""
    return sum(sonlar) / len(sonlar)

def tub_sonmi(n):
    """Sonning tub son ekanligini tekshirish"""
    if n < 2:
        return False
    for i in range(2, int(n**0.5) + 1):
        if n % i == 0:
            return False
    return True

# mening_paketim/matn.py fayl mazmuni:
def so'zlarni_sanash(matn):
    """Matndagi so'zlar sonini hisoblash"""
    return len(matn.split())

def bosh_harflar(matn):
    """Har bir so'zning birinchi harfini katta qilish"""
    return ' '.join(word.capitalize() for word in matn.split())

def teskari_qilish(matn):
    """Matnni teskari qilish"""
    return matn[::-1]

# mening_paketim/yordamchi/__init__.py fayl mazmuni:
from .utillar import *

# mening_paketim/yordamchi/utillar.py fayl mazmuni:
import os
import json

def fayl_o'qish(fayl_yo'li):
    """Faylni o'qish"""
    try:
        with open(fayl_yo'li, 'r', encoding='utf-8') as f:
            return f.read()
    except FileNotFoundError:
        return None

def json_saqlash(ma'lumot, fayl_yo'li):
    """Ma'lumotni JSON formatda saqlash"""
    with open(fayl_yo'li, 'w', encoding='utf-8') as f:
        json.dump(ma'lumot, f, ensure_ascii=False, indent=2)

def papka_yaratish(papka_yo'li):
    """Papka yaratish"""
    os.makedirs(papka_yo'li, exist_ok=True)

# Paketdan foydalanish:
# from mening_paketim import katta_topish, o'rtacha_hisobla
# from mening_paketim.yordamchi import fayl_o'qish

print("Paket strukturasi namoyish etildi")
```

### Mashhur kutubxonalar

```python
# requests kutubxonasi bilan HTTP so'rovlar
try:
    import requests
    
    # GET so'rov
    response = requests.get('https://api.github.com/users/octocat')
    if response.status_code == 200:
        ma'lumot = response.json()
        print(f"GitHub foydalanuvchi: {ma'lumot.get('name', 'Noma\'lum')}")
    else:
        print(f"Xatolik: {response.status_code}")
        
except ImportError:
    print("requests kutubxonasi o'rnatilmagan")

# numpy bilan matematik amallar (agar o'rnatilgan bo'lsa)
try:
    import numpy as np
    
    # Massiv yaratish
    arr = np.array([1, 2, 3, 4, 5])
    print(f"NumPy massiv: {arr}")
    print(f"Kvadratlari: {arr ** 2}")
    print(f"O'rtacha: {np.mean(arr)}")
    
    # 2D massiv
    matrix = np.array([[1, 2], [3, 4]])
    print(f"Matritsa:\n{matrix}")
    print(f"Matritsa determinanti: {np.linalg.det(matrix)}")
    
except ImportError:
    print("numpy kutubxonasi o'rnatilmagan")

# random moduli bilan tasodifiy sonlar
import random

print("\nTasodifiy sonlar:")
print(f"0 dan 10 gacha: {random.randint(0, 10)}")
print(f"0 dan 1 gacha: {random.random()}")

# Ro'yxatdan tasodifiy element
ro'yxat = ["olma", "banan", "apelsin", "uzum"]
print(f"Tasodifiy meva: {random.choice(ro'yxat)}")

# Ro'yxatni aralashtirish
random.shuffle(ro'yxat)
print(f"Aralashtirilgan ro'yxat: {ro'yxat}")

# os moduli bilan operatsion tizim
import os

print(f"\nHozirgi papka: {os.getcwd()}")
print(f"Foydalanuvchi nomi: {os.getenv('USERNAME', 'Noma\'lum')}")
print(f"Operatsion tizim: {os.name}")

# sys moduli bilan tizim ma'lumotlari
import sys

print(f"Python versiyasi: {sys.version}")
print(f"Platforma: {sys.platform}")
```

---

## 17. Ilg'or mavzular

### Dekoratorlar (Decorators)

```python
# Oddiy dekorator
def vaqt_o'lchash(func):
    import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} {end - start:.4f} soniyada bajarildi")
        return result
    return wrapper

@vaqt_o'lchash
def sekin_funksiya():
    import time
    time.sleep(1)
    return "Bajarildi"

sekin_funksiya()

# Parametrli dekorator
def takrorlash(marta):
    def dekorator(func):
        def wrapper(*args, **kwargs):
            for i in range(marta):
                result = func(*args, **kwargs)
            return result
        return wrapper
    return dekorator

@takrorlash(3)
def salomlash(ism):
    print(f"Salom, {ism}!")

salomlash("Ahmad")

# Sinf dekatori
class HisoblagichDekatori:
    def __init__(self, func):
        self.func = func
        self.chaqirilish_soni = 0
    
    def __call__(self, *args, **kwargs):
        self.chaqirilish_soni += 1
        print(f"{self.func.__name__} {self.chaqirilish_soni}-marta chaqirildi")
        return self.func(*args, **kwargs)

@HisoblagichDekatori
def qo'shish(a, b):
    return a + b

print(qo'shish(2, 3))
print(qo'shish(5, 7))
print(qo'shish(1, 9))

# Cache dekoratori
from functools import lru_cache

@lru_cache(maxsize=128)
def fibonachchi(n):
    if n <= 1:
        return n
    return fibonachchi(n-1) + fibonachchi(n-2)

print(f"F(50) = {fibonachchi(50)}")  # Juda tez hisoblanadi
```

### Generator va Iterator

```python
# Generator funksiya
def son_generator(max_qiymat):
    n = 0
    while n < max_qiymat:
        yield n
        n += 1

# Generator dan foydalanish
print("Generator:")
for son in son_generator(5):
    print(son, end=" ")
print()

# Generator expression
kvadratlar = (x**2 for x in range(10))
print("Generator expression:", list(kvadratlar))

# Murakkab generator
def fibonachchi_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b

# Cheksiz generator dan foydalanish
fib_gen = fibonachchi_generator()
print("Birinchi 10 Fibonachchi son:")
for i in range(10):
    print(next(fib_gen), end=" ")
print()

# Iterator sinfi yaratish
class SonIterator:
    def __init__(self, max_qiymat):
        self.max_qiymat = max_qiymat
        self.current = 0
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.current < self.max_qiymat:
            result = self.current
            self.current += 1
            return result
        else:
            raise StopIteration

# Iterator dan foydalanish
print("Iterator:")
for son in SonIterator(5):
    print(son, end=" ")
print()

# Amaliy generator misoli - fayl o'qish
def fayl_qatorlarini_o'qish(fayl_nomi):
    try:
        with open(fayl_nomi, 'r', encoding='utf-8') as fayl:
            for qator in fayl:
                yield qator.strip()
    except FileNotFoundError:
        print(f"Fayl topilmadi: {fayl_nomi}")

# Fayl yaratish va o'qish
with open("test_lines.txt", "w", encoding="utf-8") as f:
    f.write("Birinchi qator\nIkkinchi qator\nUchinchi qator\n")

print("Fayl qatorlari:")
for qator in fayl_qatorlarini_o'qish("test_lines.txt"):
    print(f"- {qator}")
```

### Context Manager

```python
# Context manager sinfi
class FaylBoshqaruvchi:
    def __init__(self, fayl_nomi, rejim):
        self.fayl_nomi = fayl_nomi
        self.rejim = rejim
    
    def __enter__(self):
        print(f"Fayl ochilmoqda: {self.fayl_nomi}")
        self.fayl = open(self.fayl_nomi, self.rejim, encoding='utf-8')
        return self.fayl
    
    def __exit__(self, exc_type, exc_val, exc_tb):
        print(f"Fayl yopilmoqda: {self.fayl_nomi}")
        self.fayl.close()
        if exc_type:
            print(f"Xatolik yuz berdi: {exc_val}")
        return False  # Xatolikni suppress qilmaslik

# Context manager dan foydalanish
with FaylBoshqaruvchi("context_test.txt", "w") as f:
    f.write("Context manager orqali yozilgan matn")

# contextlib bilan context manager yaratish
from contextlib import contextmanager
import time

@contextmanager
def vaqt_o'lchagich():
    print("Vaqt o'lchash boshlandi")
    start = time.time()
    try:
        yield
    finally:
        end = time.time()
        print(f"Vaqt: {end - start:.4f} soniya")

# Vaqt o'lchagich dan foydalanish
with vaqt_o'lchagich():
    sum(range(1000000))
    print("Hisoblash tugadi")

# suppress context manager
from contextlib import suppress

# Xatolikni bekor qilish
with suppress(FileNotFoundError):
    with open("mavjud_emas.txt", "r") as f:
        print(f.read())
print("Fayl topilmasa ham dastur davom etadi")
```

### Metaclass va ilg'or OOP

```python
# Metaclass yaratish
class Singleton(type):
    """Singleton pattern uchun metaclass"""
    _instances = {}
    
    def __call__(cls, *args, **kwargs):
        if cls not in cls._instances:
            cls._instances[cls] = super().__call__(*args, **kwargs)
        return cls._instances[cls]

class MalumotBazasi(metaclass=Singleton):
    def __init__(self):
        self.ulanish_soni = 0
        print("Ma'lumot bazasiga ulanish yaratildi")
    
    def ulanish(self):
        self.ulanish_soni += 1
        print(f"Ulanish #{self.ulanish_soni}")

# Singleton test qilish
db1 = MalumotBazasi()
db2 = MalumotBazasi()

print(f"db1 va db2 bir xil obyektmi: {db1 is db2}")
db1.ulanish()
db2.ulanish()

# Dunder methods (maxsus metodlar)
class Vektor:
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def __str__(self):
        return f"Vektor({self.x}, {self.y})"
    
    def __repr__(self):
        return f"Vektor({self.x!r}, {self.y!r})"
    
    def __add__(self, other):
        return Vektor(self.x + other.x, self.y + other.y)
    
    def __sub__(self, other):
        return Vektor(self.x - other.x, self.y - other.y)
    
    def __mul__(self, scalar):
        return Vektor(self.x * scalar, self.y * scalar)
    
    def __eq__(self, other):
        return self.x == other.x and self.y == other.y
    
    def __len__(self):
        return int((self.x**2 + self.y**2)**0.5)

# Vektor sinfi bilan ishlash
v1 = Vektor(3, 4)
v2 = Vektor(1, 2)

print(f"v1 = {v1}")
print(f"v2 = {v2}")
print(f"v1 + v2 = {v1 + v2}")
print(f"v1 - v2 = {v1 - v2}")
print(f"v1 * 2 = {v1 * 2}")
print(f"v1 == v2: {v1 == v2}")
print(f"len(v1) = {len(v1)}")

# Property va descriptor
class Harorat:
    def __init__(self, value=0):
        self._value = value
    
    def __get__(self, obj, objtype=None):
        return self._value
    
    def __set__(self, obj, value):
        if value < -273.15:
            raise ValueError("Harorat absolute noldan past bo'lishi mumkin emas")
        self._value = value
    
    def __delete__(self, obj):
        del self._value

class Laboratoriya:
    harorat = Harorat()
    
    def __init__(self, nom):
        self.nom = nom

# Descriptor test qilish
lab = Laboratoriya("Fizika laboratoriyasi")
lab.harorat = 25
print(f"{lab.nom} harorat: {lab.harorat}°C")

try:
    lab.harorat = -300  # Xatolik beradi
except ValueError as e:
    print(f"Xatolik: {e}")
```

### Asinxron dasturlash (Asyncio)

```python
import asyncio
import aiohttp
import time

# Oddiy asinxron funksiya
async def salom_asinxron(ism, kutish_vaqti):
    print(f"Salom {ism}, {kutish_vaqti} soniya kutaman...")
    await asyncio.sleep(kutish_vaqti)
    print(f"{ism} uchun kutish tugadi!")
    return f"Bajarildi: {ism}"

# Asinxron funksiyalarni parallel bajarish
async def parallel_ishlar():
    print("Parallel ishlarni boshlash...")
    start_time = time.time()
    
    # Bir vaqtning o'zida bir nechta asinxron funksiyani bajarish
    tasks = [
        salom_asinxron("Ahmad", 2),
        salom_asinxron("Vali", 1),
        salom_asinxron("Guli", 3)
    ]
    
    natijalar = await asyncio.gather(*tasks)
    
    end_time = time.time()
    print(f"Barcha ishlar {end_time - start_time:.2f} soniyada tugadi")
    return natijalar

# Asinxron web so'rovlar (aiohttp kerak)
async def web_sorov(url):
    try:
        async with aiohttp.ClientSession() as session:
            async with session.get(url) as response:
                return await response.text()
    except Exception as e:
        return f"Xatolik: {e}"

async def bir_nechta_sorov():
    urls = [
        "https://httpbin.org/delay/1",
        "https://httpbin.org/delay/2",
        "https://httpbin.org/delay/1"
    ]
    
    print("Web so'rovlarni boshlash...")
    start_time = time.time()
    
    tasks = [web_sorov(url) for url in urls]
    natijalar = await asyncio.gather(*tasks)
    
    end_time = time.time()
    print(f"Barcha so'rovlar {end_time - start_time:.2f} soniyada tugadi")
    
    for i, natija in enumerate(natijalar):
        print(f"So'rov {i+1}: {len(natija) if isinstance(natija, str) else natija} belgi")

# Producer-Consumer pattern
async def producer(queue):
    for i in range(5):
        item = f"element_{i}"
        await queue.put(item)
        print(f"Ishlab chiqarildi: {item}")
        await asyncio.sleep(0.5)

async def consumer(queue, ism):
    while True:
        try:
            item = await asyncio.wait_for(queue.get(), timeout=2.0)
            print(f"{ism} qabul qildi: {item}")
            queue.task_done()
            await asyncio.sleep(1)
        except asyncio.TimeoutError:
            print(f"{ism} kutish vaqti tugadi")
            break

async def producer_consumer_demo():
    queue = asyncio.Queue()
    
    # Producer va consumer larni parallel ishga tushirish
    await asyncio.gather(
        producer(queue),
        consumer(queue, "Iste'molchi_1"),
        consumer(queue, "Iste'molchi_2")
    )

# Asinxron kod ni ishga tushirish
if __name__ == "__main__":
    print("=== Asinxron dasturlash namoyishi ===\n")
    
    # Oddiy parallel ishlar
    asyncio.run(parallel_ishlar())
    
    print("\n" + "="*50 + "\n")
    
    # Producer-Consumer
    asyncio.run(producer_consumer_demo())
    
    # Web so'rovlar (faqat aiohttp o'rnatilgan bo'lsa)
    try:
        import aiohttp
        print("\n" + "="*50 + "\n")
        asyncio.run(bir_nechta_sorov())
    except ImportError:
        print("aiohttp kutubxonasi o'rnatilmagan")
```

### Ma'lumotlar tahlili va vizualizatsiya

```python
# pandas bilan ma'lumotlar tahlili (agar o'rnatilgan bo'lsa)
try:
    import pandas as pd
    import matplotlib.pyplot as plt
    
    # Ma'lumotlar to'plamini yaratish
    ma'lumotlar = {
        'Ism': ['Ahmad', 'Vali', 'Guli', 'Sami', 'Nuri'],
        'Yosh': [25, 30, 28, 35, 22],
        'Maosh': [5000000, 8000000, 6500000, 9500000, 4500000],
        'Shahar': ['Toshkent', 'Samarqand', 'Toshkent', 'Buxoro', 'Toshkent']
    }
    
    df = pd.DataFrame(ma'lumotlar)
    
    print("Ma'lumotlar jadvali:")
    print(df)
    
    print("\nStatistik ma'lumotlar:")
    print(df.describe())
    
    # Guruplash va tahlil
    print("\nShaharlar bo'yicha o'rtacha maosh:")
    print(df.groupby('Shahar')['Maosh'].mean())
    
    # Vizualizatsiya
    plt.figure(figsize=(10, 5))
    
    # Yosh va maosh orasidagi bog'liqlik
    plt.subplot(1, 2, 1)
    plt.scatter(df['Yosh'], df['Maosh'])
    plt.xlabel('Yosh')
    plt.ylabel('Maosh')
    plt.title('Yosh va Maosh bog\'liqlik')
    
    # Shaharlar bo'yicha maosh
    plt.subplot(1, 2, 2)
    shahar_maosh = df.groupby('Shahar')['Maosh'].mean()
    plt.bar(shahar_maosh.index, shahar_maosh.values)
    plt.xlabel('Shahar')
    plt.ylabel('O\'rtacha maosh')
    plt.title('Shaharlar bo\'yicha o\'rtacha maosh')
    plt.xticks(rotation=45)
    
    plt.tight_layout()
    plt.show()
    
except ImportError:
    print("pandas yoki matplotlib kutubxonalari o'rnatilmagan")
    
    # Oddiy statistika funksiyalari
    ma'lumotlar = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    
    def o'rtacha(sonlar):
        return sum(sonlar) / len(sonlar)
    
    def mediana(sonlar):
        sorted_sonlar = sorted(sonlar)
        n = len(sorted_sonlar)
        if n % 2 == 0:
            return (sorted_sonlar[n//2-1] + sorted_sonlar[n//2]) / 2
        else:
            return sorted_sonlar[n//2]
    
    def dispersiya(sonlar):
        ort = o'rtacha(sonlar)
        return sum((x - ort)**2 for x in sonlar) / len(sonlar)
    
    def standart_og'ish(sonlar):
        return dispersiya(sonlar)**0.5
    
    print(f"Ma'lumotlar: {ma'lumotlar}")
    print(f"O'rtacha: {o'rtacha(ma'lumotlar):.2f}")
    print(f"Mediana: {mediana(ma'lumotlar):.2f}")
    print(f"Dispersiya: {dispersiya(ma'lumotlar):.2f}")
    print(f"Standart og'ish: {standart_og'ish(ma'lumotlar):.2f}")

# Machine Learning asoslari (scikit-learn bilan)
try:
    from sklearn.linear_model import LinearRegression
    from sklearn.model_selection import train_test_split
    import numpy as np
    
    # Sun'iy ma'lumotlar yaratish
    np.random.seed(42)
    X = np.random.randn(100, 1) * 10  # mustaqil o'zgaruvchi
    y = 2 * X.flatten() + 3 + np.random.randn(100) * 5  # bog'liq o'zgaruvchi
    
    # Ma'lumotlarni o'qitish va test qismlariga ajratish
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
    
    # Model yaratish va o'qitish
    model = LinearRegression()
    model.fit(X_train, y_train)
    
    # Bashorat qilish
    y_pred = model.predict(X_test)
    
    # Model baholash
    from sklearn.metrics import mean_squared_error, r2_score
    mse = mean_squared_error(y_test, y_pred)
    r2 = r2_score(y_test, y_pred)
    
    print(f"\nLinear Regression modeli:")
    print(f"Koeffitsient: {model.coef_[0]:.2f}")
    print(f"Intercept: {model.intercept_:.2f}")
    print(f"Mean Squared Error: {mse:.2f}")
    print(f"R² Score: {r2:.2f}")
    
    # Bashorat
    yangi_qiymat = [[5.0]]
    bashorat = model.predict(yangi_qiymat)
    print(f"X=5 uchun bashorat: {bashorat[0]:.2f}")
    
except ImportError:
    print("scikit-learn yoki numpy kutubxonalari o'rnatilmagan")

print("\n" + "="*60)
print("Python dasturlash tili bo'yicha to'liq kurs tugadi!")
print("Bu kursda o'rgangan bilimlaringizni amaliyotda qo'llang!")
print("="*60)

---

## 18. Amaliy loyihalar

### 18.1 Oddiy kalkulyator

```python
class Kalkulyator:
    def __init__(self):
        self.tarix = []
    
    def qo'shish(self, a, b):
        natija = a + b
        self.tarix.append(f"{a} + {b} = {natija}")
        return natija
    
    def ayirish(self, a, b):
        natija = a - b
        self.tarix.append(f"{a} - {b} = {natija}")
        return natija
    
    def ko'paytirish(self, a, b):
        natija = a * b
        self.tarix.append(f"{a} × {b} = {natija}")
        return natija
    
    def bo'lish(self, a, b):
        if b == 0:
            raise ValueError("Nolga bo'lib bo'lmaydi!")
        natija = a / b
        self.tarix.append(f"{a} ÷ {b} = {natija}")
        return natija
    
    def daraja(self, a, b):
        natija = a ** b
        self.tarix.append(f"{a} ^ {b} = {natija}")
        return natija
    
    def tarixni_ko'rish(self):
        print("Hisoblash tarixi:")
        for i, amal in enumerate(self.tarix, 1):
            print(f"{i}. {amal}")
    
    def tarixni_tozalash(self):
        self.tarix.clear()
        print("Tarix tozalandi")

def kalkulyator_ishga_tushirish():
    calc = Kalkulyator()
    
    while True:
        print("\n=== KALKULYATOR ===")
        print("1. Qo'shish (+)")
        print("2. Ayirish (-)")
        print("3. Ko'paytirish (×)")
        print("4. Bo'lish (÷)")
        print("5. Daraja (^)")
        print("6. Tarixni ko'rish")
        print("7. Tarixni tozalash")
        print("0. Chiqish")
        
        try:
            tanlov = int(input("\nTanlovingizni kiriting: "))
            
            if tanlov == 0:
                print("Kalkulyator yopildi!")
                break
            elif tanlov in [1, 2, 3, 4, 5]:
                a = float(input("Birinchi sonni kiriting: "))
                b = float(input("Ikkinchi sonni kiriting: "))
                
                if tanlov == 1:
                    print(f"Natija: {calc.qo'shish(a, b)}")
                elif tanlov == 2:
                    print(f"Natija: {calc.ayirish(a, b)}")
                elif tanlov == 3:
                    print(f"Natija: {calc.ko'paytirish(a, b)}")
                elif tanlov == 4:
                    print(f"Natija: {calc.bo'lish(a, b)}")
                elif tanlov == 5:
                    print(f"Natija: {calc.daraja(a, b)}")
            
            elif tanlov == 6:
                calc.tarixni_ko'rish()
            elif tanlov == 7:
                calc.tarixni_tozalash()
            else:
                print("Noto'g'ri tanlov!")
                
        except ValueError as e:
            print(f"Xatolik: {e}")
        except Exception as e:
            print(f"Kutilmagan xatolik: {e}")

# Kalkulyatorni ishga tushirish (test uchun)
print("Kalkulyator dasturi yaratildi. Ishga tushirish uchun kalkulyator_ishga_tushirish() funksiyasini chaqiring.")
```

### 18.2 To-do (Vazifalar) dasturi

```python
import json
from datetime import datetime, timedelta

class VazifaBoshqaruvchi:
    def __init__(self, fayl_nomi="vazifalar.json"):
        self.fayl_nomi = fayl_nomi
        self.vazifalar = self.vazifalarni_yuklash()
    
    def vazifalarni_yuklash(self):
        try:
            with open(self.fayl_nomi, 'r', encoding='utf-8') as f:
                return json.load(f)
        except FileNotFoundError:
            return []
    
    def vazifalarni_saqlash(self):
        with open(self.fayl_nomi, 'w', encoding='utf-8') as f:
            json.dump(self.vazifalar, f, ensure_ascii=False, indent=2)
    
    def vazifa_qo'shish(self, nomi, tavsif="", muddat=None, muhimlik="o'rta"):
        vazifa = {
            "id": len(self.vazifalar) + 1,
            "nomi": nomi,
            "tavsif": tavsif,
            "yaratilgan": datetime.now().strftime("%Y-%m-%d %H:%M:%S"),
            "muddat": muddat,
            "muhimlik": muhimlik,
            "bajarilgan": False,
            "bajarilgan_vaqt": None
        }
        self.vazifalar.append(vazifa)
        self.vazifalarni_saqlash()
        print(f"Vazifa qo'shildi: {nomi}")
    
    def vazifalarni_ko'rish(self, faqat_bajarilmaganlar=True):
        if not self.vazifalar:
            print("Vazifalar yo'q")
            return
        
        print("\n=== VAZIFALAR RO'YXATI ===")
        for vazifa in self.vazifalar:
            if faqat_bajarilmaganlar and vazifa["bajarilgan"]:
                continue
            
            status = "✅" if vazifa["bajarilgan"] else "❌"
            muhimlik_belgi = {"past": "🔵", "o'rta": "🟡", "yuqori": "🔴"}.get(vazifa["muhimlik"], "⚪")
            
            print(f"{status} {muhimlik_belgi} [{vazifa['id']}] {vazifa['nomi']}")
            if vazifa["tavsif"]:
                print(f"    📝 {vazifa['tavsif']}")
            if vazifa["muddat"]:
                print(f"    📅 Muddat: {vazifa['muddat']}")
            if vazifa["bajarilgan"]:
                print(f"    ✅ Bajarilgan: {vazifa['bajarilgan_vaqt']}")
            print()
    
    def vazifa_bajarish(self, vazifa_id):
        for vazifa in self.vazifalar:
            if vazifa["id"] == vazifa_id:
                if vazifa["bajarilgan"]:
                    print("Bu vazifa allaqachon bajarilgan!")
                else:
                    vazifa["bajarilgan"] = True
                    vazifa["bajarilgan_vaqt"] = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
                    self.vazifalarni_saqlash()
                    print(f"Vazifa bajarildi: {vazifa['nomi']}")
                return
        print("Vazifa topilmadi!")
    
    def vazifa_o'chirish(self, vazifa_id):
        for i, vazifa in enumerate(self.vazifalar):
            if vazifa["id"] == vazifa_id:
                o'chirilgan = self.vazifalar.pop(i)
                self.vazifalarni_saqlash()
                print(f"Vazifa o'chirildi: {o'chirilgan['nomi']}")
                return
        print("Vazifa topilmadi!")
    
    def muddati_yaqin_vazifalar(self):
        bugun = datetime.now()
        yaqin_vazifalar = []
        
        for vazifa in self.vazifalar:
            if not vazifa["bajarilgan"] and vazifa["muddat"]:
                try:
                    muddat = datetime.strptime(vazifa["muddat"], "%Y-%m-%d")
                    farq = (muddat - bugun).days
                    if farq <= 3:  # 3 kun ichida
                        yaqin_vazifalar.append((vazifa, farq))
                except ValueError:
                    continue
        
        if yaqin_vazifalar:
            print("\n⚠️  MUDDATI YAQIN VAZIFALAR:")
            for vazifa, farq in sorted(yaqin_vazifalar, key=lambda x: x[1]):
                if farq < 0:
                    print(f"🔴 Kechikkan: {vazifa['nomi']} ({abs(farq)} kun oldin)")
                elif farq == 0:
                    print(f"🟡 Bugun: {vazifa['nomi']}")
                else:
                    print(f"🟠 {farq} kundan keyin: {vazifa['nomi']}")

def vazifa_dasturi():
    vm = VazifaBoshqaruvchi()
    
    while True:
        print("\n=== VAZIFA BOSHQARUVCHI ===")
        print("1. Vazifa qo'shish")
        print("2. Vazifalarni ko'rish")
        print("3. Vazifa bajarish")
        print("4. Vazifa o'chirish")
        print("5. Barcha vazifalarni ko'rish")
        print("6. Muddati yaqin vazifalar")
        print("0. Chiqish")
        
        try:
            tanlov = int(input("\nTanlovingizni kiriting: "))
            
            if tanlov == 0:
                print("Dastur tugadi!")
                break
            
            elif tanlov == 1:
                nomi = input("Vazifa nomi: ").strip()
                if not nomi:
                    print("Vazifa nomi bo'sh bo'lishi mumkin emas!")
                    continue
                
                tavsif = input("Tavsif (ixtiyoriy): ").strip()
                muddat = input("Muddat (YYYY-MM-DD formatda, ixtiyoriy): ").strip()
                
                print("Muhimlik darajasi:")
                print("1. Past")
                print("2. O'rta")
                print("3. Yuqori")
                muhimlik_tanlov = input("Muhimlik (1-3, default 2): ").strip()
                
                muhimlik_map = {"1": "past", "2": "o'rta", "3": "yuqori"}
                muhimlik = muhimlik_map.get(muhimlik_tanlov, "o'rta")
                
                vm.vazifa_qo'shish(nomi, tavsif, muddat if muddat else None, muhimlik)
            
            elif tanlov == 2:
                vm.vazifalarni_ko'rish(True)
            
            elif tanlov == 3:
                vm.vazifalarni_ko'rish(True)
                vazifa_id = int(input("\nBajarilgan vazifa ID raqamini kiriting: "))
                vm.vazifa_bajarish(vazifa_id)
            
            elif tanlov == 4:
                vm.vazifalarni_ko'rish(False)
                vazifa_id = int(input("\nO'chiriladigan vazifa ID raqamini kiriting: "))
                vm.vazifa_o'chirish(vazifa_id)
            
            elif tanlov == 5:
                vm.vazifalarni_ko'rish(False)
            
            elif tanlov == 6:
                vm.muddati_yaqin_vazifalar()
            
            else:
                print("Noto'g'ri tanlov!")
                
        except ValueError:
            print("Noto'g'ri qiymat kiritildi!")
        except Exception as e:
            print(f"Xatolik: {e}")

print("Vazifa boshqaruvchi dasturi yaratildi. Ishga tushirish uchun vazifa_dasturi() funksiyasini chaqiring.")
```

### 18.3 Bank hisobi boshqaruv tizimi

```python
import json
import hashlib
from datetime import datetime
import random

class BankHisob:
    def __init__(self, hisob_raqami, egasi_ismi, pin_kod, balans=0):
        self.hisob_raqami = hisob_raqami
        self.egasi_ismi = egasi_ismi
        self.pin_kod = self._hash_pin(pin_kod)
        self.balans = balans
        self.yaratilgan = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
        self.tranzaksiyalar = []
        self.bloklangan = False
        self.noto'g'ri_pin_urinishlar = 0
    
    def _hash_pin(self, pin):
        return hashlib.sha256(str(pin).encode()).hexdigest()
    
    def pin_tekshirish(self, pin):
        if self.bloklangan:
            return False
        
        if self._hash_pin(pin) == self.pin_kod:
            self.noto'g'ri_pin_urinishlar = 0
            return True
        else:
            self.noto'g'ri_pin_urinishlar += 1
            if self.noto'g'ri_pin_urinishlar >= 3:
                self.bloklangan = True
                self.tranzaksiya_qo'shish("HISOB BLOKLANDI", 0)
            return False
    
    def tranzaksiya_qo'shish(self, turi, miqdor, qoldiq=None):
        tranzaksiya = {
            "vaqt": datetime.now().strftime("%Y-%m-%d %H:%M:%S"),
            "turi": turi,
            "miqdor": miqdor,
            "qoldiq": qoldiq if qoldiq is not None else self.balans
        }
        self.tranzaksiyalar.append(tranzaksiya)
    
    def pul_qo'yish(self, miqdor, pin):
        if not self.pin_tekshirish(pin):
            return False, "Noto'g'ri PIN kod yoki hisob bloklangan!"
        
        if miqdor <= 0:
            return False, "Miqdor musbat bo'lishi kerak!"
        
        self.balans += miqdor
        self.tranzaksiya_qo'shish("DEPOZIT", miqdor)
        return True, f"{miqdor:,.0f} so'm hisobga qo'yildi. Yangi balans: {self.balans:,.0f} so'm"
    
    def pul_yechish(self, miqdor, pin):
        if not self.pin_tekshirish(pin):
            return False, "Noto'g'ri PIN kod yoki hisob bloklangan!"
        
        if miqdor <= 0:
            return False, "Miqdor musbat bo'lishi kerak!"
        
        if miqdor > self.balans:
            return False, f"Yetarli mablag' yo'q! Joriy balans: {self.balans:,.0f} so'm"
        
        self.balans -= miqdor
        self.tranzaksiya_qo'shish("YECHIM", -miqdor)
        return True, f"{miqdor:,.0f} so'm yechildi. Qolgan balans: {self.balans:,.0f} so'm"
    
    def pul_ko'chirish(self, qabul_qiluvchi_hisob, miqdor, pin):
        if not self.pin_tekshirish(pin):
            return False, "Noto'g'ri PIN kod yoki hisob bloklangan!"
        
        if miqdor <= 0:
            return False, "Miqdor musbat bo'lishi kerak!"
        
        if miqdor > self.balans:
            return False, f"Yetarli mablag' yo'q! Joriy balans: {self.balans:,.0f} so'm"
        
        # Ko'chirish amali
        self.balans -= miqdor
        qabul_qiluvchi_hisob.balans += miqdor
        
        # Tranzaksiyalarni qayd qilish
        self.tranzaksiya_qo'shish(f"KO'CHIRISH -> {qabul_qiluvchi_hisob.hisob_raqami}", -miqdor)
        qabul_qiluvchi_hisob.tranzaksiya_qo'shish(f"QABUL <- {self.hisob_raqami}", miqdor)
        
        return True, f"{miqdor:,.0f} so'm {qabul_qiluvchi_hisob.hisob_raqami} hisobiga ko'chirildi"
    
    def balans_ko'rish(self, pin):
        if not self.pin_tekshirish(pin):
            return False, "Noto'g'ri PIN kod yoki hisob bloklangan!"
        
        return True, f"Joriy balans: {self.balans:,.0f} so'm"
    
    def tranzaksiyalar_tarixi(self, pin, oxirgi_n=10):
        if not self.pin_tekshirish(pin):
            return False, "Noto'g'ri PIN kod yoki hisob bloklangan!"
        
        if not self.tranzaksiyalar:
            return True, "Tranzaksiyalar tarixi bo'sh"
        
        oxirgi_tranzaksiyalar = self.tranzaksiyalar[-oxirgi_n:]
        tarix = "=== TRANZAKSIYALAR TARIXI ===\n"
        for tr in reversed(oxirgi_tranzaksiyalar):
            tarix += f"{tr['vaqt']} | {tr['turi']} | {tr['miqdor']:+,.0f} | Qoldiq: {tr['qoldiq']:,.0f}\n"
        
        return True, tarix
    
    def hisobni_bloklash_ochish(self, admin_parol):
        # Bu yerda admin parolini tekshirish kerak
        if admin_parol == "admin123":
            self.bloklangan = False
            self.noto'g'ri_pin_urinishlar = 0
            self.tranzaksiya_qo'shish("HISOB OCHILDI", 0)
            return True
        return False

class Bank:
    def __init__(self, fayl_nomi="bank_hisoblar.json"):
        self.fayl_nomi = fayl_nomi
        self.hisoblar = {}
        self.hisoblarni_yuklash()
    
    def hisob_raqam_yaratish(self):
        while True:
            raqam = f"UZ{''.join([str(random.randint(0, 9)) for _ in range(16)])}"
            if raqam not in self.hisoblar:
                return raqam
    
    def hisoblarni_yuklash(self):
        try:
            with open(self.fayl_nomi, 'r', encoding='utf-8') as f:
                ma'lumotlar = json.load(f)
                for raqam, ma'lumot in ma'lumotlar.items():
                    hisob = BankHisob(
                        ma'lumot['hisob_raqami'],
                        ma'lumot['egasi_ismi'],
                        "dummy_pin"  # PIN hash saqlanadi
                    )
                    # Ma'lumotlarni qayta tiklash
                    hisob.pin_kod = ma'lumot['pin_kod']
                    hisob.balans = ma'lumot['balans']
                    hisob.yaratilgan = ma'lumot['yaratilgan']
                    hisob.tranzaksiyalar = ma'lumot['tranzaksiyalar']
                    hisob.bloklangan = ma'lumot.get('bloklangan', False)
                    hisob.noto'g'ri_pin_urinishlar = ma'lumot.get('noto\'g\'ri_pin_urinishlar', 0)
                    
                    self.hisoblar[raqam] = hisob
        except FileNotFoundError:
            self.hisoblar = {}
    
    def hisoblarni_saqlash(self):
        ma'lumotlar = {}
        for raqam, hisob in self.hisoblar.items():
            ma'lumotlar[raqam] = {
                'hisob_raqami': hisob.hisob_raqami,
                'egasi_ismi': hisob.egasi_ismi,
                'pin_kod': hisob.pin_kod,
                'balans': hisob.balans,
                'yaratilgan': hisob.yaratilgan,
                'tranzaksiyalar': hisob.tranzaksiyalar,
                'bloklangan': hisob.bloklangan,
                'noto\'g\'ri_pin_urinishlar': hisob.noto'g'ri_pin_urinishlar
            }
        
        with open(self.fayl_nomi, 'w', encoding='utf-8') as f:
            json.dump(ma'lumotlar, f, ensure_ascii=False, indent=2)
    
    def hisob_ochish(self, egasi_ismi, pin_kod, boshlang'ich_balans=0):
        if len(str(pin_kod)) != 4:
            return False, "PIN kod 4 xonali bo'lishi kerak!"
        
        hisob_raqami = self.hisob_raqam_yaratish()
        hisob = BankHisob(hisob_raqami, egasi_ismi, pin_kod, boshlang'ich_balans)
        
        if boshlang'ich_balans > 0:
            hisob.tranzaksiya_qo'shish("BOSHLANG'ICH BALANS", boshlang'ich_balans)
        
        self.hisoblar[hisob_raqami] = hisob
        self.hisoblarni_saqlash()
        
        return True, f"Hisob muvaffaqiyatli ochildi!\nHisob raqami: {hisob_raqami}\nEgasi: {egasi_ismi}"
    
    def hisob_topish(self, hisob_raqami):
        return self.hisoblar.get(hisob_raqami)

def bank_dasturi():
    bank = Bank()
    
    while True:
        print("\n" + "="*50)
        print("          MILLIY BANK TIZIMI")
        print("="*50)
        print("1. Yangi hisob ochish")
        print("2. Balansni ko'rish")
        print("3. Pul qo'yish")
        print("4. Pul yechish")
        print("5. Pul ko'chirish")
        print("6. Tranzaksiyalar tarixi")
        print("7. Hisob ma'lumotlari")
        print("0. Chiqish")
        print("="*50)
        
        try:
            tanlov = int(input("Tanlovingizni kiriting: "))
            
            if tanlov == 0:
                print("Milliy Bank tizimidan chiqildi!")
                break
            
            elif tanlov == 1:
                print("\n=== YANGI HISOB OCHISH ===")
                ism = input("To'liq ismingizni kiriting: ").strip()
                if not ism:
                    print("Ism bo'sh bo'lishi mumkin emas!")
                    continue
                
                pin = input("4 xonali PIN kod kiriting: ").strip()
                try:
                    pin = int(pin)
                    if len(str(pin)) != 4:
                        print("PIN kod 4 xonali bo'lishi kerak!")
                        continue
                except ValueError:
                    print("PIN kod faqat raqamlardan iborat bo'lishi kerak!")
                    continue
                
                balans = input("Boshlang'ich balans (ixtiyoriy, default 0): ").strip()
                try:
                    balans = float(balans) if balans else 0
                    if balans < 0:
                        print("Balans manfiy bo'lishi mumkin emas!")
                        continue
                except ValueError:
                    print("Noto'g'ri ID kiritildi!")
            
            elif tanlov == 5:
                print("\n📥 KITOB QAYTARISH:")
                
                # Qarzda bo'lgan kitoblarni ko'rsatish
                qarzda_kitoblar = [k for k in kitobxona.kitoblar.values() if not k.mavjud]
                if not qarzda_kitoblar:
                    print("Qaytarish uchun qarzda kitob yo'q!")
                    continue
                
                print("Qarzda bo'lgan kitoblar:")
                for kitob in qarzda_kitoblar:
                    print(f"ID: {kitob.id} - {kitob.nom} (Qarz oluvchi: {kitob.qarz_oluvchi})")
                
                try:
                    kitob_id = int(input("Qaytariladigan kitob ID sini kiriting: "))
                    muvaffaqiyat, xabar = kitobxona.kitob_qaytarish(kitob_id)
                    print(xabar)
                    
                except ValueError:
                    print("Noto'g'ri ID kiritildi!")
            
            elif tanlov == 6:
                print("\n📋 QARZ TARIXI:")
                if not kitobxona.qarz_tarixi:
                    print("Qarz tarixi bo'sh!")
                else:
                    print(f"Jami {len(kitobxona.qarz_tarixi)} ta yozuv:")
                    for i, qarz in enumerate(reversed(kitobxona.qarz_tarixi[-20:]), 1):  # Oxirgi 20 ta
                        status = "✅ Qaytarilgan" if qarz['holat'] == 'qaytarilgan' else "📖 Qarzda"
                        print(f"{i}. [{status}] {qarz['kitob_nomi']}")
                        print(f"   👤 Qarz oluvchi: {qarz['qarz_oluvchi']}")
                        print(f"   📅 Qarz olingan: {qarz['qarz_olingan_sana']}")
                        print(f"   ⏰ Muddat: {qarz['qaytarish_muddati']}")
                        if qarz['qaytarilgan_sana']:
                            print(f"   ✅ Qaytarilgan: {qarz['qaytarilgan_sana']}")
                        print()
            
            elif tanlov == 7:
                print("\n⚠️ KECHIKKAN KITOBLAR:")
                kechikkan = kitobxona.kechikkan_kitoblar()
                
                if not kechikkan:
                    print("Kechikkan kitob yo'q! 🎉")
                else:
                    print(f"{len(kechikkan)} ta kitob kechikkan:")
                    for kitob, kechikish in kechikkan:
                        print(f"🔴 {kitob.nom}")
                        print(f"   👤 Qarz oluvchi: {kitob.qarz_oluvchi}")
                        print(f"   📅 Muddat edi: {kitob.qaytarish_muddati}")
                        print(f"   ⏰ Kechikish: {kechikish} kun")
                        print()
            
            elif tanlov == 8:
                print(kitobxona.statistika())
            
            else:
                print("Noto'g'ri tanlov!")
        
        except ValueError:
            print("Noto'g'ri qiymat kiritildi!")
        except Exception as e:
            print(f"Xatolik yuz berdi: {e}")

print("Kitobxona boshqaruv tizimi yaratildi. Ishga tushirish uchun kitobxona_dasturi() funksiyasini chaqiring.")
```

---

## 19. Maslahatlar va eng yaxshi amaliyotlar

### 19.1 Kod yozishda eng yaxshi amaliyotlar

```python
# ✅ YAXshi kod yozish tamoyillari

# 1. Ma'noli nomlar ishlatish
def hisobla_oy_maoshi(ish_soatlari, soatlik_maosh):
    """Oylik maoshni hisoblash"""
    return ish_soatlari * soatlik_maosh

# ❌ Yomon nomlar
def calc(h, s):
    return h * s

# 2. Funksiyalarni kichik va aniq vazifali qilish
def fayl_o'qish(fayl_yo'li):
    """Faqat fayl o'qish vazifasini bajaradi"""
    with open(fayl_yo'li, 'r', encoding='utf-8') as f:
        return f.read()

def ma'lumot_qayta_ishlash(matn):
    """Faqat ma'lumot qayta ishlash vazifasini bajaradi"""
    return matn.strip().lower()

# 3. Izohlar va docstring ishlatish
def faktorial(n):
    """
    Berilgan sonning faktorialini hisoblash
    
    Args:
        n (int): Faktorial hisoblanadigan son
    
    Returns:
        int: n ning faktoriali
    
    Raises:
        ValueError: Agar n manfiy son bo'lsa
    
    Example:
        >>> faktorial(5)
        120
    """
    if n < 0:
        raise ValueError("Manfiy son uchun faktorial hisoblanmaydi")
    if n <= 1:
        return 1
    return n * faktorial(n - 1)

# 4. Konstantalar uchun KATTA_HARFLAR ishlatish
MAX_URINISHLAR = 3
DEFAULT_MUDDAT = 30
API_URL = "https://api.example.com"

# 5. List comprehension to'g'ri ishlatish
# ✅ Yaxshi
juft_kvadratlar = [x**2 for x in range(10) if x % 2 == 0]

# ❌ Murakkab bo'lsa, oddiy tsikl ishlatish yaxshi
# Bu o'qish qiyin:
# natija = [process(x) for x in data if condition(x) and other_condition(x)]

# Bu o'qish oson:
natija = []
for x in data:
    if condition(x) and other_condition(x):
        natija.append(process(x))

# 6. Exception handling to'g'ri qo'llash
def xavfsiz_raqam_o'qish(satr):
    """Satrni raqamga aylantirish, xatolik bo'lsa None qaytarish"""
    try:
        return int(satr)
    except ValueError:
        return None

# 7. f-string ishlatish (Python 3.6+)
ism = "Ahmad"
yosh = 25
# ✅ Yaxshi
xabar = f"Salom {ism}, siz {yosh} yoshdasiz"

# ❌ Eski usul
xabar = "Salom {}, siz {} yoshdasiz".format(ism, yosh)
```

### 19.2 Xatoliklardan qochish

```python
# Tez-tez uchraydigan xatoliklar va ularning yechimlari

# 1. Mutable default argumentlar
# ❌ XATO
def ro'yxat_qo'shish(element, ro'yxat=[]):
    ro'yxat.append(element)
    return ro'yxat

# Bu xatolik - bir xil ro'yxat barcha chaqiruvlarda ishlatiladi

# ✅ TO'G'RI
def ro'yxat_qo'shish(element, ro'yxat=None):
    if ro'yxat is None:
        ro'yxat = []
    ro'yxat.append(element)
    return ro'yxat

# 2. Late binding closure
# ❌ XATO
funksiyalar = []
for i in range(5):
    funksiyalar.append(lambda: print(i))

# Barcha funksiyalar 4 ni chop etadi

# ✅ TO'G'RI
funksiyalar = []
for i in range(5):
    funksiyalar.append(lambda x=i: print(x))

# 3. Is vs == 
# ❌ Ehtiyot bo'ling
a = [1, 2, 3]
b = [1, 2, 3]
print(a is b)  # False - turli obyektlar
print(a == b)  # True - qiymatlari bir xil

# ✅ To'g'ri ishlatish
if qiymat is None:  # None uchun 'is' ishlatish
    pass

if son == 0:  # Qiymatlar uchun '==' ishlatish
    pass

# 4. Ro'yxat kopiyasi
# ❌ XATO
asl_ro'yxat = [1, 2, 3]
yangi_ro'yxat = asl_ro'yxat  # Bu kopiya emas, bir xil obyekt!

# ✅ TO'G'RI
yangi_ro'yxat = asl_ro'yxat.copy()  # yoki list(asl_ro'yxat)
yangi_ro'yxat = asl_ro'yxat[:]      # yoki slice

# 5. Dictionary iteration da o'zgartirish
# ❌ XATO
lugat = {'a': 1, 'b': 2, 'c': 3}
for kalit in lugat:
    if lugat[kalit] == 2:
        del lugat[kalit]  # RuntimeError!

# ✅ TO'G'RI
lugat = {'a': 1, 'b': 2, 'c': 3}
o'chiriladigan_kalitlar = []
for kalit in lugat:
    if lugat[kalit] == 2:
        o'chiriladigan_kalitlar.append(kalit)

for kalit in o'chiriladigan_kalitlar:
    del lugat[kalit]

# Yoki dictionary comprehension
lugat = {k: v for k, v in lugat.items() if v != 2}
```

### 19.3 Performance optimizatsiya

```python
import time
from collections import defaultdict, Counter
import sys

# 1. List comprehension vs loop
def performance_test():
    # List comprehension tezroq
    start = time.time()
    kvadratlar1 = [x**2 for x in range(100000)]
    list_comp_time = time.time() - start
    
    # Oddiy tsikl sekinroq
    start = time.time()
    kvadratlar2 = []
    for x in range(100000):
        kvadratlar2.append(x**2)
    loop_time = time.time() - start
    
    print(f"List comprehension: {list_comp_time:.4f}s")
    print(f"Oddiy tsikl: {loop_time:.4f}s")

# 2. Set membership vs List membership
def membership_test():
    ma'lumotlar_ro'yxat = list(range(10000))
    ma'lumotlar_set = set(ma'lumotlar_ro'yxat)
    
    # List da qidirish - sekin
    start = time.time()
    for _ in range(1000):
        9999 in ma'lumotlar_ro'yxat
    list_time = time.time() - start
    
    # Set da qidirish - tez
    start = time.time()
    for _ in range(1000):
        9999 in ma'lumotlar_set
    set_time = time.time() - start
    
    print(f"List membership: {list_time:.4f}s")
    print(f"Set membership: {set_time:.4f}s")

# 3. String concatenation
def string_test():
    # ❌ Sekin usul
    start = time.time()
    natija = ""
    for i in range(1000):
        natija += str(i) + " "
    slow_time = time.time() - start
    
    # ✅ Tez usul
    start = time.time()
    qismlar = []
    for i in range(1000):
        qismlar.append(str(i))
    natija = " ".join(qismlar)
    fast_time = time.time() - start
    
    print(f"String += : {slow_time:.4f}s")
    print(f"Join method: {fast_time:.4f}s")

# 4. Collections modulidan foydalanish
def collections_example():
    # defaultdict - kalit yo'q bo'lsa default qiymat beradi
    sonlar_soni = defaultdict(int)
    matn = "python dasturlash tili"
    
    for harf in matn:
        sonlar_soni[harf] += 1
    
    print("defaultdict:", dict(sonlar_soni))
    
    # Counter - elementlarni sanash uchun
    counter = Counter(matn)
    print("Counter:", counter.most_common(5))

# 5. Generator memory saqlash uchun
def memory_efficient():
    # ❌ Katta ro'yxat - ko'p memory
    katta_ro'yxat = [x**2 for x in range(1000000)]
    print(f"List size: {sys.getsizeof(katta_ro'yxat)} bytes")
    
    # ✅ Generator - kam memory  
    katta_generator = (x**2 for x in range(1000000))
    print(f"Generator size: {sys.getsizeof(katta_generator)} bytes")
    
    # Generator dan foydalanish
    for i, qiymat in enumerate(katta_generator):
        if i >= 5:  # faqat birinchi 5 ta
            break
        print(qiymat)

print("Performance test funksiyalari yaratildi.")
print("Ishlatish: performance_test(), membership_test(), va h.k.")
```

### 19.4 Debugging va testing

```python
import unittest
import logging
from unittest.mock import patch, Mock

# 1. Logging sozlash
logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s - %(name)s - %(levelname)s - %(message)s',
    handlers=[
        logging.FileHandler('debug.log', encoding='utf-8'),
        logging.StreamHandler()
    ]
)

logger = logging.getLogger(__name__)

def debug_misol():
    """Debugging uchun logging ishlatish"""
    logger.debug("Funksiya boshlandi")
    
    try:
        natija = 10 / 2
        logger.info(f"Hisoblash muvaffaqiyatli: {natija}")
        return natija
    except Exception as e:
        logger.error(f"Xatolik yuz berdi: {e}")
        raise

# 2. Unit testing
class MathOperations:
    @staticmethod
    def qo'shish(a, b):
        return a + b
    
    @staticmethod
    def bo'lish(a, b):
        if b == 0:
            raise ValueError("Nolga bo'lib bo'lmaydi")
        return a / b

class TestMathOperations(unittest.TestCase):
    
    def setUp(self):
        """Har bir test oldidan ishlaydi"""
        self.math = MathOperations()
    
    def test_qo'shish(self):
        """Qo'shish funksiyasini test qilish"""
        self.assertEqual(self.math.qo'shish(2, 3), 5)
        self.assertEqual(self.math.qo'shish(-1, 1), 0)
        self.assertEqual(self.math.qo'shish(0, 0), 0)
    
    def test_bo'lish(self):
        """Bo'lish funksiyasini test qilish"""
        self.assertEqual(self.math.bo'lish(10, 2), 5)
        self.assertAlmostEqual(self.math.bo'lish(7, 3), 2.33333, places=4)
    
    def test_bo'lish_nolga(self):
        """Nolga bo'lish xatoligini test qilish"""
        with self.assertRaises(ValueError):
            self.math.bo'lish(10, 0)
    
    def test_bo'lish_xabar(self):
        """Xatolik xabarini tekshirish"""
        with self.assertRaisesRegex(ValueError, "Nolga bo'lib bo'lmaydi"):
            self.math.bo'lish(5, 0)

# 3. Mock ishlatish
class WeatherAPI:
    def get_weather(self, city):
        # Bu yerda haqiqiy API chaqiruvi bo'ladi
        import requests
        response = requests.get(f"https://api.weather.com/{city}")
        return response.json()

class TestWeatherAPI(unittest.TestCase):
    
    @patch('requests.get')
    def test_get_weather(self, mock_get):
        """Mock ishlatib API ni test qilish"""
        # Mock response sozlash
        mock_response = Mock()
        mock_response.json.return_value = {'temperature': 25, 'condition': 'sunny'}
        mock_get.return_value = mock_response
        
        # Test qilish
        api = WeatherAPI()
        result = api.get_weather('Toshkent')
        
        # Tekshirish
        self.assertEqual(result['temperature'], 25)
        self.assertEqual(result['condition'], 'sunny')
        mock_get.assert_called_once_with('https://api.weather.com/Toshkent')

# 4. Assert statements debugging uchun
def assert_misol(yosh):
    """Assert orqali debugging"""
    assert isinstance(yosh, int), f"Yosh int bo'lishi kerak, lekin {type(yosh)} berildi"
    assert yosh >= 0, f"Yosh manfiy bo'lishi mumkin emas: {yosh}"
    assert yosh <= 150, f"Yosh juda katta: {yosh}"
    
    return f"Yosh to'g'ri: {yosh}"

# 5. Profiling - kod tezligini o'lchash
def profiling_misol():
    """Code profiling misoli"""
    import cProfile
    import pstats
    
    def sekin_funksiya():
        time.sleep(0.1)
        return sum(range(100000))
    
    # Profiling ishga tushirish
    profiler = cProfile.Profile()
    profiler.enable()
    
    # Test kod
    for _ in range(5):
        sekin_funksiya()
    
    profiler.disable()
    
    # Natijalarni ko'rish
    stats = pstats.Stats(profiler)
    stats.sort_stats('cumulative')
    stats.print_stats(10)  # Eng sekin 10 ta funksiya

# Test ishga tushirish
def testlarni_ishga_tushirish():
    """Unit testlarni ishga tushirish"""
    unittest.main(argv=[''], exit=False)

print("Testing va debugging funksiyalari yaratildi.")
print("Testlar: testlarni_ishga_tushirish()")
print("Profiling: profiling_misol()")
```

---

## 20. Keyingi qadamlar va resurslar

### 20.1 Python bilan nima qilish mumkin?

```python
# Python ning turli sohalar bo'yicha imkoniyatlari

print("""
🚀 PYTHON BILAN NIMA QILISH MUMKIN?

1. 🌐 WEB DEVELOPMENT
   - Django (to'liq web framework)
   - Flask (yengil web framework) 
   - FastAPI (zamonaviy API yaratish)
   
2. 📊 DATA SCIENCE VA ANALYTICS
   - Pandas (ma'lumotlar tahlili)
   - NumPy (raqamli hisoblashlar)
   - Matplotlib/Seaborn (grafiklar)
   - Jupyter Notebook (interaktiv muhit)
   
3. 🤖 MACHINE LEARNING VA AI
   - scikit-learn (klassik ML)
   - TensorFlow (chuqur o'rganish)
   - PyTorch (neural networks)
   - OpenCV (kompyuter ko'rish)
   
4. 🎮 O'YIN YARATISH
   - Pygame (2D o'yinlar)
   - Panda3D (3D o'yinlar)
   - Arcade (zamonaviy 2D o'yinlar)
   
5. 🖥️ DESKTOP APPLICATIONS
   - Tkinter (standart GUI)
   - PyQt/PySide (professional GUI)
   - Kivy (cross-platform apps)
   
6. 📱 MOBILE DEVELOPMENT
   - Kivy (Android/iOS)
   - BeeWare (native mobile apps)
   
7. 🔧 AUTOMATION VA SCRIPTING
   - Selenium (web automation)
   - BeautifulSoup (web scraping)
   - Requests (HTTP so'rovlar)
   
8. 🧪 SCIENTIFIC COMPUTING
   - SciPy (ilmiy hisoblashlar)
   - SymPy (matematik formulalar)
   - Biopython (bioinformatika)
   
9. ☁️ CLOUD VA DEVOPS
   - Boto3 (AWS)
   - Docker SDK
   - Kubernetes client
   
10. 🔒 CYBERSECURITY
    - Scapy (network analysis)
    - Cryptography (shifrlash)
    - Penetration testing tools
""")
```

### 20.2 O'rganish resurslari

```python
print("""
📚 O'RGANISH RESURSLARI:

🌐 ONLAYN KURSLAR:
- Python.org (rasmiy sayt)
- Real Python (professional maqolalar)
- Codecademy Python kursi
- Coursera Python kurslari
- edX Python kurslari

📖 KITOBLAR:
- "Python Crash Course" - Eric Matthes
- "Learn Python the Hard Way" - Zed Shaw
- "Fluent Python" - Luciano Ramalho
- "Python Tricks" - Dan Bader

🎯 AMALIYOT UCHUN:
- LeetCode (algoritm masalalari)
- HackerRank (programming challenges)
- Codewars (kata masalalari)
- Project Euler (matematik masalalar)

👥 HAMJAMIYAT:
- Stack Overflow (savol-javob)
- Reddit r/Python
- Python Discord server
- Local Python meetup groups

🔧 MUHIM KUTUBXONALAR:
- requests (HTTP)
- beautifulsoup4 (web scraping)
- pandas (data analysis)  
- numpy (numerical computing)
- matplotlib (plotting)
- flask/django (web frameworks)
- selenium (web automation)
- pillow (image processing)
""")
```

### 20.3 Loyihalar g'oyalari

```python
print("""
💡 LOYIHA G'OYALARI:

🔰 BOSHLANG'ICH DARAJA:
1. Parol generatori
2. URL qisqartiruvchi
3. To-do dasturi
4. Hisob-kitob kalkulyatori
5. Fayl tashkilotchisi

🔸 O'RTA DARAJA:
6. Web scraper (yangiliklar)
7. Email yuboruvchi
8. PDF bilan ishlovchi
9. Excel ma'lumotlarini tahlil qiluvchi
10. API yaratish (REST)

🔷 ILGOR DARAJA:
11. Chatbot
12. Ma'lumotlar vizualizatsiyasi
13. Machine learning modeli
14. Web dastur (Django/Flask)
15. Kriptovalyuta tracker

🎯 REAL LOYIHALAR:
16. Inventar boshqaruv tizimi
17. Student boshqaruv tizimi  
18. E-commerce backend
19. Social media analytics
20. IoT ma'lumotlar tahlilchisi

💼 PORTFOLIO UCHUN:
- GitHub repository yarating
- README.md fayl yozing
- Kod izohlarini qo'shing
- Test yozing
- Documentation tayyorlang
""")
```

### 20.4 Karyera yo'nalishlari

```python
print("""
💼 PYTHON BILAN KARYERA YO'NALISHLARI:

👨‍💻 BACKEND DEVELOPER
- Web API yaratish
- Ma'lumotlar bazasi bilan ishlash
- Serverlar va cloud xizmatlari
- Ish haqi: $50,000-$120,000/yil

📊 DATA SCIENTIST
- Ma'lumotlar tahlili
- Machine learning modellari
- Business intelligence
- Ish haqi: $70,000-$150,000/yil

🤖 ML ENGINEER
- AI modellari ishlab chiqish
- Production ga deploy qilish
- Model optimization
- Ish haqi: $80,000-$180,000/yil

🔧 DEVOPS ENGINEER  
- Infrastructure automation
- CI/CD pipelines
- Cloud services
- Ish haqi: $60,000-$140,000/yil

🧪 QA AUTOMATION ENGINEER
- Test automation
- Performance testing
- Bug tracking
- Ish haqi: $45,000-$100,000/yil

🌐 FULL-STACK DEVELOPER
- Frontend + Backend
- Database design
- User experience
- Ish haqi: $55,000-$130,000/yil

🛡️ SECURITY ANALYST
- Penetration testing
- Vulnerability assessment
- Security automation
- Ish haqi: $65,000-$140,000/yil

TAVSIYALAR:
✅ Portfolio yarating
✅ Open source loyihalarda ishtirok eting
✅ Networking qiling
✅ Doimiy o'rganing
✅ Certifications oling
""")
```

---

## 21. Xulosa

```python
def kurs_xulosasi():
    print("""
    🎉 TABRIKLAYMIZ! 🎉
    
    Siz Python dasturlash tili bo'yicha to'liq kursni muvaffaqiyatli 
    yakunladingiz! Endi sizda quyidagi bilimlar bor:
    
    ✅ Python asoslari va sintaksisi
    ✅ Ma'lumot turlari va strukturalari  
    ✅ Funksiyalar va modullar
    ✅ Obyektga yo'naltirilgan dasturlash
    ✅ Fayllar bilan ishlash
    ✅ Xatoliklar bilan ishlash
    ✅ Ilg'or mavzular (decorators, generators, asyncio)
    ✅ Amaliy loyihalar yaratish
    ✅ Eng yaxshi amaliyotlar
    
    🚀 KEYINGI QADAMLAR:
    
    1. Har kuni kod yozing
    2. GitHub da loyihalar yarating
    3. Boshqa Python dasturchilari bilan muloqot qiling
    4. Doimiy ravishda yangi texnologiyalarni o'rganing
    5. Real loyihalarda ishtirok eting
    
    🎯 UNUTMANG:
    "Eng yaxshi dasturchi - bu doimiy o'rganuvchi dasturchi!"
    
    Omad tilaymiz va katta muvaffaqiyatlarga erishing! 💪
    """)

# Kursni yakunlash
kurs_xulosasi()

print("\n" + "="*70)
print("          🐍 PYTHON DASTURLASH KURSI TUGALLANDI 🐍")
print("="*70)
print("Muallif: Claude AI")
print("Tayyorlangan: 2024")
print("Maqsad: Python tilini noldan professional darajagacha o'rgatish")
print("="*70)
            
            elif tanlov == 5:
                print("\n📥 KITOB QAYTARISH:")
                
                # Qarzda bo'lgan kitoblarni ko'rsatish
                qarzda_kitoblar = [k for k in kitobxona.kitoblar.values() if not k.mavjud]
                if not qarzda_kitoblar:
                    print("Qaytarish uchun qarzda kitob yo'q!")
                    continue
                
                print("Qarzda bo'lgan kitoblar:")
                for kitob in qarzda_kitoblar:
                    print(f"ID: {kitob.id} - {kitob.nom} (Qarz oluvchi: {kitob.qarz_oluvchi})")
                
                try:
                    kitob_id = int(input("Qaytariladigan kitob ID sini kiriting: "))
                    muvaffaqiyat, xabar = kitobxona.kitob_qaytarish(kitob_id)
                    print(xabar)
                    
                except ValueError:
                    print("Noto'g'ri ID kiritildi!")
            
            elif tanlov == 6:
                print("\n📋 QARZ TARIXI:")
                if not kitobxona.qarz_tarixi:
                    print("Qarz tarixi bo'sh!")
                else:
                    print(f"Jami {len(kitobxona.qarz_tarixi)} ta yozuv:")
                    for i, qarz in enumerate(reversed(kitobxona.qarz_tarixi[-20:]), 1):  # Oxirgi 20 ta
                        status = "✅ Qaytarilgan" if qarz['holat'] == 'qaytarilgan' else "📖 Qarzda"
                        print(f"{i}. [{status}] {qarz['kitob_nomi']}")
                        print(f"   👤 Qarz oluvchi: {qarz['qarz_oluvchi']}")
                        print(f"   📅 Qarz olingan: {qarz['qarz_olingan_sana']}")
                        print(f"   ⏰ Muddat: {qarz['qaytarish_muddati']}")
                        if qarz['qaytarilgan_sana']:
                            print(f"   ✅ Qaytarilgan: {qarz['qaytarilgan_sana']}")
                        print()
            
            elif tanlov == 7:
                print("\n⚠️ KECHIKKAN KITOBLAR:")
                kechikkan = kitobxona.kechikkan_kitoblar()
                
                if not kechikkan:
                    print("Kechikkan kitob yo'q! 🎉")
                else:
                    print(f"{len(kechikkan)} ta kitob kechikkan:")
                    for kitob, kechikish in kechikkan:
                        print(f"🔴 {kitob.nom}")
                        print(f"   👤 Qarz oluvchi: {kitob.qarz_oluvchi}")
                        print(f"   📅 Muddat edi: {kitob.qaytarish_muddati}")
                        print(f"   ⏰ Kechikish: {kechikish} kun")
                        print()
            
            elif tanlov == 8:
                print(kitobxona.statistika())
            
            else:
                print("Noto'g'ri tanlov!")
        
        except ValueError:
            print("Noto'g'ri qiymat kiritildi!")
        except Exception as e:
            print(f"Xatolik yuz berdi: {e}")

print("Kitobxona boshqaruv tizimi yaratildi. Ishga tushirish uchun kitobxona_dasturi() funksiyasini chaqiring.")
```

---

## 19. Maslahatlar va eng yaxshi amaliyotlar

### 19.1 Kod yozishda eng yaxshi amaliyotlar

```python
# ✅ YAXshi kod yozish tamoyillari

# 1. Ma'noli nomlar ishlatish
def hisobla_oy_maoshi(ish_soatlari, soatlik_maosh):
    """Oylik maoshni hisoblash"""
    return ish_soatlari * soatlik_maosh

# ❌ Yomon nomlar
def calc(h, s):
    return h * s

# 2. Funksiyalarni kichik va aniq vazifali qilish
def fayl_o'qish(fayl_yo'li):
    """Faqat fayl o'qish vazifasini bajaradi"""
    with open(fayl_yo'li, 'r', encoding='utf-8') as f:
        return f.read()

def ma'lumot_qayta_ishlash(matn):
    """Faqat ma'lumot qayta ishlash vazifasini bajaradi"""
    return matn.strip().lower()

# 3. Izohlar va docstring ishlatish
def faktorial(n):
    """
    Berilgan sonning faktorialini hisoblash
    
    Args:
        n (int): Faktorial hisoblanadigan son
    
    Returns:
        int: n ning faktoriali
    
    Raises:
        ValueError: Agar n manfiy son bo'lsa
    
    Example:
        >>> faktorial(5)
        120
    """
    if n < 0:
        raise ValueError("Manfiy son uchun faktorial hisoblanmaydi")
    if n <= 1:
        return 1
    return n * faktorial(n - 1)

# 4. Konstantalar uchun KATTA_HARFLAR ishlatish
MAX_URINISHLAR = 3
DEFAULT_MUDDAT = 30
API_URL = "https://api.example.com"

# 5. List comprehension to'g'ri ishlatish
# ✅ Yaxshi
juft_kvadratlar = [x**2 for x in range(10) if x % 2 == 0]

# ❌ Murakkab bo'lsa, oddiy tsikl ishlatish yaxshi
# Bu o'qish qiyin:
# natija = [process(x) for x in data if condition(x) and other_condition(x)]

# Bu o'qish oson:
natija = []
for x in data:
    if condition(x) and other_condition(x):
        natija.append(process(x))

# 6. Exception handling to'g'ri qo'llash
def xavfsiz_raqam_o'qish(satr):
    """Satrni raqamga aylantirish, xatolik bo'lsa None qaytarish"""
    try:
        return int(satr)
    except ValueError:
        return None

# 7. f-string ishlatish (Python 3.6+)
ism = "Ahmad"
yosh = 25
# ✅ Yaxshi
xabar = f"Salom {ism}, siz {yosh} yoshdasiz"

# ❌ Eski usul
xabar = "Salom {}, siz {} yoshdasiz".format(ism, yosh)
```

### 19.2 Xatoliklardan qochish

```python
# Tez-tez uchraydigan xatoliklar va ularning yechimlari

# 1. Mutable default argumentlar
# ❌ XATO
def ro'yxat_qo'shish(element, ro'yxat=[]):
    ro'yxat.append(element)
    return ro'yxat

# Bu xatolik - bir xil ro'yxat barcha chaqiruvlarda ishlatiladi

# ✅ TO'G'RI
def ro'yxat_qo'shish(element, ro'yxat=None):
    if ro'yxat is None:
        ro'yxat = []
    ro'yxat.append(element)
    return ro'yxat

# 2. Late binding closure
# ❌ XATO
funksiyalar = []
for i in range(5):
    funksiyalar.append(lambda: print(i))

# Barcha funksiyalar 4 ni chop etadi

# ✅ TO'G'RI
funksiyalar = []
for i in range(5):
    funksiyalar.append(lambda x=i: print(x))

# 3. Is vs == 
# ❌ Ehtiyot bo'ling
a = [1, 2, 3]
b = [1, 2, 3]
print(a is b)  # False - turli obyektlar
print(a == b)  # True - qiymatlari bir xil

# ✅ To'g'ri ishlatish
if qiymat is None:  # None uchun 'is' ishlatish
    pass

if son == 0:  # Qiymatlar uchun '==' ishlatish
    pass

# 4. Ro'yxat kopiyasi
# ❌ XATO
asl_ro'yxat = [1, 2, 3]
yangi_ro'yxat = asl_ro'yxat  # Bu kopiya emas, bir xil obyekt!

# ✅ TO'G'RI
yangi_ro'yxat = asl_ro'yxat.copy()  # yoki list(asl_ro'yxat)
yangi_ro'yxat = asl_ro'yxat[:]      # yoki slice

# 5. Dictionary iteration da o'zgartirish
# ❌ XATO
lugat = {'a': 1, 'b': 2, 'c': 3}
for kalit in lugat:
    if lugat[kalit] == 2:
        del lugat[kalit]  # RuntimeError!

# ✅ TO'G'RI
lugat = {'a': 1, 'b': 2, 'c': 3}
o'chiriladigan_kalitlar = []
for kalit in lugat:
    if lugat[kalit] == 2:
        o'chiriladigan_kalitlar.append(kalit)

for kalit in o'chiriladigan_kalitlar:
    del lugat[kalit]

# Yoki dictionary comprehension
lugat = {k: v for k, v in lugat.items() if v != 2}
```

### 19.3 Performance optimizatsiya

```python
import time
from collections import defaultdict, Counter
import sys

# 1. List comprehension vs loop
def performance_test():
    # List comprehension tezroq
    start = time.time()
    kvadratlar1 = [x**2 for x in range(100000)]
    list_comp_time = time.time() - start
    
    # Oddiy tsikl sekinroq
    start = time.time()
    kvadratlar2 = []
    for x in range(100000):
        kvadratlar2.append(x**2)
    loop_time = time.time() - start
    
    print(f"List comprehension: {list_comp_time:.4f}s")
    print(f"Oddiy tsikl: {loop_time:.4f}s")

# 2. Set membership vs List membership
def membership_test():
    ma'lumotlar_ro'yxat = list(range(10000))
    ma'lumotlar_set = set(ma'lumotlar_ro'yxat)
    
    # List da qidirish - sekin
    start = time.time()
    for _ in range(1000):
        9999 in ma'lumotlar_ro'yxat
    list_time = time.time() - start
    
    # Set da qidirish - tez
    start = time.time()
    for _ in range(1000):
        9999 in ma'lumotlar_set
    set_time = time.time() - start
    
    print(f"List membership: {list_time:.4f}s")
    print(f"Set membership: {set_time:.4f}s")

# 3. String concatenation
def string_test():
    # ❌ Sekin usul
    start = time.time()
    natija = ""
    for i in range(1000):
        natija += str(i) + " "
    slow_time = time.time() - start
    
    # ✅ Tez usul
    start = time.time()
    qismlar = []
    for i in range(1000):
        qismlar.append(str(i))
    natija = " ".join(qismlar)
    fast_time = time.time() - start
    
    print(f"String += : {slow_time:.4f}s")
    print(f"Join method: {fast_time:.4f}s")

# 4. Collections modulidan foydalanish
def collections_example():
    # defaultdict - kalit yo'q bo'lsa default qiymat beradi
    sonlar_soni = defaultdict(int)
    matn = "python dasturlash tili"
    
    for harf in matn:
        sonlar_soni[harf] += 1
    
    print("defaultdict:", dict(sonlar_soni))
    
    # Counter - elementlarni sanash uchun
    counter = Counter(matn)
    print("Counter:", counter.most_common(5))

# 5. Generator memory saqlash uchun
def memory_efficient():
    # ❌ Katta ro'yxat - ko'p memory
    katta_ro'yxat = [x**2 for x in range(1000000)]
    print(f"List size: {sys.getsizeof(katta_ro'yxat)} bytes")
    
    # ✅ Generator - kam memory  
    katta_generator = (x**2 for x in range(1000000))
    print(f"Generator size: {sys.getsizeof(katta_generator)} bytes")
    
    # Generator dan foydalanish
    for i, qiymat in enumerate(katta_generator):
        if i >= 5:  # faqat birinchi 5 ta
            break
        print(qiymat)

print("Performance test funksiyalari yaratildi.")
print("Ishlatish: performance_test(), membership_test(), va h.k.")
```

### 19.4 Debugging va testing

```python
import unittest
import logging
from unittest.mock import patch, Mock

# 1. Logging sozlash
logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s - %(name)s - %(levelname)s - %(message)s',
    handlers=[
        logging.FileHandler('debug.log', encoding='utf-8'),
        logging.StreamHandler()
    ]
)

logger = logging.getLogger(__name__)

def debug_misol():
    """Debugging uchun logging ishlatish"""
    logger.debug("Funksiya boshlandi")
    
    try:
        natija = 10 / 2
        logger.info(f"Hisoblash muvaffaqiyatli: {natija}")
        return natija
    except Exception as e:
        logger.error(f"Xatolik yuz berdi: {e}")
        raise

# 2. Unit testing
class MathOperations:
    @staticmethod
    def qo'shish(a, b):
        return a + b
    
    @staticmethod
    def bo'lish(a, b):
        if b == 0:
            raise ValueError("Nolga bo'lib bo'lmaydi")
        return a / b

class TestMathOperations(unittest.TestCase):
    
    def setUp(self):
        """Har bir test oldidan ishlaydi"""
        self.math = MathOperations()
    
    def test_qo'shish(self):
        """Qo'shish funksiyasini test qilish"""
        self.assertEqual(self.math.qo'shish(2, 3), 5)
        self.assertEqual(self.math.qo'shish(-1, 1), 0)
        self.assertEqual(self.math.qo'shish(0, 0), 0)
    
    def test_bo'lish(self):
        """Bo'lish funksiyasini test qilish"""
        self.assertEqual(self.math.bo'lish(10, 2), 5)
        self.assertAlmostEqual(self.math.bo'lish(7, 3), 2.33333, places=4)
    
    def test_bo'lish_nolga(self):
        """Nolga bo'lish xatoligini test qilish"""
        with self.assertRaises(ValueError):
            self.math.bo'lish(10, 0)
    
    def test_bo'lish_xabar(self):
        """Xatolik xabarini tekshirish"""
        with self.assertRaisesRegex(ValueError, "Nolga bo'lib bo'lmaydi"):
            self.math.bo'lish(5, 0)

# 3. Mock ishlatish
class WeatherAPI:
    def get_weather(self, city):
        # Bu yerda haqiqiy API chaqiruvi bo'ladi
        import requests
        response = requests.get(f"https://api.weather.com/{city}")
        return response.json()

class TestWeatherAPI(unittest.TestCase):
    
    @patch('requests.get')
    def test_get_weather(self, mock_get):
        """Mock ishlatib API ni test qilish"""
        # Mock response sozlash
        mock_response = Mock()
        mock_response.json.return_value = {'temperature': 25, 'condition': 'sunny'}
        mock_get.return_value = mock_response
        
        # Test qilish
        api = WeatherAPI()
        result = api.get_weather('Toshkent')
        
        # Tekshirish
        self.assertEqual(result['temperature'], 25)
        self.assertEqual(result['condition'], 'sunny')
        mock_get.assert_called_once_with('https://api.weather.com/Toshkent')

# 4. Assert statements debugging uchun
def assert_misol(yosh):
    """Assert orqali debugging"""
    assert isinstance(yosh, int), f"Yosh int bo'lishi kerak, lekin {type(yosh)} berildi"
    assert yosh >= 0, f"Yosh manfiy bo'lishi mumkin emas: {yosh}"
    assert yosh <= 150, f"Yosh juda katta: {yosh}"
    
    return f"Yosh to'g'ri: {yosh}"

# 5. Profiling - kod tezligini o'lchash
def profiling_misol():
    """Code profiling misoli"""
    import cProfile
    import pstats
    
    def sekin_funksiya():
        time.sleep(0.1)
        return sum(range(100000))
    
    # Profiling ishga tushirish
    profiler = cProfile.Profile()
    profiler.enable()
    
    # Test kod
    for _ in range(5):
        sekin_funksiya()
    
    profiler.disable()
    
    # Natijalarni ko'rish
    stats = pstats.Stats(profiler)
    stats.sort_stats('cumulative')
    stats.print_stats(10)  # Eng sekin 10 ta funksiya

# Test ishga tushirish
def testlarni_ishga_tushirish():
    """Unit testlarni ishga tushirish"""
    unittest.main(argv=[''], exit=False)

print("Testing va debugging funksiyalari yaratildi.")
print("Testlar: testlarni_ishga_tushirish()")
print("Profiling: profiling_misol()")
```

---

## 20. Keyingi qadamlar va resurslar

### 20.1 Python bilan nima qilish mumkin?

```python
# Python ning turli sohalar bo'yicha imkoniyatlari

print("""
🚀 PYTHON BILAN NIMA QILISH MUMKIN?

1. 🌐 WEB DEVELOPMENT
   - Django (to'liq web framework)
   - Flask (yengil web framework) 
   - FastAPI (zamonaviy API yaratish)
   
2. 📊 DATA SCIENCE VA ANALYTICS
   - Pandas (ma'lumotlar tahlili)
   - NumPy (raqamli hisoblashlar)
   - Matplotlib/Seaborn (grafiklar)
   - Jupyter Notebook (interaktiv muhit)
   
3. 🤖 MACHINE LEARNING VA AI
   - scikit-learn (klassik ML)
   - TensorFlow (chuqur o'rganish)
   - PyTorch (neural networks)
   - OpenCV (kompyuter ko'rish)
   
4. 🎮 O'YIN YARATISH
   - Pygame (2D o'yinlar)
   - Panda3D (3D o'yinlar)
   - Arcade (zamonaviy 2D o'yinlar)
   
5. 🖥️ DESKTOP APPLICATIONS
   - Tkinter (standart GUI)
   - PyQt/PySide (professional GUI)
   - Kivy (cross-platform apps)
   
6. 📱 MOBILE DEVELOPMENT
   - Kivy (Android/iOS)
   - BeeWare (native mobile apps)
   
7. 🔧 AUTOMATION VA SCRIPTING
   - Selenium (web automation)
   - BeautifulSoup (web scraping)
   - Requests (HTTP so'rovlar)
   
8. 🧪 SCIENTIFIC COMPUTING
   - SciPy (ilmiy hisoblashlar)
   - SymPy (matematik formulalar)
   - Biopython (bioinformatika)
   
9. ☁️ CLOUD VA DEVOPS
   - Boto3 (AWS)
   - Docker SDK
   - Kubernetes client
   
10. 🔒 CYBERSECURITY
    - Scapy (network analysis)
    - Cryptography (shifrlash)
    - Penetration testing tools
""")
```

### 20.2 O'rganish resurslari

```python
print("""
📚 O'RGANISH RESURSLARI:

🌐 ONLAYN KURSLAR:
- Python.org (rasmiy sayt)
- Real Python (professional maqolalar)
- Codecademy Python kursi
- Coursera Python kurslari
- edX Python kurslari

📖 KITOBLAR:
- "Python Crash Course" - Eric Matthes
- "Learn Python the Hard Way" - Zed Shaw
- "Fluent Python" - Luciano Ramalho
- "Python Tricks" - Dan Bader

🎯 AMALIYOT UCHUN:
- LeetCode (algoritm masalalari)
- HackerRank (programming challenges)
- Codewars (kata masalalari)
- Project Euler (matematik masalalar)

👥 HAMJAMIYAT:
- Stack Overflow (savol-javob)
- Reddit r/Python
- Python Discord server
- Local Python meetup groups

🔧 MUHIM KUTUBXONALAR:
- requests (HTTP)
- beautifulsoup4 (web scraping)
- pandas (data analysis)  
- numpy (numerical computing)
- matplotlib (plotting)
- flask/django (web frameworks)
- selenium (web automation)
- pillow (image processing)
""")
```

### 20.3 Loyihalar g'oyalari

```python
print("""
💡 LOYIHA G'OYALARI:

🔰 BOSHLANG'ICH DARAJA:
1. Parol generatori
2. URL qisqartiruvchi
3. To-do dasturi
4. Hisob-kitob kalkulyatori
5. Fayl tashkilotchisi

🔸 O'RTA DARAJA:
6. Web scraper (yangiliklar)
7. Email yuboruvchi
8. PDF bilan ishlovchi
9. Excel ma'lumotlarini tahlil qiluvchi
10. API yaratish (REST)

🔷 ILGOR DARAJA:
11. Chatbot
12. Ma'lumotlar vizualizatsiyasi
13. Machine learning modeli
14. Web dastur (Django/Flask)
15. Kriptovalyuta tracker

🎯 REAL LOYIHALAR:
16. Inventar boshqaruv tizimi
17. Student boshqaruv tizimi  
18. E-commerce backend
19. Social media analytics
20. IoT ma'lumotlar tahlilchisi

💼 PORTFOLIO UCHUN:
- GitHub repository yarating
- README.md fayl yozing
- Kod izohlarini qo'shing
- Test yozing
- Documentation tayyorlang
""")
```

### 20.4 Karyera yo'nalishlari

```python
print("""
💼 PYTHON BILAN KARYERA YO'NALISHLARI:

👨‍💻 BACKEND DEVELOPER
- Web API yaratish
- Ma'lumotlar bazasi bilan ishlash
- Serverlar va cloud xizmatlari
- Ish haqi: $50,000-$120,000/yil

📊 DATA SCIENTIST
- Ma'lumotlar tahlili
- Machine learning modellari
- Business intelligence
- Ish haqi: $70,000-$150,000/yil

🤖 ML ENGINEER
- AI modellari ishlab chiqish
- Production ga deploy qilish
- Model optimization
- Ish haqi: $80,000-$180,000/yil

🔧 DEVOPS ENGINEER  
- Infrastructure automation
- CI/CD pipelines
- Cloud services
- Ish haqi: $60,000-$140,000/yil

🧪 QA AUTOMATION ENGINEER
- Test automation
- Performance testing
- Bug tracking
- Ish haqi: $45,000-$100,000/yil

🌐 FULL-STACK DEVELOPER
- Frontend + Backend
- Database design
- User experience
- Ish haqi: $55,000-$130,000/yil

🛡️ SECURITY ANALYST
- Penetration testing
- Vulnerability assessment
- Security automation
- Ish haqi: $65,000-$140,000/yil

TAVSIYALAR:
✅ Portfolio yarating
✅ Open source loyihalarda ishtirok eting
✅ Networking qiling
✅ Doimiy o'rganing
✅ Certifications oling
""")
```

---

## 21. Xulosa

```python
def kurs_xulosasi():
    print("""
    🎉 TABRIKLAYMIZ! 🎉
    
    Siz Python dasturlash tili bo'yicha to'liq kursni muvaffaqiyatli 
    yakunladingiz! Endi sizda quyidagi bilimlar bor:
    
    ✅ Python asoslari va sintaksisi
    ✅ Ma'lumot turlari va strukturalari  
    ✅ Funksiyalar va modullar
    ✅ Obyektga yo'naltirilgan dasturlash
    ✅ Fayllar bilan ishlash
    ✅ Xatoliklar bilan ishlash
    ✅ Ilg'or mavzular (decorators, generators, asyncio)
    ✅ Amaliy loyihalar yaratish
    ✅ Eng yaxshi amaliyotlar
    
    🚀 KEYINGI QADAMLAR:
    
    1. Har kuni kod yozing
    2. GitHub da loyihalar yarating
    3. Boshqa Python dasturchilari bilan muloqot qiling
    4. Doimiy ravishda yangi texnologiyalarni o'rganing
    5. Real loyihalarda ishtirok eting
    
    🎯 UNUTMANG:
    "Eng yaxshi dasturchi - bu doimiy o'rganuvchi dasturchi!"
    
    Omad tilaymiz va katta muvaffaqiyatlarga erishing! 💪
    """)

# Kursni yakunlash
kurs_xulosasi()

print("\n" + "="*70)
print("          🐍 PYTHON DASTURLASH KURSI TUGALLANDI 🐍")
print("="*70)
print("Muallif: Claude AI")
print("Tayyorlangan: 2024")
print("Maqsad: Python tilini noldan professional darajagacha o'rgatish")
print("="*70)
```

Bu to'liq kurs sizga Python dasturlash tilining barcha asosiy va ilg'or mavzularini o'rgatdi. Endi amaliyotga kirishing va o'z loyihalaringizni yaratish vaqti keldi! 

Omad tilayman! 🚀'ri balans kiritildi!")
                    continue
                
                muvaffaqiyat, xabar = bank.hisob_ochish(ism, pin, balans)
                print(xabar)
            
            elif tanlov in [2, 3, 4, 5, 6, 7]:
                hisob_raqami = input("Hisob raqamingizni kiriting: ").strip()
                hisob = bank.hisob_topish(hisob_raqami)
                
                if not hisob:
                    print("Hisob topilmadi!")
                    continue
                
                if hisob.bloklangan and tanlov != 7:
                    print("⚠️  Hisobingiz bloklangan! Administrator bilan bog'laning.")
                    continue
                
                pin = input("PIN kodni kiriting: ").strip()
                try:
                    pin = int(pin)
                except ValueError:
                    print("Noto'g'ri PIN kod!")
                    continue
                
                if tanlov == 2:  # Balans
                    muvaffaqiyat, xabar = hisob.balans_ko'rish(pin)
                    print(xabar)
                
                elif tanlov == 3:  # Pul qo'yish
                    miqdor = float(input("Qo'yiladigan miqdorni kiriting: "))
                    muvaffaqiyat, xabar = hisob.pul_qo'yish(miqdor, pin)
                    print(xabar)
                    if muvaffaqiyat:
                        bank.hisoblarni_saqlash()
                
                elif tanlov == 4:  # Pul yechish
                    miqdor = float(input("Yechiladigan miqdorni kiriting: "))
                    muvaffaqiyat, xabar = hisob.pul_yechish(miqdor, pin)
                    print(xabar)
                    if muvaffaqiyat:
                        bank.hisoblarni_saqlash()
                
                elif tanlov == 5:  # Pul ko'chirish
                    qabul_hisob_raqami = input("Qabul qiluvchi hisob raqami: ").strip()
                    qabul_hisob = bank.hisob_topish(qabul_hisob_raqami)
                    
                    if not qabul_hisob:
                        print("Qabul qiluvchi hisob topilmadi!")
                        continue
                    
                    if qabul_hisob.bloklangan:
                        print("Qabul qiluvchi hisob bloklangan!")
                        continue
                    
                    miqdor = float(input("Ko'chiriladigan miqdor: "))
                    muvaffaqiyat, xabar = hisob.pul_ko'chirish(qabul_hisob, miqdor, pin)
                    print(xabar)
                    if muvaffaqiyat:
                        bank.hisoblarni_saqlash()
                
                elif tanlov == 6:  # Tranzaksiyalar
                    n = input("Nechta oxirgi tranzaksiya ko'rish kerak (default 10): ").strip()
                    try:
                        n = int(n) if n else 10
                    except ValueError:
                        n = 10
                    
                    muvaffaqiyat, xabar = hisob.tranzaksiyalar_tarixi(pin, n)
                    print(xabar)
                
                elif tanlov == 7:  # Hisob ma'lumotlari
                    if hisob.pin_tekshirish(pin) or True:  # Ma'lumotlarni har doim ko'rsatish
                        print(f"\n=== HISOB MA'LUMOTLARI ===")
                        print(f"Hisob raqami: {hisob.hisob_raqami}")
                        print(f"Egasi: {hisob.egasi_ismi}")
                        print(f"Yaratilgan: {hisob.yaratilgan}")
                        print(f"Joriy balans: {hisob.balans:,.0f} so'm")
                        print(f"Status: {'🔒 Bloklangan' if hisob.bloklangan else '🔓 Faol'}")
                        print(f"Tranzaksiyalar soni: {len(hisob.tranzaksiyalar)}")
            
            else:
                print("Noto'g'ri tanlov!")
        
        except ValueError:
            print("Noto'g'ri qiymat kiritildi!")
        except Exception as e:
            print(f"Xatolik yuz berdi: {e}")

print("Bank boshqaruv tizimi yaratildi. Ishga tushirish uchun bank_dasturi() funksiyasini chaqiring.")
```

### 18.4 O'yin: Son topish o'yini

```python
import random
import json
from datetime import datetime

class SonTopishOyini:
    def __init__(self):
        self.eng_yaxshi_natijalar = self.natijalarni_yuklash()
        self.joriy_o'yin = None
    
    def natijalarni_yuklash(self):
        try:
            with open("o'yin_natijalari.json", "r", encoding="utf-8") as f:
                return json.load(f)
        except FileNotFoundError:
            return {"oson": [], "o'rta": [], "qiyin": []}
    
    def natijalarni_saqlash(self):
        with open("o'yin_natijalari.json", "w", encoding="utf-8") as f:
            json.dump(self.eng_yaxshi_natijalar, f, ensure_ascii=False, indent=2)
    
    def yangi_o'yin_boshlash(self, qiyinlik):
        if qiyinlik == "oson":
            min_son, max_son, max_urinishlar = 1, 50, 10
        elif qiyinlik == "o'rta":
            min_son, max_son, max_urinishlar = 1, 100, 8
        elif qiyinlik == "qiyin":
            min_son, max_son, max_urinishlar = 1, 500, 12
        else:
            return False, "Noto'g'ri qiyinlik darajasi!"
        
        self.joriy_o'yin = {
            "yashirin_son": random.randint(min_son, max_son),
            "min_son": min_son,
            "max_son": max_son,
            "max_urinishlar": max_urinishlar,
            "urinishlar": 0,
            "qiyinlik": qiyinlik,
            "boshlangan_vaqt": datetime.now(),
            "tarix": []
        }
        
        return True, f"{qiyinlik.title()} darajada o'yin boshlandi!\n{min_son} dan {max_son} gacha son o'ylab qo'ydim.\nSizda {max_urinishlar} ta urinish bor."
    
    def tahmin_qilish(self, tahmin):
        if not self.joriy_o'yin:
            return False, "Avval o'yinni boshlang!"
        
        o'yin = self.joriy_o'yin
        
        if o'yin["urinishlar"] >= o'yin["max_urinishlar"]:
            return False, "Barcha urinishlar tugagan!"
        
        o'yin["urinishlar"] += 1
        o'yin["tarix"].append(tahmin)
        
        if tahmin == o'yin["yashirin_son"]:
            # O'yin tugadi - g'alaba!
            tugash_vaqti = datetime.now()
            davomiylik = (tugash_vaqti - o'yin["boshlangan_vaqt"]).total_seconds()
            
            natija = {
                "urinishlar": o'yin["urinishlar"],
                "vaqt": round(davomiylik),
                "sana": tugash_vaqti.strftime("%Y-%m-%d %H:%M:%S"),
                "ball": self.ball_hisoblash(o'yin["urinishlar"], o'yin["max_urinishlar"], davomiylik)
            }
            
            self.eng_yaxshi_natijalar[o'yin["qiyinlik"]].append(natija)
            self.eng_yaxshi_natijalar[o'yin["qiyinlik"]].sort(key=lambda x: x["ball"], reverse=True)
            self.eng_yaxshi_natijalar[o'yin["qiyinlik"]] = self.eng_yaxshi_natijalar[o'yin["qiyinlik"]][:10]  # Faqat eng yaxshi 10 ta
            self.natijalarni_saqlash()
            
            xabar = f"🎉 TABRIKLAYMIZ! Siz yutdingiz!\n"
            xabar += f"Yashirin son: {o'yin['yashirin_son']}\n"
            xabar += f"Urinishlar: {o'yin['urinishlar']}/{o'yin['max_urinishlar']}\n"
            xabar += f"Vaqt: {natija['vaqt']} soniya\n"
            xabar += f"Ball: {natija['ball']}"
            
            self.joriy_o'yin = None
            return True, xabar
        
        elif tahmin < o'yin["yashirin_son"]:
            qolgan = o'yin["max_urinishlar"] - o'yin["urinishlar"]
            if qolgan > 0:
                return False, f"📈 Kattaroq son kiriting! Qolgan urinishlar: {qolgan}"
            else:
                xabar = f"😞 Barcha urinishlar tugadi!\nYashirin son: {o'yin['yashirin_son']} edi."
                self.joriy_o'yin = None
                return False, xabar
        
        else:  # tahmin > yashirin_son
            qolgan = o'yin["max_urinishlar"] - o'yin["urinishlar"]
            if qolgan > 0:
                return False, f"📉 Kichikroq son kiriting! Qolgan urinishlar: {qolgan}"
            else:
                xabar = f"😞 Barcha urinishlar tugadi!\nYashirin son: {o'yin['yashirin_son']} edi."
                self.joriy_o'yin = None
                return False, xabar
    
    def ball_hisoblash(self, urinishlar, max_urinishlar, vaqt_soniya):
        # Ball: kam urinish va kam vaqt = yuqori ball
        urinish_balli = ((max_urinishlar - urinishlar + 1) / max_urinishlar) * 500
        vaqt_balli = max(0, 500 - vaqt_soniya)  # Har soniya uchun ball kamaytirish
        return round(urinish_balli + vaqt_balli)
    
    def eng_yaxshi_natijalar_ko'rish(self):
        xabar = "🏆 ENG YAXSHI NATIJALAR 🏆\n\n"
        
        for qiyinlik in ["oson", "o'rta", "qiyin"]:
            natijalar = self.eng_yaxshi_natijalar[qiyinlik]
            xabar += f"=== {qiyinlik.upper()} DARAJA ===\n"
            
            if not natijalar:
                xabar += "Hali natija yo'q\n\n"
                continue
            
            for i, natija in enumerate(natijalar[:5], 1):
                xabar += f"{i}. {natija['ball']} ball "
                xabar += f"({natija['urinishlar']} urinish, {natija['vaqt']}s) "
                xabar += f"- {natija['sana']}\n"
            
            xabar += "\n"
        
        return xabar
    
    def o'yin_holati(self):
        if not self.joriy_o'yin:
            return "O'yin boshlanmagan"
        
        o'yin = self.joriy_o'yin
        davomiylik = (datetime.now() - o'yin["boshlangan_vaqt"]).total_seconds()
        
        xabar = f"=== JORIY O'YIN HOLATI ===\n"
        xabar += f"Qiyinlik: {o'yin['qiyinlik'].title()}\n"
        xabar += f"Oraliq: {o'yin['min_son']}-{o'yin['max_son']}\n"
        xabar += f"Urinishlar: {o'yin['urinishlar']}/{o'yin['max_urinishlar']}\n"
        xabar += f"Vaqt: {round(davomiylik)} soniya\n"
        
        if o'yin["tarix"]:
            xabar += f"Tahminlar tarixi: {', '.join(map(str, o'yin['tarix']))}"
        
        return xabar

def son_topish_o'yini():
    o'yin = SonTopishOyini()
    
    print("🎯 SON TOPISH O'YINIGA XUSH KELIBSIZ! 🎯")
    print("Men bir son o'ylab qo'yaman, siz uni topishga harakat qiling!")
    
    while True:
        print("\n" + "="*50)
        print("1. Yangi o'yin boshlash")
        print("2. Son taxmin qilish")
        print("3. O'yin holati")
        print("4. Eng yaxshi natijalar")
        print("5. O'yin qoidalari")
        print("0. Chiqish")
        print("="*50)
        
        try:
            tanlov = int(input("Tanlovingizni kiriting: "))
            
            if tanlov == 0:
                print("O'yin tugadi! Ko'rishguncha! 👋")
                break
            
            elif tanlov == 1:
                print("\nQiyinlik darajasini tanlang:")
                print("1. Oson (1-50, 10 urinish)")
                print("2. O'rta (1-100, 8 urinish)")
                print("3. Qiyin (1-500, 12 urinish)")
                
                qiyinlik_tanlov = input("Qiyinlik (1-3): ").strip()
                qiyinlik_map = {"1": "oson", "2": "o'rta", "3": "qiyin"}
                
                if qiyinlik_tanlov in qiyinlik_map:
                    muvaffaqiyat, xabar = o'yin.yangi_o'yin_boshlash(qiyinlik_map[qiyinlik_tanlov])
                    print(xabar)
                else:
                    print("Noto'g'ri tanlov!")
            
            elif tanlov == 2:
                if not o'yin.joriy_o'yin:
                    print("Avval o'yinni boshlang!")
                    continue
                
                try:
                    tahmin = int(input(f"Tahmin qiling ({o'yin.joriy_o'yin['min_son']}-{o'yin.joriy_o'yin['max_son']}): "))
                    
                    if not (o'yin.joriy_o'yin['min_son'] <= tahmin <= o'yin.joriy_o'yin['max_son']):
                        print(f"Son {o'yin.joriy_o'yin['min_son']} dan {o'yin.joriy_o'yin['max_son']} gacha bo'lishi kerak!")
                        continue
                    
                    muvaffaqiyat, xabar = o'yin.tahmin_qilish(tahmin)
                    print(xabar)
                    
                except ValueError:
                    print("Faqat son kiriting!")
            
            elif tanlov == 3:
                print(o'yin.o'yin_holati())
            
            elif tanlov == 4:
                print(o'yin.eng_yaxshi_natijalar_ko'rish())
            
            elif tanlov == 5:
                print("""
🎮 O'YIN QOIDALARI 🎮

1. Kompyuter bir son o'ylab qo'yadi
2. Siz bu sonni topishga harakat qilasiz  
3. Har tahmin qilganingizda, kompyuter sizga:
   - Son kattami yoki kichikmi deb aytadi
4. Cheklangan urinish ichida topishga harakat qiling

QIYINLIK DARAJALARI:
• Oson: 1-50 oralig'ida, 10 urinish
• O'rta: 1-100 oralig'ida, 8 urinish  
• Qiyin: 1-500 oralig'ida, 12 urinish

BALL TIZIMI:
• Kam urinishda topish = ko'p ball
• Tez topish = ko'p ball
• Eng yaxshi 10 natija saqlanadi
                """)
            
            else:
                print("Noto'g'ri tanlov!")
        
        except ValueError:
            print("Faqat raqam kiriting!")
        except Exception as e:
            print(f"Xatolik: {e}")

print("Son topish o'yini yaratildi. Ishga tushirish uchun son_topish_o'yini() funksiyasini chaqiring.")
```

### 18.5 Kitobxona boshqaruv tizimi

```python
import json
from datetime import datetime, timedelta

class Kitob:
    def __init__(self, id, nom, muallif, janr, nashr_yili, isbn=""):
        self.id = id
        self.nom = nom
        self.muallif = muallif
        self.janr = janr
        self.nashr_yili = nashr_yili
        self.isbn = isbn
        self.mavjud = True
        self.qarz_olingan_sana = None
        self.qarz_oluvchi = None
        self.qaytarish_muddati = None
    
    def kitob_malumoti(self):
        status = "📚 Mavjud" if self.mavjud else "📖 Qarzda"
        ma'lumot = f"""
🆔 ID: {self.id}
📖 Nom: {self.nom}
✍️ Muallif: {self.muallif}
📂 Janr: {self.janr}
📅 Nashr yili: {self.nashr_yili}
📊 Status: {status}
"""
        if self.isbn:
            ma'lumot += f"🔢 ISBN: {self.isbn}\n"
        
        if not self.mavjud:
            ma'lumot += f"👤 Qarz oluvchi: {self.qarz_oluvchi}\n"
            ma'lumot += f"📅 Qarz olingan: {self.qarz_olingan_sana}\n"
            ma'lumot += f"⏰ Qaytarish muddati: {self.qaytarish_muddati}\n"
        
        return ma'lumot

class Kitobxona:
    def __init__(self, fayl_nomi="kitobxona.json"):
        self.fayl_nomi = fayl_nomi
        self.kitoblar = {}
        self.qarz_tarixi = []
        self.keyingi_id = 1
        self.ma'lumotlarni_yuklash()
    
    def ma'lumotlarni_yuklash(self):
        try:
            with open(self.fayl_nomi, 'r', encoding='utf-8') as f:
                ma'lumot = json.load(f)
                
                # Kitoblarni qayta tiklash
                for kitob_id, kitob_ma'lumot in ma'lumot.get('kitoblar', {}).items():
                    kitob = Kitob(
                        kitob_ma'lumot['id'],
                        kitob_ma'lumot['nom'],
                        kitob_ma'lumot['muallif'],
                        kitob_ma'lumot['janr'],
                        kitob_ma'lumot['nashr_yili'],
                        kitob_ma'lumot.get('isbn', '')
                    )
                    kitob.mavjud = kitob_ma'lumot['mavjud']
                    kitob.qarz_olingan_sana = kitob_ma'lumot.get('qarz_olingan_sana')
                    kitob.qarz_oluvchi = kitob_ma'lumot.get('qarz_oluvchi')
                    kitob.qaytarish_muddati = kitob_ma'lumot.get('qaytarish_muddati')
                    
                    self.kitoblar[int(kitob_id)] = kitob
                
                self.qarz_tarixi = ma'lumot.get('qarz_tarixi', [])
                self.keyingi_id = ma'lumot.get('keyingi_id', 1)
                
        except FileNotFoundError:
            self.kitoblar = {}
            self.qarz_tarixi = []
            self.keyingi_id = 1
    
    def ma'lumotlarni_saqlash(self):
        ma'lumot = {
            'kitoblar': {},
            'qarz_tarixi': self.qarz_tarixi,
            'keyingi_id': self.keyingi_id
        }
        
        for kitob_id, kitob in self.kitoblar.items():
            ma'lumot['kitoblar'][str(kitob_id)] = {
                'id': kitob.id,
                'nom': kitob.nom,
                'muallif': kitob.muallif,
                'janr': kitob.janr,
                'nashr_yili': kitob.nashr_yili,
                'isbn': kitob.isbn,
                'mavjud': kitob.mavjud,
                'qarz_olingan_sana': kitob.qarz_olingan_sana,
                'qarz_oluvchi': kitob.qarz_oluvchi,
                'qaytarish_muddati': kitob.qaytarish_muddati
            }
        
        with open(self.fayl_nomi, 'w', encoding='utf-8') as f:
            json.dump(ma'lumot, f, ensure_ascii=False, indent=2)
    
    def kitob_qo'shish(self, nom, muallif, janr, nashr_yili, isbn=""):
        kitob = Kitob(self.keyingi_id, nom, muallif, janr, nashr_yili, isbn)
        self.kitoblar[self.keyingi_id] = kitob
        self.keyingi_id += 1
        self.ma'lumotlarni_saqlash()
        return f"Kitob qo'shildi! ID: {kitob.id}"
    
    def kitob_qidirish(self, kalit_soz="", janr="", muallif=""):
        topilgan_kitoblar = []
        
        for kitob in self.kitoblar.values():
            mos_keladi = True
            
            if kalit_soz:
                if kalit_soz.lower() not in kitob.nom.lower():
                    mos_keladi = False
            
            if janr and mos_keladi:
                if janr.lower() not in kitob.janr.lower():
                    mos_keladi = False
            
            if muallif and mos_keladi:
                if muallif.lower() not in kitob.muallif.lower():
                    mos_keladi = False
            
            if mos_keladi:
                topilgan_kitoblar.append(kitob)
        
        return topilgan_kitoblar
    
    def kitob_qarz_olish(self, kitob_id, qarz_oluvchi_ismi):
        if kitob_id not in self.kitoblar:
            return False, "Kitob topilmadi!"
        
        kitob = self.kitoblar[kitob_id]
        
        if not kitob.mavjud:
            return False, f"Bu kitob allaqachon qarzda! Qarz oluvchi: {kitob.qarz_oluvchi}"
        
        # Kitobni qarzga berish
        kitob.mavjud = False
        kitob.qarz_oluvchi = qarz_oluvchi_ismi
        kitob.qarz_olingan_sana = datetime.now().strftime("%Y-%m-%d")
        kitob.qaytarish_muddati = (datetime.now() + timedelta(days=14)).strftime("%Y-%m-%d")
        
        # Qarz tarixiga qo'shish
        qarz_yozuv = {
            "kitob_id": kitob_id,
            "kitob_nomi": kitob.nom,
            "qarz_oluvchi": qarz_oluvchi_ismi,
            "qarz_olingan_sana": kitob.qarz_olingan_sana,
            "qaytarish_muddati": kitob.qaytarish_muddati,
            "qaytarilgan_sana": None,
            "holat": "qarzda"
        }
        self.qarz_tarixi.append(qarz_yozuv)
        
        self.ma'lumotlarni_saqlash()
        return True, f"Kitob qarzga berildi! Qaytarish muddati: {kitob.qaytarish_muddati}"
    
    def kitob_qaytarish(self, kitob_id):
        if kitob_id not in self.kitoblar:
            return False, "Kitob topilmadi!"
        
        kitob = self.kitoblar[kitob_id]
        
        if kitob.mavjud:
            return False, "Bu kitob qarzda emas!"
        
        # Kitobni qaytarish
        qarz_oluvchi = kitob.qarz_oluvchi
        kitob.mavjud = True
        kitob.qarz_oluvchi = None
        kitob.qarz_olingan_sana = None
        kitob.qaytarish_muddati = None
        
        # Qarz tarixini yangilash
        for qarz in reversed(self.qarz_tarixi):
            if qarz['kitob_id'] == kitob_id and qarz['holat'] == 'qarzda':
                qarz['qaytarilgan_sana'] = datetime.now().strftime("%Y-%m-%d")
                qarz['holat'] = 'qaytarilgan'
                break
        
        self.ma'lumotlarni_saqlash()
        return True, f"Kitob qaytarildi! Qarz oluvchi: {qarz_oluvchi}"
    
    def kechikkan_kitoblar(self):
        bugun = datetime.now().date()
        kechikkan = []
        
        for kitob in self.kitoblar.values():
            if not kitob.mavjud and kitob.qaytarish_muddati:
                qaytarish_sanasi = datetime.strptime(kitob.qaytarish_muddati, "%Y-%m-%d").date()
                if qaytarish_sanasi < bugun:
                    kechikish_kunlari = (bugun - qaytarish_sanasi).days
                    kechikkan.append((kitob, kechikish_kunlari))
        
        return kechikkan
    
    def statistika(self):
        jami_kitoblar = len(self.kitoblar)
        mavjud_kitoblar = sum(1 for k in self.kitoblar.values() if k.mavjud)
        qarzda_kitoblar = jami_kitoblar - mavjud_kitoblar
        
        janr_statistikasi = {}
        for kitob in self.kitoblar.values():
            janr = kitob.janr
            janr_statistikasi[janr] = janr_statistikasi.get(janr, 0) + 1
        
        stats = f"""
📊 KITOBXONA STATISTIKASI 📊

📚 Jami kitoblar: {jami_kitoblar}
✅ Mavjud: {mavjud_kitoblar}
📖 Qarzda: {qarzda_kitoblar}

📂 JANR BO'YICHA:
"""
        for janr, son in sorted(janr_statistikasi.items()):
            stats += f"   {janr}: {son} ta\n"
        
        kechikkan = self.kechikkan_kitoblar()
        if kechikkan:
            stats += f"\n⚠️ Kechikkan kitoblar: {len(kechikkan)} ta"
        
        return stats

def kitobxona_dasturi():
    kitobxona = Kitobxona()
    
    # Demo ma'lumotlar qo'shish (birinchi ishga tushirishda)
    if not kitobxona.kitoblar:
        print("Demo ma'lumotlar qo'shilmoqda...")
        kitobxona.kitob_qo'shish("O'tkan kunlar", "Abdulla Qodiriy", "Tarixiy roman", 1925)
        kitobxona.kitob_qo'shish("Mehrobdan chayon", "Abdulla Qodiriy", "Roman", 1928)
        kitobxona.kitob_qo'shish("Sariq devni minib", "Xudoyberdi To'xtaboyev", "Fantastika", 1980)
        kitobxona.kitob_qo'shish("Jinoyat va jazo", "Fyodor Dostoyevskiy", "Klassik adabiyot", 1866)
        kitobxona.kitob_qo'shish("Ikki eshik orasi", "O'tkir Hoshimov", "Hikoya", 1978)
    
    while True:
        print("\n" + "="*60)
        print("                    📚 KITOBXONA TIZIMI 📚")
        print("="*60)
        print("1. 📖 Barcha kitoblarni ko'rish")
        print("2. 🔍 Kitob qidirish") 
        print("3. ➕ Yangi kitob qo'shish")
        print("4. 📤 Kitob qarz olish")
        print("5. 📥 Kitob qaytarish")
        print("6. 📋 Qarz tarixi")
        print("7. ⚠️ Kechikkan kitoblar")
        print("8. 📊 Statistika")
        print("0. 🚪 Chiqish")
        print("="*60)
        
        try:
            tanlov = int(input("Tanlovingizni kiriting: "))
            
            if tanlov == 0:
                print("Kitobxona tizimidan chiqildi! 📚")
                break
            
            elif tanlov == 1:
                print("\n📚 BARCHA KITOBLAR:")
                if not kitobxona.kitoblar:
                    print("Kitobxona bo'sh!")
                else:
                    for kitob in kitobxona.kitoblar.values():
                        print("-" * 50)
                        print(kitob.kitob_malumoti())
            
            elif tanlov == 2:
                print("\n🔍 KITOB QIDIRISH:")
                kalit_soz = input("Kitob nomi (ixtiyoriy): ").strip()
                muallif = input("Muallif (ixtiyoriy): ").strip()
                janr = input("Janr (ixtiyoriy): ").strip()
                
                natijalar = kitobxona.kitob_qidirish(kalit_soz, janr, muallif)
                
                if natijalar:
                    print(f"\n{len(natijalar)} ta kitob topildi:")
                    for kitob in natijalar:
                        print("-" * 50)
                        print(kitob.kitob_malumoti())
                else:
                    print("Hech qanday kitob topilmadi!")
            
            elif tanlov == 3:
                print("\n➕ YANGI KITOB QO'SHISH:")
                nom = input("Kitob nomi: ").strip()
                if not nom:
                    print("Kitob nomi bo'sh bo'lishi mumkin emas!")
                    continue
                
                muallif = input("Muallif: ").strip()
                if not muallif:
                    print("Muallif nomi bo'sh bo'lishi mumkin emas!")
                    continue
                
                janr = input("Janr: ").strip() or "Boshqa"
                
                try:
                    nashr_yili = int(input("Nashr yili: "))
                except ValueError:
                    print("Noto'g'ri yil kiritildi!")
                    continue
                
                isbn = input("ISBN (ixtiyoriy): ").strip()
                
                xabar = kitobxona.kitob_qo'shish(nom, muallif, janr, nashr_yili, isbn)
                print(xabar)
            
            elif tanlov == 4:
                print("\n📤 KITOB QARZ OLISH:")
                
                # Mavjud kitoblarni ko'rsatish
                mavjud_kitoblar = [k for k in kitobxona.kitoblar.values() if k.mavjud]
                if not mavjud_kitoblar:
                    print("Qarz olish uchun mavjud kitob yo'q!")
                    continue
                
                print("Mavjud kitoblar:")
                for kitob in mavjud_kitoblar:
                    print(f"ID: {kitob.id} - {kitob.nom} ({kitob.muallif})")
                
                try:
                    kitob_id = int(input("Kitob ID sini kiriting: "))
                    qarz_oluvchi = input("Qarz oluvchi ismini kiriting: ").strip()
                    
                    if not qarz_oluvchi:
                        print("Ism bo'sh bo'lishi mumkin emas!")
                        continue
                    
                    muvaffaqiyat, xabar = kitobxona.kitob_qarz_olish(kitob_id, qarz_oluvchi)
                    print(xabar)
                    
                except ValueError:
                    print("Noto'g