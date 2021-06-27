<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ignore the Price</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
</head>
<body>
    <div style='text-align: center'>
        <h1>Bitcoin is <span id="changing" style='color: orange'>Hope</span></h1>
        <p>The current Bitcoin Block Height is <span id="blockCount"></span>.</p>
        <p>We are still winning.</p>
    </div>
    <script>
        // var original = $.get("https://blockchain.info/q/getblockcount")
        var original = $.ajax({ type: "GET", url: "https://blockchain.info/q/getblockcount", async: false }).responseText
        console.log(original)
        
        document.getElementById('blockCount').innerHTML = original
        // var blockCount = ajax.get("https://blockchain.info/q/getblockcount")
        var words = ['Hope', 'Freedom', 'Inclusion', 'Time', 'Energy', 'Bitcoin'];
        let i = 0;
            do {
                task(i);
                i++;
            } while (i < 6);
            function task(i) {
                setTimeout(function () {
                    $('#changing').empty().append(words[i])
                }, 2000 * i);
            }

    </script>   
</body>
</html>