---
title: Þjónustustig og lýsing
description: Þetta efni skýrir þjónustustig og lýsingu í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 65a3a0b6c2c052c41be469591c1281c1cce2b7d0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226786"
---
# <a name="service-level-and-description"></a>Þjónustustig og lýsing

[!include [banner](../../includes/banner.md)]

 

Þegar þú býrð til verkbeiðni gætirðu viljað skilgreina þjónustustig fyrir hana og bæta við almennri lýsingu. Þú getur búið til þjónustustig verkbeiðni á síðunni **Þjónustustig verkbeiðni** og lýsingar á síðunni **Verkbeiðnilýsing**.

## <a name="create-a-service-level"></a>Stofna þjónustustig

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Þjónustustig**.
2. Veljið **Nýtt**.
3. Í reitinn **Þjónustustig** slærðu inn þjónustustigið (til dæmis tölu).
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Á flýtiflipanum **Verkbeiðnir** er hægt að skilgreina áætlaðar upphafs- og lokadagsetningar og tíma. Reitirnir á þessum flýtiflipa skilgreina tímabilið sem byrja skal og ljúka verkbeiðnum. Þeir eru notaðir fyrir verkbeiðnir sem eru stofnaðar handvirkt og verkbeiðnir sem eru stofnaðar á grundvelli viðhaldsbeiðna. 

5. Í reitinn **Upphafsdagur** slærðu inn fjölda daga til að skilgreina tímabilið þegar verkbeiðnin skal hefjast. Fjöldi daga er reiknaður úr stofndagsetningu verkbeiðninnar. Til dæmis, ef verkbeiðnin skal hefjast þegar hún er búin til, sláðu þá inn **0**. Ef verkbeiðnin skal hefjast innan einnar viku eftir að hún er búin til, sláðu þá inn **7**.
6. Til að stilla upphafstíma fyrir verkbeiðnina, auk upphafsdagsetningar, skaltu stilla valkostinn **Stilla upphafstíma** á **Já**. Sláðu síðan upphafstímann inn í reitinn **Upphafstími**. Ef þú stillir möguleikann á **Nei** er núverandi tími dags notaður.
7. Í reitinn **Lokadagur** slærðu inn fjölda daga til að skilgreina tímabilið þegar verkbeiðni skal ljúka. Fjöldi daga er reiknaður úr upphafsdagsetningu verkbeiðninnar. Til dæmis, ef verkbeiðnin skal ljúka innan viku frá upphafsdegi hennar, sláðu þá inn **7**.
8. Til að stilla lokatíma fyrir verkbeiðnina, auk lokadagsetningar, skaltu stilla valkostinn **Stilla lokatíma** á **Já**. Sláðu síðan lokastímann inn í reitinn **Lokatími**. Ef þú stillir möguleikann á **Nei** er núverandi tími dags notaður.
9. Veljið **Vista**.

![Síðan Þjónustustig verkbeiðna](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Stofna lýsingu

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Lýsingar**.
2. Veljið **Nýtt**.
3. Í reitnum **Lýsing** skal færa inn lýsinguna.
4. Veljið **Vista**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]