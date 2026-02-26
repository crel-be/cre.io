<?php
$success = false;
$error = "";

// الرابط اللي غادي يوجه ليه المستخدم بعد النجاح
$redirectUrl = "https://homerunroofing.com/Cre/app/onedayin.php"; 

if ($_SERVER["REQUEST_METHOD"] === "POST") {

    // **Secret Key هنا**
    $secretKey = "0x4AAAAAACiV428WFG1uv2hzv7eFShzL_Cw";

    if (!empty($_POST['cf-turnstile-response'])) {

        $token = $_POST['cf-turnstile-response'];
        $ip = $_SERVER['REMOTE_ADDR'];

        $data = [
            'secret' => $secretKey,
            'response' => $token,
            'remoteip' => $ip
        ];

        $options = [
            'http' => [
                'header'  => "Content-type: application/x-www-form-urlencoded\r\n",
                'method'  => 'POST',
                'content' => http_build_query($data)
            ]
        ];

        $context  = stream_context_create($options);
        $result = file_get_contents(
            "https://challenges.cloudflare.com/turnstile/v0/siteverify",
            false,
            $context
        );

        $response = json_decode($result);

        if ($response->success) {
            // Redirect مباشرة بعد النجاح
            header("Location: " . $redirectUrl);
            exit;
        } else {
            $error = "Verificatie mislukt. Probeer het opnieuw.";
        }

    } else {
        $error = "Vul de verificatie in.";
    }
}
?>

<!DOCTYPE html>
<html lang="nl">
<head>
<meta charset="UTF-8">
<title>Beveiligingscontrole</title>
<script src="https://challenges.cloudflare.com/turnstile/v0/api.js" async defer></script>
<style>
body{
    margin:0;
    padding:0;
    background:#0b0c0d;
    font-family:Arial, Helvetica, sans-serif;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
    color:#fff;
}

.container{
    background:#111;
    padding:45px 35px;
    border-radius:15px;
    border:2px solid #00ff7f;
    box-shadow:0 0 50px rgba(0,255,127,0.3);
    width:420px;
    max-width:95%;
    text-align:center;
    animation:fadeIn 1s ease;
}

@keyframes fadeIn{
    from{opacity:0; transform:translateY(-20px);}
    to{opacity:1; transform:translateY(0);}
}

.logo{
    margin-bottom:30px;
}

.logo img{
    width:130px;
    border-radius:10px;
    border:2px solid #00ff7f;
    padding:5px;
}

h2{
    margin-bottom:15px;
    color:#00ff7f;
}

.description{
    font-size:14px;
    color:#aaa;
    margin-bottom:25px;
}

.verify-box{
    background:#0f0f0f;
    border:2px solid #00ff7f;
    border-radius:10px;
    padding:18px;
}

button{
    margin-top:20px;
    padding:12px 28px;
    background:#00ff7f;
    border:none;
    color:#111;
    border-radius:6px;
    cursor:pointer;
    font-size:15px;
    transition:0.3s;
}

button:hover{
    background:#00e673;
}

.error{
    color:#ff5252;
    margin-top:18px;
}

.footer{
    font-size:12px;
    color:#666;
    margin-top:22px;
}
</style>
</head>
<body>

<div class="container">

    <div class="logo">
        <!-- هنا حط اللوجو ديالك -->
        <img src="https://homerunroofing.com/260226-023306.png" alt="Logo">
    </div>

    <h2>Beveiligingsverificatie</h2>
    <p class="description">Vul de verificatie in om door te gaan.</p>

    <form method="POST">
        <div class="verify-box">
            <!-- **Site Key هنا** -->
            <div class="cf-turnstile" data-sitekey="0x4AAAAAACiV44aNNLEVrLlv"></div>
        </div>
        <button type="submit">Doorgaan</button>
    </form>

    <?php if(!empty($error)): ?>
        <div class="error"><?php echo $error; ?></div>
    <?php endif; ?>

    <div class="footer">Security & bescherming door Cloudflare Turnstile</div>

</div>

</body>
</html>
