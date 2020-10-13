# storage-api
App Container projesi için geliştirilen storage-api

## Hangi Dil İle Yazıldı
`Golang`'in yüksek performansı ve düşük bellek kullanımından dolayı tercih edilmiştir. Ayrıca proje genel olarak `GoLang` ve `PostgreSql` ile yazıldığı için `APP-Container` Mantığı için projeler arası köprü bu şekilde kurulmuş olacaktır.

## Genel Amaç
Projenin amacı açıklamada söylendiği gibi App-Container projesi için gerekli olan depolama yönetim sistemini sağlamaktır. Bu sayede real-time database yanında depolama yönetim sistemi de projeye eklenerek bir bağımlılık daha ortadan kalkacaktır.

## Dosyalar Nasıl Yönetilecek

- Yüklenen dosyalar `100MB`'ten düşük ise sıkıştırılacaktır
  - `100MB` ve üzeri dosyaların zaman kaybı kazandırdığı alandan daha değerli olacağı için böyle bir sınır konulacaktır
  - Sunucu yoğunluğu %5 ve daha az ise `100MB`'ten daha büyük dosyalar parça parça sıkıştırılacaktır.
- Varsayılan video formatı `webm`dir ve diğer formatlar `webm` formatına dönüştürülecektir.  
- Varsayılan resim formatı `webp`dir ve diğer formatlar `webp` formatına dönüştürülecektir.
  - Resimler için genişliği 720 üzeri olanlar için otomatik thumbnail resim dosyası oluşturulacaktır.
  - Thumbnail oluşturma limiti 4k çözünürlükte 4 adet, 2.5k çözünürlükte 3, full HD çözünürlükte 2 ve HD çözünürlükte 1 tanedir
  

  
