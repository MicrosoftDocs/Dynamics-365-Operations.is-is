---
title: Uppsetning rafrænnar reikningsfærslu
description: Þessi grein inniheldur yfirlit yfir ferlið við uppsetningu og skilgreiningu rafrænnar reikningsfærslu.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272180"
---
# <a name="electronic-invoicing-setup"></a>Uppsetning rafrænnar reikningsfærslu

[!include [banner](../includes/banner.md)]

Þessi grein inniheldur yfirlit yfir ferlið til að setja upp og skilgreina rafræna reikningsfærslu. Þú verður að ljúka uppsetningunni í þeirri röð sem tilgreind er hér. Ef skref er áskilið, en þú sleppir því, virkar virknin ekki rétt og margar bilanir munu eiga sér stað í næstu skrefum eða þegar þú notar virknina. 

Áður en þú hefst handa skaltu ganga úr skugga um að allir helstu þættir séu rétt uppsettir, að þú hafir skráð þig fyrir Regulatory Configuration Service (RCS) og sért með tilvik af RCS og að innbót rafrænnar reikningsfærslu sé uppsett fyrir Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management umhverfið. Frekari upplýsingar er að finna í [Innskrá og setja upp rafræna reikningsfærslu](e-invoicing-install-add-in-microservices-lcs.md).

Næst skaltu setja upp Azure-tilföng sem rafræn reikningsfærsla krefst til að geta sinnt vinnu sinni. Frekari upplýsingar er að finna í [Setja upp Azure-tilföng fyrir rafræna reikningsfærslu](e-invoicing-set-up-azure-resources.md).

Eftir að helstu þættir hafa verið skilgreindir skal vinna með RCS til að setja upp helstu rökréttu þætti rafrænnar reikningsfærslu. Fyrst skal skilgreina fjölda þjónustuumhverfa sem þú munt viðhalda. Þannig skilgreinir þú rökrétt gögn og hlutfallsskiptingar skilgreiningar til að tryggja að þú sért með mörk á milli þróunar- og prófunarumhverfis og framleiðsluumhverfa. Til að setja upp þróunarferlið þitt á sveigjanlegan hátt gætir þú þurft nokkur aðskilin þróunar- og prófunarumhverfi. Auk þess að skilgreina þjónustuumhverfi skaltu setja upp tengil á viðskiptaforritin þín, t.d. Finance eða Supply Chain Management, beint frá RCS til að setja upp færibreytur sem eru nauðsynlegar fyrir rétta framkvæmd með rafrænni reikningsfærslu. Frekari upplýsingar um umhverfin er að finna í [Þjónustuumhverfi](e-invoicing-service-environments.md).

Þegar allt hefur verið sett upp geturðu búið til þína eigin altæku eiginleika sem skilgreina mismunandi aðstæður fyrir vinnslu rafrænna skjala og umbreytingu gagna eða fyrir innflutning skjalanna úr altæku geymslunni. Frekari upplýsingar um hvernig á að vinna með altæka eiginleika er að finna í [Vinna með altæka eiginleika](e-invoicing-working-globalization-features.md).

Ef aðstæður þínar krefjast samþættingar við tölvupóst eða SharePoint til að vinna úr rafrænum skjölum á innleið skal skoða [Að vinna úr mótteknum rafrænum skjölum](e-invoicing-process-incoming-electronic-documents.md) fyrir upplýsingar um hvernig á að setja upp og nota þessar rásir.
