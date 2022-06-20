---
title: Fínstilling áætlanagerðar, útgáfuferli og útgáfuferill
description: Þessi grein veitir upplýsingar um útgáfuferlið og útgáfuferil fyrir fínstillingu áætlanagerðar.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 45a35eb32cb9e51d9f63f6687808fb511f894887
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873725"
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
| <p>Almenn afköst, gæði og betri stöðugleiki.<p>[Áætlanagerð hagræðing miðlægt dagatal viðhald](../supply-chain-calendars-master-planning.md)<p>[Áætlanagerð Hagræðingartillögur til að hámarka núverandi framboð](../action-messages.md)<p>[Stuðningur við skipulagningu hagræðingar fyrir undirverktaka](../../production-control/manage-subcontract-work-production.md) | Engin eiginleikastjórnun er nauðsynleg. | 7.-11. mars 2022 |
| <p>Bætti við skipulagsforgangsstuðningi fyrir framleiðslupantanir. | Fáanlegt með útgáfu 10.0.25 sem hluti af eiginleikanum sem nefndur er *Forgangsdrifinn MRP stuðningur fyrir hagræðingu áætlanagerðar*. | 12.-18. nóvember 2021 |
| <p>Almenn afköst, gæði og betri stöðugleiki. | Engin eiginleikastjórnun er nauðsynleg. | 12.-18. nóvember 2021 |
| <p>Bætt við stuðningi við útreikningsformúlur fyrir vinnslutíma, framleiðsluleið með skörun og framleiðsluaðgerðanúmer á kröfufærslum.</p><p>Aukin villuboð fyrir framleiðsluáætlanir sem tengjast tímamörkum, afkastagetu fannst ekki og hjólaleið.</p><p>Bætt samræmi við útreikning á móttökudagsetningum og útgáfudagsetningum bæði á áætlunarpöntunum og staðfestum pöntunum.</p><p>Almenn afköst, gæði og betri stöðugleiki. | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 22.-27. október 2021 |
| <p>Bætt við stuðningi við að taka tillit til ruslprósentu við útreikning á vinnslutíma.</p><p>Bætti við stuðningi við aðgerðanúmer og efnisnotkun við tímaáætlun. | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 5.-7. október 2021 |
| <p>Bætt við stuðningi við gerðir framleiðsluleiða: **Biðröð áður**, **á eftir**, og **Flutningstími**.</p><p>Almenn afköst, gæði og betri stöðugleiki. | Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar* | 25.-30. september 2021 |
| <p>Viðbættur stuðningur fyrir aðaláætlanir með **Röðunaraðferð** stillta á *Aðgerðaröðun*.</p><p>Á síðunni **Leiðaflokkar** skal fara eftir stillingunum fyrir gátreitina **Virkjun**, **Vinnutími** og **Afkastageta** fyrir línur með **Gerð leiðar/vinnslu** sem *Uppsetning* eða *Ferli*. </p><p>Almenn afköst, gæði og betri stöðugleiki. | <p>Aðgerðaröðun er í boði í eiginleikastjórnun frá og með útgáfu 10.0.20.</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p>  | 9.–17. september 2021 |
| Almenn afköst, gæði og betri stöðugleiki. | Engin eiginleikastjórnun er nauðsynleg. | 25.-30. ágúst 2021 |
| <p>Reitnum **Afhendingartími** var bætt við áætlaðar pantanir.</p><p>Almenn afköst, gæði og betri stöðugleiki.</p> | Engin eiginleikastjórnun er nauðsynleg. | 12.-17. ágúst 2021 |
| <p>Bættar kröfur um tilfangagerð fyrir áætlanagerð ótakmarkaðrar afkastagetu.</p><p>Bætt skilvirkni tilfanga og skilvirkni dagatals fyrir áætlanagerð ótakmarkaðrar afkastagetu.</p><p>Frekari upplýsingar er að finna í [Röðun með ótakmarkaða getu](infinite-capacity-planning.md). | <p>Í boði í eiginleikastjórnun frá og með útgáfu 10.0.20.</p><p>Heiti eiginleika: *Ótakmörkuð afkastaáætlun fyrir fínstillingu áætlanagerðar*</p> | 6.-12. júlí 2021 |
| Almennar gæðabætingar. | Engin eiginleikastjórnun er nauðsynleg. | 6.-12. júlí 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
