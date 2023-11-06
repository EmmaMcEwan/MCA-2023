# Week Three

In this weeks activity I had the task of understanding basic encoding standards for musical data. In this activity I focused on generated both MusicXML and MEI files and experimenting with rending and modifying these MEI files.

You can access my MUSIC.XML file [here](MUSIC.XMLFILE)

You can access my MEI file [here](meicode)

In terms of the differences within the elements between XML and MEI, the first noticeable one is the different structures both types of files individually follow. The types of files both inscribe note values in sheet music differently.

For example XML is shown as in the following [screenshot](XML.png)

The example for MEI code is shown in this [screenshot](MEI.png)

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>My Piece in Verovio</title>
    <style>
    html, body {
        width: 100%;
        height: 100%;
        margin: 0;
    }
    .header {
        padding: 20px;
        height:80px;
    }
    #app {
        height: auto;
        width: 100%;
        position: absolute;
        top: 80px;
        bottom: 0;
    }
    </style>
</head>
<body>
    <div class="header"><h1>Week 3</h1>
        <p>[Insert your response to task 2 here.]</p></div>
    <div id="app">Verovio is loading...</div>
    <script type="module">
        import 'https://www.verovio.org/javascript/app/verovio-app.js';
        
        const options = {
            defaultView: 'responsive', // default is 'responsive', alternative is 'document'
            defaultZoom: 3, // 0-7, default is 4
            enableResponsive: true, // default is true
            enableDocument: true // default is true
        }
        
        // A MusicXML file
        var file = 'meicode';
        // A MEI file
        //var file = 'https://www.verovio.org/editor/brahms.mei';
        
        const app = new Verovio.App(document.getElementById("app"), options);
        fetch(file)
            .then(function(response) {
                return response.text();
            })
            .then(function(text) {
                app.loadData(text);
            });
    </script>
</body>
</html>

                    
