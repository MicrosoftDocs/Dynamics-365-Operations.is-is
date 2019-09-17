---
title: Tegundir viðhaldseiginda
description: Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 3b3247f693f5934b3fbf83b7b831c7ed221514cb
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783342"
---
# <a name="maintenance-attribute-types"></a>Tegundir viðhaldseiginda

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu. Eiginleikar eru notaðir til að lýsa eiginleikum ýmissa þátta. Hægt er að setja upp eigindi á eftirfarandi færibreytur:

- [Gerðir virkra staðsetninga](../setup-for-functional-locations/functional-location-types.md)
- [Virkar staðsetningar](../functional-locations/create-functional-locations.md)
- [Eignagerðir](../setup-for-objects/object-types.md)
- Eignir

Eiginleikarnir sem þú getur sett upp eru mismunandi eftir því hvaða þáttur er. Til dæmis, fyrir hagnýta staðsetningu, getur þú sett upp eiginleika fyrir stillingar og líkamlega stærð staðsetningarinnar. Fyrir eignategund eða eign geturðu sett upp eiginleika fyrir magn vélarinnar, orkunotkun og hámarks burðargetu við mismunandi aðstæður.

## <a name="create-attribute-types"></a>Búa til eigindargerðir

Þú getur búið til þínar eigin tegundir. Að auki geturðu flutt vöruvíddir frá Microsoft Dynamics 365 for Finance and Operations til **Eigindagerðir** síðu.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eigindagerðir**.
2. Veldu í fyrsta skipti sem þú setur upp eigindategundir **Búðu til vöruvíddir** til að flytja sjálfkrafa staðlaðar víddir í Finance and Operations.
3. Veldu **Nýr** til að stofna nýja eigindagerð.
4. Í svæðinu **Eigindagerð** er fært inn nafn fyrir eigindagerðina.
5. Í reitnum **Lýsing** skal færa inn lýsingu.
6. Í reitinn **Eining** reitinn, veldu viðeigandi eigindareining, eftir þörfum.
7. Í reitnum **Gagnagerð** skal velja gagnagerð fyrir eininguna.
8. Ef þú valdir **Strengur** sem gagnagerð, fylgdu þessum skrefum til að búa til gildi fyrir eigindategundina:

    1. Veldu eigindagerðina og veldu síðan **Gildi**.
    2. Í **Eigindagildi** reit, veldu **Nýtt**.
    3. Í reitnum **Eigindategund** velurðu tegund eiginda (vídd).
    4. Sláið inn eða veldu gildi í **Gildi** reitnum.
    5. Í reitnum **Lýsing** skal færa inn lýsingu.
    6. Vistaðu færsluna.
    7. Fara aftur í **Eigindagerðir** síðu.

9. Vistaðu færsluna.

    Reiturinn **Gerðir virkra staðsetninga** sýnir fjölda virkra staðsetninga sem eru að nota eigindagerðina. Reiturinn **Gerðir eigna** sýnir fjölda eignagerða sem eru að nota hann.