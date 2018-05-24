---
title: "Fjölpantanir viðskiptavinar"
description: "Fjölpöntun viðskiptavinar er stök pöntun, sem inniheldur vörur sem viðskiptavinur getur haft með sér úr verslun, sem og vörur sem verða sóttar eða sendar síðar."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 88d12641fa05953f7082158303237b7ba40c3fe2
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="hybrid-customer-orders"></a>Fjölpantanir viðskiptavinar

[!include [banner](includes/banner.md)]

Fjölpöntun viðskiptavinar er stök pöntun, sem inniheldur vörur sem viðskiptavinur getur haft með sér úr verslun, sem og vörur sem verða sóttar eða sendar síðar.

Í Microsoft Dynamics 365 for Retail geturðu annað vort valið að fara út með allar vörur eða fara út með valdar vörur fyrir pöntun viðskiptavinar. Vörulínur sem eru merktar sem fara með út eru reikningsfærðar sjálfkrafa eftir að pöntun er stofnuð, það sama er gert fyrir pöntun sem á að sækja eftir að pöntun er stofnuð. Upphæð til greiðslu fyrir fjölpöntun er ákvörðuð með því að bæta prósentu innborgunar á sækja og senda vörulínum við heildarupphæð lína sem á að fara með út. Fyrir fjölpantanir skiptir kerfið á milli stillingar fyrir pöntun viðskiptavinar og stillingar fyrir staðgreitt fyrir afhendingu sem hér segir:

-   Ef allar vörur í körfu eru stilltar á **Framkvæma afhending**, verður pöntun afgreidd sem Staðgreitt við afhendingu.
-   Ef allar vörur í karfa eru stilltar á annað hvort **Taka til** eða **senda afhendingu**,, verður pöntun afgreidd sem færsla á pöntun viðskiptavinar.

Ef körfulína er valin og **Taka til er valið**, **Senda er valið**, eða **Framkvæma er valið** er valið verðu aðeins tilgreind körfulína stillt á þá afhendingaraðferð. Í því tilviki heldur niðurflæði aðgerðarinnar áfram eins og venjulega. Ef hins vegar **Taka til valinn**, **Afgreiða Valið: ,**, eða **Framkvæma Valið: ,** er Valið án þess að körfulína sé valin opnast ný síða með lista yfir allar körfulínur. Á þeirri skjámynd er hægt að velja margar línur samtímis til að stilla afhendingaraðferð. Þegar þú notar þá aðferð fyrir línuval verða allar fyrri afhendingaraðferðir sem hefur verið úthlutað á línuna hnekkt.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Yfirlit pantana viðskiptavina](customer-orders-overview.md)




