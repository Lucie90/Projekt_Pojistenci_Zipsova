
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
