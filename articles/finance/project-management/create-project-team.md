---
title: Stofna verkhóp
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að stofna og stjórna verkefnishópum.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760574"
---
# <a name="create-a-project-team"></a>Stofna verkhóp

[!include [banner](../includes/banner.md)]

Til að nota hlutverk sem voru áður sett upp í verkefni verður verkefnastjóri að tengja hlutverk við verkið. Hægt er að tengja mörg hlutverk við verk. Til að koma í veg fyrir misskilning eru þessi hlutverk sjálfkrafa merkt við frátekningu. Til dæmis, ef verkefnastjóri krefst þriggja hugbúnaðarverkfræðinga eru þrjú hlutverk hugbúnaðarverkfræðinga sem eru merktir sem **hugbúnaðarverkfræðingur 1**, **hugbúnaðarverkfræðingur 2** og **hugbúnaðarverkfræðingur 3**, sjálfvirkt mynduð. Ef einkenni hlutverks hafa áður verið stillt fyrir hlutverkið, eru þau notuð sem sía við leit tilfanga. Hægt er að bæta frekari eiginleikum við sem þarf til að fínstilla leitina enn frekar.

Einnig er hægt að sérsníða skoðun á stillingum til að gefa betra yfirlit yfir tiltæk tilföng. Það eru valkostir til að sýna tiltæki eftir klukkustund, daglega, vikulega, mánaðarlega, ársfjórðungslega og árlega. Það er einnig valkostur að sýna tiltæka og eftirstandandi afkastagetu á tilföng. Þessi valkostur er gagnlegur fyrir tímastjórnun þegar verið er að meta tiltækan tíma fyrir verkþætti eða tiltæk tilföng.

Verkefnastjórinn getur valið hlutverk á síðunni og, séu tiltæk tilföng sem hentar þörfinni, valið að taka frá tilfang til að fylla hlutverkið. Athugið að ekki þarf að taka tilföng frá á þessum tíma meðan á áætlunarferli stendur. Þegar Sundurliðun verkþátta (WBS) er stofnað er hægt að skipta út hlutverk með mönnuðum tilföngum fyrir verkið. Ef hlutverkum er skipt út fyrir mönnuð tilföng í WBS, uppfærir uppsetning tilfanga sjálfkrafa skráningar og röðun í verkhópinn.

[![Verkhópur skráningar sem inniheldur bæði hlutverk og raunveruleg tilföng](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Verkefnastjórinn hefur mismunandi valkosti fyrir bókun tilfanga fyrir verk, eins og **Eftirstöðvar afkastagetu**, **Full afkastageta**, **Hlutfall Afkastagetu**, og **Tilgreina klukkustundir**. Hætta má við þessa bókunarvalkosti hvenær sem er ef úthlutun tilfanga breytist. Til eru tvær gerðir bókunar:

- **Bundin bókun** – Frátekning tilfanga var samþykkt og staðfest að vinna í úttekt fyrir tilgreinda tímalengd.
- **Óbundin bókun** – Frátekningar á tilföngum var með fyrirvara stillt á að vinna í úttekt fyrir tilgreinda tímalengd.

Notið eftirfarandi aðferðir til þess að stofna verkhóp.

## <a name="create-a-project-team"></a>Stofna verkhóp

1. Á listasíðunni **Öll verk** veldu verk og velja svo **Breyta**.
2. Á flipanum **Verkhópur Og áætlun**, á svæðinu **Áætluð lokadagsetning**, færið inn áætlaða upphafsdagsetningu plús einn mánuður. Til dæmis, ef áætluð upphafsdagsetning er 24. Júní, 2017 (24/06/2017), færa inn **24/07/2017**.
3. Veljið **Bæta við**.
4. Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk**, veljið **Yfirverkefnastjóri**.
5. Veljið **Áskilin hæfni**.
6. Á síðunni **Velja eiginleika**, eru þeir eiginleikar sem þú stilltir áður á hlutverk Yfirverkefnastjóra valdir sjálfkrafa. Veldu **Í lagi**.
7. Á síðunni **Bæta hlutverkum við verk**, í svæðinu **Fjöldi tilfanga** skal færa inn **1**.
8. Í svæðinu **Tilföng** sýnir uppfletting öll tilföng sem hafa áskilda hæfni. Velja **Daniel Goldschmidt**, og svo **Stofna**.
9. Á síðunni **Verk** síðunni er valið **Bæta við**.
10. Í rúðunni **Bæta hlutverkum við verkið**, í svæðinu **Hlutverk** veljið **Meðlimur**. Í svæðinu **Fjöldi tilfanga** skal slá inn **5**.
11. Velja **Stofna**.
12. Á síðunni **Verk** er valið **Uppfylla tilföng**.

## <a name="monitor-project-teams"></a>Fylgjast með verkhópum
1. Á síðunni **Öll verk** skal velja **Verkkenni** tengilinn fyrir verkið **XYZ uppfærsla þrep 2** project.
2. Á flýtiflipanum **Verkhópur og áætlun** sakl ganga úr skugga um að tilföng verks sem eru talin upp séu rétt.
