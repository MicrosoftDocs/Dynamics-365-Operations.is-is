---
title: Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum
description: Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86625821f8a01a6d4949f9dca538a279f52ce9c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565589"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a>Stofnun farmbréf fyrir afurðarsniðmát byggt á víddum

[!include [banner](../../includes/banner.md)]

Fyrir þetta ferli áttu að hafa lokið fyrri 4 leiðbeiningum í þessari röð af átta skráningum. Fyrstu 4 skráningar settu upp gögn sem þarf til að ljúka þessu ferli. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta verk er yfirleitt í höndum hönnuðar afurðar.

## <a name="select-the-product"></a>Velja afurð

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Í listanum skal merkja valda línu.
    * Finna útgefin afurðarsniðmát með tækni fyrir víddaskilgreiningu sem var stofnaður í fyrsta leiðarvísi í þessari röð.  
1. Á aðgerðasvæðinu skal velja **Hönnuður**.
1. Veljið **Uppskriftarútgáfur**.

## <a name="create-new-bom-and-bom-version"></a>Stofna nýja uppskrift og uppskriftarútgáfu.

1. Veljið **Nýtt**.
1. Veljið **Uppskrift og uppskriftarútgáfa**.
1. Í reitinn **Heiti** skal slá inn gildi.
    * Stillingar svæðis  
    * Í þessu ferli stillum við ekki inn tiltekið svæði fyrir Uppskriftina.  
1. Veljið **Í lagi**.
1. Veljið **Nýtt**.
    * Í þessu ferli er bætt við fjórar línur við Uppskrift. Tvær línur sýna valkosti fyrir kapal og tvær línur sýna valkosti fyrir geymslu.  
1. Í listanum skal merkja valda línu.
1. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
    * Velja vörunúmer A0001, HDMI 6' Cables.  
1. Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.
    * Veljið Afbirgðisflokkur kapals sem stofnuð var í leiðbeiningum 4 í þessari röð.  
1. Veljið **Nýtt**.
    * Velja vörunúmer A0002, HDMI 12' Cables.  
1. Í listanum skal merkja valda línu.
1. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
1. Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.
    * Veljið aftur Afbirgðisflokkur kapals.  
1. Veljið **Nýtt**.
1. Í listanum skal merkja valda línu.
1. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
    * Velja vörunúmer D0002 Cabinet.  
1. Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.
    * Veljið afbrigðaflokki xabinet fyrir þessa uppskriftarlínu.  
1. Veljið **Nýtt**.
1. Í listanum skal merkja valda línu.
1. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
    * Veljið vörunúmer M0007 StandardCabinet sem síðustu uppskriftarlínu.  
1. Sláið inn eða veldu gildi í reitnum **Afbrigðisflokkur**.
    * Veljið afbrigðaflokk Cabinet fyrir síðustu uppskriftarlínu.  

## <a name="approve-and-activate"></a>Samþykkja og virkja

1. Lokið síðunni.
1. Veljið **Samþykkja**.
1. Sláið inn eða veldu gildi í reitnum **Samþykki eftir**.
1. Veldu *Já* í reitnum **Viltu einnig að samþykkja uppskriftina?**.
1. Veljið **Í lagi**.
1. Veldu **Virkja**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]