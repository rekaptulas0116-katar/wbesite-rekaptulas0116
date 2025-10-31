# wbesite-rekaptulas0116
/* ===== GLOBAL ===== */
body {
  font-family: 'Poppins', sans-serif;
  margin: 0;
  background-color: #f8f9fa;
  color: #333;
  overflow-x: hidden;
}

/* ===== HEADER ===== */
header {
  background-color: #007bff;
  color: white;
  text-align: center;
  padding: 1.5em 0;
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo {
  width: 120px;
  height: 120px;
  object-fit: cover;
  border-radius: 50%;
  border: 3px solid white;
  box-shadow: 0 0 8px rgba(0, 0, 0, 0.3);
}

/* ===== NAV ===== */
nav {
  background-color: #0056b3;
  text-align: center;
  padding: 10px;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s;
}

nav a:hover {
  color: #ffde59;
}

/* ===== SECTIONS ===== */
section {
  padding: 25px;
  max-width: 1000px;
  margin: auto;
}

section h2 {
  color: #0056b3;
  border-bottom: 2px solid #007bff;
  display: inline-block;
  padding-bottom: 5px;
}

/* ===== GALERI ===== */

/* Tombol Galeri */
.button-container {
  text-align: center;
  margin-top: 15px;
  margin-bottom: 25px;
}

.button-container button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 18px;
  margin: 0 8px;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: background 0.3s ease, transform 0.2s ease;
}

.button-container button:hover {
  background-color: #0056b3;
  transform: scale(1.05);
}

.button-container button:active {
  background-color: #004a99;
  transform: scale(0.98);
}

/* Galeri Grid */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
  justify-items: center;
  padding: 10px;
  box-sizing: border-box;
}

/* Gambar & video di galeri */
.gallery-photo,
.gallery-video {
  width: 100%;
  max-width: 280px;
  aspect-ratio: 4 / 3;          /* menjaga proporsi */
  border-radius: 10px;
  object-fit: cover;
  cursor: pointer;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  opacity: 0;
  animation: fadeIn 0.8s ease forwards;
}

/* Hover efek */
.gallery-photo:hover,
.gallery-video:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25);
}

/* Fade-in animation */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Delay animasi agar muncul bertahap */
.gallery-photo:nth-child(1),
.gallery-video:nth-child(1) { animation-delay: 0.1s; }
.gallery-photo:nth-child(2),
.gallery-video:nth-child(2) { animation-delay: 0.2s; }
.gallery-photo:nth-child(3),
.gallery-video:nth-child(3) { animation-delay: 0.3s; }
.gallery-photo:nth-child(4),
.gallery-video:nth-child(4) { animation-delay: 0.4s; }
.gallery-photo:nth-child(5),
.gallery-video:nth-child(5) { animation-delay: 0.5s; }

/* ===== LIGHTBOX ===== */
.lightbox {
  display: none;
  position: fixed;
  z-index: 999;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.8);
  justify-content: center;
  align-items: center;
}

.lightbox-content {
  max-width: 80%;
  max-height: 80%;
  border-radius: 10px;
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
}

.close {
  position: absolute;
  top: 20px;
  right: 40px;
  color: white;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}

/* ===== UPLOAD OTOMATIS GALERI ===== */
.upload-container {
  margin: 20px 0;
  text-align: center;
}

.upload-container input {
  display: none;
}

.upload-label {
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
  transition: background 0.3s;
  font-weight: bold;
}

.upload-label:hover {
  background-color: #0056b3;
}

.upload-preview img,
.upload-preview video {
  width: 220px;
  height: 160px;
  object-fit: cover;
  border-radius: 8px;
  margin: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  animation: fadeIn 0.8s ease forwards;
}

/* ===== FOOTER ===== */
footer {
  background-color: #007bff;
  color: white;
  text-align: center;
  padding: 15px 0;
  margin-top: 20px;
}

/* ===== RESPONSIF ===== */
@media (max-width: 600px) {
  .gallery-grid {
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  }

  .gallery-photo,
  .gallery-video {
    max-width: 100%;
    height: auto;
  }
}
