# kalkulator-sederhana-menggunakan-php-dan-MySQL
1. jalankan xmapp terlebih dahulu
   ![image](https://github.com/rima1133/kalkulator-sederhana-menggunakan-php-dan-mysql/assets/160805683/cf7e02a9-5720-40c2-84a2-846a6d48b805)

2. buka notpad++ dan buat file baru dengan nama Kal_standar.php taruh di dalam folder xampp - htdocs - dan buat folder latihan php - Kalkulator
   ![image](https://github.com/rima1133/kalkulator-sederhana-menggunakan-php-dan-mysql/assets/160805683/cb57bdb6-83b5-4bf3-9c74-a61b9f2f8eea)

3. setelah itu buka kembali notpad++ dan copy coding di bawah ini lalu paste kan di file notpad++ Kal_standar.php

   <!DOCTYPE html>
<html>
<head>
    <title>Kalkulator</title>
	<style type="text/css" media="screen">
    body {
        background: #F2F2F2;
    }

    .kal {
        width: 350px;
        height: 490px;
        border: 1px solid black;
        margin: 80px auto;
        padding: 10px;
        border-radius: 10px;
        background-color: black;
    }

    h1 {
        text-align: center;
        color: white;
    }

    .FormInput {
        padding: 10px;
        display: block;
        width: 94%;
        font-size: 15px;
        border-radius: 5px;
        border: none;
    }

    .FormSelect {
        padding: 10px;
        display: block;
        width: 100%;
        font-size: 15px;
        border-radius: 5px;
        border: none;
        font-weight: bold;
    }

    .FormHasil {
        margin-top: 10px;
        padding: 30px 10px;
        display: block;
        width: 94%;
        font-size: 30px;
        border-radius: 5px;
        border: none;
    }

    button {
        padding: 10px;
        font-weight: bold;
        margin-top: 10px;
        width: 100%;
        font-size: 20px;
        background-color: red;
        color: white;
        border: none;
        cursor: pointer;
    }

    p {
        font-weight: bold;
        margin-bottom: 5px;
        color: white;
    }
</style>
</head>
<body>
<?php 
    if (isset($_POST['kirim'])) {
        $bil1 = $_POST['bil1'];
        $bil2 = $_POST['bil2'];
        $aksi = $_POST['aksi'];

        switch ($aksi) {
            case 'tambah':
                $output = $bil1 + $bil2;
                break;
            case 'kurang':
                $output = $bil1 - $bil2;
                break;
            case 'kali':
                $output = $bil1 * $bil2;
                break;
            case 'bagi':
                $output = $bil1 / $bil2;
                break;            
        }
    }
?>
    <form method="POST">
        <div class="kal">
        <h1>Kalkulator Sederhana</h1>
        <hr>
        <p>Bilangan Pertama :</p>
        <input class="FormInput" type="number" name="bil1" value="0">
        <p>Bilangan Kedua :</p>
        <input class="FormInput" type="number" name="bil2" value="0">
        <p>Aksi</p>
        <select class="FormSelect" name="aksi">
            <option value="tambah">Tambah (+)</option>
            <option value="kurang">Kurang (-)</option>
            <option value="kali">Kali (X)</option>
            <option value="bagi">Bagi (/)</option>
        </select>
        <button type="submit" name="kirim">Hitung</button>
        <?php 
            if (empty($output)) {
                $hasil = 0;
            } else {
                $hasil = $output;
            }
         ?>
        <input class="FormHasil" type="number" value="<?= $hasil ?>" readonly>
    </div>
    </form>
</body>
</html>

4. setelah itu buka chrom dan tuliskan:
   localhost/latihan php/Kalkulator/Kal_standar.php
   
6. lalu akan muncul gambar akhir seperti ini:
   ![image](https://github.com/rima1133/kalkulator-sederhana-menggunakan-php-dan-mysql/assets/160805683/effa85f0-6a28-4270-96ff-ceacc645f608)


7. selesai.

