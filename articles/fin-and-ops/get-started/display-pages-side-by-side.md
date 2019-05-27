---
title: Birta síður hlið við hlið með því að nota „Opna í nýjum glugga“-eiginleikann
description: Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið í Microsoft Dynamics 365 for Finance and Operations.
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df9b091735a4971446c5b5d0e054076260040683
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558953"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a>Birta síður hlið við hlið með því að nota „Opna í nýjum glugga“-eiginleikann

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig eigi að birta síður hlið við hlið í Microsoft Dynamics 365 for Finance and Operations.

Microsoft Dynamics 365 for Finance and Operations hjálpar til við að framkvæma aðgerðir á hagkvæman hátt. Í sumum tilfellum gætirðu viljað skoða mörg síður hlið við hlið til að ljúka verkefnum hratt. Sem dæmi, gæti verið óskað að villuleita eða færa inn línur í fleiri en einni færslubók. Venjulega til að gera þetta þyrfti að fara fram og til baka milli síðunnar sem sýnir lista yfir færslubækur og síðuna sem sýnir línur í tiltekna færslubók. Hins vegar **Opna í nýjum glugga** eiginleikinn gerir kleift að sýna þessar síður hlið við hlið þannig að hægt er að framkvæma verkefnunum fljótt.

Haldið er áfram með fyrrgreint dæmi hér fyrir ofan þegar verið er að skoða línurnar með því að smella á **Opna í nýjum glugga** tákn.

[![tákn til að opna í nýjum glugga](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)

Smella á **Opna í nýjum glugga** táknið opnar línusíðuna í nýja, vafra sem sprettur upp og flettir síðan í upprunalega vafra til baka í sögunni á síðuna sem birti lista yfir færslubækur. Hægt er að birta síðan báðar síðurnar hlið við hlið. Þegar búið er að skoðuð færslubók er hægt að breyta valinni færslubók á listasíðu færslubókar, og línusíður í sprettiglugga birta sjálfkrafa línur í nýlega valinnar færslubókar.

[![síður birtast hlið við hlið](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)

Gagnvirk tengingu og endurnýjun gerist vegna vensl sem eru til staðar á milli gagna sem hafa tekið Gert öryggisafrit af þessar síður. Ef kerfið er ekki kunnugt um tengsl milli gagna, sprettiglugga mun ekki endurnýjast sjálfkrafa til að bregðast við breytingum í glugganum sem það er upprunnið frá.

Sumar síður eru með mörgum yfirlitum eins og hnitanetsyfirlit, hausyfirlit og upplýsingayfirlit. **Opna í nýjum glugga** táknið veldur því að öll síðu opnast í nýjan vafraglugga. Þess vegna er hægt að halda tvö yfirlit yfir sömu síðu hlið við hlið með því að nota **Opna í nýjum glugga** eiginleika. Hins vegar nánast allar slíkar síður hafa flettingarlista sem þú getur notað til að skipta á milli skráa og ná fram svipaðri upplifun.

Áður **Opna í nýjum glugga** aðgerðina er notuð ætti að skilgreina sprettigluggavörn vafrans til að leyfa sprettiglugga úr SLÓÐ svæðisins Dynamics 365 for Finance and Operations. Sem dæmi, mætti heimila sprettiglugga úr "\*. dynamics.com".

**Opna í nýjum glugga** eiginleiki er aðeins tiltækur þegar fleiri en einn síða er opna í glugganum. Einnig sprettiglugga sjálfkrafa lokast þegar engar frekari síður eru opnar (þar er, þegar síðustu síðuna í glugganum er lokað). Finance and Operations lokar einnig opnum síðum þegar farið er á annað svæði í forritinu. Þess vegna ef sprettuglugga eru opnir og farið er  í annað svæði í forritinu, er sprettuglugga sjálfkrafa lokað því síðurnar í þeim gluggum var lokað af kerfinu.

Efsta sláin í sprettiglugga birtir upplýsingar um fyrirtækið sem síðuna var opnuð í og er skrifvarin. Sprettugluggar treysta á aðal vafraglugga Finance and Operations. Ef aðalglugginn er lokaður eða endurnýjuð, allar opnar sprettuglugga mun verða eingöngu lesaðgangur. Þetta þýðir að er hægt að skoða upplýsingarnar í þessum gluggum, en er ekki hægt að eiga samskipti við þá.
