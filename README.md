# tp_web_scraping_RyanX

Site: https://www.trivago.com.br/?__wr=1889&cip=55030170040101&cip_tc=1143_amplify%20privacy%20desktop%20BR_226405009683656704&cip_ext_id=226405009683656704&mfadid=adm

Código:

function medias() {
    let coisas = document.querySelectorAll("span.NnAY2J span")
    let soma = 0;
    let contar = 0;

    for (let i = 0; i < coisas.length; i++) {
        let texto = coisas[i].innerText;


        if (texto.includes("R$")) {
            let valor = coisas[i].innerText.replace("R$", "").trim();
            soma += parseInt(valor);
            console.log(coisas[i].innerText);
            contar++
        }
    }

        let media = soma / contar;
        console.log("Média:", media);
}
