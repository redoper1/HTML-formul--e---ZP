# Postup přípravy HTML formulářů ZP

1. [Stáhneme požadovaný "elektronický PDF formulář"](https://www.iczgroup.com/zakaznicka-zona/formulare-ke-stazeni/) (+ XDP šablonu).
1. Odemkenem formulář pro úpravy pomocí [online nástroje](https://smallpdf.com/unlock-pdf).
1. Zbavíme se XFA datové vrstvy pomocí [online nástroje](https://itextpdf.com/demos/flatten-dynamic-xfa-pdf-free-online) zašktnutím volby "Flatten XFA".
1. Dle PDF formuláře otevřeném v [Inkscape](https://apps.microsoft.com/store/detail/inkscape/9PD9BHGLFC7H), kde získáme rozměry a pozice, vytvoříme HTML formulář za pomoci základních a dodatečných stylů a základní struktury z ukázkového formuláře "[ppz_111_vzp.html](ppz_111_vzp.html)".

- Pro převod obrázků (nejlépe SVG) do Base64, použijeme [online nástroje](https://base64.guru/converter/encode/image) s "Output Format" nastaveným na "Data URI".
- Názvy položek a jejich kódy vycházejí z označení v odpovíjích XDP šablonách.

<p style="font-size:1.25em;margin-bottom:unset">Úpravy obecných stylů reportů (<i>style.(s)css</i>) provádějte pouze v případě, že objevíte nějakou společnou obecnou část ve více formulářích. Specifické styly k jednotlivým formulářům pak piště přímo do HTML do elementu <i>style</i> s ID "<i>report_spec</i>" u konce <i>body</i>.</p>
<br>

- V případě úpravy SASSu bude potřeba mít nasintalovaný Node.js package "Sass/Dart Sass", který dodporučuji nainstalovat pro jednoduchost globálně (`npm -g install sass`/`yarn global add sass` v případě používání Yarnu místo npm (v Byznysu standardně používáme klasické npm)) a spustit kompilaci pomocí `sass -w . --no-source-map` nad tutou složkou.

<br><br>

<p style="font-size:2em;margin-bottom:unset"><mark>Nesahejte na obsažený JS nebo špatně dopadnete!!!</mark></p>
<small style="font-size:0.5em;color:#f00">If you touch the included JS, I will kill you!</small>

![Don't try this](https://i.giphy.com/media/jSDU5qDNYk0DX8fGtM/giphy.webp)
