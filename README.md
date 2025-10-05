<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tulisan Muncul Satu Per Satu</title>
    <style>
        .text {
            font-size: 24px;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>
    <div id="text-container" class="text"></div>

    <script>
        const texts = [
            "Sudah terbiasa terjadi tanteee",
            "Teman datang ketika butuh sajaa",
            "Coba kalo lagi susahhh",
            "Mereka semua menghilang😡"
        ];

        let index = 0;
        const textContainer = document.getElementById("text-container");

        function showText() {
            if (index < texts.length) {
                textContainer.innerText = texts[index];
                index++;
                setTimeout(showText, 3000); // 3000 ms = 3 detik
            }
        }

        showText();
    </script>
</body>
</html>
