---
title: Vöruhúsapantanir fyrir einingakvarða skýja og jaðra
description: Í þessu efnisatriði er að finna upplýsingar um getu vöruhúsapöntunar sem er notuð sem hluti vinnuálags einingarkvarða í vöruhúsi.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ff1f13198a7acc35897252f3ca8f6c2b1f56852e
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938277"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Vöruhúsapantanir fyrir einingakvarða skýja og jaðra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ekki eru allar viðskiptaaðgerðir studdar að fullu í opinni forútgáfu þegar vinnuálag einingarkvarða er notað. Ef einingarkvarðar eru notaðir skal gæta þess að nota aðeins þau ferli sem þetta efnisatriði lýsir sérstaklega sem studd ferli.

## <a name="what-are-warehouse-orders"></a>Hvað eru vöruhúsapantanir?

*Vöruhúsapantanir* eru gerð pöntunar sem var stofnuð til að styðja uppsetningar á vöruhúsum miðstöðvar og einingarkvarða. Þær gera kleift að taka á móti birgðum þegar vinnuálag vöruhúss er keyrt í einingarkvarða. Þær eru aðeins notaðar með innkaupapöntunum.

Vöruhúsapantanir eru notaðar sem hluti af vinnslu vöruhúsakerfis, t.d. þegar farsímaforrit vöruhúsakerfis er notað til að skrá efnislegar lagerbirgðir við vinnslu á innkaupapöntun á innleið. Vöruhúsapantanir eru stofnaðar sem hluti af ferlinu *Losa í vöruhús* sem er í boði fyrir innkaupapantanir sem tilgreina vöruhús einingarkvarða og vörur sem gert er kleift að nota vöruhúsakerfisferli.

> [!IMPORTANT]
> Vöruhúsapantanir eru aðeins í boði í uppsetningum sem nota [Vinnuálag vöruhúsakerfis fyrir einingakvarða skýja og jaðra](cloud-edge-workload-warehousing.md).

## <a name="create-a-warehouse-order"></a>Stofna vöruhúsapöntun

Til að stofna vöruhúsapöntun, skal fylgja eftirfarandi skrefum.

1. Skráðu þig inn í tilvikið af Microsoft Dynamics 365 Supply Chain Management sem keyrir á miðstöðinni. (Nauðsynlegt er að hefja ferlið *Losa í vöruhús* meðan notandi er innskráður í miðstöðina.)
1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Til að skoða tengdar línur vöruhúsapöntunar skal opna viðeigandi innkaupapöntun, velja línu í hlutanum **Innkaupapöntunarlínur** og síðan á tækjastikunni skal velja **Vöruhús \> Línur vöruhúsapöntunar**. Til að skoða allar línur skal fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Línur vöruhúsapöntunar**.

Einnig er hægt að kveikja á ferlinu *Losa í vöruhús* úr runuvinnslu með því að fara í **Vöruhúsakerfi > Losa í vöruhús > Sjálfvirk losun innkaupapantana**. Við uppsetningu runuvinnslunnar er hægt að velja tilteknar innkaupapöntunarlínur sem byggja á fyrirspurn. Dæmigerð atburðarás væri að setja upp endurtekna runuvinnslu sem losar allar staðfestar innkaupapöntunarlínur sem búist er við að berist næsta dag.

## <a name="cancel-a-warehouse-order"></a>Hætta við vöruhúsapöntun

Sem hluti af ferlinu *Losa í vöruhús*, eru birgðafærslur innkaupapöntunar tengdar við vöruhúsapantanir og læstar fyrir uppfærslum miðstöðvarinnar. Ef losað var í vöruhúsið fyrir mistök eða önnur ástæða er fyrir því að afturkalla stofnun á línum vöruhúsapöntunar, er hægt að óska eftir því að hætta við línur vöruhúsapöntunar.

Til að hætta við línur vöruhúsapöntunar skal fylgja þessum skrefum.

1. Skráið ykkur inn í tilvik Supply Chain Management sem er keyrt í miðstöðinni.
1. Farið í **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Línur vöruhúsapöntunar**.
1. Velja skal viðeigandi línu.
1. Í aðgerðarúðunni skal velja **Hætta við vöruhúsapöntunarlínur**.

> [!NOTE]
> Beiðninni um að hætta við línur verður hafnað fyrir línur sem annaðhvort bíða afturköllunar eða sem verið að vinna úr í vöruhúsi þar sem vinnuálagið er keyrt í kvörðunareiningu.

## <a name="monitor-a-warehouse-order"></a>Fylgjast með vöruhúsapöntun

Í yfirlitinu **Línur vöruhúsapöntunar** er hægt að fylgjast með framvindu móttöku á innleið með því að fara yfir gildin í dálkinum **Magn sem er eftir til móttöku**. Til að skoða upplýsingar sem tengjast vinnu sem gerð er með farsímaforriti vöruhúsakerfis skal fylgja einu af þessum skrefum.

- Farið í **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Línur vöruhúsapöntunar** og notið síuna til að finna línurnar sem leitað er að.
- Opnið **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir** og opnið viðeigandi innkaupapöntun. Í hlutanum **Innkaupapöntunarlínur** skal velja eina eða fleiri línur og síðan á tækjastikunni skal velja **Vöruhús \> Færslur vöruhúsamóttöku**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
