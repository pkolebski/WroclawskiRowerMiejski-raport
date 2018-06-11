# *Wrocławski Rower Miejski* - analiza danych z roku 2015
Zestaw danych Wrocławskiego roweru miejskiego zawiera informacje o każdym wypożyczonym
rowerze. Możemy z nich wyczytać kiedy i w jakiej stacji rower zostaw wypożyczony oraz zwrócony. W
połączenie z danymi pogodowymi można sprawdzić jak temperatura czy opady wpływają na ilość
wypożyczonych rowerów.

![fig1](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig1.png)

Na powyższym wykresie, uzyskanym poprzez użycie estymatora Parzena, możemy zauważyć dwie
wyraźne górki. Pierwsza w okolicach 1-4 minutach prawdopodobnie dotyczy wypożyczenia zepsutych
rowerów, które były natychmiast były zwracane. Druga z nich skupia większość danych pomiarowych
i wyraźnie pokazuje, że większość osób korzysta z wypożyczalni za darmo, ponieważ pierwsze 20
minut jest darmowe.

![fig2](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig2.png)

Po usunięciu danych pomiarowych, dla których rower został wypożyczony i zwrócony w tym samym
miejscu, zgodnie z oczekiwaniami, można zauważyć zniknięcie pierwszej górki na wykresie. Usunąłem
także dane, których rower był wypożyczany na dłużej niż 40 minut, ponieważ powyżej tej liczby
wykres był już bardzo bliski zera. PO tych operacjach widzimy, że wypożyczalnia jest najczęściej
wykorzystywana do przejazdów trwających około 10 minut co jest dużo krótsze niż okres, po którym
musimy płacić za każdą minutę.

![fig3](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig3.png)

Dane dotyczące pogody, podczas gdy były wypożyczane rowery pokrywa się z rozkładem normalnym
o parametrach u = 17.04 i sigma = 7.16. Wykres pokazuje, że najwyższe prawdopodobieństwo, że
rower zostanie wypożyczony jest w temperaturze około 17 stopni Celcjusza. Jak można zauważyć,
rower miejski wypożyczany jest najczęściej w okresie wakacyjnym kiedy temperatury są wyższe, ale
chłodniejsze miesiące jak wrzesień czy październik mogły znacząco obniżyć powyższy wynik.

![fig4](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig4.png)

Mała liczba wypożyczeni w kwietniu spowodowane jest tym, że opisywana usługa działała tylko przez
ostatnie 3 tego miesiąca.

![fig5](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig5.png)

Na powyższym wykresie uzyskanym estymatorem Parzena widzimy dość oczywisty fakt, że rower
miejski wykorzystywany jest, gdy nie pada. Ciekawe jest tutaj wzniesienie, oznaczone gwiazdką, dość
znacząco wyłamujące się ze stromej krzywej. W mojej opinii, to zwiększenie się liczby wypożyczonych
rowerów świadczy o tym, że służy on także do szybkiego powrotu do domu w razie początku ulewy.

![fig6](https://github.com/pkolebski/WroclawskiRowerMiejski-raport/blob/master/fig6.png)

Na powyższym wykresie widzimy 7 najczęściej wykorzystywanych stacji z 81 dostępnych. Jak łatwo
się domyślić na szczycie znajdują się tam najczęściej odwiedzany punkty turystyczne, czyli rynek oraz
jego okolice (Rynek, Wita Stwosza – Szewska, Świdnicka – Chrobry), Sky Tower, punkty
komunikacyjne Wrocławia (Rondo Reagana, Dworzec kolejowy). Dobrym pomysłem na rozwój tej
platformy jest obserwowanie tych stacji czy zbyt często nie brakuje tam rowerów oraz, w miarę
możliwości, zagęszczenia liczby stacji w tych okolicach (głównie rynku).



W raporcie użyto danych:
- na temat Wrocławskiego roweru miejskiego ze strony https://www.wroclaw.pl/open-data/
- godzinnych na temat pogody z wrocławskiego lotniska dostępnych na stronie https://rp5.ru/
- dobowych na temat opadów dostępnych na stronie https://dane.imgw.pl/
