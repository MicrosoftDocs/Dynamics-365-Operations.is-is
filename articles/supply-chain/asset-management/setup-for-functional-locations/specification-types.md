---
title: Tegundir viðhaldseiginda
description: Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationTypeCopy, EntAssetAttributeType, EntAssetAttributeTypeValue, EntAssetFunctionalLocationType
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec5552d96473403931bbd513ae68ef0fe3069209f52e813963914417ad41b88a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739132"
---
# <a name="maintenance-attribute-types"></a>Tegundir viðhaldseiginda

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir hvernig á að stofna eigindagerðir í eignastýringu. Eiginleikar eru notaðir til að lýsa eiginleikum ýmissa þátta. Hægt er að setja upp eigindi á eftirfarandi færibreytur:

- [Gerðir virkra staðsetninga](../setup-for-functional-locations/functional-location-types.md)
- [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md)
- [Eignagerðir](../setup-for-objects/object-types.md)
- Eignir

Eiginleikarnir sem þú getur sett upp eru mismunandi eftir því hvaða þáttur er. Til dæmis, fyrir hagnýta staðsetningu, getur þú sett upp eiginleika fyrir stillingar og líkamlega stærð staðsetningarinnar. Fyrir eignategund eða eign geturðu sett upp eiginleika fyrir magn vélarinnar, orkunotkun og hámarks burðargetu við mismunandi aðstæður.

## <a name="create-attribute-types"></a>Búa til eigindargerðir

Þú getur búið til þínar eigin tegundir. Að auki geturðu flutt vöruvíddir á síðuna **Eigindagerðir**.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eigindagerðir**.
2. Veldu í fyrsta skipti sem þú setur upp eigindategundir **Stofna vöruvíddir** til að flytja sjálfkrafa staðlaðar víddir.
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]