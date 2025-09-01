<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>LEARNING SITE</title>
    <style>
        .spinner {
            margin: 100px auto;
            width: 50px;
            height: 50px;
            border: 12px solid #f3f3f3;
            border-top: 12px solid #3498db;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg);}
            100% { transform: rotate(360deg);}
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <button id="startBtn">go to w3schools</button>
    <div id="spinner" class="spinner hidden"></div>
    <div id="done" class="hidden">Done spinning!</div>
    <script>
        document.getElementById('startBtn').addEventListener('click', function() {
            document.getElementById('spinner').classList.remove('hidden');
            document.getElementById('done').classList.add('hidden');
            document.getElementById('startBtn').disabled = true;
            setTimeout(function() {
                document.getElementById('spinner').classList.add('hidden');
                document.getElementById('done').classList.remove('hidden');
                document.getElementById('startBtn').  disabled = false;
                        // Redirect to another page after spinning
                window.location.href = "index.html"; // Change to your target page
            }, 60000);
        });
    </script>
</body>
</html>