# Önizleme  -  [View Demo / Demo Görüntüle](https://anonimwebtr.github.io/Js-Random-Word/)

![Önizleme](https://raw.githubusercontent.com/anonimwebtr/Js-Random-Word/main/images/screenshot.PNG)

# Js Random Word

Bu projede json veya js dosyanızda tuttuğunuz güzel sözleri v.s random olarak ekrana yazdırmaya yer verilmiştir.
Çalışması için **jquery kütüphanesine ihtiyaç duyar** ve demoda çalışmaya eklenmiştir.

**Jquery kütüphanesini çalışmanıza eklemek için:**

    <script src="https://code.jquery.com/jquery-3.6.0.min.js" crossorigin="anonymous"></script>

# Örnek sozler.js / sozler.json içeriği

    sozler=[
    { "soz": "Tecrübe herkesin hatalarına verdiği isimdir.", "yazar": "Oscar Wilde"},
    { "soz": "Şikâyet ettiğiniz yaşam, belki de başkasının hayalidir.", "yazar": "Tolstoy"}, 
    ];
    
# Kendi tasarımınıza uygulamak

Verilerin (güzel sözlerin) bulunduğu dosyayı belirtin. 

    <script type="text/javascript" src="data/sozler.js"></script>

Ekrana yazıdırabilmek için gerekli javascript kodunu ekleyin.  Bir sonraki aşamada sözün gözükmesini istediğiniz alanın id değerine **`soz`**  , yazar isminin gözükmesini istediğiniz alanın id değerine **`yazar`** değerlerini vermeyi unutmayınız. Eğer demoda olduğu gibi bir button veya simgeye tıklayarak sözleri random olarak değiştirilebilir hale getirmek istiyorsanız, tasarımınızdaki ilgili buton yada nesnenin id değerini **`yeniSoz`** olarak düzenleyiniz.

      <script type="application/javascript">
        var json = sozler;
        var randomVal = Math.floor(Math.random() * json.length);
        var toplamSoz = json.length;
        
        document.getElementById("soz").innerHTML = json[randomVal].soz;
        document.getElementById("yazar").innerHTML = json[randomVal].yazar;
        
        
        $('#yeniSoz').click(function(){
        	var randomnum = Math.floor((Math.random() * json.length));
        	document.getElementById("soz").innerHTML = json[randomnum].soz;
        	document.getElementById("yazar").innerHTML = json[randomnum].yazar;
        });
        </script>

## Credits (Thnx)

 - [ ] Original PSD : [Dribbble - Ui_Note_large.png by Mathieu Odin](https://dribbble.com/shots/592046-Notepad/attachments/46821)
 - [ ] NotePad Html & Css : [Notepad - Design Bombs](https://www.designbombs.com/freebie/notepad/)
 - [ ] Js Code : [AnonimWeb Crew](https://www.anonim.web.tr)
