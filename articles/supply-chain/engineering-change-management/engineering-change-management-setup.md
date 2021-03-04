---
title: Setja upp algeng gildi fyrir umsjón hönnunarbreytinga
description: Þetta efnisatriði lýsir því hvernig á að koma á algengum gildum sem eru notuð fyrir færibreytur í ýmsum hlutum umsjónar hönnunarbreytinga.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductParameters, EngChgEcmSeverityTable, EngChgEcmSeverityRuleSet, EngChgEcmSeverityLookup,EngChgEcmSeverityChart,EngChgEcmRequestSeverityChart,EngChgEcmPriorityTable, EngChgEcmPriorityLookup, EngChgEcmPriorityChart, EngChgEcmMaterialDisposition, EngChgEcmEH
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 86de050ef4110e3485a77099440f3402e46cc498
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430787"
---
# <a name="establish-common-values-for-engineering-change-management"></a>Setja upp algeng gildi fyrir umsjón hönnunarbreytinga

[!include [banner](../includes/banner.md)]

Þegar umsjón hönnunarbreytinga er sett upp þarf að koma á ýmsum söfnum af gildum sem verða notuð til að fylla inn í fellilista í öðrum hlutum notandaviðmótsins. Þú ættir að tilgreina þessi gildi samkvæmt þeim tegundum afurða sem þú framleiðir og tilteknum viðskiptaþörfum.

## <a name="engineering-change-categories"></a>Flokkar breytingar á hönnun

Flokkar hönnunarbreytinga eru notaðar til að skipuleggja breytingarbeiðni á hönnun þannig að það sé auðveldara að stjórna og yfirfara þær. Til dæmis gæti hentað að setja upp verkflæði, háð flokknum sem um ræðir, þar sem tiltekin deild verður að yfirfara framlagðar breytingar. Þess vegna inniheldur breytingarbeiðni hönnunar reitinn **Flokkur**.

Til að koma á fót flokkasafni hönnunarbreytinga sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Flokkar hönnunarbreytinga**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="engineering-change-priorities"></a>Forgangsröðun breytingar á hönnun

Forgangsröðun á hönnunarbreytingum er notuð til að gefa til kynna mikilvægi breytingarbeiðni hönnunar. Hún getur auðveldað þér að fylgjast með mikilvægi breytingarbeiðni hönnunar þannig að auðvelt sé að finna út hvaða beiðnir eigi að vinna fyrst úr og hversu fljótt.

Til að koma á fót samansafni forgangsröðunar hönnunarbreytinga sem er notuð í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Forgangsröðun hönnunarbreytinga**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="engineering-change-reasons"></a>Ástæður hönnunarbreytingar

Ástæður fyrir breytingu á hönnun gefa til kynna orsök eða eðli breytinganna í breytingarbeiðninni.

Til að koma á fót samansafni af ástæðum hönnunarbreytinga sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Ástæður hönnunarbreytinga**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="material-disposal-codes"></a>Kóðar efnisförgunar

Notaðir eru kóðar efnisförgunar til að flokka efni sem er notað í fullbúinni vöru eða íhlutum sem þarf að farga á tiltekinn hátt eða þarf að meðhöndla sérstaklega áður en hægt verður að henda þeim í ruslið. Þegar viðeigandi afurð er bætt við breytingarbeiðni hönnunar er hægt að úthluta förgunarkóða sem hluta af upplýsingum um breytinguna.

Til að koma á fót samansafni af efnisförgunarkóðum sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Kóðar efnisförgunar**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="received-customer-approval"></a>Móttekið samþykki viðskiptavinar

Þegar afurðir eru hannaðar fyrir ákveðinn viðskiptavin þarf oft að staðfesta hönnunina og tæknilýsingarnar áður en afurðin verður gerð tilbúin. Reiturinn **Móttekið samþykki viðskiptavinar** gerir þér kleift að sýna hver staðan er á afurðinni í samþykktarferli viðskiptavinar og/eða hvort samþykktin hafi verið móttekin.

Til að koma á fót samansafni af gildum fyrir móttekið samþykki viðskiptavinar sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Móttekið samþykki viðskiptavinar**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="engineering-change--environmental-health-and-safety-codes"></a>Hönnunarbreyting - Umhverfisöryggi og heilsukóðar

Ef taka þarf tillit til einhverra reglugerða varðandi umhverfisöryggi, eða reglugerða eða ferla fyrirtækisins, við framleiðslu afurðar, er hægt að nota kóða umhverfisöryggis til að skilgreina þær. Í breytingarbeiðni hönnunar er hægt að tilgreina hvaða kóða eiga við um framleiðslu á afurðinni á meðan þú breytir upplýsingunum um tilheyrandi afurð.

Til að koma á fót samansafni af gildum fyrir umhverfismál sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Hönnunarbreyting - kóðar umhverfisöryggis**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

## <a name="engineering-change-severities"></a>Alvarleiki hönnunarbreytingar

Alvarleiki hönnunarbreytingar er notaður til að gefa til kynna hversu mikil áhrif afurðirnar verða fyrir í breytingarbeiðni hönnunar.

Til að koma á fót samansafni af alvarleika hönnunarbreytinga sem er notað í fyrirtækinu skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Alvarleiki hönnunarbreytinga**. Síðan er hægt að nota hnappana á aðgerðasvæðinu til að bæta við, fjarlægja og breyta gildunum og raða þeim í þá röð sem þau eiga að birtast í fellilistunum þar sem þau eru sýnd.

Hægt er að setja upp reglur sem eiga við um hvert alvarleikastig sem er stofnað. Frekari upplýsingar um hvernig á að úthluta þessum reglum er að finna í næsta kafla.

## <a name="engineering-change-severity-rule-sets"></a>Reglusett alvarleika hönnunarbreytingar

Hægt er að nota reglusett alvarleika hönnunarbreytingar til að búa til reglusafn sem hægt er að nota til að reikna út sjálfkrafa alvarleika breytingarbeiðni sem byggir á hvers konar breytingu um er að ræða í tilheyrandi afurðum. Til að nota alvarleikareglur skal opna síðuna **Færibreytur fyrir umsjón hönnunarbreytinga** og stilla reitinn **Alvarleikaregla** til að *Reikna* eða *Reikna sjálfkrafa*.

Þegar kerfið metur alvarleika vinnur úr reglunum í þeirri röð sem þær birtast á síðunni, ofan frá og niður. Til að regla sé valin og forgangur hennar settur þarf að uppfylla allar reglurnar í reglusettinu.

Til að setja upp reglurnar sem eiga við hvert alvarleikastig breytinga sem er búið að skilgreina skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Umsjón hönnunarbreytinga \> Reglusett alvarleika hönnunarbreytingar**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýtt reglusafn skal velja **Nýtt** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er síðar í þessum kafla.
- Til að breyta fyrirliggjandi reglusetti skal velja það úr listasvæðinu, velja **Breyta** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er síðar í þessum kafla.
- Til að eyða fyrirliggjandi reglusetti skal velja það úr listasvæðinu og síðan velja **Eyða** á aðgerðasvæðinu.
- Til að endurraða lista yfir reglusett skal velja reglusett á listasvæðinu og síðan nota hnappana **Upp** og **Niður** á aðgerðasvæðinu til að raða þeim.

Fyrir hvert reglusett skal stilla eftirfarandi reiti:

- **Alvarleiki** – Veljið alvarleikastig til að setja reglur fyrir. Nota skal síðuna **Alvarleiki hönnunarbreytingar** til að stofna og skíra stigin. (Sjá fyrri hluta fyrir frekari upplýsingar.)

Notið hnappana í flýtiflipanum **Reglur** til að bæta við eða fjarlægja reglu úr núverandi alvarleikastillingu. Hver regla er með reitinn **Regla** og **Heiti**. Kerfið setur á reglurnar og sýnir hvers konar breytingar hægt er að gera á afurð. Heitið táknar gerð breytingarinnar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]