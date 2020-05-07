---
title: Samstilling við Dynamics 365 Supply Chain Management verðlagningarkerfi eftir eftirspurn
description: Þetta efnisatriði lýsir því hvernig hægt er að nota verð vélina í Microsoft Dynamics 365 Supply Chain Management úr Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 5ffc0358ff58b2a05aa84b4467a27d88b5e1ec42
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270337"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Samstilling við Dynamics 365 Supply Chain Management verðlagningarkerfi eftir eftirspurn

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management felur í sér verðlagningarvél sem sér um viðskiptasamninga, verðskrár, vildarkerfi, kynningar og afslætti. Verðlagningarvélin notar flóknar reglur til að ákvarða besta verðið fyrir tiltekið tilboð eða pöntun. Þegar þú notar tvöfalda skrifa notarðu annaðhvort stöðuga verðlagningu eða verð vél frá Dynamics 365 Supply Chain Management á tilboðs- og pöntunarsíðum í Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Notaðu verðlagsvélina úr Supply Chain Management í Sales

1. Í Sales ferðu í **Sales \> Pantanir**.
2. Veldu **Nýtt** til að stofna nýja pöntun eða velja fyrirliggjandi pöntun í listanum **Mínar pantanir**.
3. Bæta við nýrri pöntunarlínu.
4. Ef þú ert að búa til nýja pöntun skaltu velja **Verðpöntun** í aðgerðarglugganum. Ef þú ert að uppfæra fyrirliggjandi pöntun skaltu velja **Endurreikna** í aðgerðarglugganum.

    Eftirfarandi reitir eru sjálfkrafa fylltir út:

    + Upplýsingar um upphæð
    + Afsláttar%
    + Afsláttur
    + Upphæð fyrir farm
    + Farmupphæð
    + Heildarskattur
    + Heildarupphæð
    
5. Gerðu eftirfarandi til að tryggja að kerfið taki mið af viðskipta- og sölusamningum til að reikna verðið:
    1. Flettu að umhverfi Supply Chain Management.
    2. Farðu í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakröfu**.
    3. Veldu flipann **Verð** á yfirlitsstikunni sem er til hliðar.
    4. Fyrir neðan **Mat verðsamnings** skal afmerkja valkostinn **Handvirk færsla**.

## <a name="how-it-works"></a>Hvernig það virkar

Þegar þú velur **Verðpöntun** í Sales er virknin **Samtölur** á flipanum **Sölupöntun \> Skoðun** í Supply Chain Management kölluð á tengdri sölupöntun. Gildin í heildarpöntuninni í Sales eru notuð til að fylla út samsvarandi reiti í Supply Chain Management.

Þegar samtala sölupöntunar er reiknuð út í Supply Chain Management metur útreikningurinn fyrirliggjandi viðskiptasamninga og sölusamninga viðskiptavinarins og vörurnar sem eru skráðar í sölupöntuninni. Þessar upplýsingar eru notaðar til að reikna út samtölurnar. Þegar **Verðpöntun** er valin endurspeglar Sales sjálfkrafa alla uppstillingu sem hefur verið gerð í Supply Chain Management.

## <a name="limitations"></a>Takmarkanir

Þegar reitirnir í Sales eru fylltir út gilda eftirfarandi takmarkanir:

+ Uppsetning gjalds og úthlutunar gjalds í Supply Chain Management er ekki endurtekin í Sales.
+ Verðlagning telur ekki sérstaka smásöluverðlagningu sem tilgreind er í reitnum **Verslunarrás** á sölupöntunarlínusíðunni í Supply Chain Management.
+ Afslættir sem eru skilgreindir í hlutanum **Stjórnun afsláttar** af Supply Chain Management eru ekki skoðaðir.
