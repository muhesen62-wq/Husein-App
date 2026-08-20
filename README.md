#Deutsch lernen
A1bis b2
<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deutsch lernen</title>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  background: #f5f5f5;
  color: #222;
}

header {
  background: #1f4e79;
  color: white;
  padding: 25px 15px;
  text-align: center;
}

main {
  padding: 15px;
}

.card {
  background: white;
  padding: 18px;
  margin-bottom: 15px;
  border-radius: 15px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
}

.word {
  font-size: 20px;
  font-weight: bold;
  color: #1f4e79;
}

.translation {
  font-size: 18px;
  margin-top: 8px;
}

.example {
  margin-top: 8px;
  color: #555;
}

button {
  background: #1f4e79;
  color: white;
  border: none;
  padding: 10px 15px;
  border-radius: 10px;
  margin-top: 10px;
  font-size: 16px;
}

.hidden {
  display: none;
}

.section {
  background: white;
  padding: 18px;
  margin-bottom: 15px;
  border-radius: 15px;
}

.section h2 {
  color: #1f4e79;
}
</style>
</head>

<body>

<header>
<h1>🇩🇪 Deutsch lernen</h1>
<p>A2 bis B2</p>
</header>

<main>

<div class="section">
<h2>📖 Seite 28</h2>
<p>Wichtige Wörter – Unternehmen und Beruf</p>
</div>

<div id="words"></div>

<div class="section">
<h2>📖 Seite 29</h2>

<h3>D – Die Organisation eines Unternehmens</h3>

<p>Hier lernen wir wichtige Wörter über die Organisation eines Unternehmens.</p>

<h3>E – Du oder Sie?</h3>

<p>Wie spricht man Menschen im Berufsleben richtig an?</p>

</div>

</main>

<script>

const words = [

["die Filiale, -n","الفرع","Die Firma hat mehrere Filialen."],
["die Öffentlichkeitsarbeit","العلاقات العامة","Sie arbeitet in der Öffentlichkeitsarbeit."],
["eine flache Hierarchie","هيكل إداري هرمي بسيط","Das Unternehmen hat eine flache Hierarchie."],
["das Geschäftsjahr, -e","السنة المالية","Das Geschäftsjahr beginnt im Januar."],
["das Organigramm, -e","المخطط التنظيمي","Das Organigramm zeigt die Struktur der Firma."],
["das Gründungsdatum, -daten","تاريخ التأسيس","Das Gründungsdatum steht auf der Webseite."],
["das Produktionsverfahren, -","طريقة الإنتاج","Das Unternehmen verwendet ein modernes Produktionsverfahren."],
["die Hierarchie, -n","التسلسل الهرمي","Die Hierarchie ist klar strukturiert."],
["die Qualitätssicherung","ضمان الجودة","Die Qualitätssicherung ist sehr wichtig."],
["im Anschluss an (+ Akk.)","بعد / عقب","Im Anschluss an das Treffen sprechen wir weiter."],
["die Rechtsabteilung, -en","القسم القانوني","Die Rechtsabteilung prüft den Vertrag."],
["das Mitspracherecht, -e","حق المشاركة في اتخاذ القرار","Die Mitarbeiter haben ein Mitspracherecht."],
["die Spitze, -n","القمة / أعلى الهرم","Er steht an der Spitze des Unternehmens."],
["nachhaltig","مستدام","Die Firma produziert nachhaltig."],
["an der Spitze von","على رأس / في قمة","Sie steht an der Spitze von dem Unternehmen."],
["etwas präsentieren","يقدم / يعرض شيئًا","Er präsentiert die neuen Produkte."],
["der Pressesprecher, -","المتحدث الصحفي","Der Pressesprecher informiert die Medien."],
["die Pressesprecherin, -nen","المتحدثة الصحفية","Die Pressesprecherin gibt ein Interview."],
["untergeordnet","تابع / أدنى رتبة","Diese Abteilung ist der Geschäftsleitung untergeordnet."],
["untergliedert","مقسّم إلى أقسام فرعية","Das Unternehmen ist in mehrere Bereiche untergliedert."],
["Produkte einführen","طرح منتجات جديدة","Die Firma führt neue Produkte ein."],
["die Verkaufsförderung","تنشيط المبيعات","Die Verkaufsförderung erhöht den Verkauf."],
["die Produktionsstätte, -n","منشأة الإنتاج","Die Produktionsstätte liegt in Leipzig."],
["der Vertrieb","المبيعات / التوزيع","Er arbeitet im Vertrieb."],
["der Rundgang, -e","جولة","Wir machen einen Rundgang durch die Firma."],
["die Verwaltung, -en","الإدارة","Die Verwaltung befindet sich im ersten Stock."],
["das Sortiment, -e","تشكيلة المنتجات","Das Geschäft hat ein großes Sortiment."],
["etwas zuordnen zu (+ Dat.)","شيئًا ينسب / يخصص إلى","Die Aufgabe wird einer Abteilung zugeordnet."],
["der Standort, -e","الموقع","Der Standort der Firma ist zentral."],
["die Terminbestätigung, -en","تأكيد الموعد","Ich habe eine Terminbestätigung bekommen."],
["die Zuständigkeit, -en","الاختصاص / المسؤولية","Die Zuständigkeit liegt bei dieser Abteilung."],
["etwas übernehmen","يتولى شيئًا","Er übernimmt die Verantwortung."],
["der Umsatz, -e","رقم الأعمال / حجم المبيعات","Der Umsatz ist dieses Jahr gestiegen."],
["die Unternehmensgeschichte, -n","تاريخ الشركة","Die Unternehmensgeschichte ist interessant."],
["die Anrede, -n","صيغة المخاطبة","Welche Anrede soll ich benutzen?"],
["die Verkaufsfläche, -n","مساحة البيع","Die Verkaufsfläche ist sehr groß."],
["distanzlos","يتصرف بدون حدود رسمية / متجاوز للحدود","Seine Art wirkt manchmal distanzlos."],
["das Verkaufsgespräch, -e","محادثة البيع","Das Verkaufsgespräch war erfolgreich."],
["das Du","صيغة المخاطبة بـ Du","Im Unternehmen benutzen alle das Du."],
["sich duzen","يخاطب بعضهم بعضًا بـ Du","Wir duzen uns im Team."],
["das Zentrallager, -","المخزن المركزي","Die Ware kommt aus dem Zentrallager."],
["das Zweigwerk, -e","المصنع الفرعي","Das Unternehmen hat ein Zweigwerk."],
["der Kompromiss, -e","حل وسط / تسوية","Wir müssen einen Kompromiss finden."],
["etwas anordnen","يأمر / يرتب / يصدر تعليمات بشأن شيء","Der Chef ordnet eine Änderung an."],
["das Controlling","الرقابة المالية والإدارية","Sie arbeitet im Controlling."],
["die Finanzabteilung, -en","القسم المالي","Die Finanzabteilung prüft die Zahlen."],
["die Fläche, -n","المساحة","Die Fläche des Geschäfts ist groß."],
["Forschung & Entwicklung","البحث والتطوير","Sie arbeitet in Forschung und Entwicklung."],
["die Geschäftsleitung, -en","إدارة الشركة","Die Geschäftsleitung entscheidet."],
["der Hauptbereich, -e","المجال الرئيسي","Das ist unser Hauptbereich."],
["die Haustechnik","تقنيات المبنى / الخدمات الفنية","Die Haustechnik kümmert sich um das Gebäude."],
["die Herstellung","الإنتاج / التصنيع","Die Herstellung dauert zwei Tage."],
["die Hierarchieebene, -n","المستوى الإداري","Er arbeitet auf einer höheren Hierarchieebene."],
["das Lager, -","المستودع","Die Ware liegt im Lager."],
["etwas leiten","يدير / يقود شيئًا","Sie leitet die Abteilung."],
["das Marketing","التسويق","Er arbeitet im Marketing."],
["die Marktuntersuchung, -en","دراسة السوق","Wir machen eine Marktuntersuchung."],
["die Mitarbeiterzahl, -en","عدد الموظفين","Die Mitarbeiterzahl ist gestiegen."],
["einen Kompromiss finden","يجد حلًا وسطًا","Wir müssen einen Kompromiss finden."],
["respektieren","يحترم","Wir müssen andere Menschen respektieren."],
["Sie","حضرتك / أنتم بصيغة رسمية","Im Berufsleben benutzt man oft Sie."],
["sich siezen","يخاطب بعضهم بعضًا بـ Sie","Wir siezen uns im Büro."],
["jemandem das Du anbieten","يعرض على شخص استخدام Du","Er bietet seiner Kollegin das Du an."]

];

const container = document.getElementById("words");

words.forEach((item, index) => {

  const card = document.createElement("div");
  card.className = "card";

  card.innerHTML = `
    <div class="word">${index + 1}. ${item[0]}</div>
    <div class="translation">🇮🇶 ${item[1]}</div>
    <div class="example">💬 ${item[2]}</div>
    <button onclick="speak('${item[0]}')">🔊 Aussprache</button>
  `;

  container.appendChild(card);

});

function speak(text) {
  const speech = new SpeechSynthesisUtterance(text);
  speech.lang = "de-DE";
  speech.rate = 0.8;
  speechSynthesis.speak(speech);
}

</script>

</body>
</html>
