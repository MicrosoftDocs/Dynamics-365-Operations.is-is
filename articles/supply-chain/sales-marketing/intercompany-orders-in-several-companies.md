---
title: Innkaupa- og sölupantanir innan samstæðu stofnaðar í nokkrum fyrirtækjum
description: Þetta efnisatriði útskýrir hvernig á að stofna innkaupapantanir eða sölupantanir innan samstæðu í nokkrum fyrirtækjum
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5d756a82abb7e7b19080128353d863f29837fc5b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548327"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Innkaupa- og sölupantanir innan samstæðu stofnaðar í nokkrum fyrirtækjum

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management takmarkast ekki við að vinna með eitt framleiðslufyrirtæki og nokkur sölufyrirtæki. Öll fyrirtæki sem eru sett upp fyrir samstæðu geta verið bæði viðskipta- og framleiðslufyrirtæki.

Ef fleiri fyrirtæki geta afhent sömu vöruna, er frjálst að velja frá hverjum er verslað og uppfærslur eru gerðar jafnvel þótt ein sölupöntun verði að mörgum innkaupapöntunum.

Á sama hátt og ein innkaupapöntun er sjálfkrafa stofnuð innan samstæðu, er hægt að stofna upprunalega sölupöntun í fyrirtækinu og láta svo marga lánardrottna innan samstæðu uppfylla pöntunina með því að stofna fleiri en eina innkaupapöntun innan samstæðu. Microsoft Dynamics 365 Supply Chain Management stofnar sjálfkrafa sölupantanir innan samstæðu í lánardrottnafyrirtækjunum.

Til að gera þetta verða öll fyrirtækin að vera sett upp sem viðskiptasamningar. Fyrirtæki lánardrottna verða að vera sett upp í Microsoft Dynamics 365 Supply Chain Management sem samstæðulánardrottnar og þau verða að vera aðallánardrottinn fyrir viðeigandi vöru. Í sölupöntuninni, í **Hausyfirlitinu**, þarf að velja reitinn **Stofna samstæðupantanir sjálfvirkt** og reitinn **Bein afhending** í flýtiflipanum **Samstæðustillingar**. Þetta er sjálfgefin stilling.

Þú býrð til sölulínurnar á venjulegan hátt. Þegar farið er úr færslunni birtast skilaboð sem segja að verið sé að stofna samstæðuinnkaupapantanir og samstæðusölupantanir. Í skeytinu eru tenglar á nýju pantanirnar. Til að skoða stofnaðar samstæðusölupantanir í fyrirtækjum lánardrottins skal opna upprunalega sölupöntun og í flipanum **Almennt**, í flokknum **Tengdar upplýsingar**, skal velja **Tilvísanir**.

Ef innkaupapantanirnar innan samstæðu fyrir lánardrottnana eru opnaðar, kemur í ljós að Microsoft Dynamics 365 Supply Chain Management fyllir sjálfkrafa inn upprunalegt númer sölupöntunarinnar og númer sölupöntunarinnar innan samstæðu fyrir hvern lánardrottinn.

Það sama er ef sölupantanirnar innan samstæðu fyrir lánardrottnana eru opnaðar, þá kemur í ljós að Microsoft Dynamics 365 Supply Chain Management fyllir sjálfkrafa inn upprunalegt númer sölupöntunarinnar og númer sölupöntunarinnar innan samstæðu fyrir hvern lánardrottinn.

> [!NOTE]
> Ef vara í pöntun er til í einu af lánardrottnafyrirtækjunum innan samstæðunnar en ekki í öðru, þá stofnar Microsoft Dynamics 365 Supply Chain Management pöntun innan samstæðu fyrir lánardrottnafyrirtækið þar sem varan er til en stöðvar stofnun pöntunar fyrir hitt fyrirtækið. Tilkynning er sýnd þegar þetta gerist.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
