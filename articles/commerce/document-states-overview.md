---
title: Staða og líftími skjala
description: Þessi grein fjallar um hinar ýmsu skjalastöður síðuþátta í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269917"
---
# <a name="document-states-and-lifecycle"></a>Staða og líftími skjala

[!include [banner](includes/banner.md)]

Þessi grein fjallar um hinar ýmsu skjalastöður síðuþátta í Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Lýsing skjalastöðu

The [Síðuþættir](page-elements-overview.md) grein listar upp ýmsar skjalagerðir í vefumsjónarkerfinu (CMS). Þessar skjalategundir geta haft nokkrar stöður í höfundatólinu. Skjalastöðurnar hjálpa til við að koma í veg fyrir árekstur gagna og framfylgja útgáfustjórnun. Þær ákvarða hverjir geta breytt skjölunum, hvenær hægt er að breyta skjölunum og hvenær aðrir geta skoðað breytingar.

Eftirfarandi tafla sýnir mögulegar skjalastöður síðueininga í Commerce.

| Staða skjals      | Aðgerð vefsvæðishönnuðar        | lýsing                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Skráð út         | Veljið **Breyta**.           | Viðeigandi skjal er skráð út til þín. Meðan skjal er í þessari stöðu geta aðrir sannvottaðir kerfisnotendur ekki breytt því og allar breytingar sem þú gerir á skjalinu eru aðeins sýnilegar þér. |
| Vistuð               | Veljið **Vista**.           | Breytingar sem gerðar hafa verið á útskráðu skjali eru vistaðar í gagnagrunninn en skjalið hefur ekki enn verið skráð inn eða birt. Vistuðu breytingarnar eru ekki sýnilegar öðrum staðfestum kerfisnotendum fyrr en höfundurinn velur **Ljúka við breytingar**. Þær eru ekki sýnilegir fyrir utanaðkomandi notendur fyrr en hluturinn er birtur. |
| Fargað við útskráningu | Veldu **Fleygja breytingum**.  | Öllum breytingum á útskráðu skjali er fargað og varan snýr aftur í síðustu útgáfu sem var innskráð. |
| Skráð inn          | Veldu **Ljúka við breytingar**. | Breytta skjalið er skráð inn. Allar breytingar eru sýnilegar öðrum staðfestum kerfisnotendum og þeir notendur geta síðan breytt skjalinu. Hver innskráning býr til útgáfu skjals í sögu hlutarins. |
| Útgefið           | Velja **Birta**.        | Skjalið er birt og breytingunum er ýtt á lifandi vefsvæðið og verða uppgötvaðar af utanaðkomandi notendum. Aðeins er hægt að birta vörur ef þær hafa fyrst verið innritaðar með því að velja **Ljúka við breytingar**. |

## <a name="additional-resources"></a>Frekari upplýsingar

[Leiðir til að bæta við efni](add-manage-content.md)

[Orðalisti síðulíkans](page-elements-overview.md)

[Vinna með birtingarhópa](publish-groups.md)

[Virkja og nota deilingu milli rása](cross-channel-sharing.md)

[Vinna með einingar](work-with-modules.md)

[Vinna með brot](work-with-fragments.md)

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Sérstilla yfirlit svæðis](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
