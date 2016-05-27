# Code Review kursu HTML#2

Film: https://www.youtube.com/watch?v=2nWSCxIpHfc

Temat: http://forum.pasja-informatyki.pl/145184/cr-html-%232-budowanie-struktury-strony-www

---

Ten branch zawiera poprawki dotyczące kodu strony – bez przepisywania jej na HTML5.

---


## Lista poprawek

_Rzeczy zmienione, a oznaczone jako **preferencja** są po prostu moimi osobistymi preferencjami co do kodu HTML i nie są lepsze/gorsze od pierwotnego sposobu; są po prostu inne._

### Ogólne

* Utworzyłem katalog `images`, do którego przeniosłem `reklama.jpg` – dobra struktura katalogów to podstawa każdego projektu (**preferencja**).
* Plik **tabele.html** całkowicie wyleciał, bo [nie ma prawa bytu od jakichś **15 lat**](http://web.archive.org/web/20130902063810/http://osiolki.net/tabelki/).
* Zmieniłem wcięcia i nowe linie w kodzie na IMO czytelniejsze (**preferencja**).
* Usunąłem zamknięcie XML-owego ze znaczników bez zamknięcia (**preferencja**).
* Zmieniłem nazwę `html` na wersję pisaną małymi literami w `DOCTYPE` (**preferencja**).
* Zmieniłem nazwę kodowania na `UTF-8` (**preferencja**, choć dawniej [walidator się tego czepiał](http://tutorials.comandeer.pl/html5-blog.html#ustawienie-kodowania)).
* Usunąłem `div.container` i jego style przeniosłem na `body`. Bo jeśli można pozbyć się dodatkowego elementu, to dlaczego tego nie zrobić? (**preferencja**)

### `head`

* Przeniosłem `meta[http-equiv="X-UA-Compatible"]` tuż po `meta[charset]` i **zostawiłem** te tagi jako pierwsze w `head` – wszystko z powodu [znanych bugów](https://github.com/h5bp/html5-boilerplate/blob/b5d6e7b1613fca24d250fa8e5bc7bcc3dd6002ef/dist/doc/html.md#the-order-of-the-title-and-meta-tags).
* Usunąłem z `meta[http-equiv="X-UA-Compatible"]` fragment `,chrome=1`, gdyż Chrome Frame [nie istnieje od lat](http://blog.chromium.org/2013/06/retiring-chrome-frame.html).

### CSS

* Przeniosłem style do osobnego arkusza – w myśl zasady [trójpodziału warstw strony WWW](http://webroad.pl/inne/3722-progressive-enhancement-zapomniany-fundament).
* Wywaliłem stylowanie po `[id]`, gdyż [jest to powszechnie znana zła praktyka](http://forum.pasja-informatyki.pl/109776/html-class-czy-id?show=109816#a109816).
* Klamerki otwierające (`{`) przeniosłem do tej samej linijki, co selektor (**preferencja**).
* Reguły dla poszczególnych elementów rozdzieliłem znakiem nowej linii (**preferencja**).

### `body`

* Wywaliłem `div#logo`, bo ten element był całkowicie niepotrzebny – z powodzeniem ostylować można samo `h1`.
* Menu zamieniłem na listę, bo to [ogólnie uznany standard](https://css-tricks.com/wrapup-of-navigation-in-lists/). Tym samym dodałem do stylów regułkę usuwają wypunktowanie w menu.
* Dodałem linkowanie do poszczególnych sekcji przy pomocy `[id]` przy nagłówkach (bo właśnie do tego służy `[id]`, a nie do stylowania!).
* Zamieniłem bezsensowne `br` na odpowiednie akapity i inne tagi.
* Dodałem `[alt]` do reklamy. **ABSOLUTNIE KAŻDY OBRAZEK MUSI MIEĆ `[alt]`!!!** Wypada to wiedzieć i znać [podstawowe zasady tworzenia `[alt]`](https://www.w3.org/TR/html51/semantics.html#alt) ([inna wersja](http://webaim.org/techniques/alttext/)). Warto też potestować, czy `[alt]` faktycznie ma sens, używając do tego [czytnika ekranowego](http://www.freedomscientific.com/Products/Blindness/JAWS). W przypadku reklamy poprawny `[alt]` zależy od kontekstu. W przypadku, gdy reklama ma sens jedynie wówczas, gdy jest widziana, można ze spokojem dać pusty `[alt]`. W innym wypadku można się pokusić o opisanie tego, co jest reklamowane.
* Pozwoliłem sobie zamienić encję `&copy;` bezpośrednio na odpowiedni znaczek Unicode (`©`).

## Inne

* Zamieniłem `-` na `—`… bo tak ;)
