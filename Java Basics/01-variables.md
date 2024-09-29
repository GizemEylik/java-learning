1. Değişken Nedir?
Değişken, programda kullanılacak verileri depolamak için bir isimle tanımlanmış bir bellek alanıdır.
Değişkenlerin belirli bir veri türü vardır; bu tür, değişkenin hangi tür verileri tutabileceğini belirtir.

1. Değişken Türleri
Java'da değişkenler temel olarak iki ana gruba ayrılır:

Primitive (Temel) Türler:

| **Veri Türü** | **Boyut**     | **Aralık**                                                                       | **Açıklama**                                         |
|---------------|---------------|----------------------------------------------------------------------------------|------------------------------------------------------|
| `byte`        | 1 byte        | -128 ile 127                                                                     | Küçük tam sayılar için kullanılır.                   |
| `short`       | 2 bytes       | -32,768 ile 32,767                                                               | Orta boyutlu tam sayılar için kullanılır.            |
| `int`         | 4 bytes       | -2,147,483,648 ile 2,147,483,647                                                 | Tam sayılar için en yaygın kullanılan türdür.        |
| `long`        | 8 bytes       | -9,223,372,036,854,775,808 ile 9,223,372,036,854,775,807                         | Çok büyük tam sayılar için kullanılır.               |
| `float`       | 4 bytes       | Yaklaşık ±3.40282347E+38 (7 basamak hassasiyet)                                  | Ondalık sayılar için kullanılır.                     |
| `double`      | 8 bytes       | Yaklaşık ±1.79769313486231570E+308 (15 basamak hassasiyet)                       | Daha yüksek hassasiyet gerektiren ondalıklı sayılar  |
| `char`        | 2 bytes       | 0 ile 65,535 (Unicode karakterleri)                                              | Tek bir karakter depolamak için kullanılır.          |
| `boolean`     | 1 bit         | `true` veya `false`                                                              | Mantıksal değerleri depolamak için kullanılır.       |


Nesne Türleri:

Java'da nesne oluşturmak için kullanılan sınıflar ve referansları temsil eder. Değişkenler nesnelerin referanslarını tutar.
Örnekler: String, ArrayList, HashMap, Date, vb.

1. Değişken Tanımlama
Java'da bir değişken tanımlamak için aşağıdaki sözdizimi kullanılır:

veri_türü değişken_ismi = değer;

Örnek:

```java
int sayi = 10;          // Tam sayı değişkeni
double pi = 3.14;      // Ondalık sayı değişkeni
char harf = 'A';       // Karakter değişkeni
boolean dogruMu = true; // Boolean değişkeni
```

4. Değişken İsimlendirme Kuralları
Java'da değişken isimleri belirli kurallara göre oluşturulmalıdır:

İsimler harf, rakam, alt çizgi (_) veya dolar işareti ($) ile başlayabilir.
Boşluk veya özel karakterler (örneğin, @, #, %, vb.) kullanılamaz.
Java'da değişken isimleri büyük/küçük harf duyarlıdır. (örneğin, sayi ile Sayi farklıdır)
İsimler anlamlı ve açıklayıcı olmalıdır. (örneğin, ogrenciSayisi gibi)

5. Değişken Kullanımı
Değişkenler, programın farklı bölümlerinde kullanılabilir. Örneğin:

```java
public class DegiskenOrnegi {
    public static void main(String[] args) {
        int a = 5;          // Değişken tanımlama
        int b = 10;         // Başka bir değişken

        int toplam = a + b; // Değişkenleri kullanarak toplama işlemi
        System.out.println("Toplam: " + toplam); // Sonucu yazdırma
    }
}
Çıktı:
Toplam: 15
```

6. Değişken Değeri Güncelleme
Değişkenlerin değerleri programın çalışması sırasında güncellenebilir:

```java
public class DegiskenGuncelleme {
    public static void main(String[] args) {
        int sayi = 10;   // İlk değer
        System.out.println("Başlangıç değeri: " + sayi);

        sayi = 20;       // Yeni değer atama
        System.out.println("Güncellenmiş değer: " + sayi);
    }
}
Çıktı:
Başlangıç değeri: 10
Güncellenmiş değer: 20
```

7. Sabit Değişkenler (final)
Eğer bir değişkenin değeri programın ilerleyen kısımlarında değişmeyecekse, bu değişkeni final anahtar kelimesi ile tanımlayarak sabit hale getirebilirsiniz.

```java
public class SabitDegisken {
    public static void main(String[] args) {
        final int MAX_SAYI = 100; // Sabit değişken
        System.out.println("Maksimum sayı: " + MAX_SAYI);

        // MAX_SAYI = 200; // Bu satır hata verecektir
    }
}
Çıktı:
Maksimum sayı: 100
```

8. Örnek Uygulamalar
a. Farklı Değişken Türlerinin Kullanımı

```java
public class DegiskenTurleri {
    public static void main(String[] args) {
        int yas = 25;
        double boy = 1.75;
        char cinsiyet = 'E';
        boolean evliMi = false;

        System.out.println("Yaş: " + yas);
        System.out.println("Boy: " + boy);
        System.out.println("Cinsiyet: " + cinsiyet);
        System.out.println("Evli mi: " + evliMi);
    }
}
Çıktı:

Yaş: 25
Boy: 1.75
Cinsiyet: E
Evli mi: false
```

b. Kullanıcı Girdisi ile Değişken Kullanımı

```java
import java.util.Scanner;

public class KullaniciGirdisi {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Yaşınızı girin: ");
        int yas = scanner.nextInt();

        System.out.println("Girdiğiniz yaş: " + yas);

        scanner.close();
    }
}
```

Sonuç

Java'da değişkenler, veri depolamak ve yönetmek için kullanılır.
Değişkenler, programın farklı bölümlerinde kullanılabilir ve değerleri güncellenebilir.
Java'daki temel değişken türleri int, double, char, boolean gibi primitive türlerdir.
Değişken isimlendirme kurallarına dikkat edilmelidir.