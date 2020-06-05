---
title: Hafist handa með kostnaðarbókhaldsþjónustu (einkaforskoðun)
description: Þetta efnisatriði inniheldur leiðbeiningar varðandi leyfi og leiðbeiningar um uppsetningu á kostnaðarbókhaldsþjónustuna.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: a82af9e8ec1806f470103897389d0316d33a4a06
ms.sourcegitcommit: 7fec9dc5297ed6e687d4a0dff099922d59d6a830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/13/2020
ms.locfileid: "3372737"
---
# <a name="get-started-with-the-cost-accounting-service-private-preview"></a>Hafist handa með kostnaðarbókhaldsþjónustu (einkaforskoðun)

[!INCLUDE [banner](../includes/banner.md)]

> [!IMPORTANT]
> Virkni sem getið er í þessu efnisatriði er tiltæk sem hluti af sérstakri prufuútgáfu. Efni þessa efnisatriðis og virknin sem þar er lýst geta breyst. Frekari upplýsingar um forútgáfur er að finna í hlutanum [Algengar spurningar um uppfærslureglur fyrir „Ein útgáfa“](../../fin-ops-core/fin-ops/get-started/one-version.md).

Kostnaðarbókhaldsþjónusta gerir þér kleift að framkvæma fjöldamörg birgðabókhöld í fjárhagi kostnaðarbókhalds sem þú hefur sett upp. Þú tengir hvern fjárhag kostnaðarbókhalds við *reglu*. Regla er safn af eftirfarandi gerðum reikningsskilaaðferða:

- Kostnaðarhlutur
- Grunnmæling inntaks
- Áætlun kostnaðarflæðis
- Kostnaðareining

> [!NOTE]
> Jafnvel eftir að þú hefur kveikt á kostnaðarbókhaldsþjónustunni geturðu samt gert birgðabókhald í Microsoft Dynamics 365 Supply Chain Management eins og áður.

Kostnaðarbókhaldsþjónustan er viðbót. Til að gera aðgerðir þess aðgengilegar verður þú að setja hana upp frá Microsoft Dynamics Lifecycle Services (LCS). Þess vegna getur þú valið að meta það í prufuumhverfi áður en þú setur það í framleiðsluumhverfi.

Kostnaðarbókhaldsþjónustan styður ekki sem stendur alla þá kostnaðarstjórnunareiginleika sem eru innbyggðir í Dynamics 365 Supply Chain Management. Þess vegna er mikilvægt að þú metir hvort grunneiginleikarnir sem nú eru tiltækir uppfylli kröfur þínar.

## <a name="how-to-get-the-cost-accounting-service-private-preview"></a><a name="sign-up"></a>Hvernig á að sækja kostnaðarbókhaldsþjónustu (einkaforskoðun)

> [!IMPORTANT]
> Til að nota kostnaðarbókhaldsþjónustuna verður þú að vera með LCS-virkt umhverfi með mikið framboð (ekki OneBox umhverfi) og þú verður að keyra útgáfu 10.0.11 af Dynamics 365 Supply Chain Management eða nýrri.

Til að skrá sig fyrir einkasniðforskoðun kostnaðarbókhalds skulu notendur senda umhverfiskenni LCS í tölvupósti á [Kostnaðarbókhaldsþjónusta (einkaforskoðun)](mailto:aevengir@microsoft.com?subject=Cost%20accounting%20service%20%28private%20preview%29). Þegar notandi er samþykktur fær hann sendan tölvupóst sem inniheldur beta-lykil fyrir kostnaðarbókhaldsþjónustu. Þegar beta-lykllinn er móttekinn er hægt að halda áfram með því að [setja upp innbótina](#install).

## <a name="licensing"></a>Leyfisveiting

Kostnaðarbókhaldþjónustan er háð leyfi ásamt stöðluðu eiginleikum birgðabókhalds sem eru í boði fyrir Supply Chain Management. Þú þarft ekki að kaupa viðbótarleyfi til að nota kostnaðarbókhaldsþjónustuna.

## <a name="install-the-add-in"></a><a name="install"></a>Setja upp innbótina

Til að nota kostnaðarbókhaldsþjónustuna, skaltu setja upp viðbót kostnaðarbókhaldsþjónustu fyrir Supply Chain Management eins og lýst er í eftirfarandi aðferð.

1. [Skráning](#sign-up) fyrir kostnaðarbókhaldsþjónustu (einkasforskoðun).

1. Skráðu þig inn í LCS.

1. Farið í **Stjórnun forskoðunareiginleika**.

1. Veldu plústáknið (**+**).

1. Sláðu inn beta-lykilinn fyrir viðbót kostnaðarbókhaldsþjónustu á svæðið **Kóði**. (Þú hefðir átt að fá lykilinn þinn með tölvupósti.)

1. Veldu síðan **Opna fyrir**.

1. Opnaðu LCS-umhverfi þar sem þú vilt bæta við þjónustunni.

1. Farðu í **Fullar upplýsingar**.

1. Flettu niður að flýtiflipanum **Umhverfisinnbætur**.

1. Veldu **Setja upp nýja innbót**.

1. Veljið **Kostnaðarbókhaldsþjónusta**.

1. Fylgdu uppsetningarleiðbeiningunum og samþykktu skilmála og skilyrði.

1. Velja **Setja upp**.

1. Í flýtiflipanum **Viðbætur fyrir umhverfi** ættir þú að sjá að kostnaðarbókhaldsþjónustan er sett upp. Eftir nokkrar mínútur ætti staðan að breytast úr **Setur upp** í **Uppsett**. (Hugsanlega verður þú að endurhlaða síðuna til að breytingin komi í ljós). Á þeim tímapunkti er kostnaðarbókhaldsþjónustan tilbúin til notkunar.

## <a name="set-up-the-integration"></a>Setja upp samþættingu

Til að setja upp samþættingu milli kostnaðarbókhaldsþjónustu og Dynamics 365 Supply Chain Management:

1. Farðu í **Kerfisstjórnun > Eiginleikastjórnun**.

1. Veldu **Leita að uppfærslum**.

1. Opnaðu flipann **Allt** og leitaðu að eiginleika sem heitir *Kostnaðarbókhaldsþjónusta*.

1. Veldu **Virkja núna**.

1. Farðu í **Kostnaðarstjórnun > Kostnaðarbókhaldsþjónusta > Uppsetning > Þjónustubreytur kostnaðarbókhalds > Samþættingarbreytur**.

1. Í **Kenni forrits** skal slá inn eftirfarandi kóða:<br> 08231eb2-a501-4edb-b3c5-aede5e5e0c3f

1. Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð gagnaþjónustu**:<br>https://operationsdataservice.operations365.dynamics.com/

1. Sláðu inn eftirfarandi vefslóð í svæðið **Endastöð kostnaðarbókhaldsþjónustu**:<br>https://costaccountingservice.operations365.dynamics.com/

1. Kostnaðarbókhaldsþjónustan er nú tilbúin til notkunar.

## <a name="related-resources"></a>Tengd tilföng

[Heimasíða kostnaðarbókhaldsþjónustu](cost-accounting-service-home.md)
