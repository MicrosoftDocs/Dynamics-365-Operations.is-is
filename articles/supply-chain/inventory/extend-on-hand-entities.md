---
title: Framlengja gagnaeiningar tiltækra birgða
description: Í þessari grein er að finna dæmi sem sýnir hvernig á að bæta stækkuðum reitum við yfirlit INVENTORSITEONHANDENTITY and INVENTWAREHOUSEONHANDENTITY þannig að möguleikar gagnaeininga lagerbirgða geti virkað með stækkuninni.
author: yufeihuang
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 352b466a185bcd0778ea17e598129864c1547987
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906038"
---
# <a name="extend-inventory-on-hand-data-entities"></a>Framlengja gagnaeiningar tiltækra birgða

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management býður upp á eiginleika [stækkunarhæfni](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) sem gera kleift að [bæta reitum við töflur í gegnum stækkun](../../fin-ops-core/dev-itpro/extensibility/add-field-extension.md). Í þessari grein er að finna dæmi sem sýnir hvernig á að bæta stækkuðum reitum við yfirlit `INVENTORSITEONHANDENTITY` og `INVENTWAREHOUSEONHANDENTITY` þannig að möguleikar gagnaeininga lagerbirgða geti virkað með stækkuninni. Frekari upplýsingar um gagnaeiningar er að finna í [Yfirlit gagnastjórnunar](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

> [!NOTE]
> Hér er listi yfir sumar gagnaeiningar lagerbirgðanna:
>
> - Birgðir á lager eftir staðsetningu
> - Birgðir á lager eftir staðsetningu V2
> - Birgðir á lager eftir vöruhúsi
> - Birgðir á lager eftir vöruhúsi v2

Eftir að reitum hefur verið bætt við töflurnar sem eru notaðar af `inventSiteOnHandView`-yfirlitinu, þarf að samstilla vélina þannig að stækkanirnar verði þekktar á réttan hátt.

1. Stækkið `InventSiteOnHandView`-yfirlitið með því að bæta við stækkuðum reit.
1. Stækkið `InventSiteOnHandAggregatedView`-yfirlitið með stækkuðum reitum.
1. Stækkið `InventSiteOnHandAggregatedViewBuilder` viewBuilder-klasann með því að breyta `getExtensionFields()`-aðferðinni. Á þennan hátt er gömlum yfirlitsreitum varpað í nýja yfirlitsreiti þegar samstilling viewBuilder er keyrð.

Til dæmis hefur eftirfarandi fjórum reitum verið bætt við `InventTable`-töfluna í gegnum stækkun:

- Sérstilltur reitur 1
- Sérstilltur reitur 2
- Sérstilltur reitur 3
- Sérstilltur reitur 4

Í tilfellinu þarf að breyta `getExtensionFields()`-aðferðinni á eftirfarandi hátt.

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

Eftir að þessum skrefum er lokið er hægt að stækka gagnaeiningarnar fyrir birgðir á lager eftir svæði og birgðir á lager eftir vöruhúsi með því að bæta nýju reitunum við. Á þennan hátt er tryggt að stækkuðu reitirnir verði þekktir og hafðir með við gagnaflutning sem notar þessar gagnaeiningar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]