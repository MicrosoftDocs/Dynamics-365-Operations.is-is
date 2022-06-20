---
title: Flýtiskoðunareining
description: Þessi grein fjallar um flýtisýnareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e9066357fda4f5d91c547622ac64d8c4eef253ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847576"
---
# <a name="quick-view-module"></a>Flýtiskoðunareining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um flýtisýnareiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Flýtiskoðunareiningin gerir notendum kleift að skoða afurðarupplýsingar á fljótlegan hátt þegar þeir fletta upp afurðum á listasíðu og bæta einni eða fleiri afurðum við körfuna úr listasíðunni án þess að þurfa að fara á upplýsingasíðu afurðar. Flýtiskoðunareiningin veitir yfirlit afurðarupplýsinga sem notandi þurfa til að geta tekið ákvörðun um „bæta við körfu“. Hún býður einnig upp á tengil á upplýsingasíðu afurðar þannig að notendur geta skoðað frekari upplýsingar um afurð og kaupmöguleika.

Flýtiskoðunareiningin er studd af einingum [vörusafns](product-collection-module-overview.md) og [leitarniðurstaðna](search-result-module.md).

> [!IMPORTANT]
> Flýtiskoðunareiningin er í boði frá og með Commerce-útgáfu 10.0.17.

Eftirfarandi mynd sýnir dæmi um flýtiskoðunareiningu á listasíðu afurða.

![Dæmi um flýtiskoðunareiningu á listasíðu afurða.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Eiginleikar einingar

Flýtiskoðunareiningin styður sumar af sömu aðgerðum kaupgluggaeiningarinnar. Þess vegna líkjast eiginleikar flýtiskoðunareiningar eiginleikum kaupgluggaeiningar.

| Eiginleiki | Gildi | lýsing |
|----------------|--------|-------------|
| Merki fyrirsagnar | **H1**, **H2**, **H3**, **H4**, **H5** eða **H6** | Þessi eiginleiki skilgreinir merki fyrirsagna fyrir afurðarheitið. Ef flýtiskoðunareiningin er efst á síðunni ætti að stilla þennan eiginleika á **H1** til að uppfylla aðgengisstaðla. |
| Leyfa sérsniðið verð | **Satt** eða **Ósatt** | Ef þessi eiginleiki er stilltur á **Satt** getur notandinn fært inn sérsniðið verð. |
| Lágmarksverð | Heiltala | Þessi eiginleiki gildir aðeins ef eiginleikinn **Leyfa sérsniðið verð** er stilltur á **Satt**. Hann skilgreinir lágmarksverðið sem notandi getur slegið inn (t.d. $1). |
| Hámarksverð | Heiltala | Þessi eiginleiki gildir aðeins ef eiginleikinn **Leyfa sérsniðið verð** er stilltur á **Satt**. Hann skilgreinir hámarksverðið sem notandi getur slegið inn (t.d. $1000). |

## <a name="commerce-site-builder-settings"></a>Stillingar Commerce-vefsmiðs

Líkt og kaupgluggaeiningin fer flýtiskoðunareiningin eftir stillingunum á **Stillingar svæðis \> Viðbætur \> Bæta afurð við körfu**. Hins vegar er stillingin **Fara á körfusíðu** hunsuð vegna þess að hún er ekki í samræmi við tilgang flýtiskoðunareiningarinnar, sem er að gera notendum kleift að fletta í mörgum afurðum á listasíðu og bæta þeim við körfuna án þess að fara af listasíðunni.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Bæta flýtiskoðunareiningu við vörusafnseiningu

Hægt er að bæta flýtiskoðunareiningu við einingar vörusafns og leitarniðurstaðna.

Til að bæta flýtiskoðunareiningu við vörusafnseiningu í Commerce-vefsmið skal fylgja þessum skrefum.

1. Opnið **Síður** og veljið síðan heimasíðuna fyrir Fabrikam-svæðið.
1. Farðu í hvaða **Vörusöfnun** mát á heimasíðunni, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Quick View** mát og veldu síðan **Allt í lagi**.
1. Á aðgerðasvæði einingarinnar **Flýtiskoðun** skal velja **Fyrirsögn**. Í svarglugganum **Fyrirsögn** skal stilla reitinn **Fyrirsagnarstig** á **H2** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Afurðasafnseining](product-collection-module-overview.md)

[Leitarniðurstöðueining](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
