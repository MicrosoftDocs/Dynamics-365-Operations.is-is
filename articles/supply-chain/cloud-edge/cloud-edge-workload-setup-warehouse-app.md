---
title: Stilltu Warehouse Management farsímaforritið fyrir skýja- og brúnkvarðaeiningar
description: Þetta efni útskýrir hvernig á að setja upp vöruhúsastjórnun farsímaforritin þín fyrir vöruhús sem þjónað er af skýja- eða brúnkvarðaeiningu.
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
ms.openlocfilehash: 1fa00b40db2f6246029876964dca9d3229567848
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071781"
---
# <a name="configure-the-warehouse-management-mobile-app-for-cloud-and-edge-scale-units"></a>Stilltu Warehouse Management farsímaforritið fyrir skýja- og brúnkvarðaeiningar

[!include [banner](../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp vöruhúsastjórnun farsímaforritin þín þannig að hægt sé að nota þau í vöruhúsum sem þjónað er af skýja- eða brúnkvarðaeiningu.

## <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar að setja upp fartækin þín til að tengjast skýja- eða brúnkvarðaeiningu skaltu staðfesta að þau geti tengst fyrirtækismiðstöðinni. Fyrir leiðbeiningar, sjá [Settu upp og tengdu Warehouse Management farsímaforritið](../warehousing/install-configure-warehouse-management-app.md).

## <a name="additional-setup-when-you-run-the-warehouse-management-mobile-app-against-a-scale-unit"></a>Viðbótaruppsetning þegar þú keyrir vöruhússtjórnun farsímaforritið gegn mælieiningu

Sem hluti af [dreifingarferli fyrir vinnuálag á vöruhúsaeiningum](cloud-edge-landing-page.md#scale-unit-manager-portal), flest gagna sem þarf til að tengja vöruhússtjórnun farsímaforritið þitt eru sjálfkrafa samstillt frá fyrirtækismiðstöðinni við mælieininguna. Hins vegar verður þú að slá inn gögnin á **Azure Active Directory umsóknir** síða (**Kerfisstjórnun \> Uppsetning \>Azure Active Directory umsóknir**) á mælikvarða eining dreifing. Að auki gætirðu þurft að uppfæra sjálfgefið **Fyrirtæki** gildi fyrir notandakennið eða búið til nýjan notanda. Notendur sem eru tengdir fyrirtæki sem er ekki til í dreifingu mælieininga munu ekki geta skráð sig inn þegar vöruhúsastjórnun farsímaforritið er tengt við þá mælieiningu.

> [!NOTE]
> Vegna þess að gögnin um **Azure Active Directory umsóknir** síða er ekki samstillt, þú verður að viðhalda þessum gögnum handvirkt ef þú vilt færa vöruhúsaálag yfir í aðra mælikvarðaeiningu.

Mundu að, sem hluti af tengingaruppsetningu hvers vöruhúsastjórnunar farsímaforrits, er tilgreint Azure Active Directory vefslóð tilfangs verður að vera fyrir mælieininguna í stað fyrirtækjamiðstöðvarinnar.
