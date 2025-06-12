# Cek-daun
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Portal Cek NISN</title>
</head>
<body>
    <h1>Portal Cek NISN</h1>
    <p>Masukkan NISN kamu di bawah ini untuk diarahkan ke situs resmi pengecekan NISN.</p>

    <form id="nisnForm">
        <label for="nisnInput">NISN:</label>
        <input type="text" id="nisnInput" name="nisn" required pattern="\d{10}" title="Masukkan 10 digit NISN" />
        <button type="submit">Cek NISN</button>
    </form>

    <script>
        document.getElementById('nisnForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const nisn = document.getElementById('nisnInput').value;
            // Situs resmi pengecekan NISN dari Kemdikbud:
            // Kita arahkan ke halaman pencarian berdasar NISN (kalau ada parameter di URL).
            // Tapi karena situs resmi belum punya parameter langsung, kita arahkan ke halaman utama.
            const url = 'https://nisn.data.kemdikbud.go.id/page/data';
            alert('Kamu akan diarahkan ke situs resmi Kemdikbud untuk pengecekan NISN.');
            window.open(url, '_blank');
        });
    </script>
</body>
</html>
