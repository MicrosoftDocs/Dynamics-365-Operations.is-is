---
title: Sniðmát áfanga
description: Þetta efnisatriði útskýrir hvernig á að setja upp áfangainnheimtuvirkni í áskriftarinnheimtu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 863ec55c8ba2fcc9d0e624fcca06f4491ce839ac
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462916"
---
# <a name="milestone-billing"></a>Áfangareikningur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að skilgreina sniðmát fyrir virkni áfangareikninga í áskriftarinnheimtu. Fyrir hverja línu í áfangasniðmátinu er hægt að skilgreina úthlutunarprósentu eða upphæð. Þú getur síðan úthlutað áfangasniðmátinu til greiðsluáætlunarliða sem nota áfangareikningavirknina.

## <a name="add-a-template"></a>Bæta við sniðmáti

Til að bæta við áfangasniðmáti skaltu fylgja þessum skrefum.

1. Fara til **Innheimta áskriftar \> Endurtekinn samningsreikningur \> Uppsetning \> Áfangasniðmát**.
2. Veljið **Nýtt**.
3. Í **Áfangasniðmát** reit, sláðu inn einstakt auðkenni fyrir nýja sniðmátið.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Í **Úthlutunaraðferð** reit, veldu úthlutunaraðferð.
6. Valfrjálst: Í **Heildarupphæð** reit, tilgreinið heildarupphæð fyrir sniðmátið.
7. Til að bæta við línu skaltu velja **Bæta við**. Þá, í **Vörunúmer** reit, veldu vörunúmerið fyrir nýju línuna.
8. Fylgdu einu af þessum skrefum, allt eftir gildinu sem þú valdir í **Úthlutunaraðferð** reit:

    - Ef þú valdir **Hlutfall** sem úthlutunaraðferð, í **Hlutfall** reit, tilgreinið úthlutunarprósentu fyrir hverja línu. Ef þú tilgreinir prósentur er summan af prósentum sem eru sýnd í **Heildarhlutfall** sviði verður að vera jafn **100**.
    - Ef þú valdir **Breytileg upphæð** sem úthlutunaraðferð, í **Magn** reit, tilgreinið upphæðina fyrir hverja línu.
    - Ef þú valdir **Jöfn upphæð** sem úthlutunaraðferð þarftu ekki að tilgreina upphæð. Hver lína verður uppfærð með réttri prósentu og upphæð, byggt á fjölda hluta sem bætt er við sniðmátið.

9. Veldu **Vista**.

## <a name="delete-a-template"></a>Eyða sniðmáti

Til að eyða áfangasniðmáti skaltu fylgja þessum skrefum.

1. Veldu eina eða fleiri línur til að eyða og veldu síðan **Eyða**.
2. Þegar þú ert beðinn um að staðfesta aðgerðina skaltu velja **Já**.

## <a name="milestone-template-fields"></a>Áfangasniðmátareiti

The **Áfangasniðmát** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------| 
| Sniðmát áfanga | Einstakt auðkenni áfangasniðmátsins. |
| Lýsing | Lýsing á áfangasniðmáti. |
| Úthlutunaraðferð | <p>Veldu úthlutunaraðferð:</p><ul><li>**Prósenta af verklokum** – Uppsafnað fullnaðargildi er notað fyrir hverja línu.</li><li>**Hlutfall** – Hægt er að tilgreina prósentuupphæð fyrir úthlutunina. Summa allra prósenta verður að vera 100.</li><li>**Breytileg upphæð** – Hægt er að tilgreina upphæð fyrir úthlutunina. Úthlutunarupphæð er tilgreind á viðskiptastigi.</li><li>**Jöfn upphæð** – Úthlutunarprósenturnar eru sjálfkrafa reiknaðar og skipt jafnt á milli liða í sniðmátinu.</li></ul> |
| Heildarfjöldi daga, heildarfjöldi tíma | Tilgreindu áfangaupphæð fyrir sniðmátið. |
| **Línur** | |
| Vörunúmer | Veldu vörunúmer fyrir áfangasniðmátið. |
| Afurðarheiti | Heiti vörunnar. |
| Prósenta | <p>Sláðu inn úthlutunarprósentu fyrir línuna:</p><ul><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Hlutfall**, tilgreindu prósentuna fyrir línuna.</li><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Jöfn upphæð**, hlutfallinu er sjálfkrafa skipt í jafna prósentu, byggt á fjölda atriða í sniðmátinu.</li></ul><p>Summa allra prósentanna verður að vera 100.</p><p>Ef að **Heildarupphæð** gildi er tilgreint í hausnum og þú breytir **Hlutfall** gildi fyrir línuna, the **Magn** gildi er uppfært. Aftur á móti, ef þú breytir **Magn** gildi, the **Hlutfall** gildi er uppfært.</p> |
| Upphæð | <p>Úthlutunarupphæð fyrir línuna:</p><ul><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Breytileg upphæð**, tilgreindu upphæðina fyrir línuna.</li><li>Ef **Úthlutunaraðferð** reiturinn er stilltur á **Jöfn upphæð**, upphæðinni er sjálfkrafa skipt í jafnar upphæðir, byggt á fjölda hluta í sniðmátinu og **Heildarupphæð** gildi sem er tilgreint í hausnum.</li></ul><p>Summa allra upphæðanna verður að vera jafngild **Heildarupphæð** gildi sem er tilgreint í hausnum.</p><p>Ef að **Heildarupphæð** gildi er tilgreint í hausnum og þú breytir **Magn** gildi fyrir línuna, the **Hlutfall** gildi er uppfært. Aftur á móti, ef þú breytir **Hlutfall** gildi, the **Magn** gildi er uppfært.</p> |
| **Samtala** | |
| Prósentusamtala | Summa prósenta. Summa allra prósenta verður að vera 100. |
| Heildarfjöldi daga, heildarfjöldi tíma | Summan af **Magn** gildi fyrir allar línur. Þessi summa verður að vera jafngild **Heildarupphæð** gildi sem er tilgreint í hausnum. |
| Upphæð eftirstöðva | Eftirstandandi upphæð. Gildið er reiknað sem **Heildarupphæð** gildi frá haus að frádregnum summan af **Magn** gildi fyrir allar línur.|

## <a name="milestone-allocation"></a>Úthlutun áfanga

Áður en þú byrjar að nota áfangavirkni, ættir þú að klára þessi verkefni.

1. Bættu við einu eða fleiri áfangasniðmátum.
2. Búðu til greiðsluáætlunarhóp. Tilgreindu **Áfangi** sem vörutegund og veldu sniðmát.
3. Á **Uppsetning hlutar** síða (**Innheimta áskriftar \> Endurtekinn samningsreikningur \> Uppsetning \> Hlutir**), veldu vörutengsl og áfangasniðmát fyrir vöruuppsetninguna.

Eftir að þú hefur búið til áfangasniðmát, innheimtuáætlunarhópa og hluti geturðu búið til innheimtuáætlun sem notar áfangaaðgerðina.

Til að setja upp innheimtuáætlun sem notar áfangastaði skaltu fylgja þessum skrefum.

1. Frá **Allar/virkar innheimtuáætlanir** lista á **Innheimtuáætlanir** síðu, veldu **Nýtt**.
2. Á **Allar innheimtuáætlanir** síðu, búðu til nýja innheimtuáætlun og tilgreindu viðskiptavinareikning og upphafsdag.
3. Í **Innheimtuáætlunarlínur** kafla, veldu **Bæta við línu**. Bættu síðan við vörunúmeri og stilltu **Tegund vöru** sviði til **Áfangi**.

    Ef sjálfgefið áfangasniðmát er sett upp fyrir vöruna er áfangaviðburðum sjálfkrafa bætt við innheimtuáætlunarlínurnar. Lokadagsetningar eru auðar fyrir áfangalínur.

    Ef ekkert áfangasniðmát er sett upp fyrir hlutinn skaltu velja **Áfangaúthlutun**. Síðan, á **Áfangaúthlutun** síðu, veldu áfangasniðmát og gerðu allar nauðsynlegar uppfærslur. Veldu síðan **Loka** til að fara aftur í innheimtuáætlunina og klára að búa til innheimtuáætlunina.

4. Til að búa til reikninga fyrir innheimtuáætlunina verður þú að uppfæra lokadagsetningu fyrir hvern áfangaviðburð. Fyrir eina innheimtuáætlun geturðu uppfært lokadagsetningu tímamótaviðburðarins á innheimtuáætlunarlínunum. Til að uppfæra margar innheimtuáætlanir skaltu velja **Uppfærsla lokadagsetningarferlis**.
5. Eftir að lokadagsetningin er uppfærð geturðu búið til reikninginn. Fyrir eina innheimtuáætlun, veldu **Búðu til reikning** á **Allar innheimtuáætlanir** síðu. Til að búa til reikninga fyrir margar innheimtuáætlanir skaltu velja **Búðu til reikning** eða **Búðu til lotuvinnslu reikninga** undir **Reglubundin verkefni**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Breyta áfangaúthlutun á innheimtuáætlunarlínu

Fylgdu þessum skrefum til að breyta áfangaúthlutun á greiðsluáætlunarlínu.

1. Á **Innheimtuáætlanir** síðu >**Allar eða virkar innheimtuáætlanir**, í **Dagskrá númer** reit, veldu áætlunarnúmer innheimtuáætlunarinnar.
2. Í **Innheimtuáætlunarlínur** kafla, slá inn hlut, tilgreina **Áfangi** sem hlutinn og veldu **Áfangaúthlutun**.
3. Í **Áfangasniðmát** reit, veldu áfangasniðmát.
4. Veldu **Ferli**. Áfangasniðmátslínunum er sjálfkrafa bætt við innheimtuáætlunarlínurnar.

## <a name="milestone-allocation-fields"></a>Áfangaúthlutunarreitir

The **Áfangaúthlutun** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------|
| Yfirvara | Vörunúmer foreldris. |
| Útvíkkað verð | <p>Hækkað verð á hlutnum. Gildið samsvarar **Virði** gildi innheimtuáætlunarlínunnar.</p></p>Fyrir áfanga yfirliði er sjálfgefið gildi **Heildarupphæð** gildi sem er tilgreint fyrir áfangasniðmátið. Ef heildarupphæðin er 0 (núll), er sjálfgefið gildi **Virði** gildi innheimtuáætlunarlínunnar.</p> |
| Sniðmát áfanga | Auðkenni áfangasniðmáts línunnar. |
| Lýsing sniðmáts | Lýsing á áfangasniðmáti. |
| Úthlutunaraðferð | Úthlutunaraðferðin sem er notuð fyrir áfangasniðmátið. |
| **Línur** | Sjálfgefin gildi fyrir allar línur eru byggðar á völdum áfangasniðmáti. Þú getur breytt þeim eftir þörfum. |
| Vörunúmer | Vörunúmer fyrir áfangaúthlutunarsniðmát. |
| Afurðarheiti | Vöruheitið. |
| Prósenta | <p>Úthlutunarprósenta fyrir línuna. Summa allra prósentanna verður að vera 100.</p><p>Ef þú breytir **Hlutfall** gildi fyrir línuna, the **Virði** gildi er uppfært. Aftur á móti, ef þú breytir **Virði** gildi, the **Hlutfall** er uppfært.</p> |
| Nettóupphæð | <p>Úthlutunarupphæð fyrir línuna. Summa nettóupphæða fyrir allar línur verður að vera jöfn **Framlengt verð** gildi sem er tilgreint í hausnum.</p><p>Ef þú breytir **Virði** gildi fyrir línuna, the **Hlutfall** gildi er uppfært. Aftur á móti, ef þú breytir **Hlutfall** gildi, the **Virði** gildi er uppfært.</p> |
| **Samtala** | |
| Heildarprósenta | Summan af **Hlutfall** gildi fyrir allar línur. Þessi summa verður að vera 100. |
| Heildarfjöldi daga, heildarfjöldi tíma | Summan af **Virði** gildi fyrir allar línur. Þessi summa verður að vera jafngild **Framlengt verð** gildi sem er tilgreint í hausnum. |
| Upphæð eftirstöðva | Eftirstandandi upphæð. Gildið er reiknað sem **Framlengt verð** gildi frá haus að frádregnum summan af **Virði** gildi fyrir allar línur. Lokaupphæðin verður að vera 0 (núll). |
