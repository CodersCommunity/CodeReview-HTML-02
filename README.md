# Code Review kursu HTML#2

Film: https://www.youtube.com/watch?v=2nWSCxIpHfc

Temat: http://forum.pasja-informatyki.pl/145184/cr-html-%232-budowanie-struktury-strony-www

---

Ten branch zawiera kod z brancha [`refactor`](https://github.com/CodersCommunity/CodeReview-HTML-02/tree/refactor) przepisany na HTML5.

---

_Dokładne wyjaśnienie takich a nie innych zmian w [moim tutorialu o HTML5](http://tutorials.comandeer.pl/html5-blog.html)._

## Lista poprawek

* Nawigację dodatkowo otoczyłem `nav`.
* Dodałem też nagłówek do menu. Można je ukryć w przeglądarkach wizualnych przy pomocy [`.visuallyhidden`](https://github.com/h5bp/html5-boilerplate/blob/b5d6e7b1613fca24d250fa8e5bc7bcc3dd6002ef/dist/doc/css.md#visuallyhidden).
* `div` z główną treścią zmieniłem na `main`.
* Serial umieściłem w `article` i przeniosłem do niego `[id]` z nagłówka.
* Stopkę zamieniłem na `footer`.
* Reklamy nie zmieniałem, bo nie ma żadnej wartości semantycznej. Chociaż można się zastanowić nad `aside`.
