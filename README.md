# kalkulator <br> PHP ☕

kalkulator sederhana<br> ``belajar bahasa PHP`` <br>
di <a href="https://www.malasngoding.com/membuat-kalkulator-sederhana-dengan-php/">MalasNgoding</a>

# Penjelasan 📑
  
```javascript

<form method="post" action="index.php">			
	<input type="text" name="bil1" class="bil" autocomplete="off" placeholder="Masukkan Bilangan Pertama">
	<input type="text" name="bil2" class="bil" autocomplete="off" placeholder="Masukkan Bilangan Kedua">
	<select class="opt" name="operasi">
		<option value="tambah">+</option>
		<option value="kurang">-</option>
		<option value="kali">x</option>
		<option value="bagi">/</option>
	</select>
	<input type="submit" name="hitung" value="Hitung" class="tombol">									
</form>

```
 - Menggunakan method ``POST`` untuk data bilangan yang di input <br> pada bilangan 1 saya beri nama ``bil1`` dan bilangan 2 saya beri nama ``bil2`` dan untuk operator aritmatika saya beri nama ``operasi`` .

<hr>
<b>Pada bagian penangkapan data</b>

```php

<?php 
if(isset($_POST['hitung'])){
	$bil1 = $_POST['bil1'];
	$bil2 = $_POST['bil2'];
	$operasi = $_POST['operasi'];
	switch ($operasi) {
		case 'tambah':
			$hasil = $bil1+$bil2;
		break;
		case 'kurang':
			$hasil = $bil1-$bil2;
		break;
		case 'kali':
			$hasil = $bil1*$bil2;
		break;
		case 'bagi':
			$hasil = $bil1/$bil2;
		break;			
	}
}
?>

``` 

- ``Function isset()`` berfungsi untuk memeriksa ketersediaan data
