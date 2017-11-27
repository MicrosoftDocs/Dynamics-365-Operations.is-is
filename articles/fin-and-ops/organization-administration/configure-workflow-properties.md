---
title: "Skilgreina eiginleika verkflæðis"
description: "Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5c24f6555508272b65aeb81c5a16a0bd2407f1b4
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="configure-the-properties-of-a-workflow"></a>Skilgreina eiginleika verkflæðis

[!include[banner](../includes/banner.md)]


Þetta efnisatriði útskýrir hvernig skilgreina á mismunandi eiginleika verkflæðis.

Opna verkflæðið í verkflæðisritlinum til að skilgreina eiginleika verkflæðis. Smellið á vinnusvæði verkflæðisritlinum, og smellið síðan á **Eiginleika** til að opna **Eiginleika** síðu. Notið síðan eftirfarandi ferli til að stilla mismunandi eiginleika fyrir verkflæðið.

## <a name="name-the-workflow"></a>Verkflæðinu er gefið heiti
Fylgið þessum skrefum til að færa inn heiti á verkflæðinu.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á svæðinu **Heiti** skal færa inn einkvæmt heiti fyrir Verkflæðið Til dæmis, gefum okkur að stofna ætti verkflæði innkaupabeiðna fyrir hvert land eða svæði starfseminnar, gefa mætti verkflæði innkaupabeiðninnar heitið **Innkaupabeiðni Danmörk** eða **Innkaupabeiðni Spánn**.

## <a name="specify-the-workflow-owner"></a>Tilgreinið eiganda verkflæðis
Eigandi verkflæðis er sá aðili sem stjórnar og viðheldur verkflæðinu. Fylgið skrefum ef tilgreina á eiganda verkflæðis.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Á listanum **Eigandi** skal velja nafn þess aðila sem á að stjórna verkflæðinu.

## <a name="select-an-email-template"></a>Velja tölvupóstssniðmát
Fylgið eftirfarandi skrefum til að velja sniðmát fyrir tölvupóst sem er notuð til að mynda skilaboð tilkynningar um verkflæðið.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Í **sniðmát fyrir Tölvupóst fyrir verkflæðistilkynningar** skal velja sniðmát.

## <a name="enter-instructions-for-users"></a>Færa skal inn notendaleiðbeiningar
Hægt er að veita þeim notendum leiðbeiningar sem senda skjöl til vinnslu og samþykktar. Þessar Notendur eru einnig nefndar *upphafsmenn*. Gefum okkur til dæmis að verið sé að búa til verkflæði fyrir innkaupabeiðni, og þú færir inn leiðbeiningar. Notendur sem færa inn innkaupabeiðnir geta skoðað leiðbeiningar á síðunni **Innkaupabeiðnir** . TIL að skoða leiðbeiningarnar, smellir upphafsmaðurinn á táknið á skilaboðastikunni. Fylgið eftirfarandi skrefum til að bæta við leiðbeiningum fyrir notendur.

1.  Í vinstri glugganum, smelltu á **grunnstillingar**.
2.  Í **leiðbeiningar við framlagningu** svæðinu, færið inn leiðbeiningar.
3.  Hægt er að sérsníða leiðbeiningarnar með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar leiðbeiningar birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á **leiðbeiningar við framlagningu** til þess að tilgreina hvar staðgengill á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

4.  Til að bæta þýðingum við leiðbeiningar skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Hægt er að sérsníða texta með því að færa inn staðgengla. Sjá skref 3 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.
    6.  Smellið á **Loka**.

## <a name="specify-when-this-workflow-is-used"></a>Tilgreina skal hvenær á að nota þetta verkflæði
Hægt er að stofna mörg verkflæði á grundvelli sama gerð. Til dæmis er hægt að stofna innkaupabeiðniverkflæði fyrir hvert land eða svæði starfseminnar, eins og Innkaupabeiðni Danmörk og Innkaupabeiðni Spánn. Þegar búið er að stofna mörg verkflæði á grundvelli sama gerðar, verður að tilgreina hvenær á nota hvert verkflæði. Fyrir dæmið hér á undan, tilgreinið eftirfarandi skilyrði:

-   Innkaupabeiðni Danmörk er notað þegar: landið/svæðið er = DK.
-   Innkaupabeiðni spánn er notað þegar: landið/svæðið er = ES.

Fylgið eftirfarandi skrefum til að tilgreina hvenær á að nota skilgreint verkflæði.

1.  Á vinstra svæðinu er smellt á **virkja**.
2.  Veldu gátreitinn **Tilgreina skilyrði fyrir keyrslu verkflæðisins**
3.  Smellt er á **Bæta við Skilyrði**.
4.  Færið inn skilyrði.
5.  Færið inn öll önnur skilyrði sem krafist er.
6.  Til að sannreyna að skilyrðin sem voru færð hafi verið stilllt rétt, skal fylgja eftirfarandi skrefum:
    1.  Smellið á **Prófun**.
    2.  Á síðunni **Kanna verkflæðisskilyrði** , í **Villuleita skilyrði** svæði, velja færslu.
    3.  Smellið á **Prófun**. Kerfið metur færsluna og ákveður hvort hún standist skilyrði sem þú skilgreindir. Til dæmis, ef verið er að búa til verkflæði fyrir innkaupabeiðni á Spáni sýnir svæðið **Villuleita skilyrði** á síðunni lista yfir innkaupabeiðnir. Þegar smellt er á **Prófun** mun kerfið meta valdar innkaupabeiðnir og ákveða hvort Land/svæði er ES.
    4.  Smelltu á **Í lagi** eða **hætta við** til að fara aftur síðuna **forstillingar**.

## <a name="specify-when-notifications-are-sent"></a>Tilgreinið hvenær tilkynningar eru sendar út
Þegar skjal er sent í vinnslu þá er verkflæðistilvik stofnað. Hægt er að senda tilkynningar til notenda þegar verkflæðistilvik á grundvelli verkflæðisins, eru sett af stað, lokið við þau, eytt, eða þau stöðvuð út af villu. Fylgið eftirfarandi skrefum til að tilgreina hvenær senda á út tilkynningar.

1.  Á svæðinu vinstra megin, smella á **tilkynningar**.
2.  Veljið gátreit fyrir hvert tilvik sem á að virkja tilkynningar:
    -   **Byrjað** — senda út tilkynningar þegar byrjað er á verkflæðistilviki.
    -   **Stöðvað (villa)** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af villu.
    -   **Byrjað** — senda út tilkynningar þegar verkflæðistilviki er lokið.
    -   **Óafturkræft** — senda út tilkynningar þegar verkflæðistilvik hefur verið stöðvað út af óafturkræfri villu.
    -   **Slitið** — senda út tilkynningar þegar verkflæðistilviki er slitið.

3.  Veljið línu fyrir tilvik sem þú valdir í skrefi 2.
4.  Á **tilkynningartexti** flipanum í textareitinn, færa inn texta tilkynningarinnar.
5.  Hægt er að sérsníða texta með því að færa inn staðgengla. Staðgenglar eru settir í stað viðeigandi gagna þegar textinn birtist notendum. Fylgið eftirfarandi skrefum til að færa inn staðgengil:
    1.  Smellið á reit til þess að tilgreina hvar staðgengill á að birtast.
    2.  Smella á **Setja inn staðgengil**
    3.  Í listanum sem birtist skal velja staðgengilinn til að setja inn.
    4.  Smellt er á **Setja inn**.

6.  Til að bæta þýðingum við textann, skal fylgja þessum skrefum:
    1.  Smellt er á **Þýðingar**.
    2.  Á síðunni sem birtist er smellt á **bæta við**.
    3.  Í listanum sem birtist skal velja tungumálið sem á að færa inn í textanum.
    4.  Í svæðið **þýddur texti** skal færa inn textann.
    5.  Hægt er að sérsníða texta með því að færa inn staðgengla. Sjá skref 5 til að fá leiðbeiningar um hvernig á að færa inn staðgengill.
    6.  Smellið á **Loka**.

7.  Á **Viðtakanda** flipanum skal nota eftirfarandi valkosti til að tilgreina hver eigi að fá tilkynningar.
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Valkostur</th>
    <th>Tilkynningar eru sendar þessum notendum.</th>
    <th>Fylgið eftirfarandi skrefum til að senda tilkynningar,</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Þátttakendur</td>
    <td>Notendur sem tilheyra tilteknum hópi eða hlutverki</td>
    <td><ol>
    <li>Á <strong>Viðtakanda</strong> flipanum, smellið <strong>Þátttakanda</strong>.</li>
    <li>Á flipanum <strong>Hlutverkamiðað</strong> , á listanum <strong>Gerð þátttakanda</strong> skal velja gerð hóps eða hlutverks til að senda tilkynningu á.</li>
    <li>Í listanum <strong>Þátttakanda</strong> skal velja hópi eða hlutverk til að senda tilkynningar til.</li>
    </ol></td>
    </tr>
    <tr class="even">
    <td>Verkflæðisnotandi</td>
    <td>Notendur sem eru þáttakendur í þessu verkflæði</td>
    <td><ol>
    <li>Á <strong>Viðtakanda</strong> flipanum, smellið <strong>verkflæðisnotandi</strong>.</li>
    <li>Á <strong>verkflæðisnotandi </strong> flipanum, á <strong>verkflæðisnotandi </strong>listanum, veldu notandann sem tekur þátt í verkflæði.</li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td>Notandi</td>
    <td>Sértækir notendur Finance and Operations</td>
    <td><ol>
    <li>Á <strong>Viðtakanda</strong> flipanum, smellið <strong>notandi</strong>.</li>
    <li>Á flipanum <strong>Notendur</strong> inniheldur listinn <strong>Tiltækir notendur</strong> alla notendur í Finance and Operations. Veldu Notendur til að senda tilkynningar á , og færðu síðan þessa notendur í <strong>Valdir notendur</strong> lista.</li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  Endurtakið skref 3 til 7 hvert tilvik sem valin var í skrefi 2.

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a>Færðu inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu.
Til að færa inn athugasemdir um þær breytingar sem þú hefur gert á verkflæðinu, fylgdu þessum skrefum.

1.  Á vinstra svæðinu er smellt á **Athugasemdir**.
2.  Í svæðinu **færa Inn athugasemdir um verkflæðið** , færið inn athugasemdir.
3.  Farðu aftur yfir Athugasemdir þitt. Þegar búið er að bæta við athugasemd er ekki hægt að breyta henni.
4.  Smellið á **Bæta við** til að bæta athugasemdir við **ferill Athugasemda** svæði.





