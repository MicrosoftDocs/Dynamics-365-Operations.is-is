---
title: Flytja út gögn úr Attract og Onboard
description: Flytja út gögn úr Dynamics 365 Talent - Attract og Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975935"
---
# <a name="export-data-from-attract-and-onboard"></a>Flytja út gögn úr Attract og Onboard

[!include [banner](includes/banner.md)]

Eins og tilkynnt var í [Forritin Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard tekin úr notkun](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) tökum við Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard úr notkun 1. febrúar 2022. Til að hjálpa við flutning þinn í aðra afurð, bjóða bæði forritin nú útflutningsgetu gagna.

## <a name="export-data-from-attract"></a>Flytja gögn út úr Attract

Þú getur flutt gögn út án þess að takmarka aðgang að umhverfi þínu. Þú gætir viljað gera þetta í prófunarskyni eða til að skilja gagnaskipan okkar. Þegar þú ert tilbúin/n að flytja skaltu takmarka aðgang að aðlaðandi umhverfi þínu með því að nota leiðbeiningarnar eftir þetta ferli. Passaðu þig að flytja gögnin út aftur. 

1. Opnið [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Undir **Gagnaútflutningur** velurðu **Biðja um gagnaflutning**.

   ![[Biðja um gagnaflutning úr Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Þegar skilaboðareiturinn **Verið er að vinna úr beiðninni** birtist velurðu **Í lagi**. Gagnaútflutningurinn getur tekið allt að 20 mínútur, fer eftir stærð útflutningsins.

4. Þegar útflutningi þínum er lokið skaltu velja hnappinn **Sækja** við hliðina. 

   >[!NOTE]
   >Allur útflutningur gagna er í boði í sjö daga, en þá rennur tengillinn **Sækja** út.</br>
   
Niðurhalið inniheldur .zip-skrá með Attract gögnum þínum, þar á meðal eftirfarandi möppum:

| Nafn möppu | Lýsing |
| --- | --- |
| Stillingar stjórnanda | Stillingar stjórnendamiðstöðvar Attract. |
| Umsækjendur | Allir umsækjendur sem bættust við störf eða hæfileikasöfn. |
| Sniðmát fyrir tölvupóst | Öll tölvupóstsniðmát sem voru stillt fyrir umhverfið. |
| Sniðmát starfstilboðspakka | Öll pakkasniðmát fyrir atvinnutilboð sem var búið til, ásamt tilheyrandi stillingum þeirra. |
| Reglusett starfstilboða |  Öllum reglusettaskrár sem hlaðið var upp til að stjórna tilboðum. |
| Sniðmát starfstilboða | Öll skjalasniðmát fyrir atvinnutilboð búin til fyrir umhverfið. |
| Laus störf | Öll stofnuð störf. Eydd störf eru ekki flutt út. Undirmöppurnar innihalda umsækjendur, með undirmöppum fyrir viðbætur við umsækjendur og bjóða upp á pakka, þar sem við á. |
| Sniðmát fyrir laus störf | Sarfsferlissniðmát sem voru stillt í umhverfinu. |
| Hæfileikasöfn | Öll stofnuð hæfileikasöfn, framlagslistar þeirra og listarnir yfir umsækjendur fyrir hæfileikasafnið. |
| Starfskraftar | Listi yfir alla starfsmenn sem eru í umhverfinu auk hlutverka þeirra. |
| (rótarmappa) | JSON skemaskrá sem lýsir reitum gagnaskipulags. |

### <a name="restrict-access-to-attract"></a>Takmarka aðgang að Attract

Þegar þú ert tilbúin/n að flytja skaltu takmarka þá sem ekki hafa umsjón með aðgangi að Attract-umhverfi þínu og flytja gögnin út.

>[!IMPORTANT]
>Takmörkun á aðgangi að Attract-umhverfi þínu er varanleg og ekki er hægt að afturkalla hana. Ef þú vilt að aðrir notendur en stjórnendur muni halda áfram að fá aðgang að umhverfinu skaltu sleppa þessu skrefi.

1. Opnið [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Til að takmarka aðgang fyrir aðra en stjórnendur að Attract-umhverfi þínu skaltu undir **Takmarka aðgang að þessu forriti** velja **Takmarka aðgang núna**. Takmörkun aðgangs fjarlægir einnig öll virk störf sem hafa verið send.

   ![[Takmarka aðgang annarra en stjórnenda að Attract](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Þegar þú sérð viðvörunina **Þetta er varanleg breyting** skaltu velja **Takmarka aðgang** til að takmarka varanlega aðra notendur en stjórnendur frá þessu umhverfi. Ef þú ert ekki tilbúin/n að ljúka þessu skrefi skaltu velja **Hætta við**.

   ![[Varað er við því takmörkun aðgangs er varanleg breyting](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Stjórnendur geta haldið áfram að fá aðgang að gagnaútflutningi og skýrslusíðum einstaklinga eftir að þú hefur takmarkað aðgang að Attract-umhverfi.

## <a name="export-data-from-onboard"></a>Flytja gögn út úr Onboard

Þegar þú ert tilbúin/n geturðu sótt sniðmát, leiðbeiningar og gögn um umsækjendur úr Onboard.

1. Opnið [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Undir **Gagnaútflutningur** velurðu **Biðja um gagnaflutning**. 

   ![[Biðja um gagnaflutning úr Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Þegar skilaboðareiturinn **Verið er að vinna úr beiðninni** birtist velurðu **Í lagi**. Gagnaútflutningurinn getur tekið allt að 20 mínútur, fer eftir stærð útflutningsins.

4. Þegar útflutningi þínum er lokið skaltu velja hnappinn **Sækja** við hliðina. 

   ![[Sækja gagnaútflutning úr Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Gagnaútflutningur þinn er í boði í sjö daga. Eftir sjö daga rennur tengillinn **Sækja** út og þú verður að biðja um nýjan útflutning ef þú þarft að sækja gögnin aftur. Þegar þú hefur nýjan gagnaflutning renna öll fyrirliggjandi niðurhöl út þegar nýi útflutningurinn tekst.

Niðurhalið er .zip-skrá sem inniheldur:

- Mappn **Sniðmát** sem inniheldur Onboard-sniðmát á Word-sniði.

- Mappn **Guides** sem inniheldur Onboard-leiðbeiningar á Word-sniði.

## <a name="see-also"></a>Sjá einnig

[Forritin Dynamics 365 Talent: Attract og Dynamics 365 Talent: Onboard tekin úr notkun](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)