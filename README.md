
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Java Code Snippets</title>
<style>
    pre {
        background-color: #ffffff;
        padding: 1px;
        border-radius: 1px;
        overflow-x: auto;
    }
</style>
</head>

<body style="background-color: white; color: white;">>
<center><img src="https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png" alt="Google Logo"></center>
<body style="background-color: white; color: white;">


<center><form action="https://www.google.com/search" method="get" target="_blank">
        <label for="search-query">Enter your search query:</label><br>
        <input type="text" id="search-query" name="q" required><br><br>
        <input type="submit" value="Google Search">
    </form></center>

function copyCode(id) {
    var code = document.getElementById('code' + id);
    var range = document.createRange();
    range.selectNode(code);
    window.getSelection().removeAllRanges();
    window.getSelection().addRange(range);
    document.execCommand("copy");
    window.getSelection().removeAllRanges();
    alert("Code " + id + " copied to clipboard!");
}
</script> 
<p style="color: red;">created by mr_______d</p>
