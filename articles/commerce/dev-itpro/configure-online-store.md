---
title: Skilgreina verslanir á netinu
description: Þessi grein veitir tengla í efni sem mun hjálpa þér að stilla miðlægt og stjórna netverslun.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ab35767beb2fa53b3fb688d986a36f0bf1d4984f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024433"
---
# <a name="configure-online-stores"></a>Skilgreina verslanir á netinu

[!include [banner](../includes/banner.md)]

Þessi grein veitir tengla í efni sem mun hjálpa þér að stilla miðlægt og stjórna netverslun.

Efnisatriðin í eftirfarandi töflu lýsa skilgreiningu Commerce-þátta og netversluninni í biðlaranum.

## <a name="configure-an-online-store"></a>Skilgreina netverslun

| Verk                                                | Upplýsingar                                                                                                                                                                                                                                                                                                                                                   | Efni                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Skilgreina íhluti.                        | Setja upp og viðhalda upplýsingum um Commerce-aðgerðir. Þessar upplýsingar taka til verslana, skatta, afurða, gjafakorta, kynningartilboða og afsláttar.                                                                                                                                                                                                          | [Uppsetning og viðhald smásölu](https://technet.microsoft.com/library/hh597201.aspx) (TechNet-efni fyrir Microsoft Dynamics AX 2012)                                                                                                                                                                                                                                                                                          |
| Grunnstilla skoðunarstigveldi rásar.    | Stofna skoðunarstigveldi rásar til að setja upp tegundaskipulag fyrir afurðir sem boðnar eru til sölu í netverslun. Þú skilgreinir tegundastigveldi og úthlutar afurð, afurðareigindaflokkum og eigindargildum í tegundrnar. Síðan er hægt að úthluta tegundastigveldinu á netverslunina.                            | [Setja upp smásölustigveldi](https://technet.microsoft.com/library/hh580593.aspx)</br> (TechNet efni fyrir AX 2012)</br> [Settu upp eiginleika og eigindategundir](https://technet.microsoft.com/library/hh227548.aspx) (TechNet efni fyrir AX 2012)</br> [Settu upp smásölu eigindahópa](https://technet.microsoft.com/library/jj728713.aspx) (TechNet efni fyrir AX 2012) |
| Bæti netversluninni við stigveldi fyrirtækis. | Áður en hægt er að úthluta afurðaúrvali eða uppfylla pantanir fyrir netverslun sem hefur verið stofnuð eða búa til skýrslur sem innihalda upplýsingar úr þeirri netverslun verður að úthluta versluninni á eitt eða fleiri stigveldi fyrirtækis. Að lágmarki þarf að úthluta netverslun á stigveldi fyrirtækis sem inniheldur afurðaúrval. | [Setja upp netverslun](https://technet.microsoft.com/library/jj682095.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                                                                                                                                                                                                     |
| Bæta afhendingarmáta við netverslun.          | Veldu afhendingaraðferðir sem netverslunin býður.                                                                                                                                                                                                                                                                                                 | [Setja upp netverslun](https://technet.microsoft.com/library/jj682095.aspx) (TechNet-efni fyrir Microsoft AX 2012)                                                                                                                                                                                                                                                                                                     |
| Varpa eigindum og bæta lýsigögnum við.                   | Veldu valkosti sem sýna hvernig eigindir fyrir hverja flokks- eða rásarafurð ættu að haga sér í netversluninni á svæði Microsoft SharePoint.                                                                                                                                                                                              | [Setja upp netverslun](https://technet.microsoft.com/library/jj682095.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Grunnstilla afurðum netverslunar

| Verk                                 | Upplýsingar                                                                                                                                           | Efni                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bæta úrvali við netverslun. | Bæta við vöruúrval sem hafa með afurð sem þú býður í netverslun.                                                                  | [Setja upp netverslun](https://technet.microsoft.com/library/jj682095.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                                              |
| Stjórna vörulistum.                     | Notaðu vörulista til að auðkenna afurðirnar sem óskað er eftir að bjóða upp í verslunum.                                                              | [Lykilverkefni: Stofna smásöluvörulista](https://technet.microsoft.com/library/jj728712.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                           |
| Stjórna verðum.                       | Setja upp og nota verðflokka sem eru miðtengill á milli verða og afslátta og rásir, vörulista, tengsl og vildarkerfa. | [Setja upp verð með verðflokkum](https://technet.microsoft.com/library/hh597169.aspx) (TechNet efni fyrir AX 2012)</br> [Setja upp skatta](https://technet.microsoft.com/library/hh580571.aspx) (TechNet efni fyrir AX 2012) |
| Stjórna afslætti.                    | Setja upp og stjórna verðleiðréttingum og fjórum gerðum afslátta.                                                                                  | [Uppsetning verðleiðréttingar og afslátta](https://technet.microsoft.com/library/hh597114.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                          |
| Stjórna sendingargjöldum.             | Setja upp og stjórna sendingargjöldum sem eru sértæk fyrir netverslunina.                                                                     | [Setja upp sendingargjöld fyrir netverslanir](https://technet.microsoft.com/library/jj728714.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                           |
| Stjórna afhendingarmátum.            | Stjórna afhendingarmátum sem eru í boði í netversluninni.                                                                                        | [Setja upp afhendingarmáta](https://technet.microsoft.com/library/jj728719.aspx) (TechNet-efni fyrir AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Setja upp gagnaskipti á milli Commerce og netverslunar

| Verk                                 | Upplýsingar                                                                                                                               | Efni                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Setja upp samþættingarreglur rása. | Forstilling gera virkjar íhluti til að hafa samskipti sín á milli. Setja upp forstillingar áður en stillingar gagnaskipta eru grunnstilltar. | [Settu upp rauntíma þjónustusnið](https://technet.microsoft.com/library/hh580631.aspx) (TechNet efni fyrir AX 2012)</br> [Settu upp rásarforstillingar](https://technet.microsoft.com/library/jj677402.aspx) (TechNet efni fyrir AX 2012) |





