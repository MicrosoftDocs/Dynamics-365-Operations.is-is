---
title: Skilgreina birgðabiðminni og birgðastöðu
description: Þessi grein útskýrir hvernig á að stilla birgðastuðla og birgðastig sem ákvarða birgðatilboðsskilaboð á Microsoft Dynamics 365 Commerce síður.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 5f882debd09a7076a52606f7ca3aca97d9ec8afe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269193"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Skilgreina birgðabiðminni og birgðastöðu

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að stilla birgðajafna og birgðastig sem ákvarða skilaboðin um framboð á birgðum á Microsoft Dynamics 365 Commerce síður.

Dynamics 365 Commerce höfuðstöðvar geyma birgðagögn og ýmsar rásir á borð við forrit sölustaðar, netverslanir og önnur sérstillt, samþætt forrit sem færa birgðir til og frá á ósamstilltan hátt. Þess vegna er tiltækt birgðavirði sem fengið er í gegnum síðu lagerbirgða í höfuðstöðvum Commerce í gegnum notandaviðmót sölustaðar og í gegnum rafrænt API birgðaframboð ekki alltaf hárnákvæmt í rauntíma.

Í stað þess að sýna raunvirði birgða í netverslun vilja margir smásalar frekar sýna skilaboð um stöðu birgðaframboðs (til dæmis „Tiltækt“ eða „Ekki til á lager“) til að upplýsa viðskiptavini um hvort hægt sé að kaupa vöru eða hún hugsanlega ekki til á lager. Fyrir þessa nálgun verður birgðabiðminni og birgðastöður sem ákvarða skilaboð um birgðaframboð að vera tiltækt og skilgreint.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Skilyrði: Kveikja á eiginleika birgðabiðminnis og birgðastaða

Eiginleiki birgðabiðminnis og birgðastaða er stjórnað í gegnum eiginleikastjórnun í Commerce Headquarters. Til að kveikja á eiginleika skal fylgja þessum skrefum.

1. Opna skal **Kerfisstjórnun** \> **Vinnusvæði** \> **Eiginleikastjórnun**.
1. Leita skal að eiginleikanum **Virkja birgðabiðminni og birgðastöður**, velja línu þess og síðan velja **Virkja núna**.

Þegar kveikt er á eiginleikanum er hægt að finna birgðastöður í **Smásala og viðskipti \> Birgðastjórnun**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Búa til og skilgreina forstillingu birgðastöðu

*Forstilling birgðastöðu* ákvarðar hvort tiltekin staða afurðarmagns sé álitið til staðar í birgðum, ekki til á lager eða einhver önnur sérstillt staða. Hægt er að búa til og skilgreina margar forstillingar birgðastöðu á hvern lögaðila. Hvert forstilling er samsett úr safni birgðastaða og hver staða er skilgreind eftir *sviði*, *kóða* og *merki*.

- **Svið** – Hvert svið er skilgreint eftir *upphafsmagni* og *lokamagni*. Gildi magns fellur innan sviðs ef það er meira en upphafsmagn þess sviðs og ekki meira en lokamagnið.
- **Kóði** – Kóði er innri skammstöfun sem stendur fyrir stöðuna. Viðskiptavinir sem samþætta beint við API-birgðir geta notað kóða til að búa til frekari reglur fyrir tiltekna birgðastöðu. Til dæmis er hægt að slökkva á innkaupamöguleika afurðar þegar kóði birgðastöðu er **ETÁL** (ekki til á lager).
- **Merki** – Merki er lýsandi skilaboð viðskiptavina sem sýnir viðskiptavinum birgðastöðu á svæði netverslunar.

### <a name="create-an-inventory-level-profile"></a>Búa til forstillingu birgðastöðu

Til að búa til forstillingu birgðastöðu skal fylgja þessum skrefum.

1. Fara í **Smásala og viðskipti** \> **Birgðastjórnun** \> **Birgðastöður**.
1. Á aðgerðasvæði skal velja **Nýtt** og slá síðan inn gildi í reitina **Forstillingarkenni** og **Lýsing**.
1. Á flýtiflipanum **Svið** skal velja **Bæta við** til að bæta við nýrri stöðu og síðan færa inn gildi í dálkana **Upphafsmagn**, **Lokamagn**, **Kóði** og **Merki** fyrir þá stöðu. Endurtakið þetta skref til að bæta við fleiri stöðum. Eftir því sem þarf, er hægt að breyta gildunum í gagnahnitanetinu eða velja **Eyða** til að fjarlægja stöðu.
1. Í aðgerðarúðunni skal velja **Vista**.

Þegar ný forstilling er búin til eru tvær birgðastöður sjálfkrafa frumstilltar:

- **ETÁL** - Staðan „ekki til á lager“, þar sem lægri mörk sviðsins stefna á mínus óendanlegt. Ekki er hægt að breyta upphafsmagni og kóða fyrir þessa stöðu.
- **TILT** – Staðan „tiltækt“, þar sem efri mörk sviðsins stefna á óendanlegt. Ekki er hægt að breyta lokamagni og kóða á þessu stigi.

> [!NOTE]
> Hvorki mega vera bil né skaranir milli sviða í skilgreiningu forstillingar.

Hægt er að nota hnappinn **Þýðingar** á aðgerðasvæðinu til að skilgreina staðbundna strengi fyrir skilaboð merkis. Þá þarf að keyra dreifingaráætlunarverkið **1110** (**Altæk skilgreining**) til að samstilla staðbundna strengi við rásir.

### <a name="configure-an-inventory-level-profile"></a>Skilgreina forstillingu birgðastigs

Hægt er að skilgreina forstillingu birgðastöðu í annaðhvort stöðu afurðategundar eða stöðu einstakrar afurðar. Þegar forstilling birgðastöðu er skilgreind fyrir afurð er birgðastaðan ákvörðuð samkvæmt sviðunum sem eru skilgreind í tengdri forstillingu. Annars er birgðastaðan „tiltækt“ eða „ekki til á lager“ ákvörðuð eftir því hvort afurðin sé með jákvæðar lagerbirgðir.

Til að skilgreina forstillingu birgðastöðu fyrir tegund, skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti** \> **Afurðir og tegundir** \> **Afurðastigveldi viðskipta**.
1. Veljið tegundina til að skilgreina forstillingu birgðastöðu fyrir.
1. Í flýtiflipanum **Selja eiginleika afurðar** skal velja lögaðila.
1. Í hlutanum **Birgðir viðskipta**, í reitnum **Forstilling birgðastöðu**, skal velja eina af fyrirframskilgreindum forstillingum birgðastöðu.

Hægt er að nota hnappinn **Uppfæra afurðir** á aðgerðasvæðinu til að dreifa gildi forstillingar á tegundarstigi á undirliggjandi afurðir tegundarinnar. Frekari upplýsingar er að finna í [Stjórna afurðarflokkum og afurðum](category-management-product-creation.md).

Til að skilgreina forstillingu birgðastöðu fyrir útgefna afurð, skal fylgja þessum skrefum.

1. Fara í **Smásölu og viðskipti** \> **Afurðir og tegundir** \> **Losaðar afurðir eftir flokki**.
1. Veljið afurð og opnið síðan afurðaupplýsingasíðu hennar.
1. Í hlutanum **Selja**, í reitnum **Birgðir viðskipta**, í reitnum **Forstilling birgðastöðu**, skal velja eina af fyrirframskilgreindum forstillingum birgðastöðu.

Þegar ný afurð er stofnuð verður reiturinn **Forstilling birgðastöðu**, eins og margar aðrar eigindir á afurðarstigi, stilltur á gildið sem skilgreint er fyrir tegundina sem afurðin tengist.

> [!NOTE]
> Forstilling birgðastöðu er eigind sem miðast við lögaðila. Fyrir sömu tegund eða afurð, getur gildið í forstillingu birgðastöðu verið mismunandi milli lögaðila.

Til að samstilla skilgreiningar á forstillingum birgðastöðu við rásir skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**.
1. Keyrið dreifingaráætlun **1040** (**Afurð**).

## <a name="configure-an-inventory-buffer"></a>Skilgreining birgðabiðminnis

*Birgðabiðminni* er gildi skilgreint af notanda sem dregur viðbótarmagn vöru frá upprunalega magninu til að reikna áætlað magn. Þetta áætlaða magn gefur smásöluaðilum öruggt biðminni þannig að þeir selji ekki of mikið af afurð með því að selja meira en raunverulega birgðir á lager. Hægt er að skilgreina birgðabiðminni á annaðhvort stigi afurðategundar eða stigi einstakrar afurðar. Ef ekkert birgðabiðminni er tilgreint verður sjálfgildið **0** (núll) notað.

Til að skilgreina birgðabiðminni fyrir tegund skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti** \> **Afurðir og tegundir** \> **Afurðastigveldi viðskipta**.
1. Veljið tegundina til að skilgreina birgðabiðminni fyrir.
1. Í flýtiflipanum **Selja eiginleika afurðar** skal velja lögaðila.
1. Í hlutanum **Birgðir viðskipta**, í reitnum **Birgðabiðminni**, skal færa inn jákvætt gildi.

Hægt er að nota hnappinn **Uppfæra afurðir** á aðgerðasvæðinu til að dreifa gildi biðminnis á tegundarstigi á undirliggjandi afurðir tegundarinnar. Frekari upplýsingar er að finna í [Stjórna afurðarflokkum og afurðum](category-management-product-creation.md).

Til að skilgreina birgðabiðminni fyrir útgefna afurð skal fylgja þessum skrefum.

1. Fara í **Smásölu og viðskipti** \> **Afurðir og tegundir** \> **Losaðar afurðir eftir flokki**.
1. Veljið afurð og opnið síðan afurðaupplýsingasíðu hennar.
1. Í flýtiflipanum **Selja**, í hlutanum **Birgðir viðskipta**, í reitnum **Birgðabiðminni**, skal færa inn jákvætt gildi.

Þegar ný afurð er stofnuð verður reiturinn **Birgðabiðminni** stilltur á gildið sem skilgreint er fyrir tegundina sem afurðin tengist.

> [!NOTE]
> Ef bæði forstilling birgðabiðminnis og birgðastöðu eru skilgreind fyrir afurð, verður áætlað magn afurðar (þ.e. upprunalegt magn mínus gildi biðminnis) notað fyrir útreikning á bili til að ákvarða birgðastöðuna.

Til að samstilla skilgreiningar birgðabiðminna við rásir skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce** \> **Upplýsingatækni í Retail og Commerce** \> **Dreifingaráætlun**.
1. Keyrið dreifingaráætlun **1040** (**Afurð**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Nota birgðabiðminni og birgðastöðu í atburðarásum rafrænna viðskipta

Svæðissmiður Commerce notar möguleika birgðabiðminnis og birgðastöðu í höfuðstöðvum Commerce til að ákvarða skilaboð um framboð birgða á svæðum rafrænna viðskipta. Nánari upplýsingar er að finna í [Nota birgðastillingar](inventory-settings.md).

Að öðrum kosti, ef samþætt er við rafræna viðskiptalausn þriðja aðila, er hægt að nota **GetEstimatedAvailability** and **GetEstimatedProductWarehouseAvailability** API til að sýna birgðaframboð fyrir afurð í atburðarás rafrænna viðskipta. Frekari upplýsingar um þessi API er að finna í [Reikna birgðaframboð fyrir smásölurásir](calculated-inventory-retail-channels.md).

Kynning á biðminni birgða og birgðastöðum gerir þessum API kleift að skila kóðum birgðastöðu og skilaboðum sem eru ákvörðuð samkvæmt heildarframboði og tiltæku efnislegu virði. Hægt er að skilgreina API enn frekar til að ákvarða hvort birgðamagninu er skilað ásamt skilaboðunum og hvort tiltækt magn er minnkað af hálfu gildis birgðabiðminnis.

Til að skilgreina svar API afurðaframboðs skal fylgja þessum skrefum.

1. Opnið **Smásala og viðskipti** \> **Uppsetning höfuðstöðva** \> **Færibreytur** \> **Viðskiptafæribreytur**.
1. Í hlutanum **Birgðir verslunar**, í flipanum **Birgðir**, í reitnum **API fyrir afurðaframboð fyrir e-Commerce**, skal velja gildi.
1. Til að nota stillingarnar fyrir rásir skal keyra **1110** (**Altæk skilgreining**) dreifingaráætlun fyrir verk.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna afurðategundum og afurðum](category-management-product-creation.md)

[Nota birgðastillingar](inventory-settings.md)

[Reikna tiltækar birgðir fyrir smásölurásir](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
