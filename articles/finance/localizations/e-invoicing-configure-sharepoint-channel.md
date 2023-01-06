---
title: Skilgreina SharePoint-rás
description: Í þessari grein er útskýrt hvernig á að skilgreina Microsoft SharePoint rás til að vinna úr rafrænum reikningum á innleið.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 92eaa357c6d72cc637d4ce353702e5d41ecf4338
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272305"
---
# <a name="configure-a-sharepoint-channel"></a>Skilgreina SharePoint-rás

[!include [banner](../includes/banner.md)]

Forsenda þess að hægt sé að skilgreina Microsoft SharePoint rás til að vinna úr skjölum á innleið er að ljúka við skrefin sem lýst er í [Skilgreina SharePoint tengingu](e-invoicing-create-sharepoint-connection.md).

Síðan er hægt að nota SharePoint rásina til að flytja inn rafræna sölureikninga úr skrám sem eru geymdar í SharePoint möppunum þínum.

1. Á SharePoint svæðinu þínu skaltu búa til eftirfarandi möppur:

    - **Aðalmappa** - Mappan sem þjónustan mun vinna skrár úr.
    - **Safnvistunarmappa** – Mappan þar sem afgreiddar skrár verða geymdar.
    - **Villumappa** – Mappan sem kerfið mun færa möppur í ef vinnslan mistekst.

2. Í Regulatory Configuration Service (RCS) skal velja eiginleika rafrænnar reikningsfærslu sem var búinn til. Gakktu úr skugga um að þú veljir útgáfuna með stöðuna **Drög**.
3. Í flipanum **Uppsetningar** skal velja **Bæta við**.
4. Í felliglugganum **Búa til uppsetningu eiginleika**, í reitahópnum **Nýtt**, skal velja valkostinn **Sérsniðin uppsetning**.
5. Í reitahópnum **Gerð uppsetningar** skal velja valkostinn **Gagnarás**.
6. Í reitnum **Velja gagnarás** skal velja **SharePoint möppu**.
7. Velja **Stofna**.
8. Veldu línuna sem þú bjóst til og veldu síðan **Breyta**.
9. Í flipanum **Gagnarás**, í hlutanum **Færibreytur**, skal stilla eftirfarandi áskilda reiti.

    | Svæði                 | Lýsing |
    |-----------------------|-------------|
    | Gagnarás          | Færið inn einkvæmt heiti til að auðkenna gagnarásina. Mest má nota 10 stafi í heitinu. Vísað verður í hann í gildissviðsreglum og í tengdum forritum í samskiptaferlinu. |
    | SharePoint-veffang    | Sláðu inn SharePoint-vefslóðina. Til dæmis er slegið inn `<domain>.sharepoint.com`. |
    | Auðkenni umsóknar        | Færðu inn heiti á leynilykli Azure-lyklageymslu sem inniheldur auðkenni fyrir SharePoint notandareikningsins. Þennan leynilykil þarf að búa til í lyklageymslu og setja upp í þjónustuumhverfinu. Gildið er gildið fyrir **Auðkenni forrits (biðlara)** úr [Skilgreina SharePoint tengingu](e-invoicing-create-sharepoint-connection.md). |
    | Leynilykill forrits    | Færðu inn heiti á leynilykli lyklageymslunnar sem inniheldur aðgangsorð fyrir SharePoint notandareikninginn. Gildið er gildið fyrir **Leynilykil forritsskráningu** úr [Skilgreina SharePoint tengingu](e-invoicing-create-sharepoint-connection.md). |
    | Heiti vefsvæðis             | Færðu inn heiti SharePoint svæðisins. |
    | Heiti skjalasafns | Færðu inn heiti SharePoint skjalasafnsins. |
    | Tími útrunninn               | Færðu inn hámarkstíma, í millisekúndum (ms), sem kerfið á að bíða eftir svari. Sjálfgefið gildi er 10.000 ms (10 sekúndur). |
    | Aðalmappa           | Tilgreindu uppruna á innflutningi skráar eða möppuna sem þjónustan á að vinna úr skrám frá. |
    | Skjalasafnsmappa        | Tilgreindu möppuna þar sem á að geyma unnar skrár. |
    | Villumappa          | Tilgreindu möppuna sem kerfið ætti að færa skrár í ef vinnslan mistekst. |
    | Hámarksstærð skráar         | Sláðu inn hámarksstærð í bætum á einni skrá sem unnið er úr. Sjálfgefið gildi er 20.000.000 bæti. |
    | Hámarksfjöldi skráa      | Sláðu inn hámarksfjöldi skráa sem á að vinna úr fyrir eina aðgerð. Ef ekki á að takmarka fjölda skráa skal stilla gildið á **0** (núll). |
    | Skráarsía           | Færðu inn streng til að sía eftir skráarheiti. Þetta svæði er valkostur. Einföld sía eins og **\*smth\*.ext** er studd, þar sem hver stjarna (\*) táknar núll eða fleiri tilvik á einhverjum staf. Til dæmis er hægt að slá inn **\*.pdf** til að stilla rásina á að lesa PDF-skrár. |
    | Sérsniðið skráarheiti      | Færðu inn sérsniðið skráarheiti frá biðlaranum. |

10. Í flipanum **Gildissviðsreglur** skal fara yfir og uppfæra skilyrðið ef á þarf að halda. Gildið í reitnum **Rás** verður að jafngilda gildinu sem þú færðir inn í reitinn **Gagnarás** í fyrra skrefinu.
11. Veljið **Vista** og lokið skjámyndinni.
