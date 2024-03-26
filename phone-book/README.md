# PhoneBook Akıllı Sözleşmesi

Bu akıllı sözleşme, isim ve telefon numaralarını içeren bir telefon rehberini yönetir. Her bir isme karşılık gelen bir telefon numarası saklar.

## Kullanılan Modüller

- **HashMap Modülü:** Anahtar-değer çiftlerini saklamak için kullanılır.
- **Text Modülü:** Metin verileriyle çalışmak için kullanılır.

## Actor Yapısı

PhoneBook actor'ü, isim ve telefon numaralarını saklamak için bir HashMap kullanır.

## Tanımlanan Veri Tipleri

- **Name:** Metin türünde bir isim.
- **Phone:** Metin türünde bir telefon numarası.
- **Entry:** Bir isim ve telefon numarasını içeren bir kayıt.

## İşlevler

- **insert(name: Name, entry: Entry):** Bir isim ve buna karşılık gelen bir kayıt ekler.
- **lookup(name: Name):** Verilen bir ismin telefon numarasını döndürür.

## Kullanım

1. Akıllı sözleşmeyi başlatmak için gerekli modülleri içe aktarın.
2. `insert` işleviyle isimler ve telefon numaraları ekleyin.
3. `lookup` işleviyle bir isme karşılık gelen telefon numarasını alın.

### Örnek Kullanım:

```motoko
import PhoneBook "phonebook";

// PhoneBook actor'ünü başlatın
let phoneBook = PhoneBook.actor();

// Bir kişi ekleyin
await phoneBook.insert("John", { desc = "John's number"; phone = "1234567890" });

// Bir kişinin telefon numarasını alın
let johnsNumber = await phoneBook.lookup("John");
```

## Katkı

Bu akıllı sözleşme projesine katkıda bulunmak isterseniz, GitHub deposunu çatallayabilir, değişikliklerinizi yapabilir ve bir pull request gönderebilirsiniz. 
