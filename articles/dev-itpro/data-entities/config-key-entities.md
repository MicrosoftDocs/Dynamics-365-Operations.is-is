---
title: Skilgreiningarlyklar og gagnaeiningar
description: Þetta umfjöllunarefni lýsir tengslunum milli skilgreiningarlykla og gagnaeininga í Microsoft Dynamics 365 for Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 8d07a0572e56e97d42c0e1b841905f828edc6f51
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "336475"
---
# <a name="configuration-keys-and-data-entities"></a>Skilgreiningarlyklar og gagnaeiningar

[!include [banner](../includes/banner.md)]

Áður en þú notar gagnaeiningar til að flytja inn eða flytja út gögn, mælum við með því að þú fyrst ákvarðir áhrif skilgreiningarlykla á gagnaeiningarnar sem þú ætlar að nota.

Til að fá frekari upplýsingar um skilgreiningarlykla í Finance and Operations, sjá [Skýrslu um leyfiskóða og skilgreiningarlykla](../sysadmin/license-codes-configuration-keys-report.md).

### <a name="configuration-key-assignments"></a>Úthlutun skilgreiningarlykla
Skilgreiningarlyklar geta verið úthlutaðir til eins eða allra eftirtaldra þátta.

- Gagnaeiningar
- Töflur sem eru notaðar sem gagnagjafar
- Töflureitir
- Gagnaeiningarreitir

Eftirfarandi tafla útlistar hvernig gildi skilgreiningarlykils á mismunandi þáttum sem liggja að baki hlut breytast væntanlegri hegðun hlutarins.

| Stillingar skilgreiningarlykils á gagnaeiningum | Stillingar skilgreiningarlykils á töflu | Stillingar skilgreiningarlykils á töflureit | Skilgreiningarlykill á gagnaeiningarsvæði | Væntanleg hegðun |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| Óvirkt                                | Ekki metið                      | Ekki metið                            | Ekki metið                          | Ef skilgreiningarlykillinn fyrir gagnaeininguna er óvirkur, mun gagnaeiningin ekki virka. Það skiptir ekki máli hvort skilgreiningarlyklarnir í undirliggjandi töflum og reitum séu virkir eða óvirkir. |
| Virkt                                 | Óvirkt                           | Ekki metið                            | Ekki metið                          | Ef skilgreiningarlykillinn fyrir gagnaeiningu er virkur, skoðar rammi gagnastjórnunar skilgreiningarlykilinn fyrir hverja undirliggjandi töflu. Ef skilgreiningarlykillinn fyrir töflu er óvirkur, mun þessi tafla ekki vera í boði í gagnaeiningunni fyrir virka notkun. Ef skilgreiningarlykill töflu er óvirkur, er tafla og stillingar skilgreiningarlykils gagnaeiningu ekki metið. Ef aðaltaflan í einingunni hefur skilgreiningarlykilinn óvirkan, þá mun kerfið virka eins og eining skilgreiningarlykils sé óvirk. |
| Virkjað                                 | Virkjað                            | Óvirkt                                 | Ekki metið                          | Ef skilgreiningarlykill fyrir gagnaeiningu er virkur og skilgreiningarlyklar undirliggjandi tafla eru virkir, mun rammi gagnastjórnunar athuga skilgreiningarlykilinn á reitunum í töflunum. Ef skilgreiningarlykillinn fyrir reit er óvirkur, þá mun þessi reitur ekki vera í boði í gagnaeiningunni fyrir virka notkun jafnvel þótt samsvarandi gagnaeiningarsvæði hafi skilgreiningarlykilinn virkan. |
| Virkt                                 | Virkt                            | Virkt                                  | Óvirkt                               | Ef skilgreiningarlykillinn er virkur á öllum öðrum stigum, en einingarreitur skilgreiningarlykils er ekki virkur, þá mun reiturinn ekki vera tiltækur til notkunar í gagnaeiningunni. |

> [!NOTE]
> Ef eining hefur aðra einingu sem gagnagjafa þá eru ofangreindum merkingum beitt á endurkvæman hátt.

### <a name="entity-list-refresh"></a>Endurnýja einingalista
Þegar einingalistinn er endurnýjaður smíðar rammi gagnastjórnunar upp lýsigögn skilgreiningarlykils til að nota á keyrslutíma. Þessi lýsigögn eru smíðuð með rökfræðinni sem lýst er hér að ofan. Við mælum eindregið með því að þú bíðir eftir endurnýjun á einingalistanum ljúki áður en þú notar verk og einingar í gagnastjórnunarrammanum. Ef þú bíður ekki getur verið að uppfærsla á lýsigögnum skilgreiningarlykils séu ekki uppfærð og það getur leitt til óvæntra útkoma. Þegar einingalistinn er endurnýjaður birtist eftirfarandi skilaboð á listasíðu einingar.

![Endurnýja einingalista](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a>Listasíða gagnaeiningu
Listasíða gagnaeiningu í vinnurými gagnastjórnunar sýnir stillingar skilgreiningarlykla fyrir einingarnar. Byrjaðu á þessari síðu til að skilja áhrif skilgreiningarlykla á gagnaeininguna.

Þessar upplýsingar eru sýndar með því að nota lýsigögnin sem eru búin til á meðan einingar eru endurnýjaðar. Dálkur skilgreiningarlykilsins birtir heiti skilgreiningarlykilsins sem tengist gagnaeiningunni. Ef þessi dálkur er auður þýðir það að enginn skilgreiningarlykill er tengdur við gagnaeininguna. Stöðudálkur skilgreiningarlykils sýnir stöðu skilgreiningarlykilsins. Ef hann er með merkimiða þýðir það að lykillinn sé virkur. Ef hann er tómur þýðir það annaðhvort að lykillinn sé óvirkur eða enginn lykill tengdur.

![Listasíða gagnaeiningar](./media/Data_entity_list_page.png)

### <a name="target-fields"></a>Markreitir
Næsta skref er að bora í gagnaeininguna til að skoða áhrif skilgreiningarlykla á töflur og reiti. Sniðmát markreita fyrir gagnaeiningar sýnir skilgreiningarlykil og upplýsingar um stöðu lykils fyrir töflur og reiti í gagnaeiningunni sem eiga við. Ef sjálf gagnaeiningin hefur skilgreiningarlykilinn sinn óvirkan birtist viðvörunarskilaboð þar sem fram kemur að töflurnar og reitirnir í markreitunum fyrir þessa einingu munu alls ekki vera aðgengilegir, óháð stöðu skilgreiningarlykils þeirra.

![Markreitir](./media/Target_fields_1.png)

### <a name="child-entities"></a>Undireiningar 
Vissar einingar hafa aðrar einingar sem gagnagjafa eða eru samsettar gagnaeiningar: upplýsingar skilgreiningarlykla fyrir þessar einingar eru sýndar í sniðmáti Child einingar. Notaðu þetta sniðmát á svipaðan hátt og listasíðu eininganna sem lýst er hér að ofan. Sniðmát markreitsins fyrir child eininguna hegðar sér einnig eins og lýst er hér að ofan.

![Markreitir](./media/Target_fields_2.png)

### <a name="using-data-entities"></a>Notkun gagnaeininga
Eftir að hafa skilið full áhrif skilgreiningarlykla, ef einhver, á gagnaeiningarnar sem þú vilt nota, geturðu nú haldið áfram að nota gagnaeiningarnar með því að bæta þeim við gagnaverk. 

### <a name="run-time-validations-for-configuration-keys"></a>Keyrslutími villuleitar fyrir skilgreiningarlykla
Notkun á lýsigögnum skilgreiningarlykils sem eru búin til á meðan einingalisti endurnýjast, eru keyrslutímar villuleitar framkvæmdar á eftirfarandi tilvikum notkunar.

- Þegar gagnaeining er bætt við verk
- Þegar notandi smellir á „sannprófa“ á einingalistanum
- Þegar notandinn hleður upp gagnapakka inn í gagnaverk
- Þegar notandi hleður sniðmáti inn í gagnaverk
- Þegar núverandi gagnaverk er hlaðið inn
- Þegar sniðmát er hlaðið inn í gagnaverk
- Áður en verk sem er flutt inn/flutt út er keyrt (runa, ekki runa, endurtekið, Odata)
- Þegar notandinn stofnar vörpun
- Þegar notandinn varpar svæðum í vörpun notendaviðmóts
- Þegar notandinn bætir aðeins við 'svæðum sem flytja má einn'

### <a name="managing-configuration-key-changes"></a>Stjórna breytingum á skilgreiningarlykli
Hvenær sem þú uppfærir skilgreiningarlykla á einingunni, á sviði töflu eða reita, verður einingalistinn í ramma gagnastjórnunar að endurnýjast. Þetta ferli tryggir að ramminn taki upp nýjustu stillingar skilgreiningarlykils. Þar til einingalistinn er endurnýjaður birtist eftirfarandi viðvörun á listasíðu einingar. Uppfærðar breytingar á skilgreiningarlykli munu taka gildi strax eftir að einingalistinn er endurnýjaður. Við mælum með því að þú sannprófir núverandi gagnaverk og störf til að ganga úr skugga um að þau virka eins og búist er við eftir að breytingar á skilgreiningarlyklunum hafa verið gerðar.

![Markreitir](./media/Target_fields_3.png)
