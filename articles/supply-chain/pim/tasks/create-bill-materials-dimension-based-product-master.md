---
title: Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum
description: Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffe30f1b5aae3e954b527e84648f4dbb4b181513
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986905"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum

[!include [banner](../../includes/banner.md)]

Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum. Fyrstu 4 skráningar settu upp gögn sem þarf til að ljúka þessu ferli. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta verk er yfirleitt í höndum hönnuðar afurðar.


## <a name="select-the-product"></a>Velja afurð
1. Smellið á Viðhald útgefinnar afurðar.
2. Smella á Útgefnar afurðir.
3. Í listanum skal merkja valda línu.
    * Finna útgefin afurðarsniðmát með tækni fyrir víddaskilgreiningu sem var stofnaður í fyrsta leiðarvísi í þessari röð.  
4. Smellið á tæknifræðingur á aðgerðarúðunni.
5. Smellt er á uppskriftarútgáfur.

## <a name="create-new-bom-and-bom-version"></a>Stofna nýja uppskrift og uppskriftarútgáfu.
1. Smellið á „Nýtt“.
2. Smellt er á uppskrift og uppskriftarútgáfa
3. Í reitinn Heiti skal slá inn gildi.
    * Stillingar svæðis  
    * Í þessu ferli stillum við ekki inn tiltekið svæði fyrir Uppskriftina.  
4. Smellið á „Í lagi“.
5. Smellið á „Nýtt“.
    * Í þessu ferli er bætt við fjórar línur við Uppskrift. Tvær línur sýna valkosti fyrir kapal og tvær línur sýna valkosti fyrir geymslu.  
6. Í listanum skal merkja valda línu.
7. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Velja vörunúmer A0001, HDMI 6' Cables.  
8. Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.
    * Veljið afbrigðisflokk Kapla sem stofnuð var í handbók 4 í þessari röð.  
9. Smellið á „Nýtt“.
    * Velja vörunúmer A0002, HDMI 12' Cables.  
10. Í listanum skal merkja valda línu.
11. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
12. Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.
    * Velja aftur Afbirgðaflokkur kapla.  
13. Smellið á „Nýtt“.
14. Í listanum skal merkja valda línu.
15. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Velja vörunúmer D0002 Cabinet.  
16. Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.
    * Veljið afbrigðaflokki Cabinet fyrir þessa uppskriftarlínu.  
17. Smellið á „Nýtt“.
18. Í listanum skal merkja valda línu.
19. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Veljið vörunúmer M0007 StandardCabinet sem síðustu uppskriftarlínu.  
20. Sláið inn eða veldu gildi í reitnum afbrigðisflokkur.
    * Veljið afbrigðaflokki Cabinet fyrir síðustu uppskriftarlínu.  

## <a name="approve-and-activate"></a>Samþykkja og virkja
1. Lokið síðunni.
2. Smellið á Samþykkja.
3. Sláið inn eða veldu gildi í reitnum samþykki eftir.
4. Veldu já í viltu einnig að samþykkja uppskriftina? reitur.
5. Smellið á „Í lagi“.
6. Smellið á Virkja.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]