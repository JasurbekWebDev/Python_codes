# Python Dasturlash Kursi - 100 Mavzu 

## 1. Boshlovchilar uchun Python darsligi

**Izoh:** Python - bu sodda va kuchli dasturlash tili. U o'rganish uchun oson va turli sohalarda qo'llaniladi.

**Misol: quydagi kodni (*python.py*) ga joylang.**
```python
# Birinchi Python dasturimiz - bu oddiy salomlashuv dasturi

print("Assalomu alaykum, Python!")  
# print() funksiyasi ekranga matn chiqaradi, bu yerda salomlashuv matni chiqarilmoqda

print("Men dasturlashni o'rganyapman")  
# Ikkinchi print() bilan dasturlash haqidagi matn chiqarilmoqda

# "#" belgisi izohlar uchun ishlatiladi
```

---

## 2. O'zgaruvchilar (Variables)

**Izoh:** O'zgaruvchilar ma'lumotlarni saqlash uchun ishlatiladi. Python-da o'zgaruvchi e'lon qilish uchun alohida kalit so'z kerak emas.

**Misol: quydagi kodni (*variables.py*) ga joylang.**
```python
# O'zgaruvchilar yaratish - ma'lumotlarni saqlash uchun o'zgaruvchilar e'lon qilinmoqda
ism = "Ahmad"  # ism o'zgaruvchisiga matn qiymati saqlanmoqda
yosh = 25  # yosh o'zgaruvchisiga butun son qiymati saqlanmoqda
balandlik = 1.75  # balandlik o'zgaruvchisiga o'nlik son qiymati saqlanmoqda
talaba_mi = True  # talaba_mi o'zgaruvchisiga boolean (rost/inchor) qiymati saqlanmoqda

print(f"Mening ismim {ism}")  # f-string orqali ism o'zgaruvchisini ekranga chiqarish
print(f"Men {yosh} yoshdaman")  # yosh o'zgaruvchisini chiqarish
print(f"Mening balandligim {balandlik} metr")  # balandlik o'zgaruvchisini chiqarish
print(f"Men talabaman: {talaba_mi}")  # talaba_mi o'zgaruvchisini chiqarish
```

---

## 3. Turdagi o'zgartirish (Type Casting)

**Izoh:** Ma'lumotlarni bir turdan boshqa turga o'zgartirish jarayoni. Masalan, raqamni matunga yoki matanni raqamga aylantirish.

**Misol (izohlangan kod):**
```python
# Turlarni o'zgartirish - tur konvertatsiyasi misollari
raqam = 123  # butun son o'zgaruvchisi yaratilmoqda
matn = str(raqam)  # 123 -> "123" - butun sonni matnga aylantirish
print(f"Raqam: {raqam}, turi: {type(raqam)}")  # raqam va uning turini chiqarish
print(f"Matn: {matn}, turi: {type(matn)}")  # matn va uning turini chiqarish

# Matnni raqamga aylantirish - matndan butun songa o'tkazish
matn_raqam = "456"  # matnli raqam o'zgaruvchisi
raqam_yangi = int(matn_raqam)  # "456" -> 456 - matnni butun songa aylantirish
print(f"Yangi raqam: {raqam_yangi}")  # yangi raqamni chiqarish

# Float va int o'rtasida konvertatsiya - o'nlik va butun sonlar o'rtasida o'tkazish
o_nlik_son = 3.14  # o'nlik son o'zgaruvchisi
butun_son = int(o_nlik_son)  # 3.14 -> 3 - o'nlikni butunga aylantirish (qoldiq tashlanadi)
print(f"O'nlik son: {o_nlik_son}, Butun son: {butun_son}")  # ikkalasini chiqarish
```

---

## 4. Foydalanuvchi kiritishi (User Input)

**Izoh:** Foydalanuvchidan ma'lumot olish uchun input() funksiyasidan foydalaniladi. Bu funksiya har doim matn (string) qaytaradi.

**Misol (izohlangan kod):**
```python
# Foydalanuvchidan ma'lumot olish - input() orqali ism va yosh olish
ism = input("Ismingizni kiriting: ")  # ismni matn sifatida olish
yosh_matn = input("Yoshingizni kiriting: ")  # yoshni matn sifatida olish
yosh = int(yosh_matn)  # Matnni raqamga aylantiramiz - matnni butun songa konvertatsiya

print(f"Salom {ism}!")  # ism bilan salomlashish
print(f"Siz {yosh} yoshdasiz")  # yoshni chiqarish

# Matematik amallar bilan - ikkita sonni olish va yig'indisini hisoblash
son1 = float(input("Birinchi sonni kiriting: "))  # birinchi sonni o'nlik sifatida olish
son2 = float(input("Ikkinchi sonni kiriting: "))  # ikkinchi sonni o'nlik sifatida olish
yig_indi = son1 + son2  # ikkala sonni qo'shish
print(f"Yig'indi: {yig_indi}")  # yig'indini chiqarish
```

---

## 5. MadLibs o'yini

**Izoh:** Foydalanuvchidan turli so'zlarni so'rab, ularni qiziqarli hikoyaga joylashtiradigan o'yin.

**Misol (izohlangan kod):**
```python
# MadLibs o'yini - foydalanuvchidan so'zlar olish va hikoya yaratish
print("MadLibs o'yiniga xush kelibsiz!")  # o'yin boshlanishini chiqarish

ot = input("Biror hayvon nomini kiriting: ")  # hayvon nomini olish
sifat1 = input("Biror sifat kiriting: ")  # sifatni olish
rang = input("Biror rang kiriting: ")  # rangni olish
joy = input("Biror joy nomini kiriting: ")  # joy nomini olish
harakat = input("Biror harakat kiriting: ")  # harakatni olish

hikoya = f"""
Bir vaqtlar {sifat1} {ot} {rang} rangdagi uyda yashagan.  # hikoya matnini yaratish, o'zgaruvchilarni joylashtirish
U har kuni {joy}ga borib, {harakat} qilgan.  # hikoyaning davomi
Barcha odamlar uning bu qiziq xususiyatidan hayron bo'lgan!  # hikoyaning oxiri
"""

print("\n--- SIZNING HIKOYANGIZ ---")  # hikoyani chiqarish sarlavhasi
print(hikoya)  # tayyor hikoyani ekranga chiqarish
```

---

## 6. Arifmetika va matematika

**Izoh:** Python-da matematik amallarni bajarish uchun turli operatorlar mavjud.

**Misol (izohlangan kod):**
```python
# Matematik operatorlar - ikkita son bilan arifmetik amallar
a = 10  # birinchi o'zgaruvchi
b = 3  # ikkinchi o'zgaruvchi

qo_shish = a + b      # 13 - qo'shish operatori
ayirish = a - b       # 7 - ayirish operatori
ko_paytirish = a * b  # 30 - ko'paytirish operatori
bo_lish = a / b       # 3.333... - bo'lish operatori (o'nlik natija)
butun_bo_lish = a // b # 3 - butun bo'lish operatori (qoldiqsiz)
qoldiq = a % b        # 1 - qoldiq operatori
daraja = a ** b       # 1000 - darajaga ko'tarish operatori

print(f"Qo'shish: {a} + {b} = {qo_shish}")  # qo'shish natijasini chiqarish
print(f"Ayirish: {a} - {b} = {ayirish}")  # ayirish natijasini chiqarish
print(f"Ko'paytirish: {a} * {b} = {ko_paytirish}")  # ko'paytirish natijasini chiqarish
print(f"Bo'lish: {a} / {b} = {bo_lish}")  # bo'lish natijasini chiqarish
print(f"Butun bo'lish: {a} // {b} = {butun_bo_lish}")  # butun bo'lish natijasini chiqarish
print(f"Qoldiq: {a} % {b} = {qoldiq}")  # qoldiq natijasini chiqarish
print(f"Daraja: {a} ** {b} = {daraja}")  # daraja natijasini chiqarish

# Math kutubxonasi bilan - matematik funksiyalarni import qilish va ishlatish
import math  # math modulini import qilish
print(f"Kvadrat ildiz: {math.sqrt(16)}")  # 16 ning kvadrat ildizini hisoblash (4.0)
print(f"Pi soni: {math.pi}")  # pi sonini chiqarish
print(f"Yaxlitlash: {math.ceil(3.2)} va {math.floor(3.8)}")  # 3.2 ni yuqoriga va 3.8 ni pastga yaxlitlash
```

---

## 7. If iboralari (If Statements)

**Izoh:** Shartli iboralar dasturda qaror qabul qilish uchun ishlatiladi.

**Misol (izohlangan kod):**
```python
# If iboralari - yosh bo'yicha shartlar bilan ishlash
yosh = int(input("Yoshingizni kiriting: "))  # yoshni input orqali olish va butunga aylantirish

if yosh >= 18:  # agar yosh 18 dan katta yoki teng bo'lsa
    print("Siz kattasiz!")  # kattalik haqida xabar
    print("Haydovchilik guvohnomasini olishingiz mumkin.")  # guvohnoma haqida xabar
elif yosh >= 16:  # agar yosh 16 dan katta yoki teng bo'lsa (avvalgi shart bajarilmasa)
    print("Siz o'sminsiz!")  # o'smirlik haqida xabar
    print("Yana 2 yil kutishingiz kerak.")  # kutish haqida xabar
else:  # boshqa barcha holatlarda
    print("Siz hali bolasiz!")  # bolalik haqida xabar
    print("Ko'proq o'sishingiz kerak.")  # o'sish haqida xabar

# Baho tizimi - baho bo'yicha harf baho berish
baho = int(input("Bahoyingizni kiriting (0-100): "))  # bahoni olish

if baho >= 90:  # 90 va undan yuqori bo'lsa
    harf_baho = "A"  # A baho berish
elif baho >= 80:  # 80 va undan yuqori bo'lsa
    harf_baho = "B"  # B baho berish
elif baho >= 70:  # 70 va undan yuqori bo'lsa
    harf_baho = "C"  # C baho berish
elif baho >= 60:  # 60 va undan yuqori bo'lsa
    harf_baho = "D"  # D baho berish
else:  # 60 dan past bo'lsa
    harf_baho = "F"  # F baho berish

print(f"Sizning harf bahoyingiz: {harf_baho}")  # harf bahoni chiqarish
```

---

## 8. Kalkulyator dasturi

**Izoh:** Foydalanuvchidan raqamlar va amal turini so'rab, natijani hisoblaydigan dastur.

**Misol (izohlangan kod):**
```python
# Oddiy kalkulyator - foydalanuvchidan sonlar va operator olish
print("=== ODDIY KALKULYATOR ===")  # sarlavha chiqarish

birinchi_son = float(input("Birinchi sonni kiriting: "))  # birinchi sonni olish
operator = input("Amalni tanlang (+, -, *, /): ")  # operatorni olish
ikkinchi_son = float(input("Ikkinchi sonni kiriting: "))  # ikkinchi sonni olish

if operator == "+":  # agar qo'shish bo'lsa
    natija = birinchi_son + ikkinchi_son  # qo'shishni hisoblash
    print(f"{birinchi_son} + {ikkinchi_son} = {natija}")  # natijani chiqarish
elif operator == "-":  # agar ayirish bo'lsa
    natija = birinchi_son - ikkinchi_son  # ayirishni hisoblash
    print(f"{birinchi_son} - {ikkinchi_son} = {natija}")  # natijani chiqarish
elif operator == "*":  # agar ko'paytirish bo'lsa
    natija = birinchi_son * ikkinchi_son  # ko'paytirishni hisoblash
    print(f"{birinchi_son} * {ikkinchi_son} = {natija}")  # natijani chiqarish
elif operator == "/":  # agar bo'lish bo'lsa
    if ikkinchi_son != 0:  # nolga bo'lishni tekshirish
        natija = birinchi_son / ikkinchi_son  # bo'lishni hisoblash
        print(f"{birinchi_son} / {ikkinchi_son} = {natija}")  # natijani chiqarish
    else:  # agar nol bo'lsa
        print("Xatolik: Nolga bo'lish mumkin emas!")  # xatolik xabari
else:  # noto'g'ri operator bo'lsa
    print("Noto'g'ri operator kiritdingiz!")  # xatolik xabari
```

---

## 9. Og'irlik konvertatsiya dasturi

**Izoh:** Kilogram va funt o'rtasida o'zgartirish dasturi.

**Misol (izohlangan kod):**
```python
# Og'irlik konvertatsiyasi - kilogram va funt o'rtasida o'zgartirish
print("=== OG'IRLIK KONVERTATSIYA DASTURI ===")  # sarlavha
print("1. Kilogramdan funtga")  # 1-tanlov
print("2. Funtdan kilogramga")  # 2-tanlov

tanlov = input("Tanlovingizni kiriting (1/2): ")  # tanlovni olish

if tanlov == "1":  # kilogramdan funtga
    kg = float(input("Kilogram miqdorini kiriting: "))  # kilogramni olish
    funt = kg * 2.205  # kilogramni funtga aylantirish
    print(f"{kg} kg = {funt:.2f} funt")  # natijani chiqarish (2 xonagacha)
elif tanlov == "2":  # funtdan kilogramga
    funt = float(input("Funt miqdorini kiriting: "))  # funtni olish
    kg = funt / 2.205  # funtni kilogramga aylantirish
    print(f"{funt} funt = {kg:.2f} kg")  # natijani chiqarish
else:  # noto'g'ri tanlov
    print("Noto'g'ri tanlov!")  # xatolik xabari

# Umumiy og'irlik konvertatsiyasi - ko'proq birliklar bilan
vazn = float(input("\nVaznni kiriting: "))  # vaznni olish
birlik = input("Birlikni kiriting (kg/g/funt): ").lower()  # birlikni olish va kichik harfga aylantirish

if birlik == "kg":  # kilogramdan boshqalarga
    print(f"{vazn} kg = {vazn * 1000} gram")  # gramga aylantirish
    print(f"{vazn} kg = {vazn * 2.205:.2f} funt")  # funtga aylantirish
elif birlik == "g":  # gramdan boshqalarga
    print(f"{vazn} g = {vazn / 1000} kg")  # kilogramga aylantirish
    print(f"{vazn} g = {vazn / 453.592:.2f} funt")  # funtga aylantirish
elif birlik == "funt":  # funtdan boshqalarga
    print(f"{vazn} funt = {vazn / 2.205:.2f} kg")  # kilogramga aylantirish
    print(f"{vazn} funt = {vazn * 453.592:.2f} gram")  # gramga aylantirish
```

---

## 10. Harorat konvertatsiya dasturi

**Izoh:** Celsius, Fahrenheit va Kelvin o'rtasida harorat o'zgartirishini amalga oshiradigan dastur.

**Misol (izohlangan kod):**
```python
# Harorat konvertatsiyasi - turli birliklar o'rtasida o'zgartirish
print("=== HARORAT KONVERTATSIYA DASTURI ===")  # sarlavha
print("1. Celsius -> Fahrenheit")  # 1-tanlov
print("2. Fahrenheit -> Celsius")   # 2-tanlov
print("3. Celsius -> Kelvin")  # 3-tanlov
print("4. Kelvin -> Celsius")  # 4-tanlov

tanlov = input("Tanlovingizni kiriting (1-4): ")  # tanlovni olish

if tanlov == "1":  # Celsiusdan Fahrenheitga
    celsius = float(input("Celsius haroratini kiriting: "))  # celsiusni olish
    fahrenheit = (celsius * 9/5) + 32  # formulaga ko'ra hisoblash
    print(f"{celsius}°C = {fahrenheit:.2f}°F")  # natijani chiqarish
elif tanlov == "2":  # Fahrenheitdan Celsiusga
    fahrenheit = float(input("Fahrenheit haroratini kiriting: "))  # fahrenheitni olish
    celsius = (fahrenheit - 32) * 5/9  # formulaga ko'ra hisoblash
    print(f"{fahrenheit}°F = {celsius:.2f}°C")  # natijani chiqarish
elif tanlov == "3":  # Celsiusdan Kelvinga
    celsius = float(input("Celsius haroratini kiriting: "))  # celsiusni olish
    kelvin = celsius + 273.15  # formulaga ko'ra hisoblash
    print(f"{celsius}°C = {kelvin:.2f}K")  # natijani chiqarish
elif tanlov == "4":  # Kelvindan Celsiusga
    kelvin = float(input("Kelvin haroratini kiriting: "))  # kelvinni olish
    celsius = kelvin - 273.15  # formulaga ko'ra hisoblash
    print(f"{kelvin}K = {celsius:.2f}°C")  # natijani chiqarish
else:  # noto'g'ri tanlov
    print("Noto'g'ri tanlov!")  # xatolik xabari

# Barcha konvertatsiya bir vaqtda - birlik bo'yicha barcha natijalarni chiqarish
temp = float(input("\nHaroratni kiriting: "))  # haroratni olish
birlik = input("Hozirgi birlikni kiriting (C/F/K): ").upper()  # birlikni olish va katta harfga aylantirish

if birlik == "C":  # Celsiusdan boshqalarga
    f = (temp * 9/5) + 32  # Fahrenheitga
    k = temp + 273.15  # Kelvinga
    print(f"{temp}°C = {f:.2f}°F = {k:.2f}K")  # natijalarni chiqarish
elif birlik == "F":  # Fahrenheitdan boshqalarga
    c = (temp - 32) * 5/9  # Celsiusga
    k = c + 273.15  # Kelvinga
    print(f"{temp}°F = {c:.2f}°C = {k:.2f}K")  # natijalarni chiqarish
elif birlik == "K":  # Kelvindan boshqalarga
    c = temp - 273.15  # Celsiusga
    f = (c * 9/5) + 32  # Fahrenheitga
    print(f"{temp}K = {c:.2f}°C = {f:.2f}°F")  # natijalarni chiqarish
```

---

## 11. Mantiqiy operatorlar (Logical Operators)

**Izoh:** and, or, not operatorlari murakkab shartlarni yaratish uchun ishlatiladi.

**Misol (izohlangan kod):**
```python
# Mantiqiy operatorlar - yosh va maosh bo'yicha shartlar
yosh = int(input("Yoshingizni kiriting: "))  # yoshni olish
maosh = float(input("Oylik maoshingizni kiriting (ming so'mda): "))  # maoshni olish

# AND operatori - barcha shartlar to'g'ri bo'lishi kerak - yosh va maoshni tekshirish
if yosh >= 18 and maosh >= 3000:  # ikkala shart ham rost bo'lsa
    print("Kredit olishingiz mumkin!")  # kredit ruxsati
else:  # aks holda
    print("Kredit uchun shart bajarmayapsiz.")  # rad etish

# OR operatori - kamida bitta shart to'g'ri bo'lishi kerak - yosh bo'yicha chegirma
if yosh < 18 or yosh > 65:  # yosh 18 dan past yoki 65 dan yuqori bo'lsa
    print("Chegirmali bilet oling!")  # chegirma xabari
else:  # aks holda
    print("To'liq narx to'lang.")  # to'liq narx xabari

# NOT operatori - shartni teskarisini tekshiradi - parol uzunligini tekshirish
parol = input("Parolni kiriting: ")  # parolni olish
if not (len(parol) >= 8):  # agar parol uzunligi 8 dan kichik bo'lsa (not orqali teskari)
    print("Parol juda qisqa!")  # qisqa xabari
else:  # aks holda
    print("Parol uzunligi yetarli.")  # yetarli xabari

# Murakkab shartlar - baho va davomiylik bo'yicha o'tish/qayta topshirish
baho = int(input("Imtihon bahoyingiz: "))  # bahoni olish
davomiylik = int(input("Davomiylik foizi: "))  # davomiylikni olish

if (baho >= 70 and davomiylik >= 80) or (baho >= 85 and davomiylik >= 60):  # murakkab shart: and va or birgalikda
    print("Siz o'tdingiz!")  # o'tish xabari
else:  # aks holda
    print("Qaytadan topshiring.")  # qayta topshirish xabari
```

---

## 12. Shartli ifodalar (Conditional Expressions)

**Izoh:** Ternary operator yoki shartli ifoda - qisqa if-else ifodasini yozishning yo'li.

**Misol (izohlangan kod):**
```python
# Oddiy ternary operator - yosh bo'yicha holatni qisqa belgilash
yosh = int(input("Yoshingizni kiriting: "))  # yoshni olish
holat = "Katta" if yosh >= 18 else "Bola"  # ternary: agar yosh >=18 bo'lsa "Katta", aks holda "Bola"
print(f"Siz {holat}sisiz")  # holatni chiqarish

# Matematik misollar - ikki sonni solishtirish va kattasini topish
a = int(input("Birinchi sonni kiriting: "))  # birinchi son
b = int(input("Ikkinchi sonni kiriting: "))  # ikkinchi son

# Katta sonni topish - ternary orqali
katta = a if a > b else b  # a > b bo'lsa a, aks holda b
print(f"Katta son: {katta}")  # kattasini chiqarish

# Juft yoki toqligini tekshirish - sonni tekshirish
son = int(input("Son kiriting: "))  # sonni olish
tur = "juft" if son % 2 == 0 else "toq"  # agar qoldiq 0 bo'lsa juft, aks holda toq
print(f"{son} - {tur} son")  # natijani chiqarish

# Baho tizimi - ball bo'yicha o'tdi/yiqildi
ball = int(input("Ballingizni kiriting: "))  # ballni olish
natija = "O'tdi" if ball >= 60 else "Yiqildi"  # 60 dan yuqori bo'lsa o'tdi, aks holda yi qildi
print(f"Natija: {natija}")  # natijani chiqarish

# Nested ternary - harorat bo'yicha havo holati
harorat = int(input("Haroratni kiriting: "))  # haroratni olish
holat = "Issiq" if harorat > 30 else "Iliq" if harorat > 15 else "Sovuq"  # nested ternary: >30 issiq, >15 iliq, aks holda sovuq
print(f"Havo: {holat}")  # holatni chiqarish

# Ro'yxatdan tanlov - haftaning kunini ro'yxatdan olish
raqam = int(input("1-5 oralig'idagi son kiriting: "))  # raqamni olish
kun = ["", "Dushanba", "Seshanba", "Chorshanba", "Payshanba", "Juma"][raqam] if 1 <= raqam <= 5 else "Noto'g'ri"  # ro'yxatdan tanlash, agar oraliqda bo'lsa
print(f"Kun: {kun}")  # kunni chiqarish
```

---

## 13. Matn metodlari (String Methods)

**Izoh:** Matnlar bilan ishlash uchun Python-da ko'plab tayyor metodlar mavjud.

**Misol (izohlangan kod):**
```python
# Matn metodlari - matn bilan ishlash metodlari
matn = "  Assalomu Alaykum Python!  "  # matn o'zgaruvchisi, boshi va oxirida bo'shliqlar
print(f"Asl matn: '{matn}'")  # asl matnni chiqarish

# Bo'shliqlarni olib tashlash - strip metodlari
print(f"strip(): '{matn.strip()}'")  # bosh va oxirdagi bo'shliqlarni olib tashlash
print(f"lstrip(): '{matn.lstrip()}'")  # chap tarafdagi bo'shliqlarni olib tashlash
print(f"rstrip(): '{matn.rstrip()}'")  # o'ng tarafdagi bo'shliqlarni olib tashlash

# Harflarni o'zgartirish - register o'zgartirish metodlari
print(f"upper(): '{matn.upper()}'")  # barcha harflarni katta qilish
print(f"lower(): '{matn.lower()}'")  # barcha harflarni kichik qilish
print(f"title(): '{matn.title()}'")  # har so'zning birinchi harfini katta qilish
print(f"capitalize(): '{matn.capitalize()}'")  # birinchi harfni katta qilish, qolganini kichik
print(f"swapcase(): '{matn.swapcase()}'")  # katta va kichik harflarni almashtirish

# Tekshirish metodlari - matn turini tekshirish
test_matn = "Python123"  # test matni
print(f"isdigit(): {test_matn.isdigit()}")  # faqat raqamlar bo'lsa True
print(f"isalpha(): {test_matn.isalpha()}")  # faqat harflar bo'lsa True
print(f"isalnum(): {test_matn.isalnum()}")  # harflar va raqamlar bo'lsa True
print(f"islower(): {test_matn.islower()}")  # barchasi kichik bo'lsa True
print(f"isupper(): {test_matn.isupper()}")  # barchasi katta bo'lsa True

# Qidirish va almashtirish - matnda qidirish va o'zgartirish
gap = "Men Python dasturlash tilini o'rganyapman. Python juda ajoyib!"  # gap matni
print(f"count('Python'): {gap.count('Python')}")  # "Python" necha marta uchrashi
print(f"find('dasturlash'): {gap.find('dasturlash')}")  # "dasturlash" ning indeksi
print(f"replace('Python', 'Java'): {gap.replace('Python', 'Java')}")  # "Python" ni "Java" ga almashtirish

# Bo'lish va birlashtirish - matnni bo'lish va birlashtirish
mevalar = "olma,nok,uzum,banan"  # vergul bilan ajratilgan matn
ro_yxat = mevalar.split(',')  # vergul bo'yicha bo'lish, ro'yxatga aylantirish
print(f"split(','): {ro_yxat}")  # ro'yxatni chiqarish
yangi_matn = ' - '.join(ro_yxat)  # ro'yxatni " - " bilan birlashtirish
print(f"join(' - '): {yangi_matn}")  # yangi matnni chiqarish

# To'ldirish - matnni to'ldirish metodlari
son = "42"  # matnli son
print(f"zfill(5): '{son.zfill(5)}'")  # 5 ta uzunlikka nol bilan to'ldirish
print(f"center(10, '*'): '{son.center(10, '*')}'")  # 10 ta uzunlikka yulduzcha bilan markazlash
```

---

## 14. Matn indekslash (String Indexing)

**Izoh:** Matnning har bir belgisiga indeks orqali murojaat qilish va qism olish.

**Misol (izohlangan kod):**
```python
# Matn indekslash - matnning belgilari bilan ishlash
matn = "Python Dasturlash"  # matn o'zgaruvchisi
print(f"Asl matn: '{matn}'")  # asl matnni chiqarish
print(f"Uzunlik: {len(matn)}")  # matn uzunligini chiqarish (len funksiyasi)

# Bitta belgini olish - indeks orqali
print(f"Birinchi belgi (0): '{matn[0]}'")  # 0-indeks: birinchi belgi
print(f"Ikkinchi belgi (1): '{matn[1]}'")  # 1-indeks: ikkinchi belgi
print(f"Oxirgi belgi (-1): '{matn[-1]}'")  # -1-indeks: oxirgi belgi
print(f"Oxiridan ikkinchi (-2): '{matn[-2]}'")  # -2-indeks: oxiridan ikkinchi

# Slicing - qism olish - matn qismlarini kesib olish
print(f"[0:6]: '{matn[0:6]}'")      # 0 dan 6 gacha (6 kirmaydi)
print(f"[7:]: '{matn[7:]}'")        # 7 dan oxirigacha
print(f"[:6]: '{matn[:6]}'")        # boshidan 6 gacha
print(f"[::2]: '{matn[::2]}'")      # har ikkinchi belgi (qadam 2)
print(f"[::-1]: '{matn[::-1]}'")    # teskarisiga aylantirish (qadam -1)

# Foydali misollar - emaildan username va domen ajratish
email = "user@example.com"  # email matni
at_joyi = email.find('@')  # "@" ning indeksi
username = email[:at_joyi]  # boshidan "@" gacha
domen = email[at_joyi+1:]  # "@" dan keyin oxirigacha
print(f"Email: {email}")  # emailni chiqarish
print(f"Username: {username}")  # usernameni chiqarish
print(f"Domen: {domen}")  # domenni chiqarish

# Telefon raqami formatlash - raqamni formatlash
telefon = "998901234567"  # telefon matni
formatted = f"+{telefon[:3]} ({telefon[3:5]}) {telefon[5:8]}-{telefon[8:10]}-{telefon[10:]}"  # slicing orqali formatlash
print(f"Formatlanmagan: {telefon}")  # asl holatini chiqarish
print(f"Formatlangan: {formatted}")  # formatlanganini chiqarish

# Matnni teskari qilish va palindrom tekshirish
so_z = input("So'z kiriting: ")  # so'zni olish
teskari = so_z[::-1]  # teskarisiga aylantirish
print(f"Teskari: {teskari}")  # teskarisini chiqarish
if so_z.lower() == teskari.lower():  # katta/kichik farqsiz solishtirish
    print("Bu palindrom!")  # palindrom xabari
else:  # aks holda
    print("Bu palindrom emas!")  # emas xabari
```

---

## 15. Format ko'rsatkichlari (Format Specifiers)

**Izoh:** Raqamlar va matnlarni ma'lum formatda chiqarish uchun ishlatiladi.

**Misol (izohlangan kod):**
```python
# Format ko'rsatkichlari - f-string bilan matn va raqamlarni formatlash
ism = "Ahmad"  # ism o'zgaruvchisi
yosh = 25  # yosh o'zgaruvchisi
balandlik = 1.75238  # balandlik o'zgaruvchisi
maosh = 5000000  # maosh o'zgaruvchisi

# f-string bilan - o'zgaruvchilarni matnga joylashtirish
print(f"Mening ismim {ism}, men {yosh} yoshdaman")  # ism va yoshni chiqarish

# Raqamlarni formatlash - o'nliklarni cheklash
pi = 3.14159265359  # pi soni
print(f"Pi soni: {pi}")  # asl holati
print(f"Pi soni 2 xona: {pi:.2f}")  # 2 o'nlik xonaga cheklash
print(f"Pi soni 4 xona: {pi:.4f}")  # 4 o'nlik xonaga cheklash

# Foizlar - o'nlikni foizga aylantirish
foiz = 0.85  # foiz qiymati
print(f"Foiz: {foiz}")  # asl holati
print(f"Foiz %: {foiz:.2%}")  # 2 xonali foiz formatida

# Pul formati - minglik ajratgich bilan
print(f"Maosh: {maosh:,} so'm")  # vergul bilan minglik ajratish
print(f"Maosh $: ${maosh:,.2f}")  # dollar va o'nlik bilan

# Joylashtirish - matnni chap/o'ng/markazga joylashtirish
ism1, ism2 = "Ali", "Vali"  # ikkita ism
print(f"|{ism1:<10}|")  # chapga, 10 joy
print(f"|{ism1:>10}|")  # o'ngga, 10 joy
print(f"|{ism1:^10}|")  # markazga, 10 joy
print(f"|{ism1:*^10}|")  # markazga, yulduzcha bilan to'ldirish

# Raqam tizimlari - raqamni ikkilik, sakkizlik va o'n oltilikka aylantirish
son = 255  # o'nlik son
print(f"O'nlik: {son}")  # asl holati
print(f"Ikkilik: {son:b}")  # ikkilik format
print(f"Sakkizlik: {son:o}")  # sakkizlik format
print(f"O'n oltilik: {son:x}")  # o'n oltilik kichik harf
print(f"O'n oltilik katta: {son:X}")  # o'n oltilik katta harf

# Ilmiy notatsiya - katta sonni ilmiy formatda chiqarish
katta_son = 1234567.89  # katta son
print(f"Oddiy: {katta_son}")  # asl holati
print(f"Ilmiy: {katta_son:e}")  # ilmiy notatsiya kichik
print(f"Ilmiy katta: {katta_son:E}")  # ilmiy notatsiya katta

# Vaqt formatlashi - datetime modulini ishlatish
import datetime  # datetime modulini import qilish
hozir = datetime.datetime.now()  # hozirgi vaqtni olish
print(f"Hozir: {hozir}")  # asl holati
print(f"Sana: {hozir:%Y-%m-%d}")  # yil-oy-kun format
print(f"Vaqt: {hozir:%H:%M:%S}")  # soat:daqiqa:soniya
print(f"To'liq: {hozir:%Y yil %B %d-kun, %A}")  # to'liq sana va kun nomi
```

---

## 16. While tsikli (While Loops)

**Izoh:** Muayyan shart bajarilguncha takrorlanadigan tsikl turi.

**Misol (izohlangan kod):**
```python
# Oddiy while tsikli - 1 dan 5 gacha sanash
print("1 dan 5 gacha sanash:")  # sarlavha
son = 1  # boshlang'ich qiymat
while son <= 5:  # son 5 dan kichik yoki teng ekan
    print(f"Son: {son}")  # sonni chiqarish
    son += 1  # son = son + 1 - sonni 1 ga oshirish

print("Tsikl tugadi!")  # tsikl oxiridan keyin

# Foydalanuvchi kiritishi bilan - parol tekshirish
print("\n=== PAROL TEKSHIRISH ===")  # sarlavha
to_g_ri_parol = "python123"  # to'g'ri parol
urinish = 0  # urinishlar soni
max_urinish = 3  # maksimal urinishlar

while urinish < max_urinish:  # urinish max dan kichik ekan
    parol = input("Parolni kiriting: ")  # parolni olish
    if parol == to_g_ri_parol:  # agar to'g'ri bo'lsa
        print("Muvaffaqiyatli kirdingiz!")  # muvaffaqiyat xabari
        break  # Tsiklni to'xtatish - tsikldan chiqish
    else:  # noto'g'ri bo'lsa
        urinish += 1  # urinishni oshirish
        qolgan = max_urinish - urinish  # qolgan urinishlar
        if qolgan > 0:  # agar qolgan bo'lsa
            print(f"Noto'g'ri parol! {qolgan} ta urinish qoldi.")  # xatolik xabari
        else:  # urinishlar tugasa
            print("Barcha urinishlar tugadi!")  # tugash xabari

# Son topish o'yini - tasodifiy sonni topish
import random  # random modulini import qilish
tasodifiy_son = random.randint(1, 100)  # 1 dan 100 gacha tasodifiy son
urinish_soni = 0  # urinishlar soni

print("\n=== SON TOPISH O'YINI ===")  # sarlavha
print("Men 1 dan 100 gacha son o'yladim. Topib ko'ring!")  # o'yin haqida xabar

while True:  # cheksiz tsikl (shart bilan to'xtatiladi)
    try:  # xatoliklarni tutish uchun try
        taxmin = int(input("Sizning taxminingiz: "))  # taxminni olish
        urinish_soni += 1  # urinishni oshirish
        
        if taxmin == tasodifiy_son:  # agar to'g'ri bo'lsa
            print(f"Tabriklayman! {urinish_soni} urinishda topdingiz!")  # tabrik xabari
            break  # tsikldan chiqish
        elif taxmin < tasodifiy_son:  # kichik bo'lsa
            print("Kattaroq son kiriting!")  # kattaroq xabari
        else:  # kattaroq bo'lsa
            print("Kichikroq son kiriting!")  # kichikroq xabari
    except ValueError:  # noto'g'ri input bo'lsa
        print("Faqat raqam kiriting!")  # xatolik xabari

# Faktorial hisoblash - sonning faktorialini while bilan hisoblash
print("\n=== FAKTORIAL ===")  # sarlavha
n = int(input("Faktorialni hisoblaydigan sonni kiriting: "))  # sonni olish
faktorial = 1  # boshlang'ich faktorial
asl_n = n  # asl sonni saqlash

while n > 0:  # n 0 dan katta ekan
    faktorial *= n  # faktorialga n ni ko'paytirish
    n -= 1  # n ni 1 ga kamaytirish

print(f"{asl_n}! = {faktorial}")  # natijani chiqarish
```

---

## 17. Murakkab foiz kalkulyatori

**Izoh:** Murakkab foizni hisoblash uchun dastur. Pul qo'yilgan paytda foiz ham asosiy summaga qo'shiladi.

**Misol (izohlangan kod):**
```python
# Murakkab foiz kalkulyatori - investitsiya foizini hisoblash
print("=== MURAKKAB FOIZ KALKULYATORI ===")  # sarlavha

# Foydalanuvchidan ma'lumotlarni olish - summa, foiz, muddat va chastota
asosiy_summa = float(input("Boshlang'ich summani kiriting (so'm): "))  # boshlang'ich summa
yillik_foiz = float(input("Yillik foiz stavkasini kiriting (%): ")) / 100  # foizni o'nlikka aylantirish
muddat_yil = int(input("Necha yil muddatga: "))  # yillar soni
yilda_qo_shish = int(input("Yilda necha marta foiz qo'shiladi: "))  # chastota

print(f"\nBoshlang'ich summa: {asosiy_summa:,.0f} so'm")  # boshlang'ichni chiqarish
print(f"Yillik foiz: {yillik_foiz*100}%")  # foizni chiqarish
print(f"Muddat: {muddat_yil} yil")  # muddatni chiqarish
print(f"Foiz qo'shilish chastotasi: {yilda_qo_shish} marta/yil")  # chastotani chiqarish

# Murakkab foiz formulasi: A = P(1 + r/n)^(nt) - formula haqida izoh
# A - yakuniy summa, P - boshlang'ich summa
# r - yillik foiz, n - yilda necha marta qo'shiladi
# t - yillar soni

joriy_summa = asosiy_summa  # joriy summani boshlang'ich bilan boshlash
yil = 0  # yil soni

print(f"\n{'Yil':<4} {'Summa (so'm)':<15} {'Foiz daromadi':<15}")  # jadval sarlavhasi
print("-" * 40)  # chiziq

while yil <= muddat_yil:  # yil muddatdan kichik yoki teng ekan
    if yil == 0:  # birinchi yilda
        foiz_daromadi = 0  # foiz daromadi 0
    else:  # keyingi yillarda
        # Har bir qo'shilish uchun - ichki tsikl
        davr_foizi = yillik_foiz / yilda_qo_shish  # davr foizi
        marta = 0  # marta soni
        while marta < yilda_qo_shish:  # chastota marta
            joriy_summa *= (1 + davr_foizi)  # summaga foiz qo'shish
            marta += 1  # martani oshirish
        
        foiz_daromadi = joriy_summa - asosiy_summa  # foiz daromadini hisoblash
    
    print(f"{yil:<4} {joriy_summa:,.0f}{'':>8} {foiz_daromadi:,.0f}")  # yil, summa va daromadni chiqarish
    yil += 1  # yilni oshirish

yakuniy_summa = asosiy_summa * (1 + yillik_foiz/yilda_qo_shish)**(yilda_qo_shish * muddat_yil)  # yakuniy summani formula bo'yicha hisoblash
umumiy_foiz = yakuniy_summa - asosiy_summa  # umumiy foiz

print(f"\n=== YAKUNIY NATIJALAR ===")  # yakuniy sarlavha
print(f"Boshlang'ich summa: {asosiy_summa:,.0f} so'm")  # boshlang'ich
print(f"Yakuniy summa: {yakuniy_summa:,.0f} so'm")  # yakuniy
print(f"Umumiy foiz daromadi: {umumiy_foiz:,.0f} so'm")  # foiz daromadi
print(f"Summa {umumiy_foiz/asosiy_summa*100:.1f}% ga oshdi")  # foiz o'sishi
```

---

## 18. For tsikllari (For Loops)

**Izoh:** Ma'lum bo'lgan takrorlanish soni yoki ro'yxat elementlari bo'ylab aylanish uchun ishlatiladi.

**Misol (izohlangan kod):**
```python
# Oddiy for tsikli - range orqali sanash
print("1 dan 5 gacha sanash:")  # sarlavha
for i in range(1, 6):  # 1 dan 5 gacha (6 kirmaydi)
    print(f"Son: {i}")  # i ni chiqarish

# Range funksiyasi turli xil usullari - range ning variantlari
print("\nRange(5): 0 dan 4 gacha")  # sarlavha
for i in range(5):  # 0 dan 4 gacha
    print(i, end=" ")  # i ni chiqarish, end bilan bo'shliq

print("\n\nRange(2, 8): 2 dan 7 gacha")  # sarlavha
for i in range(2, 8):  # 2 dan 7 gacha
    print(i, end=" ")  # chiqarish

print("\n\nRange(0, 10, 2): 0 dan 9 gacha 2 ta qadam bilan")  # sarlavha
for i in range(0, 10, 2):  # 0,2,4,6,8
    print(i, end=" ")  # chiqarish

print("\n\nTeskari sanash:")  # sarlavha
for i in range(10, 0, -1):  # 10 dan 1 gacha teskari
    print(i, end=" ")  # chiqarish

# Ro'yxat bo'ylab aylantirish - ro'yxat elementlari bo'yicha tsikl
mevalar = ["olma", "nok", "uzum", "banan", "apelsin"]  # mevalar ro'yxati
print(f"\n\nMevalar ro'yxati:")  # sarlavha
for meva in mevalar:  # har bir meva uchun
    print(f"- {meva}")  # mevani chiqarish

# Indeks va qiymat bilan - enumerate orqali indeks olish
print("\nIndeks va qiymat bilan:")  # sarlavha
for indeks, meva in enumerate(mevalar):  # indeks va meva
    print(f"{indeks + 1}. {meva}")  # chiqarish (1 dan boshlab)

# Matn bo'ylab aylantirish - matn harflari bo'yicha tsikl
matn = "Python"  # matn
print(f"\n'{matn}' so'zining harflari:")  # sarlavha
for harf in matn:  # har bir harf uchun
    print(f"'{harf}'", end=" ")  # harfni chiqarish

# Matematik misollar - 1 dan 10 gacha yig'indi
print(f"\n\n1 dan 10 gacha sonlar yig'indisi:")  # sarlavha
yigindi = 0  # boshlang'ich yig'indi
for son in range(1, 11):  # 1 dan 10 gacha
    yigindi += son  # yig'indiga qo'shish
    print(f"{son} qo'shildi, yig'indi: {yigindi}")  # har bosqichni chiqarish

# Faktorial hisoblash - for bilan faktorial
n = int(input("Faktorialni hisoblaydigan sonni kiriting: "))  # n ni olish
faktorial = 1  # boshlang'ich
for i in range(1, n + 1):  # 1 dan n gacha
    faktorial *= i  # faktorialga ko'paytirish
    print(f"{i}: {faktorial}")  # har bosqichni chiqarish
print(f"{n}! = {faktorial}")  # yakuniy natija

# Ko'paytirish jadvali - sonning jadvali
son = int(input("Ko'paytirish jadvalini ko'rmoqchi bo'lgan sonni kiriting: "))  # sonni olish
print(f"\n{son} ning ko'paytirish jadvali:")  # sarlavha
for i in range(1, 11):  # 1 dan 10 gacha
    natija = son * i  # ko'paytirish
    print(f"{son} x {i} = {natija}")  # natijani chiqarish
```

---

## 19. Ortga sanash dasturi (Countdown Timer)

**Izoh:** Belgilangan vaqtdan 0 gacha sanab, har soniyada ekranga chiqaradigan dastur.

**Misol (izohlangan kod):**
```python
# Ortga sanash dasturi - soniyalarni sanash
import time  # time modulini import qilish (kutish uchun)

print("=== ORTGA SANASH DASTURI ===")  # sarlavha

# Foydalanuvchidan vaqt olish - soniyalarni olish
try:  # xatoliklarni tutish
    soniya = int(input("Necha soniyadan boshlaymiz? "))  # soniyani olish
    
    if soniya <= 0:  # agar musbat bo'lmasa
        print("Musbat son kiriting!")  # xatolik
    else:  # musbat bo'lsa
        print(f"\n{soniya} soniyadan boshlanmoqda...\n")  # boshlanish xabari
        
        # Ortga sanash - for bilan teskari sanash
        for i in range(soniya, 0, -1):  # soniyadan 1 gacha
            print(f"⏰ {i} soniya qoldi", end="\r")  # \r orqali qatorni qayta yozish
            time.sleep(1)  # 1 soniya kutish
        
        print("🎉 VAQT TUGADI! 🎉")  # tugash xabari

except ValueError:  # noto'g'ri input
    print("Faqat raqam kiriting!")  # xatolik

# Soat, daqiqa, soniya formatida - murakkab timer
print("\n=== MURAKKAB TIMER ===")  # sarlavha
daqiqa = int(input("Daqiqalarni kiriting: "))  # daqiqani olish
qo_shimcha_soniya = int(input("Qo'shimcha soniyalarni kiriting: "))  # soniyani olish

# Umumiy soniyalarga aylantirish - daqiqa va soniyani jamlash
umumiy_soniya = (daqiqa * 60) + qo_shimcha_soniya  # umumiy soniya

print(f"\nJami: {umumiy_soniya} soniya")  # jami chiqarish
print("Boshlash uchun Enter tugmasini bosing...")  # boshlash xabari
input()  # enter kutish

# Formatli ortga sanash - umumiy soniyadan teskari
for i in range(umumiy_soniya, -1, -1):  # umumiy dan -1 gacha
    # Soat, daqiqa, soniyaga ajratish - vaqtni bo'lish
    soat = i // 3600  # soatni hisoblash
    qolgan_daqiqa = (i % 3600) // 60  # daqiqani hisoblash
    qolgan_soniya = i % 60  # soniyani hisoblash
    
    if soat > 0:  # agar soat bo'lsa
        vaqt_format = f"{soat:02d}:{qolgan_daqiqa:02d}:{qolgan_soniya:02d}"  # soat:daqiqa:soniya format
    else:  # soatsiz
        vaqt_format = f"{qolgan_daqiqa:02d}:{qolgan_soniya:02d}"  # daqiqa:soniya
    
    print(f"⏰ {vaqt_format} qoldi", end="\r")  # qayta yozish bilan chiqarish
    
    if i == 0:  # agar 0 bo'lsa
        print("\n🔔 VAQT TUGADI! 🔔")  # tugash
        # Ogohlantirish tovushi (Windows) - tovush chiqarish
        try:  # xatolik tutish
            import winsound  # winsound import
            for _ in range(3):  # 3 marta
                winsound.Beep(1000, 500)  # 1000Hz, 500ms tovush
        except ImportError:  # modul topilmasa
            print("DING! DING! DING!")  # matnli tovush
    else:  # qolgan holatlarda
        time.sleep(1)  # 1 soniya kutish

# Pomodoro timer misoli - ish va tanaffus timerlari
print("\n=== POMODORO TIMER ===")  # sarlavha
print("1. Ish vaqti (25 daqiqa)")  # 1-tanlov
print("2. Qisqa tanaffus (5 daqiqa)")   # 2-tanlov
print("3. Uzun tanaffus (15 daqiqa)")  # 3-tanlov

tanlov = input("Tanlang (1-3): ")  # tanlov olish

if tanlov == "1":  # ish vaqti
    vaqt = 25 * 60  # 25 daqiqa soniyaga
    tur = "ISH VAQTI"  # tur nomi
elif tanlov == "2":  # qisqa tanaffus
    vaqt = 5 * 60   # 5 daqiqa
    tur = "QISQA TANAFFUS"  # tur
elif tanlov == "3":  # uzun tanaffus
    vaqt = 15 * 60  # 15 daqiqa
    tur = "UZUN TANAFFUS"  # tur
else:  # noto'g'ri
    print("Noto'g'ri tanlov!")  # xatolik
    exit()  # dasturdan chiqish

print(f"\n{tur} boshlandi!")  # boshlanish xabari

for i in range(vaqt, -1, -1):  # vaqtdan teskari
    daqiqa = i // 60  # daqiqa hisoblash
    soniya = i % 60  # soniya hisoblash
    print(f"⏰ {tur}: {daqiqa:02d}:{soniya:02d}", end="\r")  # formatli chiqarish
    
    if i == 0:  # 0 bo'lsa
        print(f"\n✅ {tur} TUGADI!")  # tugash
    else:  # qolganlarda
        time.sleep(1)  # kutish
```

---

## 20. Ichma-ich tsikllar (Nested Loops)

**Izoh:** Bir tsikl ichida boshqa tsikl ishlatish. Ko'pincha jadvallar, matritsalar bilan ishlashda qo'llaniladi.

**Misol (izohlangan kod):**
```python
# Oddiy ichma-ich tsikli - tashqi va ichki tsikllar
print("=== ODDIY ICHMA-ICH TSIKL ===")  # sarlavha
for i in range(3):  # tashqi tsikl: 0-2
    print(f"Tashqi tsikl: {i}")  # tashqi qiymatni chiqarish
    for j in range(2):  # ichki tsikl: 0-1
        print(f"  Ichki tsikl: {j}")  # ichki qiymatni chiqarish

# Ko'paytirish jadvali - 5x5 jadval
print("\n=== KO'PAYTIRISH JADVALI ===")  # sarlavha
for i in range(1, 6):  # 1-5 qatorlar
    for j in range(1, 6):  # 1-5 ustunlar
        natija = i * j  # ko'paytirish
        print(f"{natija:3d}", end=" ")  # 3 joy bilan chiqarish
    print()  # Keyingi qatorga o'tish

# Yulduzcha naqsh - to'rtburchak chizish
print("\n=== YULDUZCHA NAQSHLARI ===")  # sarlavha

# To'rtburchak - 4 qator, 6 ustun yulduzcha
print("To'rtburchak:")  # sarlavha
for i in range(4):  # 4 qator
    for j in range(6):  # 6 ustun
        print("*", end="")  # yulduzcha chiqarish
    print()  # qator oxiri

# Uchburchak - o'sib boruvchi yulduzchalar
print("\nUchburchak:")  # sarlavha
for i in range(5):  # 0-4
    for j in range(i + 1):  # 1 dan i+1 gacha
        print("*", end="")  # yulduzcha
    print()  # qator oxiri

# Teskari uchburchak - kamayib boruvchi
print("\nTeskari uchburchak:")  # sarlavha
for i in range(5, 0, -1):  # 5 dan 1 gacha
    for j in range(i):  # i ta yulduzcha
        print("*", end="")  # yulduzcha
    print()  # qator oxiri

# Piramida - markazlangan uchburchak
print("\nPiramida:")  # sarlavha
for i in range(5):  # 0-4
    # Bo'shliqlar - chapdagi bo'shliqlar
    for j in range(5 - i - 1):  # bo'shliq soni
        print(" ", end="")  # bo'shliq chiqarish
    # Yulduzchalar - 2*i +1 ta yulduzcha
    for k in range(2 * i + 1):  # yulduzchalar soni
        print("*", end="")  # yulduzcha
    print()  # qator oxiri

# Romb - yuqori va pastki qismlar
print("\nRomb:")  # sarlavha
n = 5  # romb o'lchami
# Yuqori qism - o'sib boruvchi
for i in range(n):  # 0 dan n-1
    for j in range(n - i - 1):  # bo'shliqlar
        print(" ", end="")  # bo'shliq
    for k in range(2 * i + 1):  # yulduzchalar
        print("*", end="")  # yulduzcha
    print()  # qator oxiri

# Pastki qism - kamayib boruvchi
for i in range(n - 2, -1, -1):  # n-2 dan 0 gacha teskari
    for j in range(n - i - 1):  # bo'shliqlar
        print(" ", end="")  # bo'shliq
    for k in range(2 * i + 1):  # yulduzchalar
        print("*", end="")  # yulduzcha
    print()  # qator oxiri

# Matritsa yaratish va chiqarish - 3x4 matritsa
print("\n=== MATRITSA ===")  # sarlavha
qator = 3  # qator soni
ustun = 4  # ustun soni
matritsa = []  # bo'sh ro'yxat

# Matritsani to'ldirish - ichma-ich tsikllar bilan to'ldirish
for i in range(qator):  # qatorlar bo'yicha
    qator_list = []  # yangi qator ro'yxati
    for j in range(ustun):  # ustunlar bo'yicha
        qiymat = (i + 1) * (j + 1)  # Oddiy formula bo'yicha qiymat
        qator_list.append(qiymat)  # qatorga qo'shish
    matritsa.append(qator_list)  # matritsaga qo'shish

# Matritsani chiqarish - ichma-ich tsikllar bilan chiqarish
print("Matritsa:")  # sarlavha
for i in range(len(matritsa)):  # qatorlar bo'yicha
    for j in range(len(matritsa[i])):  # ustunlar bo'yicha
        print(f"{matritsa[i][j]:3d}", end=" ")  # 3 joy bilan chiqarish
    print()  # qator oxiri

# Ikki matritsa qo'shish - ikkita matritsani qo'shish
print("\n=== IKKI MATRITSA QO'SHISH ===")  # sarlavha
matritsa1 = [[1, 2, 3], [4, 5, 6]]  # birinchi matritsa
matritsa2 = [[7, 8, 9], [10, 11, 12]]  # ikkinchi matritsa
natija_matritsa = []  # natija ro'yxati

for i in range(len(matritsa1)):  # qatorlar bo'yicha
    qator = []  # yangi qator
    for j in range(len(matritsa1[i])):  # ustunlar bo'yicha
        yigindi = matritsa1[i][j] + matritsa2[i][j]  # elementlarni qo'shish
        qator.append(yigindi)  # qatorga qo'shish
    natija_matritsa.append(qator)  # natijaga qo'shish

print("Birinchi matritsa:")  # sarlavha
for qator in matritsa1:  # qatorlar bo'yicha
    for element in qator:  # elementlar bo'yicha
        print(f"{element:3d}", end=" ")  # chiqarish
    print()  # qator oxiri

print("\nIkkinchi matritsa:")  # sarlavha
for qator in matritsa2:  # qatorlar bo'yicha
    for element in qator:  # elementlar
        print(f"{element:3d}", end=" ")  # chiqarish
    print()  # oxiri

print("\nYig'indi matritsa:")  # sarlavha
for qator in natija_matritsa:  # qatorlar bo'yicha
    for element in qator:  # elementlar
        print(f"{element:3d}", end=" ")  # chiqarish
    print()  # oxiri
```

---

## 21. Ro'yxatlar, to'plamlar va kortejlar (Lists, Sets, Tuples)

**Izoh:** Python-da ma'lumotlarni saqlashning uch xil usuli: o'zgaruvchan ro'yxatlar, noyob to'plamlar va o'zgarmas kortejlar.

**Misol (izohlangan kod):**
```python
# RO'YXATLAR (Lists) - o'zgaruvchan, tartibli - ro'yxat bilan ishlash
print("=== RO'YXATLAR (LISTS) ===")  # sarlavha
mevalar = ["olma", "nok", "uzum", "banan"]  # ro'yxat yaratish
print(f"Asl ro'yxat: {mevalar}")  # asl ro'yxatni chiqarish

# Element qo'shish - ro'yxatga elementlar qo'shish
mevalar.append("apelsin")        # Oxiriga qo'shish - apelsin qo'shish
mevalar.insert(1, "shaftoli")    # 1-indeksga qo'shish - shaftoli qo'shish
print(f"Qo'shgandan keyin: {mevalar}")  # yangisini chiqarish

# Element o'chirish - ro'yxatdan elementlarni o'chirish
mevalar.remove("nok")            # Qiymat bo'yicha o'chirish - nok ni o'chirish
olib_tashlangan = mevalar.pop()  # Oxirgisini olish va o'chirish
print(f"O'chirgandan keyin: {mevalar}")  # yangisini chiqarish
print(f"Olib tashlangan: {olib_tashlangan}")  # olib tashlanganini chiqarish

# Ro'yxat metodlari - raqamli ro'yxat bilan metodlar
raqamlar = [3, 1, 4, 1, 5, 9, 2, 6, 5]  # raqamlar ro'yxati
print(f"\nRaqamlar: {raqamlar}")  # ro'yxatni chiqarish
print(f"Uzunlik: {len(raqamlar)}")  # uzunlik (len)
print(f"Maksimal: {max(raqamlar)}")  # maksimal qiymat
print(f"Minimal: {min(raqamlar)}")  # minimal qiymat
print(f"1 soni necha marta: {raqamlar.count(1)}")  # 1 ning soni
print(f"4 sonining joyi: {raqamlar.index(4)}")  # 4 ning indeksi

# Saralash - ro'yxatni tartiblash
raqamlar.sort()  # o'sish tartibida sortlash
print(f"O'sish tartibida: {raqamlar}")  # chiqarish
raqamlar.sort(reverse=True)  # kamayish tartibida
print(f"Kamayish tartibida: {raqamlar}")  # chiqarish

# TO'PLAMLAR (Sets) - noyob elementlar, tartibsiz - noyob qiymatlar
print("\n=== TO'PLAMLAR (SETS) ===")  # sarlavha
sonlar = {1, 2, 3, 4, 5, 5, 5}  # Takrorlanuvchi 5-lar o'chadi - to'plam yaratish
print(f"To'plam: {sonlar}")  # chiqarish

# Element qo'shish/o'chirish - to'plamga o'zgartirish
sonlar.add(6)  # 6 ni qo'shish
sonlar.remove(1)  # 1 ni o'chirish (yoki discard(1) - xatolik bermaydi)
print(f"O'zgargandan keyin: {sonlar}")  # yangisini chiqarish

# To'plamlar ustida amallar - ikkita to'plam bilan amallar
A = {1, 2, 3, 4, 5}  # A to'plami
B = {4, 5, 6, 7, 8}  # B to'plami

print(f"A to'plam: {A}")  # chiqarish
print(f"B to'plam: {B}")  # chiqarish
print(f"Birlashma (union): {A | B}")  # birlashma
print(f"Kesishma (intersection): {A & B}")  # kesishma
print(f"Ayirma (difference): {A - B}")  # ayirma

# KORTEJLAR (Tuples) - o'zgarmas, tartibli - kortej bilan ishlash
print("\n=== KORTEJLAR (TUPLES) ===")  # sarlavha
koordinata = (10, 20)  # kortej yaratish
print(f"Koordinata: {koordinata}")  # chiqarish
print(f"X: {koordinata[0]}, Y: {koordinata[1]}")  # indeks orqali olish

# Kortej unpacking - qiymatlarni ajratish
x, y = koordinata  # x va y ga ajratish
print(f"X = {x}, Y = {y}")  # chiqarish

# Bir nechta qiymatni qaytarish - funksiyadan kortej qaytarish
def get_info():  # funksiya ta'rifi
    ism = "Ahmad"  # ism
    yosh = 25  # yosh
    shahar = "Toshkent"  # shahar
    return ism, yosh, shahar  # Bu aslida kortej - kortej qaytarish

talaba_info = get_info()  # funksiyani chaqirish
print(f"Talaba info: {talaba_info}")  # kortejni chiqarish

# Unpacking - qiymatlarni ajratish
ism, yosh, shahar = get_info()  # ism, yosh, shaharga ajratish
print(f"Ism: {ism}, Yosh: {yosh}, Shahar: {shahar}")  # chiqarish

# REAL MISOLLAR - talabalar va baholar ro'yxati
print("\n=== REAL MISOLLAR ===")  # sarlavha

# Talabalar va baholar - ikkita ro'yxat bilan ishlash
talabalar = ["Ahmad", "Fatima", "Bobur", "Zarina"]  # talabalar ro'yxati
baholar = [85, 92, 78, 96]  # baholar ro'yxati

print("Talabalar va baholar:")  # sarlavha
for i in range(len(talabalar)):  # indeks bo'yicha tsikl
    print(f"{talabalar[i]}: {baholar[i]} ball")  # talaba va bahoni chiqarish

# Yoki zip bilan - ikkita ro'yxatni birlashtirish
print("\nzip bilan:")  # sarlavha
for talaba, baho in zip(talabalar, baholar):  # zip orqali juftlash
    print(f"{talaba}: {baho} ball")  # chiqarish

# Noyob elementlarni topish - matndan noyob harflar
matn = "python dasturlash"  # matn
noyob_harflar = set(matn)  # set orqali noyob harflar
print(f"\nMatndagi noyob harflar: {noyob_harflar}")  # chiqarish

# Eng ko'p takrorlangan element - Counter orqali
from collections import Counter  # Counter import
so_zlar = ["olma", "nok", "olma", "uzum", "nok", "olma"]  # so'zlar ro'yxati
hisoblagich = Counter(so_zlar)  # hisoblagich yaratish
print(f"So'zlar soni: {hisoblagich}")  # sonlar
print(f"Eng ko'p: {hisoblagich.most_common(1)}")  # eng ko'pini olish

# Ro'yxatlarni birlashtirish - ism va familiya birlashtirish
familiya = ["Karimov", "Sodiqov", "Rahimov"]  # familiyalar
ism = ["Ali", "Vali", "Gani"]  # ismlar
to_liq_ism = []  # bo'sh ro'yxat

for i in range(len(ism)):  # indeks bo'yicha
    to_liq_ism.append(f"{ism[i]} {familiya[i]}")  # birlashtirib qo'shish

print(f"\nTo'liq ismlar: {to_liq_ism}")  # chiqarish
```

---

## 22. Xarid qilish dasturi (Shopping Cart Program)

**Izoh:** Mahsulotlarni qo'shish, o'chirish va umumiy narxni hisoblaydigan xarid savati dasturi.

**Misol (izohlangan kod):**
```python
# Xarid qilish dasturi - onlayn do'kon simulyatsiyasi
print("=== XARID QILISH DASTURI ===")  # sarlavha

# Mahsulotlar va narxlar - lug'at bilan mahsulotlar
mahsulotlar = {  # lug'at yaratish
    "non": 3000,  # non narxi
    "sut": 12000,  # sut narxi
    "tuxum": 18000,  # tuxum
    "piyoz": 8000,  # piyoz
    "kartoshka": 6000,  # kartoshka
    "go'sht": 75000,  # go'sht
    "tovuq": 45000,  # tovuq
    "olma": 15000,  # olma
    "uzum": 25000,  # uzum
    "guruch": 14000  # guruch
}

# Xarid savati - lug'at bilan savatcha
savatcha = {}  # bo'sh lug'at
umumiy_narx = 0  # umumiy narx (dasturda ishlatilmagan, balki hisoblash uchun)

def mahsulotlar_royxatini_korsat():  # mahsulotlarni ko'rsatish funksiyasi
    """Mavjud mahsulotlar ro'yxatini ko'rsatish"""  # docstring
    print("\n=== MAVJUD MAHSULOTLAR ===")  # sarlavha
    print(f"{'Mahsulot':<12} {'Narxi (so'm)':<12}")  # jadval sarlavhasi
    print("-" * 25)  # chiziq
    for mahsulot, narx in mahsulotlar.items():  # lug'at bo'yicha tsikl
        print(f"{mahsulot:<12} {narx:<12,}")  # mahsulot va narxni chiqarish

def savatcha_korsat():  # savatchani ko'rsatish funksiyasi
    """Savatcha tarkibini ko'rsatish"""  # docstring
    if not savatcha:  # agar bo'sh bo'lsa
        print("\nSavatchangiz bo'sh!")  # xabar
        return  # funksiyadan chiqish
    
    print("\n=== SAVATCHANGIZ ===")  # sarlavha
    print(f"{'Mahsulot':<12} {'Miqdor':<8} {'Narx':<12} {'Jami':<12}")  # jadval sarlavhasi
    print("-" * 50)  # chiziq
    
    jami = 0  # jami summa
    for mahsulot, miqdor in savatcha.items():  # savatcha bo'yicha tsikl
        narx = mahsulotlar[mahsulot]  # narxni olish
        mahsulot_jami = narx * miqdor  # mahsulot jami
        jami += mahsulot_jami  # umumiyga qo'shish
        
        print(f"{mahsulot:<12} {miqdor:<8} {narx:<12,} {mahsulot_jami:<12,}")  # chiqarish
    
    print("-" * 50)  # chiziq
    print(f"UMUMIY NARX: {jami:,} so'm")  # umumiy narx

def mahsulot_qoshish():  # mahsulot qo'shish funksiyasi
    """Savatga mahsulot qo'shish"""  # docstring
    mahsulotlar_royxatini_korsat()  # mahsulotlarni ko'rsatish
    
    mahsulot = input("\nQaysi mahsulotni qo'shmoqchisiz? ").lower().strip()  # mahsulot nomini olish
    
    if mahsulot not in mahsulotlar:  # mavjud emas bo'lsa
        print("Bu mahsulot mavjud emas!")  # xatolik
        return  # chiqish
    
    try:  # xatolik tutish
        miqdor = int(input(f"{mahsulot.capitalize()} dan nechta kerak? "))  # miqdorni olish
        if miqdor <= 0:  # musbat emas bo'lsa
            print("Miqdor musbat bo'lishi kerak!")  # xatolik
            return  # chiqish
        
        if mahsulot in savatcha:  # allaqachon bo'lsa
            savatcha[mahsulot] += miqdor  # miqdorni oshirish
            print(f"{mahsulot.capitalize()} savatga qo'shildi! Umumiy: {savatcha[mahsulot]} ta")  # xabar
        else:  # yangi bo'lsa
            savatcha[mahsulot] = miqdor  # qo'shish
            print(f"{miqdor} ta {mahsulot} savatga qo'shildi!")  # xabar
            
    except ValueError:  # noto'g'ri miqdor
        print("Faqat raqam kiriting!")  # xatolik

def mahsulot_ochirish():  # o'chirish funksiyasi
    """Savatdan mahsulot o'chirish"""  # docstring
    if not savatcha:  # bo'sh bo'lsa
        print("Savatcha bo'sh!")  # xabar
        return  # chiqish
    
    savatcha_korsat()  # savatchani ko'rsatish
    
    mahsulot = input("\nQaysi mahsulotni o'chirmoqchisiz? ").lower().strip()  # nomini olish
    
    if mahsulot not in savatcha:  # mavjud emas bo'lsa
        print("Bu mahsulot savatda yo'q!")  # xatolik
        return  # chiqish
    
    try:  # xatolik tutish
        print(f"Hozir savatda {savatcha[mahsulot]} ta {mahsulot} bor")  # hozirgi miqdor
        print("1. Barchasini o'chirish")  # 1-tanlov
        print("2. Ma'lum miqdorini o'chirish")  # 2-tanlov
        
        tanlov = input("Tanlovingiz (1/2): ")  # tanlov olish
        
        if tanlov == "1":  # barchasini
            del savatcha[mahsulot]  # lug'atdan o'chirish
            print(f"{mahsulot.capitalize()} savatdan olib tashlandi!")  # xabar
        elif tanlov == "2":  # miqdorni
            miqdor = int(input("Nechta o'chirmoqchisiz? "))  # miqdorni olish
            
            if miqdor >= savatcha[mahsulot]:  # butunlay o'chirish kerak bo'lsa
                del savatcha[mahsulot]  # o'chirish
                print(f"{mahsulot.capitalize()} butunlay olib tashlandi!")  # xabar
            else:  # qisman
                savatcha[mahsulot] -= miqdor  # miqdorni kamaytirish
                print(f"{miqdor} ta {mahsulot} olib tashlandi. Qoldi: {savatcha[mahsulot]} ta")  # xabar
        
        else:  # noto'g'ri tanlov
            print("Noto'g'ri tanlov!")  # xatolik
            
    except ValueError:  # noto'g'ri miqdor
        print("Faqat raqam kiriting!")  # xatolik

def hisob_chiqarish():  # hisob chiqarish funksiyasi
    """Yakuniy hisob"""  # docstring
    if not savatcha:  # bo'sh bo'lsa
        print("Savatcha bo'sh!")  # xabar
        return  # chiqish
    
    savatcha_korsat()  # savatchani ko'rsatish
    
    # Chegirma hisoblash - umumiy summani hisoblash
    jami = sum(mahsulotlar[mahsulot] * miqdor for mahsulot, miqdor in savatcha.items())  # jami summa
    
    if jami > 100000:  # agar 100000 dan ortiq bo'lsa
        chegirma_foiz = 10  # 10% chegirma
        chegirma_summa = jami * chegirma_foiz / 100  # chegirma summa
        yakuniy_narx = jami - chegirma_summa  # yakuniy narx
        
        print(f"\n🎉 100,000 so'mdan ortiq xarid qildingiz!")  # xabar
        print(f"Chegirma ({chegirma_foiz}%): -{chegirma_summa:,.0f} so'm")  # chegirma chiqarish
        print(f"To'laydigan summa: {yakuniy_narx:,.0f} so'm")  # yakuniy
    else:  # chegirmasiz
        print(f"\nTo'laydigan summa: {jami:,} so'm")  # jami chiqarish
    
    tasdiqlash = input("\nXaridni tasdiqlaysizmi? (ha/yo'q): ").lower()  # tasdiqlash olish
    
    if tasdiqlash in ['ha', 'yes', 'y']:  # ha bo'lsa
        print("\n✅ Xaridingiz uchun rahmat!")  # rahmat
        print("Yetkazib berish 1-2 kun ichida amalga oshiriladi.")  # yetkazish xabari
        savatcha.clear()  # Savatni tozalash - savatchani bo'shatish
    else:  # yo'q bo'lsa
        print("Xarid bekor qilindi.")  # bekor xabari

# Asosiy dastur - cheksiz tsikl bilan menyuni takrorlash
while True:  # cheksiz tsikl
    print("\n" + "="*40)  # chiziq
    print("       ONLAYN DO'KON MENYUSI")  # menyusi sarlavha
    print("="*40)  # chiziq
    print("1. Mahsulotlarni ko'rish")  # 1
    print("2. Savatga qo'shish")  # 2
    print("3. Savatdan o'chirish")  # 3
    print("4. Savatni ko'rish")  # 4
    print("5. Hisob chiqarish")  # 5
    print("6. Chiqish")  # 6
    print("="*40)  # chiziq
    
    tanlov = input("Tanlovingizni kiriting (1-6): ")  # tanlov olish
    
    if tanlov == "1":  # mahsulotlarni ko'rish
        mahsulotlar_royxatini_korsat()  # funksiya chaqirish
    elif tanlov == "2":  # qo'shish
        mahsulot_qoshish()  # funksiya
    elif tanlov == "3":  # o'chirish
        mahsulot_ochirish()  # funksiya
    elif tanlov == "4":  # ko'rish
        savatcha_korsat()  # funksiya
    elif tanlov == "5":  # hisob
        hisob_chiqarish()  # funksiya
    elif tanlov == "6":  # chiqish
        print("Xayr! Keyingi safar ko'rishguncha! 👋")  # xayrlashuv
        break  # tsikldan chiqish
    else:  # noto'g'ri
        print("❌ Noto'g'ri tanlov! 1-6 oralig'ida kiriting.")  # xatolik
```

---

## 23. Ikki o'lchovli to'plamlar (2D Collections)

**Izoh:** Matritsa, jadval ko'rinishidagi ma'lumotlar tuzilmasi. Ro'yxat ichida ro'yxatlar.

**Misol (izohlangan kod):**
```python
# 2D Collections - Ikki o'lchovli to'plamlar - matritsa bilan ishlash
print("=== IKKI O'LCHOVLI TO'PLAMLAR ===")  # sarlavha

# 2D ro'yxat yaratish - ro'yxat ichida ro'yxat
matritsa = [  # matritsa ro'yxati
    [1, 2, 3],  # birinchi qator
    [4, 5, 6],   # ikkinchi
    [7, 8, 9]  # uchinchi
]

print("3x3 matritsa:")  # sarlavha
for qator in matritsa:  # qatorlar bo'yicha
    for element in qator:  # elementlar bo'yicha
        print(f"{element:3d}", end=" ")  # 3 joy bilan chiqarish
    print()  # qator oxiri

# Elementga murojaat - matritsa elementlariga indeks orqali
print(f"\nmatritsa[1][2] = {matritsa[1][2]}")  # 2-qator, 3-ustun (6)
print(f"matritsa[0][0] = {matritsa[0][0]}")    # 1-qator, 1-ustun (1)

# 2D ro'yxatni dinamik yaratish - o'lcham bo'yicha matritsa to'ldirish
qator_soni = 4  # qatorlar
ustun_soni = 5  # ustunlar
dinamik_matritsa = []  # bo'sh matritsa

for i in range(qator_soni):  # qatorlar bo'yicha
    qator = []  # yangi qator
    for j in range(ustun_soni):  # ustunlar bo'yicha
        qiymat = i * ustun_soni + j + 1  # 1, 2, 3, ... tartibda qiymat hisoblash
        qator.append(qiymat)  # qatorga qo'shish
    dinamik_matritsa.append(qator)  # matritsaga qo'shish

print(f"\n{qator_soni}x{ustun_soni} dinamik matritsa:")  # sarlavha
for qator in dinamik_matritsa:  # qatorlar bo'yicha
    for element in qator:  # elementlar
        print(f"{element:3d}", end=" ")  # chiqarish
    print()  # oxiri
```

**Eslatma:** Faylning qolgan qismi (24 dan 100 gacha bo'limlar) truncatlangan bo'lib, shuning uchun ularni izohlamadim. Agar to'liq fayl bo'lsa, shunga o'xshash tarzda davom ettirish mumkin. Bu izohlangan versiya asl faylning boshlanish qismiga asoslangan.