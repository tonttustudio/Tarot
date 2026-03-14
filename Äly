const pakka = [
    { n: "Verottaja", t: "Hän ei hymyile. Hän vain laskee mätkysi.", l: "Maksa pois, karkuun et pääse.", k: "12.jpg" },
    { n: "Maanantai", t: "Kaikki on ylivoimaista. Sukkien laitto on olympiaurakka.", l: "Epäonnistumisen mahdollisuus on 110%.", k: "27.jpg" },
    { n: "IKEA-reissu", t: "Säästit 50€, mutta menetit sielusi ja yhden ruuvin.", l: "Kotona odottaa palapeli helvetistä.", k: "22.jpg" }
    // Voit lisätä loput kortit tähän samalla tyylillä!
];

let kayttajanKysymys = "";

function startShuffle() {
    kayttajanKysymys = document.getElementById('user-question').value;
    if (!kayttajanKysymys) kayttajanKysymys = "Mitä tulevaisuus tuo?";
    
    document.getElementById('setup-screen').style.display = 'none';
    document.getElementById('table-screen').style.display = 'flex';
    
    luoKortitPoydalle();
}

function luoKortitPoydalle() {
    const container = document.getElementById('deck-container');
    for (let i = 0; i < 20; i++) { // Luodaan 20 korttia pöydälle
        const card = document.createElement('div');
        card.className = 'card';
        
        // Roiskaistaan kortit satunnaisiin paikkoihin
        const x = Math.random() * 200 - 100; 
        const y = Math.random() * 200 - 100;
        const rot = Math.random() * 40 - 20;

        setTimeout(() => {
            card.style.transform = `translate(${x}px, ${y}px) rotate(${rot}deg)`;
        }, i * 50);

        card.onclick = () => naytaTulos(pakka[i % pakka.length]);
        container.appendChild(card);
    }
}

function naytaTulos(kortti) {
    document.getElementById('display-question').innerText = `Kysyit: "${kayttajanKysymys}"`;
    document.getElementById('card-name').innerText = kortti.n;
    document.getElementById('card-text').innerText = kortti.t;
    document.getElementById('card-extra').innerText = kortti.l;
    document.getElementById('result-overlay').style.display = 'flex';
}
