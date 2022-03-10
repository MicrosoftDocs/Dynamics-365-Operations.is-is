---
title: Stilla a SharePoint rás
description: Þetta efni útskýrir hvernig á að stilla Microsoft SharePoint rás til að vinna úr innkomnum rafrænum reikningum.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ea3e14ed00b0661d3923c1839135378a8a550499
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371952"
---
# <a name="configure-a-sharepoint-channel"></a>Stilla a SharePoint rás

[!include [banner](../includes/banner.md)]

Sem forsenda þess að hægt sé að stilla Microsoft SharePoint rás til að vinna úr skjölum sem berast, kláraðu skrefin sem lýst er í [Stilla a SharePoint Tenging](e-invoicing-create-sharepoint-connection.md).

Þú getur þá notað SharePoint rás til að flytja inn rafræna reikninga söluaðila úr skrám sem eru geymdar í þínum SharePoint möppur.

1. Á þínu SharePoint síðu, búðu til eftirfarandi möppur:

    - **Aðal mappa** – Mappan sem þjónustan mun vinna úr skrám.
    - **Skjalasafnsmappa** - Mappan þar sem unnar skrár verða geymdar.
    - **Villa mappa** – Mappan sem kerfið mun flytja skrár í ef vinnslan mistekst.

2. Í Regulatory Configuration Service (RCS) skaltu velja eiginleikann Rafræn reikningagerð sem þú bjóst til. Gakktu úr skugga um að þú veljir útgáfuna sem hefur stöðuna **Drög**.
3. Á **Uppsetningar** flipa, veldu **Bæta við**.
4. Í **Búðu til eiginleikauppsetningu** fellivalmynd, í **Nýtt** reitahópur, veldu **Sérsniðin uppsetning** valmöguleika.
5. Í **Gerð uppsetningar** reitahópur, veldu **Gagnarás** valmöguleika.
6. Í **Veldu gagnarás** reit, veldu **SharePoint möppu**.
7. Velja **Stofna**.
8. Veldu línuna sem þú bjóst til og veldu síðan **Breyta**.
9. Á **Gagnarás** flipa, í **Færibreytur** kafla, stilltu eftirfarandi nauðsynlega reiti.

    | Reitur                 | Lýsing |
    |-----------------------|-------------|
    | Gagnarás          | Sláðu inn einstakt nafn til að auðkenna gagnarásina. Nafnið má að hámarki vera 10 stafir. Það verður vísað til þess í gildandi reglum og í tengdum forritum meðan á samskiptaferlinu stendur. |
    | SharePoint-veffang    | Sláðu inn SharePoint URL. Til dæmis er slegið inn `<domain>.sharepoint.com`. |
    | Auðkenni umsóknar        | Sláðu inn nafn Azure Key Vault leyndarmálsins sem inniheldur auðkenni SharePoint notandareikningur. Þetta leyndarmál verður að búa til í Key Vault og setja upp í þjónustuumhverfi þínu. Gildið er **Auðkenni umsóknar (viðskiptavinar).** verðmæti frá [Stilla SharePoint Tenging](e-invoicing-create-sharepoint-connection.md). |
    | Leynilykill forrits    | Sláðu inn nafn Key Vault leyndarmálsins sem inniheldur lykilorðið fyrir SharePoint notandareikningur. Gildið er **App Skráning leyndarmál** verðmæti frá [Stilla SharePoint Tenging](e-invoicing-create-sharepoint-connection.md). |
    | Heiti svæðis             | Sláðu inn nafnið á SharePoint síða. |
    | Heiti skjalasafns | Sláðu inn nafnið á SharePoint skjalasafn. |
    | Tímalokun               | Sláðu inn hámarkstíma, í millisekúndum (ms), sem kerfið ætti að bíða eftir svari. Sjálfgefið gildi er 10.000 ms (10 sekúndur). |
    | Aðalmappa           | Tilgreindu uppruna skráainnflutnings eða möppuna sem þjónustan ætti að vinna úr skrám. |
    | Skjalasafnsmappa        | Tilgreindu möppuna þar sem unnar skrár á að geyma. |
    | Villumappa          | Tilgreindu möppuna sem kerfið á að flytja skrár í ef vinnslan mistekst. |
    | Hámarksstærð skráar         | Sláðu inn hámarksstærð, í bætum, á einni skrá sem er unnin. Sjálfgefið gildi er 20,000,000 bæti. |
    | Hámarksfjöldi skráa      | Sláðu inn hámarksfjölda skráa til að vinna úr fyrir eina aðgerð. Ef þú vilt ekki takmarka fjölda skráa skaltu stilla gildið á **0** (núll). |
    | Skráarsía           | Sláðu inn streng til að sía eftir skráarnafni. Þessi reitur er valfrjáls. Einfaldur maski eins og **\* smth\* .ext** er stutt, þar sem hver stjörnu (\*) táknar núll eða fleiri tilvik af hvaða staf sem er. Til dæmis, slá inn **\* .pdf** til að stilla rásina til að lesa PDF skjöl. |
    | Sérsniðið skráarheiti      | Sláðu inn sérsniðið skráarheiti frá viðskiptavininum. |

10. Á **Gildisreglur** flipa, endurskoða og uppfæra viðmiðin eftir þörfum. Verðmæti **Rás** reiturinn verður að jafngilda gildinu sem þú slóst inn í **Gagnarás** reit í fyrra skrefi.
11. Veljið **Vista** og lokið skjámyndinni.
