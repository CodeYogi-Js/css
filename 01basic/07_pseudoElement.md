```html
<!--All Pseudo Element selection, first-letter, first-line, placeholder, file-selector-button -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Pseudo Elements Tutorial</title>
  <meta name="description" content="Learn how to use CSS pseudo-elements like ::before and ::after with practical examples.">
  <meta name="robots" content="index, follow">
  <meta name="author" content="Brendan Eich">
  
  <link rel="stylesheet" href="css/style.css">
  <link rel="shortcut icon" type="image/x-icon" href="favicon.ico">
  <script defer src="js/script.js"></script>
  
  <link rel="canonical" href="https://www.pseudoelement.com">
  <meta name="theme-color" content="#23adbf">

  <!-- Open Graph -->
  <meta property="og:title" content="CSS Pseudo Elements Tutorial">
  <meta property="og:description" content="Step-by-step guide to mastering CSS pseudo-elements.">
  <meta property="og:image" content="https://www.pseudoelement.com/images/og-image.png">
  <meta property="og:url" content="https://www.pseudoelement.com">
  <meta property="og:type" content="website">

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="CSS Pseudo Elements Tutorial">
  <meta name="twitter:description" content="Step-by-step guide to mastering CSS pseudo-elements.">
  <meta name="twitter:image" content="https://www.pseudoelement.com/images/twitter-card.png">
  <meta name="twitter:url" content="https://www.pseudoelement.com">
  <style>
        body::selection{
            background-color: bisque;
            color: maroon;
        }
        #parent > p::first-line{
            background-color: antiquewhite;
            font-family: Arial, Helvetica, sans-serif;
        }
        #parent p::first-letter{
            font-size: 3rem;
            color: magenta;
        }
        form ::placeholder{
            font-family: Georgia, 'Times New Roman', Times, serif;
            font-size: .8rem;
            letter-spacing: 1px;
            word-spacing: 2px;
        }
        form ::file-selector-button{
            border: 1px solid grey;
            border-radius: 5px;
            padding: 5px 10px;
            font-family: Arial, Helvetica, sans-serif;
        }
        input[type="file"]:enabled{
            font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            letter-spacing: 1px;
        }

  </style>
</head>
<body>
    <div id="parent">
        <h1>this is a simple</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Error quisquam harum repudiandae illo! Commodi perspiciatis aut hic vitae et ipsam harum perferendis qui quod eum. Pariatur sit labore itaque a atque odio fuga illum iusto temporibus ex inventore deleniti doloribus dolore fugiat, quos repellat! Error eos nulla dignissimos magnam laudantium!</p>
        <div id="child">
            <h2>inside heading 2</h2>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eius reprehenderit dolorem aperiam veniam excepturi, cum mollitia pariatur exercitationem maxime fugit odio est atque nesciunt! Hic.</p>
        </div>
    </div>
    <section id="form-container">
        <fieldset>
            <legend>template form</legend>
            <form action="">
                <div>
                    <label for="userName">user name &colon;</label>
                    <br>
                    <input type="text" name="name" id="userName" placeholder="enter your name">
                </div>
                <div>
                    <label for="file">upload file under 2m.b.</label>
                    <input type="file" name="document" id="file">
                </div>
            </form>
        </fieldset>
    </section>
</body>
</html>
```