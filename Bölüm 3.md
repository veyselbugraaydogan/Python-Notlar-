# Python'a Gayri resmi Bir Giriş

### Yorum satırları

print("Tekli yorum satırları :") #Bu bir yorum satırı

print("Çoklu yorum satırları :")

"""
Burası 
Çoklu 
yorum 
satırı 

"""

### Sayılar

Pythonda +, -, *, / (aslında çoğu) operatörleri bildiğiniz gibi aynı(C deki gibi).

```
>>> 2 + 2
4
>>> 50 - 5*6
20

```
Bölme (/) her zaman kayan noktalı sayı döndürür (float).
```
>>> (50 - 5*6) / 4
5.0

```
Eğer integer bölmesi yapmak istiyorsanız // operatörünü kullanmanız gerekiyor. Kalanı 
% operatörüyle bulabilirsiniz. 

#### Üstel ifadeler

2^4 (2 üzeri 4) şu şekilde ifade edilebilir `2 ** 4`
3^2 (3 ün karesi) `3**2`

Python aynı zamanda ondalıklı, kesirli ve hatta kompleks sayıları da destekler.
(Decimal, Fraction sınıfları). Kompleş sayılar `x = 3 + 5j` şeklinde tanımlanabilir.

### Stringler

'Tek tırnak' ve "Çift tırnak" olabilirler. \ kaçış (escape) karakteri olarak 
kullanılabilir. Eğer kaçış karakterinin işe yaramasını istemiyorsanız stringi çiğ
(raw) olarak kullabilirsiniz.
```
print(r'C:\some\name')

```
Bu kod satırında r ifadesi string de kaçış karakterinin işe yaramayacağını gösteriyor
ve stringi olduğu gibi yorumluyor.

Birden fazla satırlık stringi olduğu gibi işlemek için `"""..."""` veya `'''...'''`
kullanılır.
```
print("""\
Usage: thingy [OPTIONS]
     -h                        Bu stringde satır sonları otomatik olarak var sayılır.
     -H hostname               Bunu engellemek için \ kullanılabilir.
""")

```
Stringler `+` ile toplanabilir veya `*` ile çoğaltılabilir.
İki string yan yana getirilip toplanabilir/birleştirilebilir (Concatenate).
```
'Py' 'thon'

```
gibi. Ancak bu değişkenlerle veya işleme tabi tutulurken işe yaramaz. Yani 
`Py 'thon'` birleştirme işlemi hata verir(Burada Py değişkeni içinde 'Py' değeri 
olan bir değişkeni ifade ediyor). 

String değişkenlerine bir char dizisi gibi erişilebilir. 
```
>>> word = 'Python'
>>> word[0] 
'P'

```
Ayrıca Python da dizilerin indisleri biraz garip. Örneğin biraz önceki word
değişkeninde indislerin hangi karakterlere geldiğini şöyle gösterebiliriz.

```
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1


```

Görüldüğü gibi 0. indis ve 6. indis aynı zamanda -6. indis te aynı karaktere denk 
geliyor. İlk bakışta dairesel mantıkla gidiyormuş gibi görünse de bu stringin 7.
indisi yok, -7. indisi de yok. Sadece -6 dan +6 ya kadar indislenebilir.

### Python da dilimleme (slicing)

