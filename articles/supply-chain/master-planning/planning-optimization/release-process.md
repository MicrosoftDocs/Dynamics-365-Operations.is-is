---
title: Fínstilling áætlanagerðar, útgáfuferli og útgáfuferill
description: Þessi grein veitir upplýsingar um útgáfuferlið og útgáfuferil fyrir áætlanagerð fínstillingu.
author: t-benebo
ms.date: 10/14/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: e2437214b4a2a850f121bb86272bf7dc3d313507
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682561"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Fínstilling áætlanagerðar, útgáfuferli og útgáfuferill

[!include [banner](../../includes/banner.md)]

Microsoft uppfærir fínstillingu áætlanagerðar mánaðarlega. Hinsvegar, byggt á viðskiptaþörfum, gefum við út aukalegar uppfærslur af og til á milli áætlaðra útgáfa.

Hver útgáfa er gefin út á svæðum þar sem fínstilling áætlanagerðar er í boði. Ferlið tekur yfirleitt þrjá daga.

Meðan verið er að uppfæra fínstillingu áætlanagerar gæti aðaláætlanagerð gengið hægar fyrir sig en vanalega.

Umhverfi sem nota fínstillingu áætlanagerðar sjálfkrafa fá nýjustu útgáfuna. Aðgerða er ekki krafist af notanda: þjónustan er uppfærð sjálfkrafa. Hinsvegar eru breytingar sem geta valdið bilunum aldrei sendar sjálfkrafa til umhverfa. Sjálfgefið er slökkt á öllum breytingum sem geta valdið bilunum og þarf að kveikja sérstaklega á þeim með því að nota [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Því munu þessar breytingar ekki birtast í umhverfum fyrr en þú velur að virkja þær.

Þar sem tilkynningar eru ekki sýndar þegar fínstilling áætlanagerðar er uppfærð í umhverfinu þínu, geturðu farið yfir útgáfuupplýsingarnar í eftirfarandi töflu til að komast að því hvenær breytingar voru gefnar út og hvaða virkni fylgdi þeim. Þessi tafla sýnir breytingarnar sem voru gefnar út fyrir fínstilling áætlanagerðar, hvort þessar breytingar tengist eiginleika úr eiginleikastjórnun og dagsetningu útgáfunnar.

| Breytingar | Eiginleikastjórnunarupplýsingar | Útgáfudagar |
|---|---|---|
| <p>[Ráðstöfunarkóðar runu](../../inventory/batch-disposition-codes.md)</p><p>Hafa færibreytur birgðabirgða og birgðafærslu í aðalskipulagi</p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | Engin eiginleikastjórnun krafist | 10.-14. október 2022 |
| <p>[Auðlindaáætlun með takmarkaðri getu](finite-capacity.md)</p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | Engin eiginleikastjórnun krafist | 19.-23. september 2022 |
| Almennar umbætur á frammistöðu, gæðum og stöðugleika | Engin eiginleikastjórnun krafist | 29. ágúst - 3. september 2022 |
| <p>[Miðstýrt dagatalsviðhald](../supply-chain-calendars-master-planning.md)</p><p>[Tillögur til að hámarka núverandi framboð](../action-messages.md)</p><p>[Stuðningur við undirverktaka](../../production-control/manage-subcontract-work-production.md)</p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | Engin eiginleikastjórnun krafist | 7.-11. mars 2022 |
| Skipulagsforgangsstuðningur fyrir framleiðslupantanir | Fáanlegt með útgáfu 10.0.25 sem hluti af eiginleikanum sem nefndur er *Forgangsdrifinn MRP stuðningur fyrir hagræðingu áætlanagerðar*. | 12.-18. nóvember 2021 |
| Almennar umbætur á frammistöðu, gæðum og stöðugleika | Engin eiginleikastjórnun krafist | 12.-18. nóvember 2021 |
| <p>Stuðningur við útreikningsformúlur fyrir vinnslutíma, framleiðsluleið með skörun og framleiðsluaðgerðanúmer á kröfufærslum</p><p>Aukin villuboð fyrir framleiðsluáætlanir sem tengjast tímamörkum, afkastagetu fannst ekki og hjólaleið</p><p>Bætt samræmi við útreikning á móttökudagsetningum og útgáfudagsetningum bæði á áætlunarpöntunum og staðfestum pöntunum</p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 22.-27. október 2021 |
| <p>Stuðningur við að taka tillit til brotahlutfalls við útreikning á afgreiðslutíma</p><p>Stuðningur við aðgerðanúmer og efnisnotkun við tímaáætlun</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 5.-7. október 2021 |
| <p>Stuðningur við verkgerðir framleiðsluleiða: **Biðröð áður**, **á eftir**, og **Flutningstími**</p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 25.-30. september 2021 |
| <p>Stuðningur við aðalskipulag með **Tímasetningaraðferð** stillt á *Rekstraráætlun*</p><p>Á **Leiðarhópar** síðu, virða stillingar fyrir **Virkjun**, **·**, og **Getu** gátreitir fyrir línur með a **Leið/starfstegund** af *Uppsetning* eða *Ferli* </p><p>Almennar umbætur á frammistöðu, gæðum og stöðugleika</p> | <p>Rekstraráætlun er fáanleg í eiginleikastjórnun frá og með útgáfu 10.0.20</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p> | 9.–17. september 2021 |
| Almennar umbætur á frammistöðu, gæðum og stöðugleika | Engin eiginleikastjórnun krafist | 25.-30. ágúst 2021 |
| <p>Reitnum **Afhendingartími** var bætt við áætlaðar pantanir.</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engin eiginleikastjórnun krafist | 12.-17. ágúst 2021 |
| <p>Bætt við kröfum um gerð tilfanga fyrir óendanlega afkastagetu tímasetningu</p><p>Bætt auðlindanýting og dagatalsnýtni fyrir óendanlega getu tímasetningar</p><p>Fyrir frekari upplýsingar, sjá [Tímasetningar með óendanlega getu](infinite-capacity-planning.md)</p> | <p>Í boði í eiginleikastjórnun frá og með útgáfu 10.0.20</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p> | 6.-12. júlí 2021 |
| Almennar gæðabætingar | Engin eiginleikastjórnun krafist | 6.-12. júlí 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
