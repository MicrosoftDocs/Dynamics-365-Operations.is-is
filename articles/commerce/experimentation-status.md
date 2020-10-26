---
title: Fara yfir stöðu tilraunar
description: Í þessu efnisatriði er útskýrt hvaða staða tilraun er með í tilraunaferlinu í Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930217"
---
# <a name="review-the-status-of-an-experiment"></a>Fara yfir stöðu tilraunar
Mörg skref fylgja því að setja upp og keyra tilraun í Dynamics 365 Commerce. Upplýsingar um tilraunaferlið er að finna í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).

Til að komast að því hvar tilraun er stödd í ferlinu skal fara í flipann **Tilraunir** í vefsmiðnum. Listi yfir tilraunir er sýndur með stöðu hverrar tilraunar í bæði Commerce og þjónustu þriðja aðila sem er notaður til að gera kleift að stofna tilraunir, úthluta afbrigðum og greina gögn.

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

[ ![Stöður tilraunavinnu](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)
