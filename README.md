<!DOCTYPE html>
<html lang="cz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="styly.css">
    <title>Projekt ke zkoušce</title>
</head>
<body>
  <header>
          
            <h3>POJIŠTĚNÍ</h3> 
            <div>
            <a href=" Pojistenci.html "> Pojištěnci </a>
            <a href=" O aplikaci.html "> O aplikaci</a> 
            </div>
    </header>
    
        <div>
            <div class="main-flex">
            <h3> Pojištěnci </h3>  
        
        <table border="1" class="tabulka-pojistenych">
            <thead>
                <th>Jméno a přijmení</th>
                <th> Telefon</th></br>
                <th> Věk</th>
            </thead>
        </table>
        </div>

            <h3>Nový pojištěnec</h3>
        <form>
            Jméno <input class="jmeno" type="text">
            Příjmení <input class="prijmeni" type="text">
            Telefonní číslo <input class="telefon" type="number">
            Věk <input class="vek" type="number">           
            <a href="#" class="button">Uložit pojištěnce</a>
            
        </form>
    </div>

    <script src="index.js"></script>
    <script src="Pojistenec.js"></script>

</body>

</html>


    class Pojistenec{
        constructor(jmeno, prijmeni, telefon, vek){
            this.prijmeni = prijmeni;
            this.jmeno = jmeno;
            this.telefon = telefon;
            this.vek = vek;
        }
    }

    const jmeno = document.querySelector(".jmeno ")
    const prijmeni = document.querySelector(".prijmeni ")
    const telefon = document.querySelector(".telefon ")
    const vek = document.querySelector(".vek ")
    const tlacitko = document.querySelector(".button")
    const seznam = document.querySelector(".tabulka-pojistenych")

    const pojistenci = []



    tlacitko.addEventListener("click",function (e) {
        e.preventDefault();

        const pojistenec = new Pojistenec(jmeno.value, prijmeni.value, telefon.value, vek.value);

        pojistenci.push(pojistenec);
        const polozka = document.createElement("tr");
    
        polozka.innerHTML = `<td> ${pojistenec.jmeno + " " + pojistenec.prijmeni} </td>    
            <td> ${ pojistenec.telefon} </td> <td> ${pojistenec.vek}</td>`
        seznam.appendChild(polozka)
    

        console.log(pojistenci);
});




let lucka = new Pojistenec("Alena", "Nová", "123123123", "20");
let jirka = new Pojistenec("Jirka", "Zelený", "654654654", "60")
let michal = new Pojistenec("Michal", "Druhý")

console.log(lucka)
console.log(jirka)
console.log(michal)


table {
    border-spacing:0;
    border: 1px solid black;
    width: 450px;
}
table, table td {
    padding:0;
    margin: 0;
}
table td {
    border: 1px solid black;
}

.main-flex {
    display: grid;
    justify-content: left;
   
}
header h3 {
    padding: 20px;;
   
}

header {
  
    height: 100px;
    width: 100%;
    top: 1;
    background: #1d84ec;
    color: white;
    display: flex;
    justify-content: left;
}

.button {
    padding: 3px 6px;
    font-weight: 600;
    background: #55aaf9;
    color: #fff;
    border: none;
    cursor: pointer;
    transition: .5s;
    border: 1px solid #fff;
    border-radius: 10px;
    
}

* {
    padding: 5px 6px;
    font-weight: 600;
    box-sizing: border-box;
}

body {
    display: grid;
    justify-content: left;
}

div {
    color: #0359ab;
}

a {
    color: whitesmoke;
   
}

th {
    text-decoration: none;

}





