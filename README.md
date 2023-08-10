# olegariotrem-social-links
Social Medias from the rapper @olegariotrem

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro do Militar</title>
    <link rel="stylesheet" href="style.css">
    <script src="./script.js"></script>
</head>
<body>
    <div class="loginContainer">

        <h1>Cadastro</h1>

        <div class="dados-container">
            <input type="text" name="Nome Completo" id="nomeCompleto" class="dadosItem">
            <input type="text" name="Nome de Guerra" id="nomeGuerra" class="dadosItem">
            <select name="posto" id="postoLista" class="dadosItem">
                <option value="none" selected disabled hidden </option>
                <option value="Brigadeiro">Brigadeiro</option>
                <option value="Coronel">Coronel</option>
                <option value="Tenente-Coronel">Tenente-Coronel</option>
                <option value="Major">Major</option>
                <option value="Capitão">Capitão</option>
                <option value="1º Tenente">1º Tenente</option>
                <option value="2º Tenente">2º Tenente</option>
                <option value="Aspirante">Aspirante</option>
                <option value="Suboficial">Suboficial</option>
                <option value="1º Sargento">1º Sargento</option>
                <option value="2º Sargento">2º Sargento</option>
                <option value="3º Sargento">3º Sargento</option>
                <option value="Cabo">Cabo</option>
                <option value="S1">S1</option>
                <option value="S2">S2</option>
                <option value="Civil">Civil</option>
            </select>
            <select name="especialidade" id="especialidadeLista" class="dadosItem">
                <option value="none" selected disabled hidden>Especialidade</option>
                <option value="BCT">BCT</option>
                <option value="BEP">BEP</option>
                <option value="BEV">BEV</option>
                <option value="BEI">BEI</option>
                <option value="BCO">BCO</option>
                <option value="BFT">BFT</option>
                <option value="BMA">BMA</option>
                <option value="BMB">BMB</option>
                <option value="BMT">BMT</option>
                <option value="BSP">BSP</option>
                <option value="SCF">SCF</option>
                <option value="SDE">SDE</option>
                <option value="SEM">SEM</option>
                <option value="SGS">SGS</option>
                <option value="SAI">SAI</option>
                <option value="SML">SML</option>
                <option value="BET">BET</option>
                <option value="SAD">SAD</option>
                <option value="SEL">SEL</option>
                <option value="SEF">SEF</option>
                <option value="SMU">SMU</option>
                <option value="SOB">SOB</option>
                <option value="SIN">SIN</option>
                <option value="Não possuo">Não possuo</option>
            </select>
            <input type="date" class="dadosItem">
            <button onclick="registrar()">Registrar</button>
        </div>
    </div>
    <a href="./listaMilitares.html" id="listaLink">Pesquisar militar cadastrado</a>
    <script src="script.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.0/jquery.min.js"></script>
</body>
</html>

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro do Militar</title>
</head>
<body>
    <ul id="listaMilitares">
        <li>aaa</li>
    </ul>
    <script src="script.js"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.7.0/jquery.min.js"></script>
</body>
</html>


const localStorageKey = 'listaMilitares'

function registrar(){
    let militar1 = document.getElementById('#nomeGuerra');

    if(!militar1.value = 0){
        alert('digite seu nome de Guerra.')
    }else {
        let values = JSON.parse(localStorage.getItem(localStoraKey) || "[]")
        values.push({
            name: input.value
        })
        localStorage.setItem(localStorageKey, JSON.stringify(values))
        mostrarRegistrados();
    }

}



function mostrarRegistrados(){
    let values = JSON.parse(localStorage.getItem(localStoraKey) || "[]");
    let lista = document.getElementById('#listaMilitares');
    lista.innerHTML = ''
    for(let i = 0; i<values.length; i++){
        lista.innerHTML = `<li>${values[i]['name']}`
    }
}


*{
    margin: 0%;
    padding: 0%;
    font-family: Arial, Helvetica, sans-serif;
}
body{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
.loginContainer{
    width: 300px;
    height: 300px;
    background-color: rgb(111, 125, 255);
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 15px;
    box-shadow: 5px 5px 5px rgb(68, 68, 68);
    margin-top: 50px;
    color: white;
}
.dados-container{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 5px;
    margin-top: 10px;
}
.dadosItem{
    width: 210px;
    border-radius: 5px;
    border: 0;
}
#listaLink{
    margin-top: 30px;
    font-weight: normal;
}










