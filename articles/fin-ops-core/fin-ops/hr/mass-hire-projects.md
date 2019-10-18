---
title: Fjöldaráðningarverk
description: Fjöldaráðningarverk leyfa mannauðssérfræðingum að búa til margar stöður og ráða starfsmenn á skilvirkan hátt í þær stöður.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 7481
ms.assetid: 5f5eb271-76eb-4305-bd1c-5d171dafccc9
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7dacc8b0ca8659d3ae69c81385918ef6fa39c04
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178398"
---
# <a name="mass-hire-projects"></a>Fjöldaráðningarverk

[!include [banner](../includes/banner.md)]

Fjöldaráðningarverk leyfa mannauðssérfræðingum að búa til margar stöður og ráða starfsmenn á skilvirkan hátt í þær stöður.

## <a name="overview"></a>Yfirlit

Þegar margir starfsmenn eru ráðnir á sama tíma, eins og þegar fólk er ráðið til að mæta vertíðarálagi, er gagnlegt að stofna fjöldaráðningaverk. Að stofna fjöldaráðningarverk er gagnlegt þar sem hægt er að stofna stöðufærslur, starfsmannaskrár, og starfsmannaúthlutun fyrir stöður á sama tíma. Þegar stöður eru stofnaðar fyrir fjöldaráðningarverk er hægt að tilgreina eftirfarandi upplýsingar:

- Fjöldi staða sem á að stofna
- Gerð starfsmanns fyrir fólk sem verður ráðið í stöður
- Starf og deild sem stöðurnar tengjast.
- Gildi fulls starfs fyrir stöðuna

## <a name="example"></a>Dæmi

Á sumrin, er yfirleitt ráðnir 15 20 skólakrakkar í hlutastarf til að fylla tiltækar starfsnámsstöður í fyrirtækinu. Nú í ár, á að ráða fimm bókhaldara, fimm starfsmenn í pantanavinnslu og fimm gjaldkera. Í stað þess að stofna hverja stöðufærslu og starfsmannaskrá sér, er stofnað eitt fjöldaráðningarverk sem kallast „SummerInterns“. Upphafs- og lokadagsetningar verksins er í samræmi við upphags og lokadagsetningar tímalengdar fyrir stöðurnar sem þú stofnar fyrir fjöldaráðningarverkið.

Á síðunni **Fjöldaráðningarverk** skal velja verkið „SummerInterns“ og smella síðan á **Opna verk**. Í Opna fjöldaráðningarverk, er smellt **Stofna stöður** og færa inn upplýsingar um stöðu bókarans. Hægt er að tilgreina að fimm bókarastöður ættu að vera stofnuð með því að nota sömu upplýsingar fyrir hverja og eina, og smellið svo á í lagi. Endurtakið þetta ferli fyrir afgreiðslumaður pantana og gjaldkerastöður.

Eftir val á námsmönnum til að ráða fyrir starfsnámsstöður, verður að færa inn upplýsingar hvers námsmanns á **Stöðuupplýsingar** fyrir stöðu sem verið er að ráða þá í. Þegar að hafa verið færðar inn allar upplýsingar um stöðu, veljið stöðuna í fjöldaráðningarverk síðu, og smellið síðan á **Ráða**. Stöðufærsla verður stofnuð fyrir hverja stöðu og skrá starfsmanns stofnuð og úthlutað á rétta stöðu fyrir hvern einstakling sem þú ræður.

## <a name="mass-hire-project-statuses"></a>Stöður fjöldaráðningarverks

ráðningarverk getur verið með eftirfarandi stöður:

- Stofnaður
- Opna
- Lokað

Á **fjöldaráðningarverk** síðunni er smellt á **Opna verk** eða **Loka verki** til að breyta stöðu fjöldaráðningarverks. Eftirfarandi tafla lýsir því hvað hægt er að gera við verk eftir því hver staða þess er.

<table>
<thead>
<tr>
<th>Staða</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr>
<td>Stofnaður</td>
<td>Hægt er að stofna og breyta upplýsingum en ekki er hægt að stofna stöður fyrir verkið. Þetta er sjálfgefin staða fyrir ný verk.</td>
</tr>
<tr>
<td>Opna</td>
<td>Hægt er að breyta upplýsingum um verk, stofna stöður fyrir fjöldaráðningarverk og ráða fólk í stöður. Þetta er staða virkra verka.</td>
</tr>
<tr>
<td>Lokað</td>
<td>Ekki er hægt að bæta stöðum við verkið. Til að bæta stöðum við fjöldaráðningarverkið, opna verkið aftur. Þetta er staða lokaðra verka.
<blockquote>[!NOTE] Áður en hægt er að loka fjöldaráðningaverki, verða allar stöður í verkinu að hafa stöðu annað hvort Stofnuð eða Lokuð.</blockquote>
</td>
</tr>
</tbody>
</table>
