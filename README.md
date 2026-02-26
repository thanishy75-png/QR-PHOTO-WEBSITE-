<!DOCTYPE html>
<html>
<head>
  <title>Image Viewer</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      margin: 0;
      background: #111;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial;
      color: white;
      text-align: center;
      flex-direction: column;
    }

    img {
      max-width: 90%;
      max-height: 80vh;
      border-radius: 12px;
    }
  </style>
</head>
<body>

<h2>📷 Image Viewer</h2>
<img id="displayImage" />

<script>
  const params = new URLSearchParams(window.location.search);
  const imageUrl = params.get("img");

  if (imageUrl) {
    document.getElementById("displayImage").src = imageUrl;
  } else {
    document.body.innerHTML = "<h2>No image URL provided</h2>";
  }
</script>

</body>
</html>
