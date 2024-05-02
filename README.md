# Bebeginizin-Otizmli-Olma-Olasiligini-Hesaplama

import pandas as pd
from sklearn.tree import DecisionTreeClassifier

data = pd.read_csv("data.csv")

x = data.drop(columns=["Otizmli_Olma_Olasiligi"])
y = data["Otizmli_Olma_Olasiligi"]

model = DecisionTreeClassifier()
model.fit(x, y)

yas_degerleri = [1, 2, 3]
values = [0, 1]

yas = int()
belirti1, belirti2, belirti3, belirti4, belirti5 = int(), int(), int(), int(), int()
yas_secimi = False
while yas_secimi is not True:
    yas = int(input('Bebeğin yaşını girin(1,2,3):'))
    if yas in yas_degerleri:
        yas_secimi = True

if yas == 1:
    choice = False
    while choice is not True:
        belirti1 = int(input('Hangisi (0-1) birini seç ? (Rol Yapma Becerisi Az (0), Rol Yapabiliyor (1):'))
        if belirti1 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti2 = int(input('Hangisi (0-1) birini seç ? (Icine Kapanik (0), Sosyal Etkilesimi Sever (1):'))
        if belirti2 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti3 = int(input(
            'Hangisi (0-1) birini seç ? (Sozlu ve Sozsuz Iletisim Kurma Az (0), Sozlu ve Sozsuz Iletisim Kurmayi Sever (1):'))
        if belirti3 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti4 = int(input('Hangisi (0-1) birini seç ? (Goz temasi kurmaz (0), Goz temasi normal(1):'))
        if belirti4 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti5 = int(input(
            'Hangisi (0-1) birini seç ? (Ebeveynin sesine karsilik vermez (0), Ebeveynin sesine karsilik verir (1): '))
        if belirti5 in values:
            choice = True
    tahmin = model.predict([[yas, belirti1, belirti2, belirti3, belirti4, belirti5]])
    print(tahmin)

elif yas == 2:
    choice = False
    while choice is not True:
        belirti1 = int(input(
        'Hangisi (0-1) birini seç ? (Gorme, Isitme, Koku, Dokunma,Tat Hassasligi (0), Gorme, Isitme, Koku, Dokunma,Tat Normal (1):'))
        if belirti1 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti2 = int(input(
            'Hangisi (0-1) birini seç ? (Giysi Giymek Zorunda Kaldiklarinda Huysuzlanma (0), Giysi Giymek Zorunda Kaldiklarinda Problem Yok (1):'))
        if belirti2 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti3 = int(input(
            'Hangisi (0-1) birini seç ? (Vucut Hareketlerini Defalarca Tekrarlama (0), Vucut Hareketleri Normal (1):'))
        if belirti3 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti4 = int(
            input('Hangisi (0-1) birini seç ? (Alisilmadik Sekilde Objelere Bagli Olma (0), Objelere Baglilik Normal (1):'))
        if belirti4 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti5 = int(input(
            'Hangisi (0-1) birini seç ? (Gunluk Yasam Rutinleri Degisince Cok Sikinti Duymalari (0), Gunluk Yasam Rutinleri Degisince Cabuk Adapte Olma (1):'))
        if belirti5 in values:
            choice = True

    tahmin2 = model.predict([[yas, belirti1, belirti2, belirti3, belirti4, belirti5]])
    print(tahmin2)

elif yas == 3:
    choice = False
    while choice is not True:
        belirti1 = int(
            input('Hangisi (0-1) birini seç ? (Kelimeler Yerine Jest Kullanma (0), Kelimeleri Duzgunce Kullanma (1):'))
        if belirti1 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti2 = int(
            input('Hangisi (0-1) birini seç ? (Dilin Yavas Gelismesi Veya Hic Gelismemesi (0), Guzel Dil Gelisimi (1):'))
        if belirti2 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti3 = int(input(
            'Hangisi (0-1) birini seç ? (Nesnelere Bakmak Icin Bakis Ayarlama Guclugu (0), Nesnelere Bakmak Icin Bakis Ayarlama Problemi Yok (1):'))
        if belirti3 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti4 = int(input(
            'Hangisi (0-1) birini seç ? (Reklamlar Gibi Ezberlenmis Sozleri Durmadan Tekrarlar (0), Reklamlar Gibi Ezberlenmis Sozleri Durmadan Tekrarlamaz (1):'))
        if belirti4 in values:
            choice = True

    choice = False
    while choice is not True:
        belirti5 = int(input(
            'Hangisi (0-1) birini seç ? (Kendinden Dogru Sekilde Bahsetmez (0), Kendinden Dogru Sekilde Bahsedebilir (1):'))
        if belirti5 in values:
            choice = True

    tahmin3 = model.predict([[yas, belirti1, belirti2, belirti3, belirti4, belirti5]])
    print(tahmin3)
