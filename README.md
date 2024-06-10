<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Display</title>
    <style>
        .code-container {
            width: 80%;
            margin: 0 auto;
            overflow-x: auto;
            white-space: pre-wrap;
            border: 1px solid #ccc;
            padding: 10px;
            background-color: #f9f9f9;
        }
        .copy-button {
            background-color: #4caf50;
            border: none;
            color: white;
            padding: 10px 20px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 16px;
            margin: 4px 2px;
            cursor: pointer;
            border-radius: 8px;
        }
    </style>
</head>
<body>

<div class="code-container" id="codeContainer">
    &lt;!DOCTYPE html&gt;
    &lt;html lang="en"&gt;
    &lt;head&gt;
        &lt;meta charset="UTF-8"&gt;
        &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
        &lt;title&gt;Code Display&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
        &lt;h1&gt;Hello, world!&lt;/h1&gt;
    &lt;/body&gt;
    &lt;/html&gt;
</div>

<button class="copy-button" onclick="copyCode()">Copy Code</button>

<script>
    function copyCode() {
        var codeContainer = document.getElementById('codeContainer');
        var range = document.createRange();
        range.selectNode(codeContainer);
        window.getSelection().removeAllRanges();
        window.getSelection().addRange(range);
        document.execCommand('copy');
        window.getSelection().removeAllRanges();
        alert('Code copied to clipboard!');
    }
</script>

</body>
</html>
