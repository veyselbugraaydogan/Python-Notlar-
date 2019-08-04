# Python yorumlayıcısını kullanmak

Python yorumlayıcısını komut satırından;

```
python
python3
python3.7

```
gibi seçeneklerle çağırmak mümkün.

Ayrıca Python modülleri de 
```
python -m modul_ismi [arg] ...

```
Şeklinde çağrılabiliyor.

### Python scriptine argüman vermek

```
python script_ismi [arg] ...

```
[arg] ... -> Argüman listesi aralarında boşluk brakılarak verilebilir.

Script içinden ` import sys ` şeklinde verilen argümanlara ulaşılabilir. `sys.argv[0]`
scriptin adıdır. Eğer -m parametresi verilirse verilen argümanı modül olarak algılar 
ve 0. indis modülün ismine setlenir.? Diğer parametrelere `sys.argv[1]` , 2 .. şeklinde
erişilebilir.

### Kaynak kodu

Kaynak kodu dosyaları default olarak UTF-8 kullanır. Değiştirmek için ilk satıra 
`# -*- coding: encoding -*-` satırı yazılabilir. Örneğin : `# -*- coding: latin-1 -*-`
İlk satıra bunun yazılmasının istisnası "shebang satırı" nın en üste yazılmasıdır 
`#!/usr/bin/env python3`.
