Darbs ar DOM elementiem un dinamiska satura veidošana



Vārds, uzvārds: Vladimirs Požarskis
Datums: 2026-01-19



1. uzdevums – DOM jēdziens (teorija)



1.1. Kas ir DOM?
DOM (Document Object Model) ir veids, kā pārlūks attēlo HTML dokumentu kā objektu koku. Ar JavaScript mēs varam piekļūt šiem objektiem un mainīt lapas saturu un izskatu.



1.2. Kāpēc DOM ir nepieciešams dinamiskos tīmekļa produktos?
DOM ir nepieciešams, lai tīmekļa lapa varētu mainīties bez pārlādēšanas: piemēram, atjaunināt tekstu, rādīt vai slēpt elementus, pievienot jaunus blokus, reaģēt uz lietotāja klikšķiem un ievadi.



2. uzdevums – DOM elementu atlase



2.1. Nosauc vismaz 3 DOM elementu atlases metodes:

1. document.getElementById("id")
2. document.querySelector("selektors")
3. document.querySelectorAll("selektors")
   Papildus piemēri: getElementsByClassName, getElementsByTagName.



2.2. Kuru atlases metodi Tu šodien izmantoji visbiežāk? Kāpēc?
Visbiežāk izmantoju querySelector(), jo ar to var atlasīt elementu gan pēc id, gan pēc class, gan pēc jebkura CSS selektora, un tas ir ērti un universāli.



3. uzdevums – Esoša HTML elementa maiņa ar JavaScript

Koda fragments:
Atlasu elementu pēc id
const virsraksts = document.querySelector("#title");

Mainu saturu
virsraksts.textContent = "Sveiki!";

Mainu stilu
virsraksts.style.color = "darkblue";
virsraksts.style.fontSize = "32px";
virsraksts.style.textTransform = "uppercase";



3.1. Apraksti, kas notiek lapā, kad šis kods tiek izpildīts:
Kad kods izpildās, tiek atrasts elements ar id title. Tam tiek nomainīts teksts uz “Sveiki! DOM ir foršs”, un vizuāli virsraksts kļūst tumši zils, lielāks un ar lielajiem burtiem.



4. uzdevums – Dinamiska HTML elementa izveide

Koda fragments:
Izveidoju jaunu elementu
const p = document.createElement("p");
p.textContent = "Šis parādījās dinamiski ar JavaScript";
p.classList.add("dynamic-note");

Pievienoju lapai
document.body.appendChild(p);



5. uzdevums – HTML elementa noņemšana

Koda fragments:
const dynamic = document.querySelector(".dynamic-note");
if (dynamic) {
dynamic.remove();
}



6. uzdevums – DOM nozīme dinamiskā produktā



6.1. Raksturo DOM manipulāciju nozīmi dinamiskos tīmekļa produktos.
DOM manipulācijas ļauj lapai būt interaktīvai un mainīt saturu bez pārlādēšanas. Ar tām var parādīt vai paslēpt elementus, atjaunināt informāciju un reaģēt uz lietotāja darbībām. Bez DOM JavaScript nevarētu ietekmēt HTML elementus, tāpēc tas ir pamats dinamiskām tīmekļa lietotnēm.



7. uzdevums – Refleksija

Šajā stundā iemācījos, ka HTML dokumentu var uztvert kā objektu koku un ar JavaScript var mainīt lapas saturu reāllaikā. Iemācījos atlasīt elementus, mainīt tekstu un stilus, kā arī izveidot un dzēst elementus.

