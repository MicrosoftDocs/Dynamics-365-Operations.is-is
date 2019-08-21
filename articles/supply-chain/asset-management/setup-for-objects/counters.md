---
title: Eignamælingar
description: Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783357"
---
# <a name="asset-measures"></a>Eignamælingar

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu. Gerðir eignamælinga eru notaðar til að skrá mælingar á eignir, til dæmis varðandi fjölda framleiðslutíma eða magn framleitt á eigninni. Tegundir eigna eru tengdar tegundum eignamats. Þetta þýðir að einungis er hægt að nota eignamæli á eign ef eignamælingin er sett upp á eignategundinni sem notuð er á eigninni.

Áður en þú getur gert skráningar á eignir þarf fyrst að stofna þær tegundir eigna sem þú vilt nota í **Teljendur**. Næst geturðu búið til skráningar á eignum í **Eignamælingar**. 

Hægt er að nota eignir í viðhaldsáætlunum. Viðhaldsáætlunarlína getur verið af gerðinni „Teljari“, til dæmis varðandi fjölda framleiðslutíma eða framleitt magn. 

Hægt er að uppfæra eignamælingaskráningu handvirkt eða sjálfkrafa út frá framleiðslutíma eða framleiddu magni. Hægt er að setja upp eignamæli til að nota eina af þremur uppfærsluaðferðum (valið í reitnum **Uppfæra** í **Teljendur**):
  
- Handvirkt - þú verður að skrá eignamælingargildi handvirkt.  
- Framleiðslutímar - teljarinn er sjálfkrafa uppfærður út frá fjölda framleiðslutíma.  
- Framleiðslumagn - teljarinn er sjálfkrafa uppfærður út frá framleiddu magni.  

>[!NOTE]
>Ef framleitt magn er notað eru *allir* skráðir hlutir með í mælingaskráningu, gott magn sem og villumagn. Það er alltaf mögulegt að gera handvirkar skráningar á eignamati, ef þess þarf.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Búðu til gagnategundir fyrir skráningar eignateljara

1. Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**.
2. Veldu **Nýr** til að stofna nýja gerð eignamælingar.
3. Settu inn auðkenni í reitinn **Teljari** og teljaraheiti í reitinn **Heiti**.
4. Á flýtiflipanum **Almennt** velurðu mælieiningu í reitnum **Eining**.
5. Í retinum **Uppfæra** velurðu uppfærsluaðferðina sem á að nota fyrir eignamælinguna.
6. Veldu „Já“ á skiptihnappnum **Erfa teljaragildi** ef undireignir í eignaskipan ættu sjálfkrafa að erfa eignamælingarskráningar sem gerðar eru á yfireigninni.
7. Í retinum **Samtals samanlagt** velurðu samantektaraðferðina sem á að nota fyrir eignamælingu með þessari eignamælingargerð. „Summa“ er staðalvalið sem notað er til að bæta skráðum gildi stöðugt við heildargildið. Hægt er að nota „meðaltal“ ef eignamæling er sett upp til að fylgjast með þröskuldi, til dæmis varðandi hitastig, titring eða slit á eign. 
8. Í reitnum **Frávik yfir** seturðu efra stigið inn í prósentu til að sannprófa hvort handvirkar eignaskráningar séu innan áætlaðs sviðs. Sannprófunin er byggð á línulegri aukningu á núverandi eignamælingaskráningum.
9. Í reitnum **Frávik undir** seturðu neðra stigið inn í prósentu til að sannprófa hvort handvirkar eignaskráningar séu innan áætlaðs sviðs. Sannprófunin er byggð á línulegri lækkun á núverandi eignamælingaskráningum.
10. Í reitnum **Tegund** velurðu gerð skilaboðanna (upplýsingar, viðvörun, villu) sem á að sýna ef frávik utan skilgreinds sviðs eiga sér stað þegar þú gerir handvirkar skráningar á eignamati.
11. Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að geta notað eignamælinguna.
12. Á flýtiflipanum **Tengdar eignamælingar** bætirðu við eignamælingunum sem þú vilt að uppfærist sjálfkrafa þegar þessi eignamæling er uppfærð.


>[!NOTE]
>Tengd eignamæling er sjálfkrafa uppfærð ef viðkomandi eignamæling hefur eignagerðina sem hún er tengd við í uppsetningu eignaáætlunarinnar. Til dæmis: Þú setur upp eignamælikvarða fyrir „Framleiðslutíma“ og bætir við eignategundinni „Truck Engine“. Þegar sú eignamæling er uppfærð er tengdur teljari „Olía“ einnig uppfærður með sömu eignamælingargildum. Uppsetningin í **Teljendur** felur í sér uppsetningu á „Klukkutímum“. Einnig, í eignamælingunni „Olía“ ætti að bæta eignagerðinni „Truck Engine“ við á flýtiflipanum **Eignagerðir** til að tryggja tengsl eignamælingar. Sjá skjámyndirnar hér að neðan til að sjá dæmi um skipulag á eignamælingunum Tímar og Olía.

Þegar eignagerðum er bætt við í eignamælingagerð í **Teljarar** er þeirri eignamælingu sjálfvirkt bætt við eignagerðirnar á flýtiflipanum **Teljarar** í [Eignagerðir](../setup-for-objects/object-types.md).

![Mynd 1](media/071-setup-for-objects.png)


