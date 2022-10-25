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

kalimat yang ada di dalam lingkup tag `<p>` akan menjadi warna pink. termasuk yang ada didalam `<em>`. itulah yang disebut `inheritance`.


## The Cascade
jika ada beberapa CSS class yang mempunyai style yang sama, maka yang diambil adalah yang paling `spesifik` diantara beberapa class CSS tsb

## Directions
untuk horizontal, disebut `inline`. dan untuk vertical disebut `block`