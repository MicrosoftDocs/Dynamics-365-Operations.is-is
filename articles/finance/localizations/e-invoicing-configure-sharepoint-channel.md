---
title: Skilgreina SharePoint-rás
description: Þessi grein útskýrir hvernig á að stilla Microsoft SharePoint rás til að vinna úr innkomnum rafrænum reikningum.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272305"
---
# <a name="configure-a-sharepoint-channel"></a>Skilgreina SharePoint-rás

[!include [banner](../includes/banner.md)]

Sem forsenda þess að hægt sé að stilla Microsoft SharePoint rás til að vinna úr mótteknum skjölum skaltu ljúka skrefunum sem lýst er sem lýst er í [Stilla a SharePoint Tenging](e-invoicing-create-sharepoint-connection.md).

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
    | Heiti vefsvæðis             | Sláðu inn nafnið á SharePoint síða. |
    | Heiti skjalasafns | Sláðu inn nafnið á SharePoint skjalasafn. |
    | Tími útrunninn               | Sláðu inn hámarkstíma, í millisekúndum (ms), sem kerfið ætti að bíða eftir svari. Sjálfgefið gildi er 10.000 ms (10 sekúndur). |
    | Aðalmappa           | Tilgreindu uppruna skráainnflutnings eða möppuna sem þjónustan ætti að vinna úr skrám. |
    | Skjalasafnsmappa        | Tilgreindu möppuna þar sem unnar skrár á að geyma. |
    | Villumappa          | Tilgreindu möppuna sem kerfið á að flytja skrár í ef vinnslan mistekst. |
    | Hámarksstærð skráar         | Sláðu inn hámarksstærð, í bætum, á einni skrá sem er unnin. Sjálfgefið gildi er 20,000,000 bæti. |
    | Hámarksfjöldi skráa      | Sláðu inn hámarksfjölda skráa til að vinna úr fyrir eina aðgerð. Ef þú vilt ekki takmarka fjölda skráa skaltu stilla gildið á **0** (núll). |
    | Skráarsía           | Sláðu inn streng til að sía eftir skráarnafni. Þessi reitur er valfrjáls. Einfaldur maski eins og **\* smth\* .ext** er stutt, þar sem hver stjörnu (\*) táknar núll eða fleiri tilvik af hvaða staf sem er. Til dæmis, slá inn **\* .pdf** til að stilla rásina til að lesa PDF skjöl. |
    | Sérsniðið skráarheiti      | Sláðu inn sérsniðið skráarheiti frá viðskiptavininum. |

10. Á **Gildisreglur** flipa, endurskoða og uppfæra viðmiðin eftir þörfum. Verðmæti **Rás** reiturinn verður að jafngilda gildinu sem þú slóst inn í **Gagnarás** reit í fyrra skrefi.
11. Veljið **Vista** og lokið skjámyndinni.
