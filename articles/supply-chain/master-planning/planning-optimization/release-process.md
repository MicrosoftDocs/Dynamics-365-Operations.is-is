---
title: Fínstilling áætlanagerðar, útgáfuferli og útgáfuferill
description: Í þessari grein eru gefnar upplýsingar um útgáfuferlið og útgáfusöguna fyrir fínstilling áætlanagerðar.
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
ms.translationtype: HT
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
| <p>[Ráðstöfunarkóðar runu](../../inventory/batch-disposition-codes.md)</p><p>Taka með lagerbirgðir og færibreytur fyrir birgðafærslur á aðaláætlunum</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engrar eiginleikastjórnunar er krafist | 10.-14. október 2022 |
| <p>[Tímasett tilföng með takmarkaða getu](finite-capacity.md)</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engrar eiginleikastjórnunar er krafist | 19.–23. september 2022 |
| Almenn afköst, gæði og betri stöðugleiki. | Engrar eiginleikastjórnunar er krafist | 29. ágúst - 3. september 2022 |
| <p>[Miðlægt dagbókarviðhald](../supply-chain-calendars-master-planning.md)</p><p>[Tillögur til að fínstilla núverandi framboð](../action-messages.md)</p><p>[Stuðningur fyrir úthýsingu](../../production-control/manage-subcontract-work-production.md)</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engrar eiginleikastjórnunar er krafist | 7.-11. mars 2022 |
| Forgangur í áætlanagerð stuðningur fyrir framleiðslupantanir | Í boði með útgáfu 10.0.25 sem hluti af eiginleika sem kallast *Forgangsraðaður stuðningur við MRP fyrir fínstillingu áætlanagerðar*. | Nóvember 12-18, 2021 |
| Almenn afköst, gæði og betri stöðugleiki. | Engrar eiginleikastjórnunar er krafist | Nóvember 12-18, 2021 |
| <p>Stuðningur við formúluútreikninga vinnslutíma, framleiðsluleið með skörun og aðgerðarnúmer framleiðslu á þarfafærslum</p><p>Endurbætt villuskilaboð fyrir framleiðsluáætlun í tengslum við tímamörk, getu fundust ekki og hringvísun</p><p>Bætt samræmi við útreikninga á móttökudagsetningum og dagsetningum innhreyfingar í bæði áætluðum pöntunum og staðfestum pöntunum</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 22.-27. október 2021 |
| <p>Stuðningur við að taka til greina rýrnunarprósentu í útreikningi vinnslutíma</p><p>Stuðningur við aðgerðarnúmer og efnisnotkun við áætlanagerð</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 5.-7. október 2021 |
| <p>Stuðningur við vinnslugerðir framleiðsluleiðar: **Biðröð fyrir**, **Biðröð eftir** og **Flutningstími**</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 25.–30. september 2021 |
| <p>Stuðningur fyrir aðaláætlanir með **Röðunaraðferð** stillta á *Aðgerðaröðun*.</p><p>Á síðunni **Leiðaflokkar** skal fara eftir stillingunum fyrir gátreitina **Virkjun**, **Vinnutími** og **Afkastageta** fyrir línur með **Gerð leiðar/vinnslu** sem *Uppsetning* eða *Ferli*. </p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | <p>Aðgerðaröðun er í boði í eiginleikastjórnun frá og með útgáfu 10.0.20.</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p> | 9.–17. september 2021 |
| Almenn afköst, gæði og betri stöðugleiki. | Engrar eiginleikastjórnunar er krafist | 25.-30. ágúst 2021 |
| <p>Reitnum **Afhendingartími** var bætt við áætlaðar pantanir.</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engrar eiginleikastjórnunar er krafist | 12.-17. ágúst 2021 |
| <p>Bættar kröfur um tilfangagerð fyrir áætlanagerð ótakmarkaðrar afkastagetu</p><p>Bætt skilvirkni tilfanga og skilvirkni dagatals fyrir áætlanagerð ótakmarkaðrar afkastagetu</p><p>Frekari upplýsingar er að finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md).</p> | <p>Í boði í eiginleikastjórnun frá og með útgáfu 10.0.20</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p> | 6.-12. júlí 2021 |
| Almennar gæðabætingar | Engrar eiginleikastjórnunar er krafist | 6.-12. júlí 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
