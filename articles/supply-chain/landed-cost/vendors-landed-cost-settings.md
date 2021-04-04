---
title: Stillingum lánardrottins bætt við fyrir heildarkostnað
description: Þetta efnisatriði lýsir nýjum reitum sem verið er að bæta við fyrirliggjandi síðu lánardrottna þegar Heildarkostnaður einingin er gerð virk. Þessir reitir eru notaðir til að setja upp lánardrottna sem verða notaðir með eiginleikum heildarkostnaðar.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8cc0622cd761a671ebb88addc36b777cfefb7dc7
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500911"
---
# <a name="vendor-settings-added-for-landed-cost"></a>Stillingum lánardrottins bætt við fyrir heildarkostnað

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þegar einingin **Heildarkostnaður** er virkjaður er nokkrum nýjum reitum bætt við núverandi síðu **Lánardrottna**. Þessir reitir eru notaðir til að setja upp lánardrottna sem verða notaðir með eiginleikum heildarkostnaðar.

Til að stilla viðeigandi reiti skal fara í **Innkaup og aðföng \> Lánardrottnar \> Allir lánardrottnar**. Opnið fyrirliggjandi lánardrottin eða stofnið nýjan lánardrottin og veljið flýtiflipann **Ýmsar upplýsingar**. Allir nýju reitirnir sem einingin **Heildarkostnaður** bætir við birtast undir fyrirsögninni **Ferðir**. Eftirfarandi tafla lýsir þessum reitum.

| Svæði | lýsing |
|---|---|
| Sendingargerð | <p>Veljið hlutverk lánardrottins í sambandi við Heildarkostnað:</p><ul><li>**Ekkert** – Lánardrottinn hefur ekkert sértækt hlutverk sem tengist Heildarkostnaði. Þetta gildi er sjálfgefin stilling vegna þess að flestir lánardrottnar hafa sennilega ekkert sértækt hlutverk.</li><li>**Flutningsfyrirtæki** – Lánardrottinn er flutningsfyrirtæki. Lánardrottna sem eru með þessa sendingargerð er hægt að velja í reitnum **Flutningsfyrirtæki** á síðunni **Ferðir**.</li><li>**Tollmiðlari** – Lánardrottinn er tollmiðlari. Lánardrottna sem eru með þessa sendingargerð er hægt að velja í reitnum **Tollmiðlari** á síðunni **Fólíó**.</li><li>**Umboðsaðili** – Lánardrottinn er umboðsaðili. Lánardrottnar sem eru með þessa sendingargerð er hægt að velja í reitnum **Umboðsaðili** á síðunum **Lánardrottnar** og **Innkaupapantanir**.</li></ul> |
| Kostnaðargerðarflokkur | Úthluta lánardrottinn á kostnaðargerðarflokk í þeim tilgangi að velja [sjálfvirkan kostnað](auto-cost-setup.md). |
| Frá höfn | Veljið upprunalega höfn ferðarinnar. |
| Umboðsmaður | Sjálfgefinn aðili þegar keypt er frá lánardrottni. |
| Flytja inn lánardrottin kostnaðarútreiknings | <p>Gefa til kynna hvort lánardrottinn sé lánardrottinn Heildarkostnaðar.</p><p>**Ábending:** Hægt er að nota þennan reit með öryggi á færslustigi til að takmarka innkaupapantanirnar sem eru sýndar þegar ferð er búin til.</p> |
| Flutningsfyrirtæki | Veljið sjálfgefið flutningsfyrirtæki sem er notað þegar innkaupapantanir eru stofnaðar fyrir lánardrottininn. |
| Þjónustuaðili | Gefa til kynna hvort lánardrottinn sé þjónustuaðili. |
| Yfir/undir vikmarkaflokkur | Veljið sjálfgefinn yfir/undir vikmarkaflokk fyrir lánardrottin. |
