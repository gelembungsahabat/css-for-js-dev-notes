# Rendering Logic 1

## Inheritance
Ada <b>`beberapa`</b> CSS properties yang akan menurunkan/mewariskan (inherit) style-nya ke dalam children. contoh: <br><br>
CSS:<br/>
```
p {
  color: deeppink;
}
```

HTML:
<br/>
```
<p>
  I know <em>you</em> are, but what am I?
</p>
```

kalimat yang ada di dalam lingkup tag `<p>` akan menjadi warna pink. termasuk yang ada didalam `<em>`. itulah yang disebut `inheritance`.<br><br>


## The Cascade
jika ada beberapa CSS class yang mempunyai style yang sama, maka yang diambil adalah yang paling `spesifik` diantara beberapa class CSS tsb<br><br>

## Directions
untuk horizontal, disebut `inline`. dan untuk vertical disebut `block`<br><br>

## The Box Model
Box model bisa dianalogikan sebagai orang yang ada di musim dingin: <br>
![](screenshot/Screenshot%20from%202022-10-25%2016-27-15.png)
<br><br>

## Margin Collapse
Margin akan rusak/collapse pada beberapa kondisi:
### Vertical Margin
contoh: 
```
<style>
  p {
    margin-top: 24px;
    margin-bottom: 24px;
  }
</style>

<p>Paragraph One</p>
<p>Paragraph Two</p>
```
![](screenshot/Screenshot%20from%202022-10-25%2017-00-40.png)

![](screenshot/Screenshot%20from%202022-10-25%2017-00-45.png)

### Flow layout
Margin akan rusak/collapse jika pakai flow layout, kalo pake `Flex` dia aman.

### The bigger margin wins
jika ada 2 vertical margin, margin yang paling besarlah yang menang
![](screenshot/Screenshot%20from%202022-10-25%2017-06-52.png)

### Margins can collapse in the same direction
Margin akan rusak/collapse jika ada margin di arah yang sama. dan margin yang paling besarlah yang menang.
![](screenshot/Screenshot%20from%202022-10-25%2017-09-26.png)
 