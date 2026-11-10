
<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Satoh Kiyoshi | Personal Profile</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    padding: 35px 15px;
    min-height: 100vh;
    background: #071522;
    font-family: Georgia, serif;
    color: #e9e5d8;
}

/* KHUNG CHÍNH */
.main-frame {
    max-width: 900px;
    margin: auto;
    border: 2px solid #c9a84e;
    padding: 12px;
    background: #0c2030;
    box-shadow: 0 0 20px #b99a3c25;
}

/* THANH ĐIỀU HƯỚNG */
.navbar {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 10px;
    padding: 15px;
    border-bottom: 1px solid #c9a84e;
}

.navbar button {
    background: transparent;
    color: #d9bd70;
    border: 1px solid #9e813e;
    padding: 11px 22px;
    font-family: Georgia, serif;
    font-size: 13px;
    letter-spacing: 2px;
    cursor: pointer;
    transition: 0.3s;
}

.navbar button:hover,
.navbar button.active {
    background: #c9a84e;
    color: #071522;
}

/* NỘI DUNG */
.content {
    padding: 35px 25px;
    min-height: 430px;
}

.page {
    display: none;
    animation: fadeIn 0.5s ease;
}

.page.active {
    display: block;
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(8px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* HOME */
.name {
    text-align: center;
    font-size: clamp(32px, 6vw, 55px);
    font-weight: bold;
    letter-spacing: 3px;
    margin: 15px 0 30px;
    background: linear-gradient(
        120deg,
        #d5b75d,
        #fff0a8,
        #8da99a,
        #e7c86d
    );
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
    text-shadow: 0 0 15px #c9a84e25;
}

.avatar {
    display: block;
    width: 220px;
    max-width: 100%;
    height: 280px;
    object-fit: cover;
    margin: 0 auto 30px;
    border: 2px solid #c9a84e;
    padding: 5px;
}

.info {
    max-width: 550px;
    margin: auto;
    border-top: 1px solid #8f793e;
    padding-top: 20px;
}

.info h3 {
    color: #d9bd70;
    font-size: 18px;
    margin-bottom: 10px;
}

.info p {
    line-height: 1.8;
    margin: 5px 0;
    font-size: 15px;
}

.info strong {
    color: #e5ca79;
}

.page-title {
    text-align: center;
    color: #d9bd70;
    font-size: 28px;
    letter-spacing: 4px;
    margin-bottom: 30px;
}

.placeholder {
    text-align: center;
    color: #9ca9ad;
    line-height: 2;
}

/* FOOTER */
footer {
    border-top: 1px solid #9e813e;
    text-align: center;
    padding: 20px 10px 10px;
    color: #9e9b86;
    font-size: 12px;
    letter-spacing: 2px;
}

@media (max-width: 500px) {
    body {
        padding: 15px 8px;
    }

    .content {
        padding: 25px 12px;
    }

    .navbar button {
        padding: 10px 13px;
        font-size: 11px;
    }
}
</style>
</head>

<body>

<div class="main-frame">

    <!-- MENU -->
    <nav class="navbar">
        <button class="active" onclick="showPage('home', this)">HOME</button>
        <button onclick="showPage('about', this)">ABOUT ME</button>
        <button onclick="showPage('attention', this)">ATTENTION</button>
        <button onclick="showPage('fandom', this)">FANDOM</button>
    </nav>

    <main class="content">

        <!-- HOME -->
        <section id="home" class="page active">

            <h1 class="name">Satoh Kiyoshi</h1>

            <img
                src="images/avatar.jpg"
                alt="Profile picture"
                class="avatar"
            >

            <div class="info">

                <h3>Pronouns</h3>
                <p>He / Him</p>

                <h3>Another names</h3>
                <p>- Bạch Song Thiên</p>
                <p>- Ciel la Neiges</p>

            </div>
        </section>

        <!-- ABOUT ME -->
        <section id="about" class="page">
            <h2 class="page-title">ABOUT ME</h2>
            <div class="placeholder">
                <p>Welcome to my little world.</p>
                <p>Phần giới thiệu bản thân sẽ được đặt ở đây.</p>
            </div>
        </section>

        <!-- ATTENTION -->
        <section id="attention" class="page">
            <h2 class="page-title">ATTENTION</h2>
            <div class="placeholder">
                <p>Những điều cần lưu ý khi tương tác với mình.</p>
            </div>
        </section>

        <!-- FANDOM -->
        <section id="fandom" class="page">
            <h2 class="page-title">FANDOM</h2>
            <div class="placeholder">
                <p>My favorite characters, series and fandoms.</p>
            </div>
        </section>

    </main>

    <footer>
        SAT0H KIYOSHI · PERSONAL WEBSITE
    </footer>

</div>

<script>
function showPage(pageId, button) {

    // Ẩn tất cả các trang
    document.querySelectorAll('.page').forEach(page => {
        page.classList.remove('active');
    });

    // Hiện trang được chọn
    document.getElementById(pageId).classList.add('active');

    // Đổi trạng thái nút
    document.querySelectorAll('.navbar button').forEach(btn => {
        btn.classList.remove('active');
    });

    button.classList.add('active');
}
</script>

</body>
</html>
