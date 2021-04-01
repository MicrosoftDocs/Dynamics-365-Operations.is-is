---
title: Eignamælingar
description: Umræðuefnið útskýrir hvernig á að stofna eignamælingar í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 41bedaaace09f632ca7506f504c3086a1dabf193
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217150"
---
# <a name="counters"></a>Teljarar

[!include [banner](../../includes/banner.md)]

Umræðuefnið útskýrir hvernig á að stofna teljaramælingar í eignastýringu. Gerðir teljaramælinga eru notaðar til að gera teljaraskráningar á eignir, til dæmis varðandi fjölda framleiðslutíma eða magn framleitt á eigninni. Tegundir eigna eru tengdar gerðum teljara. Þetta þýðir að einungis er hægt að nota teljara á eign ef teljarinn er sett upp á eignategundinni sem notuð er á eigninni.

Áður en þú getur gert teljaraskráningar á eignir þarf fyrst að stofna þær teljaragerðir sem þú vilt nota í **Teljarar**. Næst geturðu búið til teljaraskráningar á eignum í **Teljarar**. 

Hægt er að nota teljara í viðhaldsáætlunum. Viðhaldsáætlunarlína getur verið af gerðinni „Teljari“, til dæmis varðandi fjölda framleiðslutíma eða framleitt magn. 

Hægt er að uppfæra teljaraskráningu handvirkt eða sjálfkrafa út frá framleiðslutíma eða framleiddu magni. Hægt er að setja upp teljara til að nota eina af þremur uppfærsluaðferðum (valið í reitnum **Uppfæra** í **Teljarar**):
  
- Handvirkt - þú verður að skrá teljaragildi handvirkt.  
- Framleiðslutímar - teljarinn er sjálfkrafa uppfærður út frá fjölda framleiðslutíma.  
- Framleiðslumagn - teljarinn er sjálfkrafa uppfærður út frá framleiddu magni.  

>[!NOTE]
>Ef framleitt magn er notað eru *allir* skráðir hlutir með í teljaraskráningu, gott magn sem og villumagn. Það er alltaf mögulegt að gera handvirkar teljaraskráningar, ef þess þarf.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Búðu til gagnategundir fyrir skráningar eignateljara

1. Veldu **Eignastýring** > **Uppsetning** > **Eignagerðir** > **Teljarar**.
2. Veldu **Nýr** til að stofna nýja teljaragerð.
3. Settu inn auðkenni í reitinn **Teljari** og teljaraheiti í reitinn **Heiti**.
4. Á flýtiflipanum **Almennt** velurðu teljaraeiningu í reitnum **Eining**.
5. Í retinum **Uppfæra** velurðu uppfærsluaðferðina sem á að nota fyrir teljarann.
6. Veldu „Já“ á skiptihnappnum **Erfa teljaragildi** ef undireignir í eignaskipan ættu sjálfkrafa að erfa teljaraskráningar sem gerðar eru á yfireigninni.
7. Í retinum **Samtals samanlagt** velurðu samantektaraðferðina sem á að nota fyrir teljara með þessari teljaragerð. „Summa“ er staðalvalið sem notað er til að bæta skráðum gildi stöðugt við heildargildið. Hægt er að nota „meðaltal“ ef teljari er settur upp til að fylgjast með þröskuldi, til dæmis varðandi hitastig, titring eða slit á eign. 
8. Í reitnum **Frávik yfir** seturðu efra stigið inn í prósentu til að sannprófa hvort handvirkar teljaraskráningar séu innan áætlaðs sviðs. Sannprófunin er byggð á línulegri aukningu á núverandi teljaraskráningum.
9. Í reitnum **Frávik undir** seturðu neðra stigið inn í prósentu til að sannprófa hvort handvirkar teljaraskráningar séu innan áætlaðs sviðs. Sannprófunin er byggð á línulegri lækkun á núverandi teljaraskráningum.
10. Í reitnum **Tegund** velurðu gerð skilaboðanna (upplýsingar, viðvörun, villu) sem á að sýna ef frávik utan skilgreinds sviðs eiga sér stað þegar þú gerir handvirkar teljaraskráningar.
11. Á flýtiflipanum **Eignagerðir** bætirðu við eignagerðum sem ættu að geta notað teljarann.
12. Á flýtiflipanum **Tengdir eignateljarar** bætirðu við teljaranum sem þú vilt að uppfærist sjálfkrafa þegar þessi teljari er uppfærður.


>[!NOTE]
>Tengdur teljari er sjálfkrafa uppfærður ef viðkomandi teljari hefur eignagerðina sem hún er tengd við í teljarauppsetningunni. Til dæmis: Þú setur upp teljara fyrir „Framleiðslutíma“ og bætir við eignategundinni „Truck Engine“. Þegar sá teljari er uppfærður er tengdur teljari „Olía“ einnig uppfærður með sömu teljaragildum. Uppsetningin í **Teljendur** felur í sér uppsetningu á „Klukkutímum“. Einnig, í teljaranum „Olía“ ætti að bæta eignagerðinni „Truck Engine“ við á flýtiflipanum **Eignagerðir** til að tryggja teljaratengsl. Sjá skjámyndirnar hér að neðan til að sjá dæmi um skipulag á teljurunum Tímar og Olía.

Þegar eignagerðum er bætt við í teljaragerð í **Teljarar** er þeim teljara sjálfvirkt bætt við eignagerðirnar á flýtiflipanum **Teljarar** í [Eignagerðir](../setup-for-objects/object-types.md).

![Mynd 1](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]