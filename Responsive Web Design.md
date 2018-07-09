# Responsive Web Design

## Introduction to Basic HTML & HTML5

HTML, or HyperText Markup Language, is a markup language used to describe the structure of a web page. It uses a special syntax or notation to organize and give information about the page to the browser. Elements usually have opening and closing tags that surround and give meaning to content. For example, there are different tag options to place around text to show whether it is a heading, a paragraph, or a list.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>CatPhoto</title>
    </head>
    <body>
        <h2>CatPhotoApp</h2>
        <main>
        <p>Click here to view more <a href="#">cat photos</a>.</p>
        
        <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>
        
        <p>Things cats love:</p>
        <ul>
            <li>cat nip</li>
            <li>laser pointers</li>
            <li>lasagna</li>
        </ul>
        <p>Top 3 things cats hate:</p>
        <ol>
            <li>flea treatment</li>
            <li>thunder</li>
            <li>other cats</li>
        </ol>
        
        <form action="/submit-cat-photo">
            <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
            <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
            <label><input type="checkbox" name="personality" checked> Loving</label>
            <label><input type="checkbox" name="personality"> Lazy</label>
            <label><input type="checkbox" name="personality"> Energetic</label><br>
            <input type="text" placeholder="cat photo URL" required>
            <button type="submit">Submit</button>
        </form>
        </main>
    </body>
</html>
```

## Introduction to Basic CSS