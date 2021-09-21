---
title: Gerðir birgðablöndunar þegar forstilling dreifingarstjórnunar er notuð
description: Til að forstilling dreifingarstjórnunar geti haft umsjón með blöndun birgða, þarf fyrst að setja upp vinnuhausaskil. Þessi síða útskýrir hvernig á að gera það.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cc660a2f9839e886240c97a7f60d2e264653074a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476644"
---
# <a name="inventory-types-are-being-mixed-when-using-a-dock-management-profile"></a>Birgðagerðir eru blandaðar þegar forstilling dreifingarstjórnunar er notuð

## <a name="symptoms"></a>Einkenni

Þú ert að nota *samstæðureglur sendingar*. Setja þarf upp *forstillingu dreifingarstjórnunar* fyrir *staðsetningarforstillingu*, en þegar vinna er stofnuð er tegundum birgða blandað saman á lokastaðsetningunni.

## <a name="resolution"></a>Lausn

Forstilling dreifingarstjórnunar krefst þess að vinnu sé skipt upp fyrirfram. Með öðrum orðum býst forstilling dreifingarstjórnunar við því að vinnuhaus verði ekki með mörgum frágangsstaðsetningum.

Til að forstilling dreifingarstjórnunar geti haft umsjón með blöndun birgða, þarf að setja upp vinnuhausaskil.

Í þessu dæmi er forstilling dreifingarstjórnunar skilgreind á þann hátt að **Birgðagerðir sem ætti ekki að blanda saman** er stillt á *Auðkenni sendingar* og við munum setja upp vinnuhausaskil fyrir hana:

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Veljið **Gerð verkbeiðni** til að breyta (t.d. *Innkaupapantanir*).
1. Velið vinnusniðmátið til að breyta.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Opnið flipann **Röðun** og bætið við línu með eftirfarandi stillingum:
    - **Tafla** - *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** - *Tímabundnar vinnufærslur*
    - **Reitur** - *Auðkenni sendingar*
1. Veljið **Í lagi**.
1. Þú ferð til baka á síðuna **Vinnusniðmát**. Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Veljið gátreitinn sem tengist **Heiti reits** *Auðkenni sendingar*.
1. Í aðgerðarúðunni skal velja **Vista**.
