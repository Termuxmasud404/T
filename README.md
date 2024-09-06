<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Masud Rana's Website</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f12711, #f5af19);
            color: #fff;
        }

        header {
            background: linear-gradient(90deg, #00c6ff, #0072ff);
            padding: 20px;
            text-align: center;
            color: #fff;
            font-size: 2.5em;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        section {
            padding: 40px;
            text-align: center;
            margin: 20px;
            border-radius: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            box-shadow: 0 6px 15px rgba(0, 0, 0, 0.3);
        }

        .info {
            margin: 20px 0;
            font-size: 1.5em;
            color: #ffeb3b;
        }

        .upload-section {
            background: linear-gradient(45deg, #ff6b6b, #ff8c42);
            padding: 30px;
            border-radius: 10px;
            margin-top: 30px;
        }

        input[type="file"], button {
            padding: 10px;
            margin: 10px;
            border-radius: 5px;
            border: none;
            font-size: 1em;
            background-color: #fff;
            color: #333;
            cursor: pointer;
        }

        button {
            background-color: #34d399;
            color: #fff;
            padding: 10px 20px;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #059669;
        }

        footer {
            background-color: #4b5563;
            color: white;
            padding: 20px;
            text-align: center;
        }

        .file-list {
            background-color: #4b5563;
            padding: 20px;
            border-radius: 10px;
            margin-top: 30px;
            color: white;
        }

        .file-item {
            background-color: #fca5a5;
            color: #333;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            text-align: left;
        }

    </style>
</head>
<body>

    <header>
        Welcome to Masud Rana's Website
    </header>

    <section>
        <h2>Contact Information</h2>
        <p class="info">Name: Masud Rana</p>
        <p class="info">Email: termuxmasud@gmail.com</p>
        <p class="info">Phone: 01300143398</p>
    </section>

    <section class="upload-section">
        <h2>Upload Your File</h2>
        <input type="file" id="fileUpload" name="fileUpload">
        <button onclick="uploadFile()">Upload</button>
    </section>

    <section class="file-list">
        <h3>Uploaded Files</h3>
        <div id="fileContainer">
            <!-- Uploaded files will be displayed here -->
        </div>
    </section>

    <footer>
        © 2024 Masud Rana's Colorful Website
    </footer>

    <script>
        function uploadFile() {
            const fileInput = document.getElementById('fileUpload');
            const fileContainer = document.getElementById('fileContainer');
            
            if (fileInput.files.length > 0) {
                const fileName = fileInput.files[0].name;

                // Create a new div element to display the uploaded file
                const fileItem = document.createElement('div');
                fileItem.className = 'file-item';
                fileItem.innerText = fileName;

                // Append the new file item to the file container
                fileContainer.appendChild(fileItem);

                // Reset the file input
                fileInput.value = '';

                alert('File uploaded successfully!');
            } else {
                alert('Please select a file to upload.');
            }
        }
    </script>

</body>
</html>
