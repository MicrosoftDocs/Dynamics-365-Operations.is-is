---
title: Grunnstilla farsímaforrit Warehouse Management fyrir einingakvarða skýja og jaðra
description: Þessi grein útskýrir hvernig á að setja upp vöruhúsastjórnun farsímaforritin þín fyrir vöruhús sem þjónað er af skýja- eða brúnkvarðaeiningu.
author: perlynne
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysAADClientTable, SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 86edef2dfa6e9c71c04d50f185148be3a622fea1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865239"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Grunnstilla farsímaforrit Warehouse Management fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp vöruhúsastjórnun farsímaforritin þín þannig að hægt sé að nota þau í vöruhúsum sem þjónað er af skýja- eða brúnkvarðaeiningu.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar að setja upp fartækin þín til að tengjast skýja- eða brúnkvarðaeiningu skaltu staðfesta að þau geti tengst fyrirtækismiðstöðinni. Fyrir leiðbeiningar, sjá [Settu upp og tengdu Warehouse Management farsímaforritið](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Viðbótaruppsetning þegar þú keyrir vöruhússtjórnun farsímaforritið gegn mælieiningu

Sem hluti af [dreifingarferli fyrir vinnuálag á vöruhúsaeiningum](cloud-edge-landing-page.md#scale-unit-manager-portal), flest gagna sem þarf til að tengja vöruhússtjórnun farsímaforritið þitt eru sjálfkrafa samstillt frá fyrirtækismiðstöðinni við mælieininguna. Hins vegar verður þú að slá inn gögnin á **Azure Active Directory umsóknir** síða (**Kerfisstjórnun \> Uppsetning \>Azure Active Directory umsóknir**) á mælikvarða eining dreifing. Að auki gætirðu þurft að uppfæra sjálfgefið **Fyrirtæki** gildi fyrir notandakennið eða búið til nýjan notanda. Notendur sem eru tengdir fyrirtæki sem er ekki til í dreifingu mælieininga munu ekki geta skráð sig inn þegar vöruhúsastjórnun farsímaforritið er tengt við þá mælieiningu.

> [!NOTE]
> Vegna þess að gögnin um **Azure Active Directory umsóknir** síða er ekki samstillt, þú verður að viðhalda þessum gögnum handvirkt ef þú vilt færa vöruhúsaálag yfir í aðra mælikvarðaeiningu.

Mundu að, sem hluti af tengingaruppsetningu hvers vöruhúsastjórnunar farsímaforrits, er tilgreint Azure Active Directory vefslóð tilfangs verður að vera fyrir mælieininguna í stað fyrirtækjamiðstöðvarinnar.
