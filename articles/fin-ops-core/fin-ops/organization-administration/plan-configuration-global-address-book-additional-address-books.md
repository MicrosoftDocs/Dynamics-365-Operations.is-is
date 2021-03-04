---
title: Skipuleggja altæku aðsetursbókina og aðrar aðsetursbækur
description: Þetta efnisatriði lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d83d6536d85100ef6a91e909be5a8e57e423371
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693931"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a>Skipuleggja altæku aðsetursbókina og aðrar aðsetursbækur

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir umhugsunarefni og ákvarðanir sem þarf að taka í áætlunarferli, áður en hægt er setja upp og stilla altæka aðsetursbók og allar aðrar aðsetursbækur. Sumir af þeim ákvörðunum munu krefjast þess að þú staðfestir þær ákvarðanir sem hafa verið gerðar fyrir önnur svið vörunnar, svo sem stigveldi fyrirtækis.

## <a name="global-address-book"></a>Altæk aðsetursbók

Áður en byrjað er að vinna með í altækri aðsetursbók verður að ákvarða sjálfgefin gildi fyrir hana. Þessi sjálfgildi eru síðan notaðar fyrir allar aðrar aðsetursbækur sem eru stofnaðar.

**Ákvarðanir**

- Hvaða röð ætti nöfn að birtast í fyrir aðilafærslur fyrir gerðina **Einstaklingur**? Til dæmis er ein röð eftirnafn, millinafn fornafn.
- Á eyða aðilafærslur úr aðsetursbókinni þegar hlutverk færslu er eytt? Til dæmis, ef færslu um viðskiptavin er eytt er á einnig að eyða færslu aðila?
- Þegar ný færsla er stofnuð á notendum að tilkynna ef tvítekin færsla fannst í altæku aðsetursbókinni?
- Á DUNS-númer (Data Universal Numbering System) að fylgja með í upplýsingum aðilafærslu?
- Ef duns-númer er innifalin í aðilafærslu þarf að athuga einkvæmni númersins?
- Þegar aðilafærsla er stofnuð í altæku aðsetursbókinni á aðilagerð, manneskju eða fyrirtæki að vera sjálfgefin, ?
- Hvaða notandahlutverk ætti að hafa aðgang að persónulegum aðsetrum og tengslaupplýsingum fyrir aðilafærslur?

## <a name="additional-address-books"></a>Auka aðsetursbækur

Þegar Búið er að stofna altæka aðsetursbók, er hægt að stofna viðbótar aðsetursbækur sem þörf er á, svo sem aðskilda aðsetursbókar fyrir hvert fyrirtæki í þínu samsteypu eða fyrir hverja atvinnugrein. Til dæmis er Fabrikam alþjóðlegt fyrirtæki sem er með mörg fyrirtæki og margar atvinnugreinar. Fabrikam áformar að stofna aðsetursbók fyrir hverja atvinnugrein. Fyrir atvinnugreinar sem eru á fleiri en einum stað, eins og viðskipti með loftknúin verkfæri, áformar Fabrikam að stofna aðsetursbók fyrir hverja staðsetningu. Chris, tæknistjóri hjá Fabrikam, hefur stofnað eftirfarandi listi yfir aðsetursbækur sem krafist er. Þessi listi lýsir einnig aðilafærslum sem hver aðsetursbók verður að hafa.

- **Samningar hins opinbera (PubSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum hins opinbera sem Fabrikam býr yfir.
- **Samningar almenns vinnumarkaðar (PriSC)** – Aðilafærslur fyrir alla aðila sem koma að samningum almenns vinnumarkaðar sem Fabrikam býr yfir.
- **Rafræn Verkfæri (ET)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á rafræna verkfæri, eða verkfæra sem annars tengjast á einhvern hátt rafrænum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.
- **Loftknúin Verkfæri (PTJPN)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-Japan fyrirtækinu.
- **Loftknúin Verkfæri (PTUSA)** – aðilafærslur fyrir alla aðila sem tengjast innkaupum eða sölu á loftknúnum verkfæri, eða verkfæra sem annars tengjast á einhvern hátt loftknúnum verkfærum sem Fabrikam veitir eða Fabrikam kaupir í Fabrikam-US fyrirtækinu.

**Ákvörðun:**

- Hversu margar viðbótar aðsetursbækur muntu stofna?


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]