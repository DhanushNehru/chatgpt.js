<div id="repo-cover" align="center">

<div align="center">

###### <a href="https://github.com/kudoai/chatgpt.js/tree/main/docs"><img height=15 style="margin: 0 3px -2px" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/0fc3060273fcff77d3e2ff968d5c74acdab62beb/media/images/icons/earth-americas-icon32.svg"></a> Deutsch | <a href="../..#readme">English</a> | <a href="../zh-cn#readme">简体中文</a> | <a href="../zh-tw#readme">繁體中文</a> | <a href="../ja#readme">日本</a> | <a href="../ko#readme">한국인</a> | <a href="../hi#readme">हिंदी</a> | <a href="../es#readme">Español</a> | <a href="../fr#readme">Français</a> | <a href="../it#readme">Italiano</a> | <a href="../nl#readme">Nederlands</a> | <a href="../pt#readme">Português</a> | <a href="../vi#readme">Việt</a>

</div>

<br>

<h3>

<picture>
    <source type="image/png" media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/chatgpt.js-logo-dark-mode-5995x619.png">
    <img width=700 src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/chatgpt.js-logo-light-mode-5995x619.png">
</picture>
<br><br>

🤖 Eine leistungsstarke clientseitige JavaScript-Bibliothek für ChatGPT
<br><br>

</div>
</h3>

<div id="shields" align="center">

[![](https://img.shields.io/badge/Lizenz-MIT-green.svg?logo=internetarchive&logoColor=white&labelColor=464646&style=for-the-badge)](LICENSE.md)
[![](https://img.shields.io/github/commit-activity/m/kudoai/chatgpt.js?label=Commits&logo=github&logoColor=white&labelColor=464646&style=for-the-badge)](https://github.com/kudoai/chatgpt.js/commits/main)
![](https://img.shields.io/github/size/kudoai/chatgpt.js/dist/chatgpt-2.1.1.min.js?label=Minimierte+Größe&logo=databricks&logoColor=white&labelColor=464646&color=ff69b4&style=for-the-badge)
[![](https://img.shields.io/codefactor/grade/github/kudoai/chatgpt.js?label=Codequalität&logo=codefactor&logoColor=white&labelColor=464646&style=for-the-badge)](https://www.codefactor.io/repository/github/kudoai/chatgpt.js)
[![](https://img.shields.io/badge/Erwähnt_in-Awesome-cca8c4?logo=awesomelists&logoColor=white&labelColor=464646&style=for-the-badge)](https://github.com/sindresorhus/awesome-chatgpt#javascript)
[![](https://img.shields.io/badge/Vorgestellt_auf-Product_Hunt-ff6154?logo=producthunt&logoColor=white&labelColor=464646&style=for-the-badge)](https://www.producthunt.com/posts/chatgpt-js)
[![](https://img.shields.io/badge/Inkubiert_von-100.builders-9146ff?logo=gamejolt&logoColor=white&labelColor=464646&style=for-the-badge)](https://app.100.builders/directory)
![](https://img.shields.io/jsdelivr/gh/hm/kudoai/chatgpt.js?label=jsDelivr+Treffer&logo=jsdelivr&logoColor=white&labelColor=464646&color=gold&style=for-the-badge)

</div>

<div id="bat-signal" align="center">

<br>

📣 _Sind Sie ein OSS-Unterstützer? Liebst du JavaScript? Warum tragen Sie dann nicht zur Zukunft der AI-App-Entwicklung bei? **chatgpt.js** sucht Mitarbeiter für genau diesen Zweck! Öffnen Sie einfach eine [Diskussion](https://github.com/KudoAI/chatgpt.js/discussions/new?category=ideas) oder eine [Pull-Anfrage](https://github.com/KudoAI/chatgpt.js/pulls) (ideen jeder Größe sind willkommen) oder schauen Sie sich unsere [Roadmap](https://github.com/orgs/KudoAI/projects/1) an, um etwas zu finden, zu dem Sie beitragen können!_
    
</div>

<div id="intro">

## Um

</div>

<span style="color: white">chatgpt.js</span> ist eine <span style="color: white">leistungsstarke</span> JavaScript-Bibliothek, die eine <span style="color: white">supereinfache</span> Interaktion mit dem ChatGPT-DOM ermöglicht.

- Reich an Funktionen
- Objektorientierte
- Einfach zu verwenden
- Leicht (und dennoch optimal leistungsfähig)

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

## ⚡ Importieren der Bibliothek

### ES6:

```js
(async () => {
    await import('https://code.chatgptjs.org/chatgpt-latest.min.js');
    // Ihr Code hier...
})();
```

### ES5:

```js
var xhr = new XMLHttpRequest();
xhr.open('GET', 'https://code.chatgptjs.org/chatgpt-latest.min.js');
xhr.onload = function () {
    if (xhr.status === 200) {
        var chatgptJS = document.createElement('script');
        chatgptJS.textContent = xhr.responseText;
        document.head.appendChild(chatgptJS);
        yourCode(); // führt Ihren Code aus
    }
};
xhr.send();

function yourCode() {
    // Ihr Code hier...
}
```

### <img style="margin: 0 2px -0.065rem 0" height=17 src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/starters/media/images/icons/tampermonkey-icon28.png"></picture><img style="margin: 0 2px -0.035rem 1px" height=17.5 src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/starters/media/images/icons/violentmonkey-icon100.png"> Greasemonkey:

> **Hinweis** _Um eine Starter-Vorlage zu verwenden: [kudoai/chatgpt.js-greasemonkey-starter](https://github.com/kudoai/chatgpt.js-greasemonkey-starter)_

Userscript-Repositories wie Greasy Fork führen eine Whitelist vorab genehmigter CDNs (z. B. commitspezifische Referenzen von `cdn.jsdelivr.net`), sodass die Import-URL wesentlich länger ist, um die Veröffentlichung auf diesen Websites zu gewährleisten:

```js
...
// @require https://cdn.jsdelivr.net/gh/kudoai/chatgpt.js@a73c962d8ea7a48d81e8fd260c91b23175753b59/dist/chatgpt-2.1.1.min.js
// ==/UserScript==

// Ihr Code hier...
```

Wenn Sie nicht vorhaben, in diesen Repos zu veröffentlichen, kann stattdessen das einfachere `https://code.chatgptjs.org/chatgpt-latest.min.js` verwendet werden, um die neueste minimierte Version zu importieren.

### <img style="margin: 0 2px -1px 0" height=16 src="https://www.google.com/chrome/static/images/favicons/apple-icon-60x60.png"> Chrome:

> **Hinweis** _Um eine Starter-Vorlage zu verwenden: [kudoai/chatgpt.js-chrome-starter](https://github.com/kudoai/chatgpt.js-chrome-starter)_

Da Google Manifest V2 [irgendwann auslaufen lässt](https://developer.chrome.com/docs/extensions/migrating/mv2-sunset/), ist Remote-Code nicht mehr zulässig, daher ist der lokale Import von chatgpt.js ideal:

1. Speichern Sie https://raw.githubusercontent.com/kudoai/chatgpt.js/main/chatgpt.js in einem Unterverzeichnis (in diesem Beispiel `lib`).

2. Fügen Sie die ES6-Exportanweisung am Ende von `lib/chatgpt.js` hinzu
```js
...
export { chatgpt }
```

3. Fügen Sie in `manifest.json` des Projekts (V3) `lib/chatgpt.js` als über das Internet zugängliche Ressource hinzu
```json
    "web_accessible_resources": [{
        "matches": ["<all_urls>"],
        "resources": ["lib/chatgpt.js"]
    }],
```

4. In Skripten, die `chatgpt.js` benötigen (Vordergrund/Hintergrund gleichermaßen), importieren Sie es wie folgt:
```js
(async () => {
    const { chatgpt } = await import(chrome.runtime.getURL('lib/chatgpt.js'));
    // Ihr Code hier...
})();
```

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

<div id="usage">

## 💻 Verwendung

</div>

**chatgpt.js** wurde mit Blick auf höchste Flexibilität geschrieben.

Zum Beispiel:

```js
chatgpt.getLastResponse();
chatgpt.getLastReply();
chatgpt.response.getLast();
chatgpt.get('reply', 'last');
```

Jeder Aufruf ruft gleichermaßen die letzte Antwort ab. Wenn Sie glauben, dass es funktioniert, wird es wahrscheinlich auch funktionieren ... also geben Sie es einfach ein! (Wer hat Zeit für Dokumente?)

Wenn dies nicht der Fall ist, schauen Sie sich den erweiterten [benutzerleitfaden](https://github.com/kudoai/chatgpt.js/blob/main/docs/USERGUIDE.md) an oder reichen Sie einfach ein [Problem](https://github.com/kudoai/chatgpt.js/issues) ein oder [PR](https://github.com/kudoai/chatgpt.js/pulls) und es wird integriert, ganz einfach!

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

<div id="showcase">

## 🤖 Erstellt mit chatgpt.js

</div>

### <picture><source media="(prefers-color-scheme: dark)" srcset="https://i.imgur.com/RduASbD.png"><img width=16 src="https://raw.githubusercontent.com/adamlui/chatgpt-addons/main/media/icons/openai-favicon64.png"></picture> [ChatGPT-Verlauf löschen](https://autoclearchatgpt.com) <a href="https://github.com/awesome-scripts/awesome-userscripts#chatgpt" target="_blank" rel="noopener"><img src="https://awesome.re/mentioned-badge.svg" style="margin:0 0 -2px 5px"></a>

Löschen Sie Ihren ChatGPT-Abfrageverlauf automatisch, um maximalen Datenschutz zu gewährleisten.
<br>[Installieren](https://github.com/adamlui/autoclear-chatgpt-history#installation) /
[Liesmich](https://github.com/adamlui/autoclear-chatgpt-history#readme) /
[Diskutieren](https://autoclearchatgpt.com/discuss)

### <img width=16 src="https://i.imgur.com/1yjmK3W.png"> [Automatic ChatGPT DAN](https://github.com/madkarmaa/automatic-chatgpt-dan)

Automatically send DAN prompts to ChatGPT.
<br>[Installieren](https://github.com/madkarmaa/automatic-chatgpt-dan#%EF%B8%8F-installation) /
[Liesmich](https://github.com/madkarmaa/automatic-chatgpt-dan#readme) /
[Diskutieren](https://github.com/madkarmaa/automatic-chatgpt-dan/issues)

### <img src="https://media.bravegpt.com/images/bravegpt-icon48.png" width=18> [BraveGPT](https://bravegpt.com) <a href="https://www.producthunt.com/posts/bravegpt?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-bravegpt" target="_blank" rel="noopener"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=385630&theme=light" style="width: 112px; height: 24px; margin:0 0 -4px 5px;" width="112" height="24" /></a>

ChatGPT-Antworten in der Brave Search-Seitenleiste anzeigen (unterstützt von GPT-4!)
<br>[Installieren](https://github.bravegpt.com/#installation) /
[Liesmich](https://github.bravegpt.com/#readme) /
[Diskutieren](https://github.bravegpt.com/discussions)

### <picture><source media="(prefers-color-scheme: dark)" srcset="https://i.imgur.com/RduASbD.png"><img width=16 src="https://raw.githubusercontent.com/adamlui/chatgpt-userscripts/main/media/icons/openai-favicon64.png"></picture> [ChatGPT Automatisches Fortfahren ⏩](https://chatgptautocontinue.com) <a href="https://github.com/awesome-scripts/awesome-userscripts#chatgpt" target="_blank" rel="noopener"><img src="https://awesome.re/mentioned-badge.svg" style="margin:0 0 -3px 3px"></a>

Generieren Sie automatisch mehrere ChatGPT-Antworten weiterhin.<br>
[Installieren](https://github.com/adamlui/chatgpt-auto-continue#installation) /
[Liesmich](https://github.com/adamlui/chatgpt-auto-continue#readme) /
[Diskutieren](https://chatgptautocontinue.com/discuss)

### <picture><source media="(prefers-color-scheme: dark)" srcset="https://i.imgur.com/RduASbD.png"><img width=16 src="https://raw.githubusercontent.com/adamlui/chatgpt-addons/main/media/icons/openai-favicon64.png"></picture> [ChatGPT Automatisches Aktualisieren ↻](https://chatgptautorefresh.com) <a href="https://github.com/awesome-scripts/awesome-userscripts#chatgpt" target="_blank" rel="noopener"><img src="https://awesome.re/mentioned-badge.svg" style="margin:0 0 -2px 5px"></a>

Hält ChatGPT-Sitzungen aktuell, um Netzwerkfehler zu vermeiden + Cloudflare-Prüfungen.
<br>[Installieren](https://github.com/adamlui/chatgpt-auto-refresh#installation) /
[Liesmich](https://github.com/adamlui/chatgpt-auto-refresh#readme) /
[Diskutieren](https://chatgptautorefresh.com/discuss)

### <img src="https://media.duckduckgpt.com/images/ddgpt-icon48.png" width=17> [DuckDuckGPT](https://duckduckgpt.com) <a href="https://www.producthunt.com/posts/duckduckgpt?utm_source=badge-featured&utm_medium=badge&utm_souce=badge-duckduckgpt" target="_blank" rel="noopener"><img src="https://api.producthunt.com/widgets/embed-image/v1/featured.svg?post_id=379261&theme=light" style="width: 112px; height: 24px; margin:0 0 -4px 5px;" width="112" height="24" /></a>

ChatGPT-Antworten in der DuckDuckGo-Seitenleiste anzeigen (unterstützt von GPT-4!)
<br>[Installieren](https://github.duckduckgpt.com/#installation) /
[Liesmich](https://github.duckduckgpt.com/#readme) /
[Diskutieren](https://github.duckduckgpt.com/discussions)

<p><br>

<a href="https://chatgptinfinity.com" target="_blank" rel="noopener">
    <img width=555 src="https://raw.githubusercontent.com/adamlui/chatgpt-infinity/main/chrome/media/images/tiles/marquee-promo-tile-1400x560.png">
</a>

<p><br>

<a href="https://chatgptwidescreen.com" target="_blank" rel="noopener">
    <img width=555 src="https://raw.githubusercontent.com/adamlui/chatgpt-widescreen/main/chrome/media/images/tiles/marquee-promo-tile-1400x560.png">
</a>

<p><br>

<p id="showcase-cta">
Wenn Sie etwas mit chatgpt.js erstellt haben, das Sie teilen möchten, senden Sie eine E-Mail an <a href="mailto:showcase@chatgptjs.org">showcase@chatgptjs.org</a> oder öffnen Sie einfach eine <a href="https://github.com/kudoai/chatgpt.js/pulls" target="_blank" rel="noopener">Pull-Anfrage</a>!
</p>

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

<div id="contributors">

## 🧠 Mitwirkende

</div>

Diese Bibliothek existiert dank Code, Übersetzungen, Problemen und Ideen der folgenden Mitwirkenden:

[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/10906554?first-contrib=2023.03.15&h=41&w=41&mask=circle&maxage=7d '@adamlui')](https://github.com/adamlui)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/71683364?first-contrib=2023.03.16-get-functions&h=41&w=41&mask=circle&maxage=7d '@mefengl')](https://github.com/mefengl)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/131989355?first-contrib=2023.04.30-doc-translations&h=41&w=41&mask=circle&maxage=7d '@Zin6969')](https://github.com/Zin6969)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/30551844?first-contrib=2023.05.02-getlastresponse-bug-report&h=41&w=41&mask=circle&maxage=7d '@madruga8')](https://github.com/madruga8)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/54934866?first-contrib=2023.05.01-clearchats-discard-fix&h=41&w=41&mask=circle&maxage=7d '@XiaoYingYo')](https://github.com/XiaoYingYo)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/129722778?first-contrib=2023.05.24-css-readability&h=41&w=41&mask=circle&maxage=7d '@AliAlSarre')](https://github.com/AliAlSarre)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/100418457?first-contrib=2023.06.02-send-function-bug-report&h=41&w=41&mask=circle&maxage=7d '@madkarmaa')](https://github.com/madkarmaa)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/1170326?first-contrib=2023.06.10-html-parser-idea&h=41&w=41&mask=circle&maxage=7d '@wamoyo')](https://github.com/wamoyo)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/33952?first-contrib=2023.06.10-html-parser-idea&h=41&w=41&mask=circle&maxage=7d '@meiraleal')](https://github.com/meiraleal)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/22633385?first-contrib=2023.07.11-fix-ja-doc-md&h=41&w=41&mask=circle&maxage=7d '@eltociear')](https://github.com/eltociear)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/72805486?first-contrib=2023.07.14-enhance-ko-docs&h=41&w=41&mask=circle&maxage=7d '@Rojojun')](https://github.com/Rojojun)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/62183023?first-contrib=2023.07.24-fix-hi-doc&h=41&w=41&mask=circle&maxage=7d '@iamnishantgaharwar')](https://github.com/iamnishantgaharwar)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/629429?first-contrib=2023.07.31-homepage-starry-bg&h=41&w=41&mask=circle&maxage=7d '@hakimel')](https://github.com/hakimel)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/73983677?first-contrib=2023.08.23-fix-readme-typos&h=41&w=41&mask=circle&maxage=7d '@omahs')](https://github.com/omahs)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/in/29110&h=41&w=41&mask=circle&maxage=7d 'Dependabot')](https://github.com/dependabot)
[![](https://images.weserv.nl/?url=https://i.imgur.com/tNyIPmG.jpg?h=41&w=41&mask=circle&maxage=7d 'ChatGPT')](https://chat.openai.com)
[![](https://images.weserv.nl/?url=https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/icons/poe-icon128.svg?first-contrib=2023.07.27-getandshowreply-method&h=41&w=41&mask=circle&maxage=7d 'Poe')](https://poe.com)
[![](https://images.weserv.nl/?url=https://avatars.githubusercontent.com/u/31427850?h=41&w=41&mask=circle&maxage=7d "@ImgBotApp")](https://github.com/ImgBotApp)

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

<div id="partners">

## 🤝 Partners

</div>

**chatgpt.js** ist teil von [100.builders](https://100.builders), einem KI-inkubator, der finanziert wird von:

<div id="partners-collage" align="center">

<picture>
    <source type="image/png" media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/logos/partners/collage/chatgpt.js-partners-white.png">
    <img width=675 src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/logos/partners/collage/chatgpt.js-partners-black.png">
</picture>

</div>

<br>

<img height=8px width="100%" src="https://raw.githubusercontent.com/kudoai/chatgpt.js/main/media/images/separators/aqua.png">

<div id="star-history" align="center">

<br>

<a href="https://star-history.com/#kudoai/chatgpt.js&Timeline" target="_blank" rel="noopener">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=kudoai/chatgpt.js&type=Timeline&theme=dark" />
    <img width=665 src="https://api.star-history.com/svg?repos=kudoai/chatgpt.js&type=Timeline" />
  </picture>
</a>

<br>_Erwägen Sie, diesem Repo ein ⭐ zu geben, wenn es Ihnen geholfen hat!_

</div>

#

<div align="center">

**[Veröffentlichungen](https://github.com/kudoai/chatgpt.js/tree/main/dist)** /
[Benutzerhandbuch](https://github.com/kudoai/chatgpt.js/blob/main/docs/USERGUIDE.md) /
[Diskutieren](https://github.com/kudoai/chatgpt.js/discussions) /
<a href="#">Zurück nach oben ↑</a>

</div>
