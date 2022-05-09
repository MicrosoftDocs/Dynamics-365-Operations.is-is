---
title: Uppsetning rafrænna reikninga
description: Þetta efnisatriði veitir yfirlit yfir ferlið við að setja upp og stilla rafræna reikningagerð.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 42e617e26e7658fae9ee54cb8a4dee45314fddaa
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661693"
---
# <a name="electronic-invoicing-setup"></a>Uppsetning rafrænna reikninga

[!include [banner](../includes/banner.md)]

Efnið veitir yfirlit yfir ferlið við að setja upp og stilla rafræna reikningagerð. Þú verður að ljúka uppsetningarskrefunum í þeirri röð sem tilgreind er hér. Ef skref er skylt, en þú sleppir því, mun virknin ekki virka rétt og margar bilanir eiga sér stað í síðari skrefum eða þegar þú notar virknina. 

Áður en þú byrjar skaltu ganga úr skugga um að allir aðalhlutar séu rétt settir upp, að þú hafir skráð þig í Regulatory Configuration Service (RCS) og sét með tilvik af RCS og að rafræn reikningsviðbót sé sett upp fyrir Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management umhverfi. Fyrir frekari upplýsingar, sjá [Skráðu þig og settu upp rafræna reikninga](e-invoicing-install-add-in-microservices-lcs.md).

Næst skaltu setja upp Azure tilföngin sem rafræn reikningagerð krefst til að vinna sína vinnu. Fyrir frekari upplýsingar, sjá [Settu upp Azure tilföng fyrir rafræna reikningagerð](e-invoicing-set-up-azure-resources.md).

Eftir að aðalhlutirnir hafa verið stilltir skaltu vinna með RCS til að setja upp helstu rökréttu íhluti rafrænnar reikninga. Fyrst skaltu tilgreina fjölda þjónustuumhverfa sem þú munt viðhalda. Á þennan hátt skilgreinir þú rökrænu gögnin og stillingarskiptingu til að tryggja að þú hafir mörk á milli þróunar- eða prófunarumhverfis og framleiðsluumhverfisins. Til að setja upp þróunarferlið þitt á sveigjanlegan hátt gætir þú þurft nokkur aðskilin þróunar- og prófunarumhverfi. Auk þess að skilgreina þjónustuumhverfi skaltu setja tengil á viðskiptaforritin þín, svo sem fjármál eða framboðsstjórnun, beint frá RCS til að setja upp þær breytur sem eru nauðsynlegar fyrir réttan rekstur með rafrænum reikningum. Fyrir frekari upplýsingar um umhverfi, sjá [Þjónustuumhverfi](e-invoicing-service-environments.md).

Eftir að allt hefur verið sett upp geturðu búið til þína eigin hnattvæðingareiginleika sem skilgreina mismunandi aðstæður til að vinna rafræn skjöl og umbreyta gögnum, eða til að flytja inn skjölin úr alþjóðlegu geymslunni. Fyrir frekari upplýsingar um hvernig á að vinna með hnattvæðingareiginleika, sjá [Vinna með hnattvæðingareiginleika](e-invoicing-working-globalization-features.md).

Ef aðstæður þínar krefjast samþættingar við tölvupóst eða SharePoint að vinna rafræn skjöl á innleið, sbr [Vinnsla rafrænna skjala sem berast](e-invoicing-process-incoming-electronic-documents.md) til að fá upplýsingar um hvernig eigi að setja upp og nota þessar rásir.
