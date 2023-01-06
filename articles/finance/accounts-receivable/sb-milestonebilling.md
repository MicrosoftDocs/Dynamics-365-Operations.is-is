---
title: Sniðmát áfanga
description: Þessi skrá útskýrir hvernig á að setja upp áfangainnheimtuvirkni í áskriftarinnheimtu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856771"
---
# <a name="milestone-billing"></a>Útskrift samkvæmt þáttaskilum

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að skilgreina sniðmát fyrir aðgerð áfangagreiðslu í áskriftargreiðslu. Fyrir hverja línu í áfangasniðmátinu er hægt að skilgreina úthlutunarhlutfall eða upphæð. Síðan er hægt að úthluta áfangasniðmáti á vörur greiðsluáætlunar sem nota aðgerð áfangagreiðslu.

## <a name="add-a-template"></a>Bæta við sniðmáti

Til að bæta við áfangasniðmáti skal fylgja þessum skrefum.

1. Opnið **Áskriftargreiðslur \> Endurteknar samningsgreiðslur \> Uppsetning \> Áfangasniðmát**.
2. Veljið **Nýtt**.
3. Einkvæmt kenni fyrir nýju mælinguna er fært í reitinn **Sniðmát áfanga**.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í svæðinu **Úthlutunaraðferð** skal velja úthlutunaraðferð.
6. Valfrjálst: Í reitnum **Heildarupphæð** skal tilgreina heildarupphæð fyrir sniðmátið.
7. Veljið **Bæta við** til að bæta við línu. Síðan skal velja vörunúmerið fyrir nýju línuna á svæðinu **Vörunúmer**.
8. Fylgdu einu af þessum skrefum, allt eftir gildinu sem þú valdir á svæðinu **Úthlutunaraðferð**:

    - Ef **Prósenta** var valin sem úthlutunaraðferð skal í reitnum **Prósenta** tilgreina úthlutunarprósentu fyrir hverja línu. Ef prósentur eru tilgreindar verður samanlögð prósenta sem sýnt er í reitnum **Samtals prósenta** að vera jafnt og **100**.
    - Ef **Breytileg upphæð** er valið sem úthlutunaraðferð skal í reitnum **Upphæð** tilgreina upphæðina fyrir hverja línu.
    - Ef þú valdir **Jöfn upphæð** sem úthlutunaraðferð þarftu ekki að tilgreina upphæð. Hver lína verður uppfærð með réttri prósentu og upphæð samkvæmt vörufjölda sem bætt er við sniðmátið.

9. Veldu **Vista**.

## <a name="delete-a-template"></a>Sniðmáti eytt

Til að eyða áfangasniðmáti skal fylgja þessum skrefum.

1. Veljið eina eða fleiri línur til að eyða og veljið svo **Eyða**.
2. Ef þú færð kvaðningu um að staðfesta aðgerðina velurðu **Já**.

## <a name="milestone-template-fields"></a>Áfangasniðmátsreitir

Síðan **Sniðmát áfanga** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|-------|-------------| 
| Sniðmát áfanga | Einkvæmt auðkenni áfangasniðmáts. |
| Lýsing | Lýsing á áfangasniðinu. |
| Úthlutunaraðferð | <p>Velja úthlutunaraðferð:</p><ul><li>**Prósentum lokið** – Uppsafnað lokagildi er notað fyrir hverja línu.</li><li>**Prósenta** – Hægt er að tilgreina prósentuupphæð fyrir úthlutunina. Samtala allra prósenta verður að vera jöfn 100.</li><li>**Breytileg upphæð** – Hægt er að tilgreina upphæð fyrir úthlutunina. Úthlutunarupphæð er tilgreind á færslustigi.</li><li>**Jöfn upphæð** – Úthlutunarprósenturnar eru reiknaðar sjálfkrafa og skipt jafnt á vörurnar í sniðmátinu.</li></ul> |
| Heildarfjöldi daga, heildarfjöldi tíma | Tilgreinið áfangaupphæð fyrir sniðmátið. |
| **Línur** | |
| Vörunúmer | Velja vörunúmerið fyrir áfangasniðmátið. |
| Afurðarheiti | Heiti vörunnar. |
| Prósenta | <p>Sláðu inn úthlutunarprósenta fyrir línuna:</p><ul><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Prósenta** skal tilgreina prósentuna fyrir línuna.</li><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Jöfn upphæð** er prósentunni sjálfkrafa skipt niður í jafnar prósentur út frá vörufjölda í sniðmátinu.</li></ul><p>Samtala allra hlutfalla verður að vera jöfn 100.</p><p>Ef gildið **Heildarupphæð** er tilgreint í hausnum og gildinu **Prósenta** er breytt fyrir línuna er gildið **Upphæð** uppfært. Ef þú breytir aftur á móti gildi **Upphæð** er gildi **Prósenta** uppfært.</p> |
| Upphæð | <p>Úthlutunarupphæðin fyrir línuna:</p><ul><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Breytileg upphæð**, tilgreinið upphæð fyrir línuna.</li><li>Ef reiturinn **Úthlutunaraðferð** er stilltur á **Jöfn upphæð** er upphæðinni sjálfkrafa skipt niður í jafnar upphæðir út frá vörufjöldanum í sniðmátinu og gildinu **Heildarupphæð** sem er tilgreint í hausnum.</li></ul><p>Samtala allra upphæðanna verður að vera jöfn gildi **Heildarupphæð** sem er tilgreind í hausnum.</p><p>Ef gildið **Heildarupphæð** er tilgreint í hausnum og gildinu **Upphæð** er breytt fyrir línuna er gildið **Prósenta** uppfært. Ef þú breytir aftur á móti gildi **Prósenta** er gildi **Upphæð** uppfært.</p> |
| **Samtala** | |
| Prósentusamtala | Samtala prósenta. Samtala allra prósenta verður að vera jöfn 100. |
| Heildarfjöldi daga, heildarfjöldi tíma | Summa gilda fyrir **Upphæð** fyrir allar línur. Þessi summa verður að vera jöfn gildi **Heildarupphæð** sem er tilgreind í hausnum. |
| Upphæð eftirstöðva | Upphæð eftirstöðvanna. Gildið er reiknað sem gildið **Heildarupphæð** úr hausnum mínus summan af gildunum **Upphæð** fyrir allar línurnar.|

## <a name="milestone-allocation"></a>Úthlutun áfanga

Áður en byrjað er að nota áfangavirkni ætti að ljúka þessum verkefnum.

1. Bæta við einum eða fleiri áfangasniðmátum.
2. Stofnið greiðsluáætlunarflokk. Tilgreinið **Áfangi** sem vörutegund og veljið sniðmát.
3. Á **Vöruuppsetning** síðunni (**Áskriftargreiðslur \> Endurteknar samningsgreiðslur \> Uppsetning \> Vörur**), sskal velja vöruvensl og áfangasniðmát fyrir uppsetningu vörunnar.

Þegar áfangasniðmátið, greiðsluáætlunarflokkarnir og vörurnar hafa verið búin til er hægt að búa til greiðsluáætlun sem notar áfangaaðgerðina.

Til að setja upp greiðsluáætlun sem notar áfanga skal fylgja þessum skrefum.

1. Á listanum **Allar/Virkar greiðsluáætlanir** á síðunni **Greiðsluáætlun** skal velja **Ný**.
2. Á síðunni **Allar greiðsluáætlanir** skal búa til nýja greiðsluáætlun og tilgreina viðskiptavinalykil og upphafsdagsetningu.
3. Í hlutanum **Greiðsluáætlunarlínur** skal velja **Bæta við línu**. Bætið síðan við vörunúmeri og stillið svæðið **Vörutegund** á **Áfangi**.

    Ef sjálfgefið áfangasniðmát er sett upp fyrir vöruna er áfangatilvikunum sjálfkrafa bætt við greiðsluáætlunarlínurnar. Lokadagsetningar eru auðar fyrir áfangalínur.

    Ef ekkert áfangasniðmát er sett upp fyrir vöruna skal velja **Úthlutun áfanga**. Á síðunni **Áfangaúthlutun** skal síðan velja áfangasniðmát og gera nauðsynlegar uppfærslur. Veldu síðan **Loka** til að fara aftur í greiðsluáætlunina og kláraðu að búa til greiðsluáætlunina.

4. Til að búa til reikninga fyrir greiðsluáætlunina þarf að uppfæra lokadagsetningu fyrir hvert áfangatilvik. Fyrir eina greiðsluáætlun er hægt að uppfæra lokadagsetningu fyrir áfangatilvik í greiðsluáætlunarlínum. Veljið **Uppfæra ferli fyrir dagsetningu loka** til að uppfæra margar greiðsluáætlanir.
5. Þegar lokadagur hefur verið uppfærður er hægt að stofna reikninginn. Fyrir eina greiðsluáætlun skaltu velja **Mynda reikning** á síðunni **Allar greiðsluáætlanir**. Til að búa til reikninga fyrir margar greiðsluáætlanir skal velja **Búa til reikning** eða **Búa til runuvinnslu reiknings** undir **Reglubundin verk**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Breyta áfangaúthlutun á greiðsluáætlunarlínu

Til að breyta áfangaúthlutun á greiðsluáætlunarlínu skaltu fylgja þessum skrefum.

1. Á síðunni **Greiðsluáætlanir** > **Allar eða virkar greiðsluáætlanir**, í reitnum **Númer áætlunar**, skal velja áætlunarnúmer greiðsluáætlunarinnar.
2. Í hlutanum **Greiðsluáætlunarlínur** skal færa inn vöru, tilgreina **Áfanga** sem vöruna og velja **Úthlutun áfanga**.
3. Í reitnum **Sniðmát áfanga** skal velja áfangasniðmát.
4. Veljið **Ferli**. Línum fyrir áfangasniðmát er sjálfkrafa bætt við línur greiðsluáætlunarinnar.

## <a name="milestone-allocation-fields"></a>Reitir áfangaúthlutunar

Á síðunni **Úthlutun áfanga** eru eftirfarandi reitir.

| Svæði | Lýsing |
|-------|-------------|
| Yfirvara | Vörunúmer yfireiningarinnar. |
| Útvíkkað verð | <p>Reiknað verð vörunnar. Gildið samsvarar gildi **Nettóupphæð** á greiðsluáætlunarlínunni.</p></p>Fyrir yfirvöru áfanga er sjálfgefna gildið **Heildarupphæð** sem er tilgreint fyrir áfangasniðmátið. Ef heildarupphæðin er 0 (núll) er sjálfgefið gildi gildið **Nettóupphæð** fyrir greiðsluáætlunarlínuna.</p> |
| Sniðmát áfanga | Auðkenni áfangasniðmáts línuvörunnar. |
| Lýsing sniðmáts | Lýsing á áfangasniðinu. |
| Úthlutunaraðferð | Úthlutunaraðferðin sem er notuð fyrir áfangasniðmátið. |
| **Línur** | Sjálfgefin gildi fyrir allar línur er byggð á völdu áfangasniðmáti. Hægt er að breyta þeim eftir þörfum. |
| Vörunúmer | Vörunúmerið fyrir sniðmátið áfangaúthlutunar. |
| Afurðarheiti | Afurðarheitið. |
| Prósenta | <p>Úthlutunarprósenta fyrir línuna. Samtala allra hlutfalla verður að vera jöfn 100.</p><p>Ef gildi **Prósenta** er breytt fyrir línuna er gildið **Nettóupphæð** uppfært. Ef þú breytir aftur á móti gildi **Nettóupphæð** er **Prósenta** uppfært.</p> |
| Nettóupphæð | <p>Úthlutunarupphæðin fyrir línuna. Summa nettóupphæða fyrir allar línurnar verður að vera jafnt og gildið **Heildarverð** sem tilgreint er í hausnum.</p><p>Ef gildinu **Nettóupphæð** er breytt fyrir línuna er gildið **Prósenta** uppfært. Á hinn bóginn, ef **Prósenta** er breytt er gildið **Nettóupphæð** uppfært.</p> |
| **Samtala** | |
| Heildarprósenta | Summa gilda **Prósenta** fyrir allar línur. Þessi summa verður að vera 100. |
| Heildarfjöldi daga, heildarfjöldi tíma | Summa gilda **Nettóupphæð** fyrir allar línur. Þessi summa verður að vera jöfn gildinu **Heildarverð** sem er tilgreint í hausnum. |
| Upphæð eftirstöðva | Upphæð eftirstöðvanna. Gildið er reiknað sem gildið **Heildarverð** úr hausnum mínus summan af gildunum **Nettóupphæð** fyrir allar línur. Lokaupphæð verður að vera 0 (núll). |
