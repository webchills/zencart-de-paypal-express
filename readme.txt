English visitors please note:
This repository formerly contained a modification to solve the Shipping Adress issues in the PayPal Express module integrated in Zen Cart as described here: 
https://www.zen-cart.com/showthread.php?186414-Paypal-Express-Checkout-Shipping-Address-Issue
As this issue is now resolved in the German Zen Cart version this modification has been removed as it breaks Seller Protection
If you are still suffering from this issue in current American Zen Cart versions, I suggest posting your issues in the American forum thread.
This repository is now holding the new PayPal Express module for the German Zen Cart version 1.5.5f only.

Dieses Modul ist nur für Zen Cart 1.5.5f deutsch geeignet und ersetzt das in 1.5.5f deutsch bereits enthaltene PayPal Express Modul (paypalwpp)

Das in der deutschen Zen Cart Version 1.5.5f enthaltene PayPal Express Modul ist in vielen Szenarien nicht für einen echten Express Checkout geeignet und überschreibt in vielen Szenarien die Lieferadresse der Bestellung ohne Kontrolle mit der bei PayPal hinterlegten Adresse.
Da die Adressdaten bei PayPal oft veraltet sind, kann der Shopbetreiber bei abweichenden Lieferadressen oft nicht sicher sein, ob die Adresse wirklich so gewünscht oder eine veraltete Lieferadresse bei PayPal ist.
Um diese Problematik zu umgehen gab es eine Zeit lang eine Modifikation, die gar keine Lieferadresse übergab und die Bestellung wie eine Lieferung nicht physischer Waren behandelte.
Der Nachteil dieser Modifikation war, dass dadurch der PayPal Verkäuferschutz verloren ging. Und die Modifikation war für einen echten Express Checkout nicht geeignet.

Dieses Update behebt diese Problematiken und ermöglicht den Einsatz von PayPal Express so wie es eigentlich gedacht ist. Natürlich kann es auch weiterhin ohne Express Button im Warenkorb verwendet werden, die Aktivierung dieses Features ist aber empfohlen, da es den Checkout für den Kunden vor allem am Mobile wesentlich einfacher macht. Das Anbieten von Express Checkout erhöht die Conversions nachweislich.

Bei aktiviertem Express Checkout Button kann ein nicht eingeloggter Kunde direkt im Warenkorb oder auf der Loginseite den Checkout mit PayPal starten. Er loggt sich bei PayPal ein und ähnlich wie bei einem Amazon Checkout wird automatisch ein Kundenkonto im Shop angelegt, falls es diese Emailadresse im Shop noch nicht gibt. Der Kunde bekommt ein Willkommensmail mit einem automatisch generierten Passwort, damit er sich später auch normal im Shop einloggen kann. Bei PayPal wählt der Kunde dann seine gewünschte Lieferadresse aus, die wird an den Shop übertragen.

Um sicher zu stellen, dass der Kunde nicht einfach bei PayPal auf weiter geclickt und die Lieferadresse nicht wirklich geprüft hat, wird er auf jeden Fall nochmal auf die checkout_shipping Seite im Shop geleitet, wo ihm angezeigt wird, dass er die Lieferadresse bitte nochmals prüfen soll.
Das dient auch dazu, die gewünschte Versandart auswählen zu können, falls es im Shop mehrere Versandarten gibt. Und es wird sichergestellt, dass die Versandkosten korrekt berechnt und an PayPal übergeben werden. Ändert der Kunde hier seine Lieferadresse, so wird diese Lieferdresse in sein PayPal Adressbuch für künftige Bestellungen synchronisiert.

Ein Kunde, dessen Adressdaten bei PayPal korrekt sind, muss bei einem Express Checkout im Endeffekt also keinerlei Daten manuell im Shop eintippen.

Voraussetzungen:

* Zen Cart 1.5.5f deutsch
* Shop verwendet durchgehend SSL

Änderungen gegenüber dem in 1.5.5f integrierten Originalmodul:

* Konfiguration vollständig auf deutsch übersetzt, mit empfohlenen asführlich erläuterten Einstellungen vorkonfiguriert
* Behebung der Lieferadressenproblematik
* Korrektes Handling der automatisch erstellten Kundenkonten auch bei Verwendung von Bestellen ohne Kundenkonto
* Aktualisierung der PayPal Express Buttons auf die aktuellen Versionen
* Prominentere Plazierung der automatisch generierten Zugangsdaten am Beginn des Willkommensmails
*  Prominentere Plazierung des Express Checkouts auf der Loginseite mit Infotext
