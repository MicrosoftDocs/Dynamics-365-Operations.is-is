---
title: "Grunnstilla altæka aðsetursbók"
description: "Þessi grein lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur í Microsoft Dynamics 365 for Operations. Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: abd9ec44530522657f758b35e8f987aa92c3b0e3
ms.lasthandoff: 03/31/2017


---

# <a name="configure-global-address-books"></a>Grunnstilla altæka aðsetursbók

[!include[banner](../includes/banner.md)]


Þessi grein lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur í Microsoft Dynamics 365 for Operations. Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis.

<a name="global-address-book"></a>Altæk aðsetursbók
-------------------

Áður en byrjað er að vinna með í altækri aðsetursbók verður að ákvarða sjálfgefin gildi fyrir hana. Þessi sjálfgildi eru síðan notaðar fyrir allar aðrar aðsetursbækur sem eru stofnaðar. **Ákvarðanir:**

-   Hvaða röð ætti nöfn að birtast í fyrir aðilafærslur fyrir gerðina **Einstaklingur**? Til dæmis er ein röð eftirnafn, millinafn fornafn.
-   Á eyða aðilafærslur úr aðsetursbókinni þegar hlutverk færslu er eytt? Til dæmis, ef færslu um viðskiptavin er eytt er á einnig að eyða færslu aðila?
-   Þegar ný færsla er stofnuð á notendum að tilkynna ef tvítekin færsla fannst í altæku aðsetursbókinni?
-   Á að fylgja DUNS-númer (Data Universal Numbering System-númer) með í upplýsingum aðilafærslu?
-   Ef duns-númer er innifalin í aðilafærslu þarf að athuga einkvæmni númersins?
-   Þegar aðilafærsla er stofnuð í altæku aðsetursbókinni á aðilagerð, manneskju eða fyrirtæki að vera sjálfgefin, ?
-   Hvaða notandahlutverk ætti að hafa aðgang að persónulegum aðsetrum og tengslaupplýsingum fyrir aðilafærslur?

## <a name="additional-address-books"></a>Auka aðsetursbækur
Þegar Búið er að stofna altæka aðsetursbók, er hægt að stofna viðbótar aðsetursbækur sem þörf er á, svo sem aðskilda aðsetursbókar fyrir hvert fyrirtæki í þínu samsteypu eða fyrir hverja atvinnugrein. Til dæmis er Fabrikam alþjóðlegt fyrirtæki sem er með mörg fyrirtæki og margar atvinnugreinar. Fabrikam áformar að stofna aðsetursbók fyrir hverja atvinnugrein. Fyrir atvinnugreinar sem eru á fleiri en einum stað, eins og viðskipti með loftknúin verkfæri, áformar Fabrikam að stofna aðsetursbók fyrir hverja staðsetningu. Chris, tæknistjóri hjá Fabrikam, hefur stofnað eftirfarandi listi yfir aðsetursbækur sem krafist er. Þessi listi lýsir einnig aðilafærslur sem hver aðsetursbók verður að hafa.

-   **Samningar hins opinbera (PubSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum hins opinbera sem Fabrikam býr yfir.
-   **Samningar almenns vinnumarkaðar (PriSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum almenns vinnumarkaðar sem Fabrikam býr yfir.
-   **Rafræn Verkfæri (ET)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á rafræna verkfæri, eða verkfæra sem annars tengjast á einhvern hátt rafrænum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.
-   **Loftknúin Verkfæri (PTJPN)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.
-   **Loftknúin Verkfæri (PTUSA)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-US fyrirtækinu.

**Ákvörðun:**

-   Hversu margar viðbótar aðsetursbækur muntu stofna?

### <a name="address-book-security"></a>Öryggi Aðsetursbókar

Hægt er að stofna aðsetursbækur hvenær sem er, og einnig er hægt að stilla öryggisfæribreytur fyrir aðsetursbækurnar hvenær sem er. Ekki þarf að setja öryggisréttindi fyrir aðsetursbók, en það er ekki gert geta alla starfsmenn í fyrirtækinu þínu skoða allar færslur allra aðila sem eru í aðsetursbók. Hægt er að setja upp öryggisréttindi fyrir aðilafærslu í gegnum aðsetursbækur. Öryggisréttindi á grundvölluð á teymi. Þessi nálgun tryggir að aðeins starfsmenn sem eru úthlutaðar teymi sem hefur aðgang að aðsetursbók geta skoðað færslur aðila í þeirri aðsetursbók. Þú verður að velja hópa sem hefur aðgang að hverju aðsetursbók. Fyrir hverja aðsetursbók hægt er að setja öryggisréttindi sem heimila eða hafna aðgang fyrir tilteknum teymi. Þegar er hóp er veittur réttindi fyrir aðgang að aðsetursbók, geta allir hópmeðlimum skoða færslurnar í aðsetursbók. Þegar er hóp er ekki veittur aðgangur fyrir aðgang að aðsetursbók, geta hópmeðlimir ekki skoða færslurnar í aðsetursbók eða efni hennar. **Ákvörðun:**

-   Hvaða teymi ætti að hafa aðgang að hverju nýja aðsetursbók sem verður stofnað?





