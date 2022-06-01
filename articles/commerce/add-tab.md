---
title: Flipaeining
description: Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 104fb57cfdcd96a0da50899c0eac576074282017
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780615"
---
# <a name="tab-module"></a>Flipaeining

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.

Flipaeiningar líta út eins og hólfaeiningar og eru notaðar við skipulagningu upplýsinga á síðusvæði í flipum. Hægt er að nota þær á sérhverri síðu þar sem upplýsingar þurfa að koma fram í flipum.

Í hverri flipaeiningu er hægt að bæta við einu eða fleiri flipaeiningaratriðum. Hvert flipaeiningaratriði stendur fyrir einn flipa. Í hverja einingu flipaatriðis er hægt að bæta við einni eða fleiri einingum. Engar takmarkanir eru á þeim gerðum eininga sem hægt er að bæta við flipaeiningaratriði.

Eftirfarandi mynd sýnir dæmi um flipaeiningu á síðusvæði. Í þessu dæmi er flipinn **Sending** valinn.

![Dæmi um flipaeiningu.](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a>Eiginleikar flipaeiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus | Texti | Þessi eiginleiki sýnir valfrjálsa textafyrirsögn fyrir flipaeininguna. |
| Virkur flipavísir | Númer | Þessi eiginleiki sýnir flipann sem á að vera sjálfgefið virkur þegar síða er hlaðin. Ef ekkert gildi er gefið upp verður fyrsta flipaatriðið virkt að sjálfgefnu. |

## <a name="tab-item-module-properties"></a>Eiginleikar flipaeiningaratriða

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Titill | Texti | Þessi eiginleiki sýnir titiltexta fyrir atriði flipaeiningar. |

## <a name="add-a-tab-module-to-a-page"></a>Bæta flipaeiningu við síðu

Til að bæta flipaeiningu við síðu og stilla eiginleikana skal fylgja þessum skrefum.

1. Notið markaðssniðmát Fabrikam (eða annað sniðmát sem er með engum takmörkunum) til að búa til nýja síðu sem heitir **Reglusíða verslunar**.
1. Í **Aðal** rifa á **Sjálfgefin síða**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Tab** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði flipaeiningar skal velja **Fyrirsögn** við hliðina á blýantstákninu.
1. Í glugganum **Fyrirsögn**, undir **Texti fyrirsagnar**, skal færa inn texta fyrirsagnar (til dæmis **Reglur**). Veljið síðan **Í lagi**.
1. Í **Tab** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Flipi atriði** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði flipaeiningaratriðis, undir **Titill**, skal færa inn titiltexta (til dæmis **Afhending**).
1. Í **Flipi atriði** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Textablokk** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði textabálkseiningar, undir **Sniðinn texti**, skal slá inn stuttan texta.
1. Í hólfinu **Flipi** skal bæta við nokkrum flipaeiningaratriðum til viðbótar sem eru með titlum. Í hverju flipaeiningaratriði skal bæta við textabálkseiningu með innihaldi.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Síðan birtir flipaeningu sem inniheldur flipaeiningaratriði með innihaldinu sem var bætt við.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Fellingareining](add-accordion.md)

[Textabálkseining](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
