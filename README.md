# Timedoor Training Teen
## Intermediate A - Meeting 6

Pertemuan 6 mempelajari function parameter dan return statement, Terdapat dua jenis statement return pada pemrograman, yaitu 
statement return tanpa pengembalian nilai dan statement return 
dengan nilai yang spesifik

## Link
What is th internet?
>>https://www.youtube.com/watch?v=Dxcc6ycZ73M&t=3s
How the internet works?
>>https://www.youtube.com/watch?v=x3c1ih2NJEg

Contoh aplikasi yang akan dibuat :
>https://timedoor-temperature-converter.netlify.app/

untuk memulai pembuatan aplikasi download terlebih dahulu di dalam repo
>https://github.com/timedoorAcademy-smp/int1-6-temperature-convert



###  HTML Code Basic

```html
<body>
    <div class="container">

        <div class="toppane">
            <div class="centered">
                <h1>Thermometer Converter</h1>
                <button onclick="convertTemp()">Click to convert</button>
            </div>
        </div>

        <div class="leftpane">
            <div class="centered">
                <img src="img/thermo.jpg" alt="Avatar woman">
                <h2>Termometer Celcius</h2>
                <input type="text" id="Celcius" class="Celcius">
            </div>
        </div>

        <div class="rightpane">
            <div class="centered">
                <img src="img/thermo.jpg" alt="Avatar man">
                <h2>Termometer Fahrenheit</h2>
                <input type="text" id="Fahrenheit" class="Fahrenheit">
            </div>
        </div>

    </div>
</body>
```



### Javascript Basic
```html
   <script>

    function convertTemp() {
        var celcius = document.getElementById("Celcius");
        var fahrenheit = document.getElementById("Fahrenheit");
        var celc = parseFloat(celcius.value);
        var fahr = parseFloat(fahrenheit.value);
        var convert;
        //conditionals
        if (isNaN(celc) && isNaN(fahr)) {
            return alert('Fill with number');
        }
        else if (isNaN(celc) || isNaN(fahr)) {
            if (isNaN(celc)) {
                convert = (5 * (fahr - 32)) / 9;
                return celcius.value = convert;
            }
            else if (isNaN(fahr)) {
                convert = ((9 * celc) / 5) + 32;
                return fahrenheit.value = convert;
            }
        }
        else {
            alert('Fill in one form!');
            celcius.value = "";
            fahrenheit.value = "";
            return;
        }
    }

</script>
```
