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

## Looping

### While
Looping dengan syarat kondisinya true

```php
<?php
    $a = 1;
    while($a <= 10){
        echo "Saya bernilai " . $a . '<br/>';
        $a++;
    }
?>
```

### Do While

```php
<?php
    $a = 1;
    do {
        echo "Saya bernilai " . $a . '<br/>';
        $a++;
    } while($a <= 10);
?>
```

### For

```php
<?php
    for($i=0; $i < 10; $i++>){
        echo "Ini adalah nomor " . $i . "<br/>";
    }
?>
```

### Foreach

```php
<?php
    $buah = ["Anggur", "Apel", "Jeruk", "Buah Naga"];
	foreach ($buah as $value) {
		echo $value . "<br/>";
	}
?>
```

```php
<?php
    $buah = ["Anggur", "Apel", "Jeruk", "Buah Naga"];
	foreach ($buah as $key => $value) {
		echo $value . " dengan key " . $key . "<br/>";
	}
?>
```

## Lebih Lanjut

### Function

```php
<?php
    function halo($nama){
		echo "Hallooo.. $nama";
	}
	halo("Lerian");
?>
```

```php
<?php
    function tambah($a, $b){
		$total = $a + $b;
		echo $total;
	}

	tambah(1,2);
?>
```

Jika kosong.

```php
<?php
    function halo($nama = null){
		echo "Hallooo.." . "<br/>";
	}
	halo();
?>
```

Jika ingin pakai default.
```php
<?php
    function halo($nama = 'Tanpa nama'){
		echo "Hallooo.." . "<br/>";
	}
	halo();
?>
```


### Array

**Indexed Array**
```php
<?php
    $a = ['BMW', 'Honda', 'Suzuki'];
    var_dump($a);
    echo $a[2];
?>
```

**Associative Array**
```php
<?php
    $b = [
        'Indonesia' => 'Nasi padang',
        'Malaysia' => 'Nasi lemak',
        'Amerika' => 'Steak',
    ];
    var_dump($b);
    echo $b['Indonesia'];
?>
```

**Multidimensional Array**

```php
<?php
    $c = [
        'a' => ['BMW', 'Honda', 'Suzuki'],
        'b' => [
            'Indonesia' => 'Nasi padang',
            'Malaysia' => 'Nasi lemak',
            'Amerika' => 'Steak',
        ],
    ];
    var_dump($c);
    echo $c['a'][1];
?>
```

```php
<?php
    $c = [
        'a' => $a,
        'b' => $b
    ];
    var_dump($c);
?>
```