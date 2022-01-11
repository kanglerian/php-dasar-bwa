# Kelas PHP Dasar

> Ini adalah catatan pembelajaran


## Dasar

### Menulis syntax dasar PHP
```php
<?php
    echo "Hello World!";
?>
```

### Komentar pada PHP
```php
<?php
    // komentar 1
    /* */ komentar 2
    # komentar 3
?>
```

### Variable PHP
Tempat menyimpan data.

```php
<?php
    $teks = "Halo dunia";
    $angka = 5;
    $angkadua = 10.5;

    echo $teks;
?>
```

### Tipe data PHP
```php
<?php
    $a = "Ini adalah string";
    $b = 10; // ini adalah integer
    $c = 10.5; // ini adalah float
    $d = true; // ini adalah boolean
    $e = ['satu', 2, 'tiga']; // ini adalah array
    $f = null; // ini adalah null atau kosong

    echo var_dump($f);
?>
```

### Operator pada PHP

**Operator Aritmatika**
Diantaranya: +, -, /, *, %, **

```php
<?php
    $a = 10;
    $b = 20;

    $total = $a + $b;

    echo $total;
?>
```

**Operator Assignment**

```php
<?php
    $a = 20;
    $b = 30;

    $total = 10;
	$total = $total + $a; // ini cara satu bisa pakai $total += $a;

    echo $total;
?>
```

**Operator Comparisson (pembanding)**

- `==` Jika hasil angkanya sama maka TRUE tanpa memperhatikan tipe data string atau integer
- `===` Jika hasil angkanya sama tetapi berbeda tipe data (string dan integer) maka hasilnya FALSE
- `!=` tidak sama dengan, tanpa memperhatikan tipe data
- `!==` tidak sama dengan, dengan memperhatikan tipe data
- `>` lebih besar dari
- `<` kurang dari
- `<=` lebih kecil sama dengan
` `>=` lebih besar sama dengan

```php
<?php
    $a = 4;
    $b = 7;

    $hasil = $a == $b;
    echo var_dump($hasil);
?>
```
**Operator Increment / Decrement**
Jika ingin menambahkan atau mengurangi 1 angka maka tinggal tambahkan `$a++` atau `$a--`

```php
<?php
    $a = 10;
    $a++;

    echo $a;
?>
```

**Operator String**
Menggabungkan string.

```php
<?php
    $a = "Hello";
    $b = "World";

    echo $a . " " . $b;
?>
```

## Kondisional

### If-Else

```php
<?php
    $suhu = 38;

    if($suhu > 38){
        echo "Kamu tidak boleh masuk!";
    }elseif($suhu == 38){
        echo "Kamu hati-hati";
    }
    else{
		echo "Kamu boleh masuk!";
	}
?>
```

### Switch

```php
$warna = "Merah";
switch($warna){
    case 'Merah':
        echo "Berhenti!";
    break;

    case 'Kuning':
        echo "Hati-hati!";
    break;

    case 'Hijau':
        echo "Maju!";
    break;

    default:
        echo "Lampu rusak";
    break;
}
```


