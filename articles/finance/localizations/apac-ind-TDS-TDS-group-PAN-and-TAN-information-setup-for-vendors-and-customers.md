---
title: Uppsetning á TDS-flokki, PAN- og TAN-upplýsingum fyrir lánardrottna og viðskiptavini
description: Í þessari grein er útskýrt hvernig á að setja upp upplýsingar um flokkinn fyrir skatt sem er dreginn frá í upphafi (TDS), varanlegt lykilnúmer (PAN) og skattlykilnúmer (TAN) fyrir lánardrottna og viðskiptavini.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1a29f59e380360b6f828dcddbe84cad229b42d17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859767"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Uppsetning á TDS-flokki, PAN- og TAN-upplýsingum fyrir lánardrottna og viðskiptavini

[!include [banner](../includes/banner.md)]

Í þessari grein er útskýrt hvernig á að setja upp upplýsingar um flokkinn fyrir skatt sem er dreginn frá í upphafi (TDS), varanlegt lykilnúmer (PAN) og skattlykilnúmer (TAN) fyrir lánardrottna og viðskiptavini.

1. Farið í **Viðskiptaskuldir \> Lánardrottnar \> Allir lánardrottnar** eða **Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**.

    [![Síða allra lánardrottna.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Á aðgerðasvæðinu skal velja **Nýr** til að búa til lánardrottin eða viðskiptavin og færa inn nauðsynlegar upplýsingar. Einnig er hægt að velja núverandi lánardrottin eða viðskiptavin.
3. Í flýtiflipanum **Reikningur og afhending**, í hlutanum **Staðgreiðsluskattur**, skal stilla valkostinn **Reikna staðgreiðsluskatt** á **Já** til að reikna staðgreiðsluskatt, TDS eða skatt dreginn frá upprunalegri færslu (TCS) fyrir lánardrottin eða viðskiptavin.
4. TDS fyrir innkaupareikning er reiknað út frá sjálfgefnum TDS-flokki sem er skilgreindur fyrir lánardrottin eða viðskiptavin. Í reitnum **TDS-flokkur** skal velja sjálfgefinn TDS-flokk.

    > [!NOTE]
    > Þegar TDS-flokkur er valinn í reitnum **TDS-flokkur** verða reitirnir **Staðgreiðsluskattsflokkur** og **TCS-flokkur** ekki í boði.

5. Í flýtiflipanum **Skattaupplýsingar**, í hlutanum **Upplýsingar um PAN**, í reitnum **Staða**, skal velja stöðu varanlegs reikningsnúmers fyrir lánardrottin eða viðskiptavin:

    - **Ekki fyrir hendi** – Lánardrottinn eða viðskiptavinur er ekki með PAN.
    - **Móttekið** – Lánardrottinn eða viðskiptavinur er með PAN.
    - **Sótt um** – Lánardrottinn eða viðskiptavinur hefur sótt um PAN.
    - **Ógilt** – Lánardrottinn eða viðskiptavinur er með PAN en það er ekki gilt.

6. Ef **Móttekið** var valið í reitnum **Staða** til að gefa til kynna að lánardrottin eða viðskiptavinur sé með PAN skal færa inn PAN í reitinn **Númer**. PAN verður að samanstanda af fimm bókstöfum, síðan fjórum tölustöfum og síðan einum bókstaf. Eftirfarandi er dæmi: **ABCDE1260A**.
7. Ef **Sótt um** var valið í reitnum **Staða** til að gefa til kynna að lánardrottin eða viðskiptavinur hafi sótt um PAN skal færa inn tilvísunarnúmerið í reitinn **Tilvísunarnúmer**.
8. Í reitnum **Eðli skattgreiðanda** skal velja eðli skattgreiðendaflokks sem lánardrottinn eða viðskiptavinur tilheyrir:

    - Fyrirt.  
    - HUF
    - Staðfesta
    - Sérstakt
    - AOP
    - BOI
    - Staðaryfirvald
    - Aðrir

    [![Flýtiflipi skattaupplýsinga.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Skráning**, skal velja **Skráningarkenni** til að opna síðuna **Stjórna aðsetrum**.
10. Á síðunni **Stjórna aðsetrum**, í flýtiflipanum **Skattaupplýsingar**, skal velja **Bæta við** eða **Breyta** til að opna síðuna **Stjórna skattaupplýsingum** þar sem hægt er að vinna með færslu skattskráningar.
11. Á síðuna **Stjórna skattaupplýsingum**, í flýtiflipann **Staðgreiðsluskattur**, í reitinn **Skattlykilnúmer (TAN)** skal færa inn TAN. TAN verður að samanstanda af fjórum bókstöfum, síðan fimm tölustöfum og síðan einum bókstaf. Eftirfarandi er dæmi: **AFGH54821T**.
12. Lokið síðunni.
