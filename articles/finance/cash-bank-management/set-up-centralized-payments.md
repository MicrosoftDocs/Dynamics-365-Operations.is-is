---
title: Uppsetning miðstýrðra greiðslna
description: Fylgið eftirfarandi skrefum til að undirbúa vinnslu greiðslna í einu lögaðila fyrir hönd annars lögaðila í þínu fyrirtæki.
author: kweekley
manager: AnnBe
ms.date: 05/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: roschlom
ms.custom: 62243
ms.assetid: ffd17b5f-9aea-40e0-be49-d8702f615256
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b890b3bd8d88615b3e1846b10a0f3a06e29679cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208896"
---
# <a name="set-up-centralized-payments"></a>Uppsetning miðstýrðra greiðslna

[!include [banner](../includes/banner.md)]

Fylgið eftirfarandi skrefum til að undirbúa vinnslu greiðslna í einu lögaðila fyrir hönd annars lögaðila í þínu fyrirtæki. Áður en byrjað er verður að ljúka við eftirfarandi uppsetningu:

-   Stofna lögaðila
-   Setja upp færibreytur og Bókhaldslykil fyrir fjárhag
-   Setja upp færibreytur viðskiptaskuldir og færibreytur viðskiptakrafna (eftir einingum sem nota miðstýrðar greiðslur).
-   Setja upp bókhald innan samstæðu

## <a name="set-up-an-organizational-hierarchy-for-centralized-payments"></a>Setja upp stigveldi fyrirtækis fyrir miðstýrðar greiðslur
Setja verður upp stigveldi fyrirtækis fyrir miðstýrðar greiðslur. Sama stigveldi fyrirtækis er notað til að vinna miðstýrðar lánardrottnagreiðslur og miðstýrðar viðskiptavinagreiðslur. **Athugasemd** Skipulag stigveldisins er ekki mikilvægt fyrir miðstýrðar greiðslur. Allir lögaðilar geta unnið greiðslur fyrir hönd annars lögaðila í stigveldinu. Á **stigveldum fyrirtækja** síðu er hægt að stofna nýtt stigveldi fyrirtækis. Í reitnum **Tilgangur** verður að velja **Miðstýrðar greiðslur**. 

## <a name="set-up-an-intercompany-account-for-centralized-payments"></a>Setjið upp samstæðubókhald fyrir miðstýrðar greiðslur
Þegar greiðslufærslur í núverandi lögaðila er jafnað gagnvart reikningum í öðrum lögaðilum, skal stofna viðeigandi færslur á gjalddaga til og á gjalddaga frá fyrir hvern lögaðila. Tilgreina þarf lögaðila þar sem allar viðeigandi upphæðir staðgreiðsluafsláttar og allar raunupphæðir hagnaðar eða taps eru bókaðar. Áður en hafist er handa skal ákveða hvaða lögaðila á að nota til að vinna greiðslur viðskiptamanns og lánardrottins. Ef einn lögaðila vinnur lánardrottnagreiðslur en annan lögaðila vinnur viðskiptavinagreiðslur, verður að skipta yfir á hvern lögaðila. Á síðunni **samstæðubókhald** er hægt að velja vensl færsla innan samstæðu fyrir lögaðila sem á að vinna greiðslur fyrir. 

Á fliðanum **Miðstýrðar greiðslur** er hægt að velja hvort bóka á staðgreiðsluafslætti á lögaðila greiðslunnar (eða aðra færslu sem minnkar stöðu lánadrottinslykilsins) eða lögaðila reikningsins (eða aðra færslu sem eykur við stöðu lánadrottinslykils). Þetta val vinnur í samvinnu við **stýring staðgreiðsluafsláttar** á í **Færibreytur viðskiptaskulda** og **Færibreytur viðskiptakrafna** síður. Stilling lögaðila greiðslunnar er notuð fyrir ofgreiðslur og vikmörk á auramismun. Fyrir vangreiðslur og vikmörk á auramismun er stilling lögaðila reikningsins notuð.

## <a name="map-vendor-accounts-across-legal-entities"></a>Varpa lánadrottnalyklum á milli lögaðila
Ef þú greiðir lánadrottni úr einum lögaðila og vilt velja á reikning fyrir þann lánadrottinn hjá öðrum lögaðilum verður að tryggja að samsvarandi lánadrottnalyklar hjá hverjum lögaðila noti allir sama aðsetursbókarkenni. Ef þú tekur við greuslu frá viðskiptavini sem greiðir reikninga í fleiri en einum lögaðila, verður þú að tryggja að allir samsvarandi viðskiptavinalyklar hjá hverjum lögaðila noti allir sama aðsetursbókarkenni.

## <a name="set-up-posting-profiles-for-centralized-payments"></a>Setjið upp bókunarreglur fyrir miðstýrðar greiðslur
Þegar greiðsla er stofnuð fyrir einn lögaðila sem jafnar reikninga fyrir aðra lögaðila verður kenni bókunarreglu að vera hið sama fyrir báða lögaðila. Svo tryggt sé að greiðslur séu rétt stofnaðar þarf að setja upp bókunarreglu fyrir hvern reikning lögaðila sem samsvarar bókunarreglum í notkun hjá lögaðila greiðslunnar. Skipta yfir í fyrsta lögaðili reikningsins og síðan, á síðunni **Bókunarreglur lánardrottna** er hægt að stofna nýja bókunarreglu eða breyta fyrirliggjandi bókunarreglu. Kostirnir sem valdir eru fyrir bókunarreglu í lögaðila reikningsins þurfa ekki að samsvara uppsetningu bókunarreglunnar fyrir lögaðila greiðslunnar.

## <a name="set-up-methods-of-payment-for-centralized-payments"></a>Setjið upp greiðsluhætti fyrir miðstýrðar greiðslur
Þegar greiðsla er stofnuð fyrir einn lögaðila sem jafnar reikninga fyrir aðra lögaðila verður kenni greiðsluaðferða að vera hið sama fyrir báða lögaðila. Svo tryggt sé að greiðslur séu rétt stofnaðar þarf að setja upp greiðslumáta fyrir hvern reikning lögaðila sem samsvarar greiðslumáta í notkun hjá lögaðila greiðslunnar. Skipta yfir í fyrsta lögaðili reikningsins og síðan, á í **Greiðsluhættir** síðu er hægt að stofna nýjan greiðsluhátt eða breyta fyrirliggjandi greiðsluhátt. Kostirnir sem valdir eru fyrir greiðsluhátt lögaðila reikningsins þurfa ekki að samsvara því hvernig greiðsluhátturinn er settur upp fyrir lögaðila greiðslunnar.

## <a name="set-up-default-descriptions"></a>Setja upp sjálfgefnar lýsingar
Hægt er að skilgreina sjálfgefnar lýsingar fyrir fylgiskjöl samstæðujöfnunar. Sjálfgefna lýsingin er höfð með í færslunum á gjalddaga til og á gjalddaga frá á meðan á jöfnunarferlinu milli fyrirtækja stendur. Á **Sjálfgefnar lýsingar** síðu er hægt að stofna nýja lýsingar fyrir bæði **Samstæðujöfnun viðskiptavina** og **Samstæðujöfnun lánardrottna** með því að velja tungumál og færa síðan inn texta.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]