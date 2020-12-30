---
title: Stofna verkbeiðnir úr viðhaldsbeiðnum
description: Þetta efni útskýrir hvernig á að stofna verkbeiðni úr viðhaldsbeiðni í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6bd98796140ab7aa3e7813ff1526413504554c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430394"
---
# <a name="create-work-orders-from-maintenance-requests"></a>Stofna verkbeiðnir úr viðhaldsbeiðnum

[!include [banner](../../includes/banner.md)]

 


Eftir að þú hefur búið til viðhaldsbeiðnir geturðu auðveldlega umbreytt þeim í vinnupantanir. Þetta efni lýsir skjótustu leiðinni til að vinna með viðhaldsbeiðnir, uppfæra nokkrar viðhaldsbeiðnir á sama tíma og búa síðan til vinnupöntun fyrir nokkrar viðhaldsbeiðnir á sama tíma. Á síðunni **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu** geturðu líka unnið með eina viðhaldsbeiðni í einu og umbreytt einni viðhaldsbeiðni í vinnupöntun.

> [!NOTE]
> Sérhver viðhaldsbeiðni getur tengst aðeins einni verkbeiðni. Hins vegar geta margar viðhaldsbeiðnir verið með í einni verkbeiðni, jafnvel þó að viðhaldsbeiðnirnar hafi mismunandi eignir.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir**.
2. Áður en þú getur búið til verkbeiðni úr viðhaldsbeiðnum, verðurðu að velja, að lágmarki, tegund viðhalds fyrir viðhaldsbeiðnir, og einnig afbrigði og viðskipti af viðhaldsvinnu, ef þessar upplýsingar eru viðeigandi. Í netskjánum geturðu auðveldlega uppfært upplýsingar vegna viðhaldsbeiðni.
3. Þegar þú ert tilbúinn að búa til verkbeiðni skaltu velja viðhaldsbeiðnirnar sem á að hafa í henni.

    - Ef þú velur nokkrar viðhaldsbeiðnir til að umbreyta í verkbeiðni, verða bæði reiturinn **Eignir** og reiturinn **Gerð viðhaldsverks** að vera stilltir áður en þú stofnar verkbeiðnina.
    - Ef þú velur eina viðhaldsbeiðni til að umbreyta í verkbeiðni, verður aðeins reiturinn **Eignir** verður að vera stilltur áður en þú stofnar verkbeiðnina. Hins vegar, þegar þú býrð til verkbeiðnina, getur þú valið viðhaldsverkefna gerð (og tengt viðhaldstegundarafbrigði og viðskipti, ef þessar upplýsingar eru viðeigandi) í valmyndinni **Búðu til vinnu röð**.

4. Veldu **Verkbeiðni**.
5. Í valmyndinni **Stofna verkbeiðni** stillirðu reitina og velur síðan **Í lagi**.

    Skilaboðastika gæti tilkynnt þér að ný verkbeiðni hafi verið búin til.

    Að auki, þegar þú býrð til verkbeiðni sem er byggð á viðhaldsbeiðni, ef eignin sem er tengd viðhaldsbeiðninni er innifalin í ábyrgðarsamningi, tilkynnir skilaboðastikan þér um ábyrgðarsamninginn.

6. Veldu **Eignastýring** \> **Sameiginlegt** \> **Verkbeiðni** \> **Allar verkbeiðnir**, og opnaðu nýju vinnupöntunina.

    ![Opna nýja vinnupöntun](media/05-manage-maintenance-requests.png)

