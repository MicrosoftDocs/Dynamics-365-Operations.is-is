---
title: "Yfirlit reikninga lánardrottna"
description: "Þessi grein veitir almennar upplýsingar um reikninga lánardrottins. Reikningar lánardrottins eru beiðnir um greiðslu fyrir vörur og þjónustu sem voru mótteknar. Lánardrottnareikningar geta táknað reikning fyrir yfirstandandi þjónustu, eða þær geta verið byggðir á innkaupapantanir fyrir tilteknar vörur og þjónustu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a6b18343337ca7058c5027c8d4325c4301f1abed
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-invoices-overview"></a>Yfirlit reikninga lánardrottna

[!include[banner](../includes/banner.md)]


Þessi grein veitir almennar upplýsingar um reikninga lánardrottins. Reikningar lánardrottins eru beiðnir um greiðslu fyrir vörur og þjónustu sem voru mótteknar. Lánardrottnareikningar geta táknað reikning fyrir yfirstandandi þjónustu, eða þær geta verið byggðir á innkaupapantanir fyrir tilteknar vörur og þjónustu. 

<a name="vendor-invoices"></a>Reikningar frá lánardrottni
---------------

Reikning lánardrottins úr innkaupapöntun er reikningur sem er búinn til þegar afurðir eða þjónustur eru mótteknar samkvæmt innkaupapöntun sem var gerð hjá lánardrottni. Reikningur lánardrottins inniheldur haus og ein eða fleiri línur fyrir vörur eða þjónustu. Reikningur lánardrottins lýkur ferlinu úr innkaupapöntun til innhreyfingarskjals afurðar til reiknings lánardrottins. 

Þó að sumir reikningar lánardrottins eru tengdar við innkaupapöntun, getur reikninga lánardrottins líka innihaldið línur sem samsvara ekki innkaupapöntunarlínum. Hægt er að búa líka til reikninga lánardrottna sem eru ekki tengdir við neinar innkaupapantanir. Þessir reikningar lánardrottins gæti standa fyrir yfirstandandi þjónustu eins og rafmagnsreikningur, og þarf ekki að vísa í innkaupapöntun þegar þeim er bætt við. 

Það eru nokkrar leiðir til að færa inn reikning lánardrottins:

-   Komubók lánardrottins gerir kleift að slá hratt inn reikninga sem ekki vísa til innkaupapöntunar, þannig að hægt er að safna upp kostnaðinum. Með því að nota samþykktarbók reikninga lánardrottins, er hægt að velja þá reikninga og bóka á stöðu lánardrottna til að bakfæra uppsöfnun.
-   Reikningabók lánardrottins leyfir þér að færa inn reikninga fljótt sem ekki vísa til innkaupapöntun, í einu skrefi.
-   Ásamt Reikningasafn lánardrottna, leyfir komubók lánardrottins að slá hratt inn reikninga til að safna upp kostnaðar. Hægt er að opna tengd innkaupapantanir seinna til að bóka reikning gagnvart á kostnaðarlykil.
-   **Opna lánardrottnareikninga** og **Biðreikninga lánardrottins** síður gera mögulegt að stofna reikninga lánardrottna frá staðfestar innkaupapantanir.

Eftirfarandi umræðu veita meiri upplýsingar um hvernig á að nota **Opna lánardrottnareikninga** eða **Biðreikninga lánardrottins** síðu til að búa til reikning lánardrottins úr innkaupapöntun.

## <a name="understanding-invoice-line-quantities"></a>Skilja magn reikningslínu
Þegar reikningur lánardrottins er opnuð úr tengdri innkaupapöntun eru reikningslínur stofnaðar úr innkaupapöntuninni. Sjálfgefið er að magn er tekið frá magn á innhreyfingarskjali afurða. Hins vegar er hægt að nota eitthvað af eftirfarandi sjálfgefinni hegðun:

-   **Magn sem móttaka á nú** – Nota þennan valkost fyrir hlutasendingar. Sjálfgefna gildið í reitnum **Magn** er tekið úr **Móttaka nú** magnsvæðinu á innkaupapöntuninni.
-   **Pantað magn** – hægt er að Nota þennan valkost fyrir fullbúnar sendingar. Sjálfgefna gildið í **Magnreit** er tekinn úr **pantað** magnsvæðinu á innkaupapöntuninni.
-   **Skráð magn** – notið þennan valkost ef varan þarfnast skráningar sem tilgreind er í **vörulíkanaflokkur** síðu. Sjálfgefna gildið í svæðinu **magn** er efnislega uppfærslumagnið sem hefur verið skráð.
-   **Magn á innhreyfingarskjali afurða** – Notið þennan valkost ef innhreyfingarskjal afurða hefur þegar verið móttekinn fyrir pöntuninni. Sjálfgefna gildið í svæðinu **magn** er frá heildarmagni tiltækra innhreyfingarskjala afurða.
-   **Skráð magn og þjónustur** – Notið þennan valkost ef magn hefur verið skráð í komubókum fyrir vörur í birgðum eða vörur sem ekki eru í birgðum. Þessi valkostur inniheldur einnig þjónustu, án tillits til þess hvort hún sé skráð.

Ef lögaðili þinn notar reikningsjöfnun, geturðu skoða niðurstöður úr jöfnun magns í **jöfnun magns fyrir Innhreyfingarskjal afurða** dálkur. Einnig er hægt að nota **Jöfnunarupplýsingar** valmyndinni á **Yfirferð** flipa til að skoða niðurstöður jöfnunar magns.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Bæta við línu sem ekki var á innkaupapöntun
Hægt er að bæta við nýrri línu sem ekki var á innkaupapöntun við reikning lánardrottins. Velja verður við vörunúmer eða innkaupategund. Þá er Hægt að bæta magn, verð og upphæðir á línu. Línan verða teknar með aðeins í jöfnunarreglur fyrir heildarupphæð reiknings.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sendir reikning lánardrottins til yfirferðar
Fyrirtækið gæti notað verkflæði til að stjórna endurskoðunarferli fyrir lánardrottnareikninga. Hægt er að nota verkflæði yfirferðar fyrir reikningshausa, reikningslínu, eða bæði. Verkflæðisstýringin á við haus eða línu, eftir því hvað var auðkennt áður en smellt er á stýringuna. Í stað **Bóka** hnappinn sjást í **Senda** hnappur sem hægt er að nota til að senda reikning lánardrottins í gegnum yfirferðarferlið.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Jafna lánardrottnareikninga við innhreyfingarskjöl afurða
Hægt er að færa inn og vista upplýsingar fyrir reikninga lánardrottins og hægt er að jafna reikningslínur við línur í innhreyfingarskjali afurðar. Einnig er hægt að jafna hlutamagn fyrir línu 

Hægt er að stofna reikning lánardrottins á grundvelli línuvara innhreyfingarskjals afurða sem hefur verið móttekið fram að þessu, jafnvel þó allar vörurnar fyrir tiltekna innkaupapöntun hafa ekki verið mótteknar enn. Þetta er t.d. hægt að nota þennan valkost ef lánardrottinn sendir einn reikning á mánuði sem nær yfir allar afhendingar sem hann sendir þennan mánuð. Hvert innhreyfingarskjal afurða birtir hluta eða alla afhendingu varanna á innkaupapöntuninni. 

Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu móttekins magns úr völdum innhreyfingarskjal afurða. Ef bæði **Reikningsafgangur** magnið og **Eftirstöðvar afhendingar** fyrir allar og vörur á innkaupapöntun jafngildir núlli (0), breytist staða innkaupapöntunar í **Reikningsfært**. Ef magn **Reikningsafgangs** er ekki 0, er staða sölupöntunar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.

Þetta ferli gerir ráð fyrir að minnsta kosti eitt innhreyfingarskjal afurða hafi verið bókað fyrir innkaupapöntunina. Reikningur lánardrottisins er byggður á viðkomandi innhreyfingarskjali afurða og endurspeglar magnið á þeim. Fjárhagslegar upplýsingar sem koma fram á reikningnum eru byggðar á upplýsingunum sem færðar eru inn þegar reikningurinn er bókaður.

## <a name="working-with-multiple-invoices"></a>Vinna með marga reikninga

Hægt er að vinna með marga reikninga á sama tíma og bókaðar þá svo samtímis. Ef stofna þarf marga reikninga eru notuð **Biðreikninga lánardrottins** síðu. Ef Bóka þarf og prenta marga reikninga lánardrottna skal nota síðuna staðfestingarbók reikninga Ef þú ert að nota samþykktarbók reikninga, þarf að minnsta kosti eitt innhreyfingarskjal afurða hafi verið bókað fyrir innkaupapöntunina og að reikningur fyrir innkaupapöntunina þarf að hafa verið bókaður í komubók. Fjárhagsupplýsingarnar fyrir reikninginn koma úr reikningnum sem var bókaður í komubókina.





