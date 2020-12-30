---
title: Stofna úthýstan vinnuflokk fyrir lean-framleiðslu
description: Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bc1e8551bbebd11cad18d47f9e74a2dedcb908d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430045"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a>Stofna úthýstan vinnuflokk fyrir lean-framleiðslu

[!include [banner](../../includes/banner.md)]

Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna. Vinnuflokkur í undirverktöku tengist lánardrottninum í gegnum vensl við tilföng af gerð lánardrottins. Ef þú spilar þessa upptöku í USMF sýnifyrirtækinu, geturðu valið kenni lánardrottnalykils 1002 og svæði 1.


## <a name="create-a-vendor-resource"></a>Stofna tilfang lánardrottins
1. Fara á tilföng
2. Smellið á „Nýtt“.
3. Í reitinn Tilfang skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum Tegund skal velja „lánardrottinn“.
6. Í reitnum lánardrottinn skal smella á fellilistahnappinn til að opna leitina.

## <a name="create-the-resource-group"></a>Stofna tilfangaflokk
1. Fara á tilfangaflokkur
2. Smellið á „Nýtt“.
3. Færa inn gildi í svæðið tilfangaflokkur.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
    * Veldu svæðið sem vinnuflokkinum ætti að vera úthlutað til. Svæði getur, fræðilega séð, táknað stakt svæði sem er starfrækt af lánardrottni. Í flestum tilfellum eru tilföng undirverktaka hins vegar úthlutað til svæðisins sem pantar vinnu í undirverktöku. Athugið að inntaks og úttaks vöruhúsin fyrir undirverktaka vinnuflokka verða að vera á sama svæðinu.  
6. Í reitinn Svæði skal slá inn gildi.
7. @SysTaskRecorder:_RequestClose
8. Velja eða hreinsa gátreitinn vinnuflokkur.
9. Í reitnum inntaksvöruhús skal smella á fellilistahnappinn til að opna leitina.
    * Veljið vöruhúsið og staðsetninguna sem eru notuð til að skipuleggja efni fyrir vinnuflokkana, sem stjórnað er af lánardrottni. Í mörgum tilfellum er vöruhúsið og staðsetningin gerð með því að nota mismunandi vöruhús fyrir hvern lánardrottinn og eina staðsetningu fyrir hvern vinnuflokk.  
10. Í reitnum inntaksstaðsetning skal smella á fellilistahnappinn til að opna leitina.
11. Í reitnum úttaksvöruhús skal smella á fellilistahnappinn til að opna leitina.
    * Skilgreinið vöruhúsið og staðsetningu þar sem efnið er bókað þegar verkþættir undirverktaka í vinnuflokki eru bókaðir. Vöruhús og staðsetning geta verið á svæði lánardrottins ef lánardrottinn skráir kanban-vinnsluna. Að öðrum kosti geta vöruhúsið og staðsetningin verið staðsetningin sem tekur við og er tengd við næsta skref framleiðsluflæðisins.  
12. Í reitnum úttaks staðsetning skal smella á fellilistahnappinn til að opna leitina.
13. Útvíkka eða draga saman hlutann dagatal.
14. Smelltu á Bæta við.
15. Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.
    * Tengja vinnutímadagatal vinnuflokksins við tilfangaflokkinn. Fyrir mikilvæg tilföng, mælum við með að þú skilgreinir sérstök dagatöl sem sýna nákvæma tölu vinnutíma og skyldra afkasta vinnuflokksins eða svæði lánardrottins.  
16. Stækka eða fella saman hlutann Tilföng
17. Smelltu á Bæta við.
    * Tilfangaflokkur í undirverktöku verður að hafa tengd tilföng af gerð lánardrottins sem tengir tilfangaflokkinn við lánardrottnalykil.  
18. Í reitnum Tilföng skal smella á fellilistahnappinn til að opna leitina.
    * Smella á eða fara inn á tilföng lánardrottins sem voru stofnuð í síðasta undirverkefni.  
19. Útvíkka eða draga saman hluta afkastageta vinnuflokks.
20. Smelltu á Bæta við.
    * Vinnuflokkur verður að hafa skilgreinda afkastagetu. Í þessu dæmi, sköpum við gegnstreymi afkasta upp á 100 stykki fyrir venjulegan vinnudag.  
21. Í reitnum líkan framleiðsluflæðis skal smella á fellilistahnappinn til að opna leitina.
22. Í svæðinu tímabil Afkastageta skal velja valkost.
23. Færið inn tölu í svæðið Meðaltal gegnumstreymi magn.
24. Í reitnum Eining skal smella á fellilistahnappinn til að opna leitina.
25. Leysa breytir Einingu.

