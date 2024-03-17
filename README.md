# renrennnn.github.io
<!doctype html>
<html lang="ja">
<head>
    <title>Index</title>
    <meta charset="utf-8"/>
    <!-- cssの読み込み -->
    <link rel="stylesheet" href="static/css/style.css">
</head>
<body>
    <h1>Index</h1>
    <p>This is Flask sample.</p>
    <p>{{ msg }}</p>
    <p>Welcome to {{course1}}{{course2}} course!</p>
    <a href="/ai">aiページへ遷移する</a>
    <a href="/game">gameページへ遷移する</a>

    <!-- actionを「'/'」、methodを「'GET'」にする-->
    <form action="/" method="GET">
        <input type="submit" value="GETを送信">
        <p>{{data}}<p>
        {% for i in data %}
            <p>{{ i }}</p>
        {% endfor %}
        
        {% if user_name %}
        <p>{{user_name}}</p>
        {% else %}
        <p>名無し</p>
        {% endif %}
    </form>
    <!-- actionを「'/'」、methodを「'POST'」にする-->
    <form action="/" method="POST">
        <!-- 「name」属性を「input_text」と定義-->
        <input type="text" name="input_text">
        <input type="submit" value="POSTを送信">
    </form>
</body>
</html>
