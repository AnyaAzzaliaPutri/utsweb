<h1>KODE EXPERIMEN XSS</h1>

<?php
error_reporting(E_ALL);
ini_set('display_errors', 1);

$komentar = '';
if (isset($_POST['komentar'])) {
    $komentar = $_POST['komentar'];
}
?>

<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Form Komentar - Uji Coba XSS</title>
</head>
<body>
    <h1>Form Komentar</h1>
    <form method="POST" action="">
        <input type="text" name="komentar" placeholder="Tulis komentar..." value="">
        <button type="submit">Kirim</button>
    </form>

    <h2>Hasil Komentar:</h2>
    
    <div>
        <?php
        echo $komentar;
        ?>
    </div>
</body>
</html>

<h1>MASUKAN KODE PAYLOAD</h1>

<img src=”x” onerror=”alert(‘XSS Berhasil!’)”>

<h1>HASIL</h1>

![Screenshot 2025-04-28 001747](https://github.com/user-attachments/assets/3156becf-db95-4fb5-9474-f01f5913212a)


