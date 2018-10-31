<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <ul id="ulScores">
        <li>85</li>
        <li>76</li>
        <li>92</li>
        <li>61</li>
    </ul>
    <script>   
        var html=ulScores.innerHTML;
        console.log(html);
        html=html.replace(/^\s*$/i,"");
        console.log(html);
        html=html.replace(/^\/li>\s*$/i,"")
        console.log(html);
        var scores=
        html.split(/<\/li>\s*<li>/)
        console.log(scores);
        //[85,76,92,61]
        scores.sort(
            function(a,b){return b-a}
        );
        console.log(scores);
        html="<li>";
    </script>
</body>
</html>
