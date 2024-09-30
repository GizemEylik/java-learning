

Açıklamalar:
    1. final Anahtar Kelimesi: final ifadesi, bu değişkenin değerinin daha sonra değiştirilemeyeceğini belirtir. Yukarıdaki örnekte PI sabiti 3.14159 olarak atanmıştır ve başka bir değer atanamaz.
    2. Sabit İsimlendirme Konvansiyonu: Sabitler genellikle büyük harflerle yazılır ve kelimeler arasına alt çizgi (_) eklenir. Örneğin, MAX_VALUE, MIN_AGE gibi isimlendirmeler kullanılır.
    3. Statik Sabitler (Static Constants): Sabitler genellikle static olarak tanımlanır. Bu, sabitin sınıf seviyesinde bir özellik olduğu ve her nesne için ayrı ayrı depolanmadığı anlamına gelir. static final kullanımıyla sabitler doğrudan sınıf üzerinden erişilebilir hale gelir (örneğin SabitOrnek.PI).

Sabitlerin Tanımlanması
Java'da bir değişkeni sabit yapmak için final anahtar kelimesi kullanılır. Sabitler, bir kez başlatıldığında (initialize) programın geri kalanında değiştirilemez. Bu da onların "sabit" (constant) olmasını sağlar.

Sabit Tanımlarken Kullanılan Kurallar
    • final anahtar kelimesi ile tanımlanırlar.
    • Başlangıç değerleri mutlaka verilmelidir (ilk değer atama zorunluluğu).
    • Sabit bir kez tanımlandıktan sonra değeri değiştirilemez.
    • Genellikle büyük harfler ile adlandırılır.



 ```java
public class Main {
    public static void main(String[] args) {
        final int MAX_VALUE = 100; // Sabit tanımı
        System.out.println("Max Value: " + MAX_VALUE);
        
        // MAX_VALUE = 200; // Bu satır hata verecektir çünkü sabit değiştirilmez
    }
}
```

Sabitlerin Özellikleri
Değiştirilemez: Sabit bir kez atandıktan sonra değeri değiştirilemez. Yukarıdaki örnekte MAX_VALUE sabitini değiştirmeye çalışmak derleme hatasına yol açar.
Genel Kullanım: Sabitler genellikle büyük harfle ve alt çizgi ile ayrılmış kelimelerle adlandırılır. Örneğin, PI, MAX_LENGTH.
Statik Olabilir: Sabitler, sınıf seviyesinde tanımlandığında static olarak da tanımlanabilir, böylece tüm sınıf için tek bir değer paylaşılmış olur.

Statik Sabitler
Eğer sabitin tüm nesneler için ortak olmasını istiyorsanız, onu statik olarak tanımlayabilirsiniz:

```java

public class Constants {
    public static final double PI = 3.14159; // Statik sabit
}

public class Main {
    public static void main(String[] args) {
        System.out.println("Pi: " + Constants.PI);
    }
}

```
Sabitlerin Avantajları
Değiştirilemezlik: Sabitler, değerleri bir kez belirlendikten sonra değiştirilemez. Bu, programın güvenilirliğini artırır.
Kod Okunabilirliği: Sabitlerin anlamlı isimler ile tanımlanması, kodun okunabilirliğini artırır.
Kolay Bakım: Bir sabit değiştiğinde, kodun tüm parçalarında sadece sabit tanımının güncellenmesi yeterli olur.

Kullanım Yerleri
Matematiksel Sabitler: Pi gibi matematiksel sabitler.
Hata Kodları: Uygulamada kullanılan hata kodları.
Konfigürasyon Ayarları: Uygulama ayarları (örneğin, maksimum kullanıcı sayısı, dosya yolları).

Uygulama Örneği
Aşağıdaki örnek, bir uygulamanın kullanıcı sayısını sınırlamak için sabitlerin nasıl kullanılabileceğini gösterir:

```java

public class UserManagement {
    public static final int MAX_USERS = 5; // Maksimum kullanıcı sayısı sabiti
    private int currentUserCount = 0;

    public void addUser() {
        if (currentUserCount < MAX_USERS) {
            currentUserCount++;
            System.out.println("Kullanıcı eklendi. Mevcut kullanıcı sayısı: " + currentUserCount);
        } else {
            System.out.println("Maksimum kullanıcı sayısına ulaşıldı!");
        }
    }

    public static void main(String[] args) {
        UserManagement userManagement = new UserManagement();
        for (int i = 0; i < 7; i++) { // 7 kullanıcı eklemeye çalışıyoruz
            userManagement.addUser();
        }
    }
}

```
Bu örnekte, MAX_USERS sabiti, mevcut kullanıcı sayısını kontrol etmek için kullanılır. Bu sayede, kullanıcı sayısını değiştirmek istediğinizde yalnızca sabit tanımını güncellemeniz yeterli olacaktır.