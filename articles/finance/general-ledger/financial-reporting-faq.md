---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um fjárhagsskýrslugerð.
author: jiwo
ms.date: 07/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3690a541b503281f204221a72bfb5a371984d9e4
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605280"
---
# <a name="financial-reporting-faq"></a>Algengar spurningar um fjárhagsskýrslugerð

Þetta efnisatriði veitir svör við algengum spurningum um fjárhagsskýrslugerð.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Hvernig takmarka ég aðgang að skýrslu með öryggistré?

Eftirfarandi dæmi sýnir hvernig hægt er að takmarka aðgang að skýrslu með öryggistré.

USMF-sýnifyrirtækið er með **efnahagsreikningsskýrslu** sem það vill ekki að allir notendur fjárhagsskýrslugerðar hafi aðgang að. Hægt er að nota öryggistré til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur hafi aðgang að henni.

1. Skráðu þig inn á Financial Reporter Report Designer.
2. Veldu **Skrá \> Ný \> Trjáskilgreining** til að búa til nýja trjáskilgreiningu.
3. Pikkaðu tvisvar (eða tvísmelltu) á línuna **Samantekt** í dálknum **Einingaröryggi**.
4. Veldu **Notendur og hópar**.
5. Veldu notendur eða hópa sem þurfa aðgang að skýrslunni.
6. Veldu **Vista**.
7. Í skýrsluskilgreiningu skal bæta við nýrri trjáskilgreiningu.
8. Í trjáskilgreiningunni skal velja **Stilling**. Síðan undir **Einingaval skipurits** skal velja **taka allar einingar með**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Hvernig auðkenni ég hvaða lyklar passa ekki við stöður mínar?

Ef þú ert með skýrslu sem er ekki með samsvarandi stöðu skaltu nota eftirfarandi ferli til að auðkenna hvern lykil og hvert frávik.

### <a name="in-financial-reporter-report-designer"></a>Í Financial Reporter Report Designer

1. Búa til nýja línuskilgreiningu.
2. Veldu **Breyta \> Setja inn línur úr víddum**.
3. Veldu **MainAccount**.
4. Veldu **Í lagi**.
5. Vista línuskilgreininguna.
6. Stofna nýja dálkskilgreiningu.
7. Stofna nýja skýrsluskilgreiningu.
8. Veldu **Stillingar** og afveldu þennan valkost.
9. Mynda skýrslu. 
10. Flytja skýrsluna út í Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>Í Dynamics 365 Finance

1. Opnaðu **Fjárhagur \> Fyrirspurnir og skýrslur \> Prófjöfnuður**.
2. Stilltu eftirfarandi svæði:

    - **Frá dagsetningu** – Færðu inn upphafsdag fjárhagsárs.
    - **Að dagsetningu** – Færðu inn dagsetninguna sem skýrslan er mynduð fyrir.
    - **Fjárhagsvídd** – Stilltu þetta svæði á **Aðallykill stilltur**.

3. Veldu **Reikna út**.
4. Flytja út skýrslu í Excel.

Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu Financial Reporter yfir í **prófjafnaðarskýrslu** til að bera saman dálkana **Lokastaða**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Þegar ég hanna skýrslu í Report Designer, eða þegar ég mynda fjárhagsskýrslu, fékk ég eftirfarandi skilaboð: „Ekki var hægt að ljúka við aðgerðina vegna bilunar í gagnaveitukerfi.“ Hvernig ætti ég að svara?

Skilaboðin gefa til kynna að vandamál hafi komið upp þegar kerfið reyndi að sækja fjárhagsleg lýsigögn úr gagnaskemmunni á meðan þú notaðir fjárhagsskýrslugerð. Hægt er að leysa úr þessu á tvo vegu:

- Farðu yfir samþættingarstöðu gagnanna með því að fara í **Verkfæri \> Samþættingarstaða** í Report Designer. Ef samþættingunni er ekki lokið skaltu bíða þar til henni líkur. Reyndu svo að gera það aftur sem þú varst að gera þegar skilaboðin birtust.
- Hafðu samband við notendaþjónustu til að finna vandamálið og lagfæra það. Það kann að vera ósamræmi í gögnum í kerfinu. Tæknimenn hjá notendaþjónustu geta aðstoðað þig við að finna vandamálið á þjóninum og þau tilgreindu gögn sem kunna að þarfnast uppfærslu.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Hvernig hefur val á umreikningi sögulegs gengis áhrif á útkomu skýrslunnar?

Sögulegt gengi er yfirleitt notað fyrir reikninga með óráðstöfuðu eigin fé, varanlegum rekstrarfjármunum og eigin fé. Sögulegt gengi gæti verið áskilið, í samræmi við reglur frá Fjárhagsreikningsskilaráði (FASB) eða settar reikningsskilareglur (GAAP). Nánari upplýsingar eru í [Gjaldmiðilsgeta í fjárhagsskýrslugerð](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Hversu margar tegundir af gjaldmiðilsgengi eru til?

Það eru þrjár tegundir:

- **Núverandi gengi** – Þessi tegund er venjulega notuð með efnahagsreikningum. Það er oftast kallað *stundargengi* og getur verið gengi síðasta dags mánaðarins eða á öðrum fyrirframákveðnum degi.
- **Meðalgengi** – Þessi tegund er venjulega notuð með rekstrarreikningum (tap/hagnaður). Hægt er að stilla meðalgengi til að fá ýmist einfalt meðaltal eða vegið meðaltal.
- **Sögulegt gengi** – Þessi tegund er yfirleitt notuð fyrir reikninga með óráðstöfuðu eigin fé, varanlegum rekstrarfjármunum og eigin fé. Þessir reikningar gætu verið áskildir í samræmi við FASB- eða GAAP-reglur.

## <a name="how-does-historical-currency-translation-work"></a>Hvernig virkar sögulegur umreikningur gjaldmiðils?

Gengi fylgir færsludagsetningunni. Því er hver færsla fyrir sig umreiknuð í samræmi við gengið sem á best við.

Við sögulegan umreikning gjaldmiðils má nota forreiknaða stöðu tímabils í stað færsluupplýsinga. Þetta er ólíkt því sem gert er við umreikning núverandi gengis.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Hvernig hefur sögulegur umreikningur gjaldmiðils áhrif á afkomu?

Þegar gögn í skýrslum eru uppfærð gæti orðið töf þar sem endurreikna þarf upphæðir með því að skoða færsluupplýsingar. Þessi töf kemur í hvert skipti sem gengið er uppfært eða fleiri færslur eru bókaðar. Sem dæmi má nefna að ef þúsundir af lyklum eru uppsettir til að gera sögulegan umreikning nokkrum sinnum á dag gæti orðið töf í allt að eina klukkustund áður en gögnin í skýrslunni eru uppfærð. Ef þetta eru hins vegar fáir tilteknir lyklar verður vinnslutími fyrir uppfærslu skýrslugagna aðeins nokkrar mínútur eða minna.

Að sama skapi verða framkvæmdir aukaútreikningar á færslum þegar skýrslur eru búnar til með því að nota umreikning gjaldmiðils fyrir sögulega lykla. Tími við skýrslumyndun getur orðið meira en tvöfalt lengri, allt eftir fjölda lykla.

## <a name="what-are-the-estimated-data-mart-integration-intervals"></a>Hvert er áætlað tímabil milli samþættingar á gagnaskemmu?

Financial Reporter notar 16 verk til að afrita gögn úr Dynamics 365 Finance í gagnagrunn Financial Reporter. Eftirfarandi tafla sýnir þessi 16 verk og sýnir tímabilið sem tilgreinir hversu oft hvert verk er keyrt. Ekki er hægt að breyta þessum tímabilum.

| Heiti                                                       | Tímabil | Tímasetning tímabils |
|------------------------------------------------------------|----------|-----------------|
| Flokkar lykla í AX 2012 í „Lykilflokkur“            | 41       | Mínútur         |
| Lyklar í AX 2012 í „Lykill“                                | 7        | Mínútur         |
| Fyrirtæki í AX 2012 í „Fyrirtæki“                               | 300      | Sekúndur         |
| Fyrirtæki í AX 2012 í „Stofnun/fyrirtæki“                          | 23       | Mínútur         |
| Víddasamsetningar í AX 2012 í „Víddasamsetning“    | 1        | Mínútur         |
| Víddargildi í AX 2012 í „Víddargildi“                | 11       | Mínútur         |
| Víddir í AX 2012 í „Vídd“                            | 31       | Mínútur         |
| Gengi í AX 2012 í „Gengi“                    | 17       | Mínútur         |
| Fjárhagsár í AX 2012 í „Fjárhagsár“                        | 13       | Mínútur         |
| Fjárhagsfærslur í AX 2012 í „Staðreynd“                | 1        | Mínútur         |
| Stigveldi fyrirtækis í AX 2012 í „Tré“                   | 3600    | Sekúndur         |
| Sviðsmyndir í AX 2012 í „Sviðsmynd“                              | 29       | Mínútur         |
| Skilyrði færslugerðar í AX 2012 í „Skilyrði upplýsingagerðar“ | 19       | Mínútur         |
| Viðhaldsverk                                           | 1        | Mínútur         |
| MR-skýrsluskilgreiningar í AX7-fjárhagsskýrslur             | 45       | Sekúndur         |
| Útgáfur MR-skýrslna í „Útgáfur fjárhagsskýrslna“ í AX         | 45       | Sekúndur         |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
