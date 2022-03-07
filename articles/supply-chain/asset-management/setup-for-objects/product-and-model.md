---
title: Eignaframleiðendur og líkön
description: Þetta efni útskýrir hvernig á að setja upp eignaframleiðendur og skyld líkön í eignastjórnun.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80fcb493d96209d78f842414c198a8275e4818ba365759466034faf5f3405540
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739899"
---
# <a name="asset-manufacturers-and-models"></a>Eignaframleiðendur og líkön

[!include [banner](../../includes/banner.md)]

 

Þetta efni útskýrir hvernig á að setja upp eignaframleiðendur og skyld líkön í eignastjórnun. Líkön geta verið tengd eignategundum.

## <a name="set-up-product-model-relations"></a>Setja upp afurða-líkanavensl

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Framleiðandi og líkan**.
2. Veldu **Nýr** til að stofna nýja afurð.
3. Í **Framleiðandi** reitinn, sláðu inn nafn fyrir eignaframleiðandann.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Á flýtiflipanum **Líkön**, veldu **Bæta við** til að búa til eignalíkan sem ætti að tengjast eignaframleiðandanum.
6. Í **Líkan** reitinn, sláðu inn nafn fyrir eignalíkanið.
7. Í reitnum **Lýsing** skal færa inn lýsingu.
8. Í **Tegund eigna** reit, veldu þá eignategund sem framleiðandamódelið ætti að tengjast.

    > [!NOTE]
    > Þú getur einnig sett upp sambönd fyrir eignategundir, framleiðendur og gerðir í uppflettingunni **Gerðir eigna**. Nánari upplýsingar sjá [Eignagerðir](../setup-for-objects/object-types.md).

    Í flýtiflipanum **Upplýsingar** sýnir reiturinn **Líkön** fjölda eignalíkana sem eru settir upp á völdum eignaframleiðanda. Reiturinn **Eignir** sýnir fjölda eigna sem eru að nota valda framleiðanda.
    
    Reiturinn **Eignir** sýnir fjölda hluta sem eru að nota líkan framleiðanda.

> [!NOTE]
> Eignategund getur ekki haft nein sambönd eignaframleiðanda, hún getur tengst einni eignaframleiðslulíkani eða hún getur verið tengd fjölmörgum eignaframleiðanda. Ef eignategund tengist að minnsta kosti einni framleiðslulíkani, eru aðeins samsetningarnar sem settar eru upp í uppflettingunni **Framleiðandalíkan** hægt er að velja á þeim eignastýringarsíðum þar sem hægt er að setja upp samsetningu eigna, framleiðanda og líkans. Þessar síður innihalda **Allar eignir**, **Eignaþjónustustig**, **Sjálfgefin starfstegund**, og **Viðhald fjárlagalínur**. Ef sumar eignategundir eru ekki tengdar neinni framleiðslulíkani, eru aðeins þær eignategundir og framleiðendamódel sem hafa heldur ekki tengsl við eignategundir sýndar á síðunum.

## <a name="select-a-manufacturer-and-model-on-an-object"></a>Veldu framleiðanda og gerð á hlut

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir**.
2. Í **Eignir** dálki, veldu hlekkinn fyrir eignina. Síðan **Upplýsingar** birtist.
3. Veljið **Breyta**.
4. Á flýtiflipanum **Almennt**, veldu gildi í reitunum **Framleiðandi** og **Líkan**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]