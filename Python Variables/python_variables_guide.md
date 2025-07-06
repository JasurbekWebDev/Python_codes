# Python O'zgaruvchilari - To'liq Qo'llanma

## Mundarija
1. [O'zgaruvchi nima?](#ozgaruvchi-nima)
2. [O'zgaruvchilarni e'lon qilish](#ozgaruvchilarni-elon-qilish)
3. [O'zgaruvchi nomlash qoidalari](#ozgaruvchi-nomlash-qoidalari)
4. [O'zgaruvchilarni ishlatish bo'yicha maslahatlar](#ozgaruvchilarni-ishlatish-boyicha-maslahatlar)
5. [Amaliy misollar](#amaliy-misollar)

---

## 1. O'zgaruvchi nima?

O'zgaruvchi (variable) - bu dastur xotirasida ma'lumotlarni saqlash uchun ishlatiladigan nom yoki identifikator. Python tilida o'zgaruvchi qiymatni saqlash uchun konteyner vazifasini bajaradi.

### Asosiy xususiyatlari:
- O'zgaruvchi qiymati dastur davomida o'zgarishi mumkin
- Har xil turdagi ma'lumotlarni saqlash mumkin (raqam, matn, ro'yxat va boshqalar)
- Python tilida o'zgaruvchi turini oldindan belgilash shart emas (dinamik tipizatsiya)

### Qisqa misol:
```python
ism = "Ahmad"
yosh = 25
```

---

## 2. O'zgaruvchilarni e'lon qilish

Python tilida o'zgaruvchi e'lon qilish uchun maxsus kalit so'zlar ishlatilmaydi. Shunchaki o'zgaruvchi nomini yozib, unga qiymat beriladi.

### Asosiy sintaksis:
```python
ozgaruvchi_nomi = qiymat
```

### Turli xil ma'lumot turlari:

#### Raqamli ma'lumotlar:
```python
# Butun sonlar (int)
yosh = 25
soni = 100

# O'nlik sonlar (float)
narx = 15.99
pi = 3.14159

# Kompleks sonlar (complex)
z = 3 + 4j
```

#### Matnli ma'lumotlar:
```python
# String (str)
ism = "Ahmad"
familiya = 'Karimov'
manzil = """Toshkent shahri,
Mirzo Ulug'bek tumani"""
```

#### Mantiqiy ma'lumotlar:
```python
# Boolean (bool)
togri = True
notogri = False
```

#### Maxsus qiymat:
```python
# None
bosh_qiymat = None
```

### Bir vaqtda bir nechta o'zgaruvchi e'lon qilish:
```python
# Bir xil qiymat
a = b = c = 10

# Har xil qiymatlar
x, y, z = 1, 2, 3
ism, yosh, shahar = "Ali", 30, "Samarqand"
```

---

## 3. O'zgaruvchi nomlash qoidalari

### Majburiy qoidalar:
1. **Harf yoki pastki chiziq bilan boshlash**: O'zgaruvchi nomi harf (a-z, A-Z) yoki pastki chiziq (_) bilan boshlanishi kerak
2. **Raqam bilan boshlanmasligi**: O'zgaruvchi nomi raqam bilan boshlanishi mumkin emas
3. **Faqat ruxsat etilgan belgilar**: Harf, raqam va pastki chiziq (_) ishlatish mumkin
4. **Bo'sh joy bo'lmasligi**: O'zgaruvchi nomida bo'sh joy bo'lishi mumkin emas
5. **Kalit so'zlar emas**: Python kalit so'zlarini o'zgaruvchi nomi sifatida ishlatish mumkin emas

### To'g'ri misollar:
```python
# To'g'ri
ism = "Ali"
yosh_1 = 25
_maxfiy = "parol"
PI = 3.14159
isActive = True
user_name = "admin"
```

### Noto'g'ri misollar:
```python
# Noto'g'ri
2ism = "Ali"          # Raqam bilan boshlangan
ism-familiya = "Ali"  # Chiziqcha ishlatilgan
if = 10              # Kalit so'z
user name = "admin"  # Bo'sh joy
```

### Python kalit so'zlari:
```python
# Bu so'zlarni o'zgaruvchi nomi sifatida ishlatish mumkin emas:
False, None, True, and, as, assert, break, class, continue, 
def, del, elif, else, except, finally, for, from, global, 
if, import, in, is, lambda, nonlocal, not, or, pass, raise, 
return, try, while, with, yield
```

### Yaxshi amaliyotlar:
```python
# Yaxshi
user_age = 25
total_price = 150.50
is_valid = True
MAX_SIZE = 100

# Yomon
a = 25
tp = 150.50
flag = True
```

---

## 4. O'zgaruvchilarni ishlatish bo'yicha maslahatlar

### 1. Tushunarli nomlar tanlash
```python
# Yaxshi
student_count = 30
monthly_salary = 5000000

# Yomon
n = 30
ms = 5000000
```

### 2. Nomlar konvensiyasi
```python
# Snake case (tavsiya etiladi)
user_name = "admin"
total_amount = 1000

# Camel case (ba'zan ishlatiladi)
userName = "admin"
totalAmount = 1000

# Konstantalar uchun
MAX_USERS = 100
DEFAULT_PORT = 8080
```

### 3. O'zgaruvchi turlari bilan ishlash
```python
# Tur tekshirish
name = "Ahmad"
print(type(name))  # <class 'str'>

# Tur o'zgartirish
age_str = "25"
age_int = int(age_str)  # Stringdan int ga
price_str = str(15.99)  # Float dan string ga
```

### 4. Global va lokal o'zgaruvchilar
```python
# Global o'zgaruvchi
global_var = "Men global o'zgaruvchiman"

def my_function():
    # Lokal o'zgaruvchi
    local_var = "Men lokal o'zgaruvchiman"
    print(local_var)
    print(global_var)  # Global o'zgaruvchiga kirish

my_function()
# print(local_var)  # Xato! Lokal o'zgaruvchiga tashqaridan kirish mumkin emas
```

### 5. O'zgaruvchilarni yo'q qilish
```python
temp_var = "Vaqtinchalik"
del temp_var  # O'zgaruvchini yo'q qilish
# print(temp_var)  # Xato! O'zgaruvchi mavjud emas
```

---

## 5. Amaliy misollar

### Misol 1: Oddiy kalkulyator
```python
# Foydalanuvchidan raqamlar olish
print("=== Oddiy Kalkulyator ===")
birinchi_raqam = float(input("Birinchi raqamni kiriting: "))
ikkinchi_raqam = float(input("Ikkinchi raqamni kiriting: "))

# Hisoblash
yigindi = birinchi_raqam + ikkinchi_raqam
ayirma = birinchi_raqam - ikkinchi_raqam
kopaytma = birinchi_raqam * ikkinchi_raqam
bolish = birinchi_raqam / ikkinchi_raqam if ikkinchi_raqam != 0 else "Nolga bo'lish mumkin emas"

# Natijalarni chiqarish
print(f"Yig'indi: {yigindi}")
print(f"Ayirma: {ayirma}")
print(f"Ko'paytma: {kopaytma}")
print(f"Bo'lish: {bolish}")
```

### Misol 2: Talaba ma'lumotlari
```python
# Talaba ma'lumotlari
print("=== Talaba Ma'lumotlari ===")
talaba_ismi = input("Talaba ismini kiriting: ")
talaba_yoshi = int(input("Talaba yoshini kiriting: "))
talaba_kursi = int(input("Qaysi kursda o'qiydi: "))
talaba_bahosi = float(input("O'rtacha bahosini kiriting: "))

# Ma'lumotlarni saqlash
talaba_malumotlari = {
    "ism": talaba_ismi,
    "yosh": talaba_yoshi,
    "kurs": talaba_kursi,
    "baho": talaba_bahosi
}

# Natijalarni chiqarish
print("\n=== Talaba Ma'lumotlari ===")
print(f"Ism: {talaba_malumotlari['ism']}")
print(f"Yosh: {talaba_malumotlari['yosh']}")
print(f"Kurs: {talaba_malumotlari['kurs']}")
print(f"O'rtacha baho: {talaba_malumotlari['baho']}")

# Baholash
if talaba_bahosi >= 4.5:
    baho_darajasi = "A'lo"
elif talaba_bahosi >= 3.5:
    baho_darajasi = "Yaxshi"
elif talaba_bahosi >= 2.5:
    baho_darajasi = "Qoniqarli"
else:
    baho_darajasi = "Qoniqarsiz"

print(f"Baho darajasi: {baho_darajasi}")
```

### Misol 3: Do'kon hisob-kitobi
```python
# Do'kon hisob-kitobi
print("=== Do'kon Hisob-kitobi ===")

# Mahsulotlar va narxlari
mahsulotlar = {
    "non": 3000,
    "sut": 8000,
    "tuxum": 15000,
    "go'sht": 85000,
    "sabzi": 5000
}

# Xaridlar ro'yxati
xaridlar = []
umumiy_summa = 0

print("Mavjud mahsulotlar:")
for mahsulot, narx in mahsulotlar.items():
    print(f"{mahsulot}: {narx} so'm")

print("\nXaridlarni kiriting (to'xtatish uchun 'stop' yozing):")

while True:
    mahsulot_nomi = input("Mahsulot nomini kiriting: ").lower()
    
    if mahsulot_nomi == 'stop':
        break
    
    if mahsulot_nomi in mahsulotlar:
        miqdor = int(input(f"{mahsulot_nomi} miqdorini kiriting: "))
        narx = mahsulotlar[mahsulot_nomi] * miqdor
        
        xarid_malumoti = {
            "mahsulot": mahsulot_nomi,
            "miqdor": miqdor,
            "narx": narx
        }
        
        xaridlar.append(xarid_malumoti)
        umumiy_summa += narx
        print(f"{mahsulot_nomi} qo'shildi: {narx} so'm")
    else:
        print("Bunday mahsulot yo'q!")

# Chek chiqarish
print("\n=== CHEK ===")
print("-" * 30)
for xarid in xaridlar:
    print(f"{xarid['mahsulot']} x {xarid['miqdor']} = {xarid['narx']} so'm")

print("-" * 30)
print(f"Umumiy summa: {umumiy_summa} so'm")

# Chegirma hisoblash
if umumiy_summa > 100000:
    chegirma = umumiy_summa * 0.1
    yakuniy_summa = umumiy_summa - chegirma
    print(f"Chegirma (10%): {chegirma} so'm")
    print(f"To'lash kerak: {yakuniy_summa} so'm")
else:
    print(f"To'lash kerak: {umumiy_summa} so'm")
```

### Misol 4: Ob-havo ma'lumotlari
```python
# Ob-havo ma'lumotlari
print("=== Ob-havo Ma'lumotlari ===")

# Haftalik harorat ma'lumotlari
hafta_kunlari = ["Dushanba", "Seshanba", "Chorshanba", "Payshanba", "Juma", "Shanba", "Yakshanba"]
haroratlar = []

# Haroratlarni kiritish
for kun in hafta_kunlari:
    harorat = float(input(f"{kun} kuni haroratni kiriting (°C): "))
    haroratlar.append(harorat)

# Statistika hisoblash
ortacha_harorat = sum(haroratlar) / len(haroratlar)
eng_issiq_kun = hafta_kunlari[haroratlar.index(max(haroratlar))]
eng_sovuq_kun = hafta_kunlari[haroratlar.index(min(haroratlar))]
eng_yuqori_harorat = max(haroratlar)
eng_past_harorat = min(haroratlar)

# Natijalarni chiqarish
print("\n=== Haftalik Ob-havo Hisoboti ===")
print("-" * 40)
for i, kun in enumerate(hafta_kunlari):
    print(f"{kun}: {haroratlar[i]}°C")

print("-" * 40)
print(f"O'rtacha harorat: {ortacha_harorat:.1f}°C")
print(f"Eng issiq kun: {eng_issiq_kun} ({eng_yuqori_harorat}°C)")
print(f"Eng sovuq kun: {eng_sovuq_kun} ({eng_past_harorat}°C)")

# Tavsiyalar
if ortacha_harorat > 30:
    tavsiya = "Havo juda issiq. Soyada qoling va ko'p suv iching."
elif ortacha_harorat < 10:
    tavsiya = "Havo juda sovuq. Iliq kiyining va salqindan saqlaning."
else:
    tavsiya = "Havo qulay. Yaxshi vaqt o'tkazing!"

print(f"\nTavsiya: {tavsiya}")
```

### Misol 5: Parol tekshiruvchi
```python
import re

# Parol tekshiruvchi
print("=== Parol Tekshiruvchi ===")

def parol_tekshir(parol):
    """Parol kuchliligini tekshirish"""
    natija = {
        "uzunlik": len(parol) >= 8,
        "kichik_harf": bool(re.search(r'[a-z]', parol)),
        "katta_harf": bool(re.search(r'[A-Z]', parol)),
        "raqam": bool(re.search(r'[0-9]', parol)),
        "maxsus_belgi": bool(re.search(r'[!@#$%^&*(),.?":{}|<>]', parol))
    }
    return natija

# Foydalanuvchidan parol olish
user_parol = input("Parolingizni kiriting: ")

# Parolni tekshirish
tekshiruv_natijasi = parol_tekshir(user_parol)

# Natijalarni chiqarish
print("\n=== Parol Tekshiruv Natijasi ===")
print(f"Uzunlik (kamida 8 ta): {'✓' if tekshiruv_natijasi['uzunlik'] else '✗'}")
print(f"Kichik harf: {'✓' if tekshiruv_natijasi['kichik_harf'] else '✗'}")
print(f"Katta harf: {'✓' if tekshiruv_natijasi['katta_harf'] else '✗'}")
print(f"Raqam: {'✓' if tekshiruv_natijasi['raqam'] else '✗'}")
print(f"Maxsus belgi: {'✓' if tekshiruv_natijasi['maxsus_belgi'] else '✗'}")

# Kuchlilik darajasi
kuchlilik_ball = sum(tekshiruv_natijasi.values())

if kuchlilik_ball == 5:
    kuchlilik = "Juda kuchli"
elif kuchlilik_ball >= 4:
    kuchlilik = "Kuchli"
elif kuchlilik_ball >= 3:
    kuchlilik = "O'rtacha"
else:
    kuchlilik = "Zaif"

print(f"\nParol kuchliligi: {kuchlilik} ({kuchlilik_ball}/5)")
```

---

## Xulosa

Python o'zgaruvchilari dasturlashning asosiy tushunchalaridan biridir. Ular yordamida:
- Ma'lumotlarni saqlash va boshqarish
- Dastur mantiqini qurilish
- Foydalanuvchi bilan o'zaro ta'sir qilish
- Murakkab hisob-kitoblarni bajarish

O'zgaruvchilar bilan ishlashda asosiy qoidalar:
1. **Tushunarli nomlar tanlash**
2. **Nomlar konvensiyasiga rioya qilish**
3. **To'g'ri ma'lumot turlarini ishlatish**
4. **Global va lokal o'zgaruvchilarni to'g'ri boshqarish**
5. **Xotirani samarali ishlatish**

Ushbu qo'llanma Python tilida o'zgaruvchilar bilan ishlashning asosiy tamoyillarini o'rgatadi va amaliy misollar orqali bilimlarni mustahkamlash imkonini beradi.

---

**Maslahat:** Har doim amaliyot qiling va turli xil misollar ustida ishlang. Dasturlashni faqat nazariy o'rganish kifoya qilmaydi - amaliyot muhim!