---
title: Líftímastöður afurðar og færslur
description: Þetta efnisatriði útskýrir hvernig skal stjórna hvaða færslur eru leyfðar fyrir hverja líftímastöðu sem hönnunarafurð fer í gegnum á líftíma hennar.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12f95feda887b5f1284624e5f072b498a78d00e1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574642"
---
# <a name="product-lifecycle-states-and-transactions"></a>Líftímastöður afurðar og færslur

[!include [banner](../includes/banner.md)]

Um leið og hönnunarafurð fer í gegnum líftíma sinn er mikilvægt að geta stjórnað hvaða færslur eru leyfðar fyrir hverja líftímastöðu. Til dæmis ætti ekki að setja óþroskaðar afurðir á sölupöntun. Einnig er hægt að stjórna innflæði umræddrar vöru ef hún nálgast lok líftímastöðu sinnar.

Hvað breytingar á líftímastöðu hönnunarafurðar varða, eru slíkar breytingar tengdar við hönnunarútgáfur afurðarinnar. Þar af leiðandi er einnig hægt að tengja líftímastöðu afurðarinnar við hönnunarútgáfur. Þegar líftímastaða afurðar er tengd við hönnunarútgáfu er hægt að nota líftímastöðu til að hafa eftirlit með því hvaða færslur eru leyfðar fyrir hönnunarútgáfuna.

## <a name="create-and-manage-product-lifecycle-states"></a>Búa til og stjórna líftímastöðu afurðar

Til að vinna með líftímastöðu afurðar er farið í **Umsjón hönnunarbreytinga \> Uppsetning \> Líftímastaða afurðar**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýja líftímastöðu skal velja **Nýtt** á aðgerðasvæðinu og stilla síðan svæðin eins og lýst er í eftirfarandi undirköflum.
- Til að breyta fyrirliggjandi líftímastöðu skal velja hana á aðgerðarsvæðinu, velja **Breyta** á aðgerðasvæðinu og stilla síðan reitina eins og lýst er í eftirfarandi undirköflum.
- Til að eyða fyrirliggjandi líftímastöðu skal velja hana á aðgerðasvæðinu og velja svo **Eyða** á aðgerðasvæðinu.

> [!NOTE]
> Hönnunarafurðir nota sömu líftímastöður og staðlaðar afurðir (ekki hönnunarafurðir). Einnig er hægt að opna **Líftímastaða afurðar** sem er lýst í þessu efnisatriði með því að opna **Afurðaupplýsingastjórnun \> Uppsetning \> Líftímastaða afurðar**. Frekari upplýsingar um líftímastöður afurðar, bæði fyrir hönnunarafurðir og staðlaðar afurðir, er að finna í [Yfirliti líftímastöðu afurðar](../pim/product-lifecycle.md).

### <a name="header"></a>Haus

Stilltu eftirfarandi svæði á haus líftímastöðu afurðar.

| Svæði | lýsing |
|---|---|
| Ríki | Sláðu inn heiti líftímastöðu afurðarinnar. |
| lýsing | Sláðu inn lýsingu á líftímastöðu afurðarinnar. |

### <a name="general-fasttab"></a>Flýtiflipinn Almennt

Stilltu eftirfarandi svæði á flýtiflipanum **Almennt**.

| Svæði | lýsing |
|---|---|
| Sjálfgefið þegar losað er til lögaðila | Fyrir staðlaðar afurðir skal stilla þennan valkost á *Já* ef þessi líftímastaða skal gilda fyrir allar sjálfgefnar afurðir þegar þær eru fyrst losaðar. Stillið á *Nei* ef þessi líftímastaða verður notuð handvirkt síðar.<p>Þessi stilling á ekki við um hönnunarafurðir. Líftímastaða útgáfu hönnunarafurðar eftir að hún er stofnuð í hönnunarfyrirtækinu er tilgreind í viðkomandi flokki breytinga á hönnun. Þegar afurðin er losuð til rekstrarfyrirtækis er líftímastaða afurðarinnar afrituð. Nánar tiltekið, þegar hönnunarafurð er losuð til rekstrarfyrirtækis hefur hún sömu líftímastöðu og hún hafði í hönnunarfyrirtækinu. Hægt er að skrifa yfir líftímastöðuna í rekstrarfyrirtækinu.</p> |
| Er virk fyrir áætlunargerð | Stillið þennan valkost á *Já* til að taka með afurðir sem hafa þessa líftímastöðu í útreikningum á stigi aðaláætlanagerðar og uppskriftar. Stillið hana á *Nei* til að taka ekki með afurðir sem eru í þessari líftímastöðu í útreikningum. |

### <a name="enabled-business-processes-fasttab"></a>Flýtiflipi virkjaðra viðskiptaferla

Notaðu flýtiflipann **Virkjaðir viðskiptaferlar** til að stjórna hvaða tiltæku viðskiptaferli má nota fyrir afurðir í núverandi líftímastöðu. Ferlin sem eru skráð á þessum flipa finnast sjálfkrafa á eftirfarandi hátt:

- Í fyrsta skipti sem ný líftímastaða er vistuð, hleður síðan viðskiptaferlin sem eru tiltæk sem stendur.
- Þegar nýjum viðskiptaferlum er bætt við kerfið getur þú uppfært listann á flýtiflipanum **Virkjaðir viðskiptaferlar** fyrir núverandi líftímastöðu með því að velja **Leita að uppfærslum** á aðgerðasvæðinu.

Eftirfarandi reitir eru tiltækir fyrir hvert ferli sem er skráð á flýtiflipann **Virkjaðir viðskiptaferlar**.

| Svæði | lýsing |
|---|---|
| Vinna | Þessi skrifvarða svæði sýnir heiti fyrirliggjandi viðskiptaferlis. |
| Úrvinnslusvæði | Þetta skrifvarða svæði sýnir heiti fyrirliggjandi vinnslusvæðis. |
| Tryggingasamningur | Veldu eitt af eftirfarandi gildum til að stjórna hvort og hvernig núverandi ferli verður heimilað fyrir afurðir með eftirfarandi líftímastöðu:<ul><li>**Virkjað** – Viðskiptaferlið er leyft.</li><li>**Lokað** – Ferlið er ekki leyft. Þegar notandi reynir að nota ferlið fyrir afurð með þessa líftímastöðu, stöðvar kerfið slíkt og birtir villu þess í stað. Þú ætlar t.d. að útiloka kaup á afurðum sem eru við lok líftíma.</li><li>**Virkjað með viðvörun** – Ferlið er leyft en viðvörun birtist. Þú vilt t.d. setja frumgerð afurðar á framleiðslupöntun sem er stofnuð af deild rannsóknar- og þróunarsviðsins. Hins vegar ættu aðrar deildir að fá að vita að þær eiga ekki að hefja framleiðslu á afurðinni strax.</li></ul> |

Þegar þú bætir við fleiri reglum um líftímastöðu sem sérstillingar er hægt að skoða þessar reglur í notandaviðmótinu (UI) með því að velja **Uppfæra ferli** á efra svæðinu. Hnappurinn **Uppfæra ferli** er aðeins tiltækur fyrir stjórnendur.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Líftímastöður fyrirútgefnar afurðir og afurðarafbrigði

Fyrir vöru sem hefur afbrigði (aðal og afbrigði) verður varan (aðal) með líftímastöðu og hvert afbrigði getur einnig verið með mismunandi líftímastöðu.

Ef lokað er á afbrigðið eða vöruna í tilteknum ferlum verður einnig lokað á ferlið. Til að ákvarða hvort ferli sé lokað mun kerfið því framkvæma eftirfarandi athuganir:

- Fyrir vélstýrðar vörur:
  - Ef núverandi hönnunarútgáfa er lokuð skal loka ferlinu.
  - Ef núverandi afbrigði er lokað skal loka ferlinu.
  - Ef losuð vara er lokuð skaltu loka ferlinu.
- Fyrir staðlaðar afurðir:
  - Ef núverandi afbrigði er lokað skal loka ferlinu.
  - Ef losuð vara er lokuð skaltu loka ferlinu.

Gefum okkur til dæmis að aðeins eigi að selja eitt afbrigði (rautt) af tiltekinni vöru (bolur) og loka fyrir sölu á öllum öðrum afbrigðum í bili. Þú gætir útfært þetta með eftirfarandi uppsetningu:

- Tilgreindu líftímastöðu vörunnar sem leyfir ferlið. Til dæmis getur þú úthlutað vörunni (bolnum) líftímastöðunni *Seljanleg* sem leyfir viðskiptaferlið *Sölupöntun*.
- Tilgreindu líftímastöðu fyrir seljanlegt afbrigði sem leyfir ferlið. Einnig er t.d. hægt að úthluta rauða afbrigðinu líftímastpðunni *Seljanlegt*.
- Öll önnur afbrigði verða úthlutuð í aðra líftímastöðu þar sem ferlið er lokað. Til dæmis, úthlutaðu hvíta afbrigðinu (og öllum öðrum afbrigðum) líftímastöðunni *Ekki seljanlegt*, sem lokar fyrir viðskiptaferlið *Sölupöntun*.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
