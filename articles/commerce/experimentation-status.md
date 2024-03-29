---
title: Fara yfir stöðu tilraunar
description: Þessi grein útskýrir hvaða stöðu tilraun hefur í líftíma tilrauna í Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 818435a7c901d2a6b876b9c9db27faffc8b322fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877250"
---
# <a name="review-the-status-of-an-experiment"></a>Fara yfir stöðu tilraunar
Mörg skref fylgja því að setja upp og keyra tilraun í Dynamics 365 Commerce. Upplýsingar um tilraunaferlið er að finna í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).

Til að sjá hvar tilraun er í ferlinu skal velja **Tilraunir** í vinstra yfirlitssvæði í Comerce vefsmið. Listi yfir tilraunir er sýndur með stöðu hverrar tilraunar í bæði Commerce og þjónustu þriðja aðila sem er notaður til að gera kleift að stofna tilraunir, úthluta afbrigðum og greina gögn.

Í dálknum **Staða Commerce** er hugsanlegt að eftirfarandi gildi séu sýnd. 
- **Drög** - Tilraunin er tengd við síðu eða brot í Commerce og verið er að breyta henni.
- **Birt** - Afbrigði tilrauna eru tilbúin til birtingar á vefsvæðinu. Ef tilraunin er í gangi í þjónustu þriðja aðila, sjá notendur vefsvæðisins afbrigði síðunnar eða brotsins eins og þjónusta þriðja aðila hefur valið.
- **Óbirt** - Tilraunin er ekki lengur í boði á vefsvæðinu. Notendur vefsvæðis sjá aðeins sjálfgefna útgáfu síðunnar eða brotsins, jafnvel þótt tilraunin sé í gangi í þjónustu þriðja aðila.
- **Lokið** - Tilraunin hefur haft sinn gang og afbrigði var sett á netið fyrir alla notendur vefsvæðisins.

Á sama hátt, í dálknum **staða þriðja aðila**, verða eftirfarandi gildi sýnd til að gefa til kynna stöðu tilraunanna í þjónustu þriðja aðila.
- **Drög** - Tilraunin er sett upp í þjónustu þriðja aðila en hefur ekki verið sett í gang.
- **Í gangi** - Tilraunin var sett í gang í þjónustu þriðja aðila og er að safna gögnum.
- **Gert hlé** - Tilraunin hefur verið stöðvuð og er ekki að safna gögnum. Nauðsynlegt er að halda áfram með tilraunina til að hún geti safnað gögnum á nýjan leik.
- **Safnvistað** - Tilraunin hefur haft sinn gang og hefur verið skrásett í þjónustu þriðja aðila til síðari nota.

Skýringarmyndin hér að neðan sýnir bæði settin af stöðum og hvernig þau tengjast hvort öðru.

[ ![Stöður tilraunavinnu.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]