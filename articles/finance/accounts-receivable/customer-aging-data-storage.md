---
title: Geymsla aldursgreiningargagna viðskiptavinar
description: Þessi grein lýsir ferlinu við að nota ytri geymslu fyrir aldursgreiningargögn viðskiptavinar. Hægt er að keyra geymsluferli aldursgreiningargagna viðskiptavinar til gera úttakið tiltækt fyrir útflutning í ytra kerfi.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7a66485cc9a538f5c3999009b6dbe295d7a5b9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894143"
---
# <a name="customer-aging-data-storage"></a>Geymsla aldursgreiningargagna viðskiptavinar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir ferlinu við að nota ytri geymslu fyrir aldursgreiningargögn viðskiptavinar. Í Microsoft Dynamics 365 Finance er hægt að keyra ferlið **Geymsla aldursgreiningargagna viðskiptavinar** til að gera úttakið tiltækt fyrir útflutning í ytra kerfi. Þegar ferlið er keyrt eru sömu valkostir aldursgreiningarskýrslu og eru í boði í kerfinu í boði í ytri kerfum. Upplýsingarnar eru alltaf í útfluttu gögnunum.

Það getur verið gagnlegt að gera aldursgreiningargögn viðskiptavinar aðgengileg ytra kerfi fyrir geymslu í tilfellum þar sem úttakið inniheldur marga viðskiptavini og/eða margar færslur. Ef fyrirliggjandi skýrsla um **aldursgreiningu viðskiptavinar** rennur út á tíma eru of mörg gögn í henni til að prenta, þessi eiginleiki býður upp á aðra leið til að ná í sömu gögnin.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Virkja eiginleika fyrir geymslu aldursgreiningargagna viðskiptavinar

Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu. Stjórnendur geta notað stillingar eiginleikastjórnunar til að athuga stöðu eiginleikans og virkja hann ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** Geymsla aldursgreiningargagna viðskiptavinar
- **Heiti eiginleika:** Geymsla aldursgreiningargagna viðskiptavinar

## <a name="run-the-customer-aging-data-storage-process"></a>Keyra geymsluferli aldursgreiningargagna viðskiptavinar

1. Farðu í **Skuldir og innheimta \> Fyrirspurnir og skýrslur \> Viðskiptavinur \> Geymsla aldursgreiningargagna viðskiptavinar**.
2. Veljið **Nýtt**.
3. Í **Heiti** reitinn skal slá inn heiti fyrir ferlið.
4. Stilltu þær breytur sem eftir eru eins og þú þarft.

    > [!NOTE]
    > Færsluupplýsingar fylgja alltaf með og úrvinnslan fer alltaf fram í runuvinnslu.

5. Veldu **Í lagi**.
6. Uppfærðu síðuna **Geymsla aldursgreiningargagna viðskiptavinar** til að sjá gildin fyrir **Heiti runu** og **Keyrslutími runu** sem eru sýnd saman með gildinu **Vinnslustaða**. Þegar runuvinnslunni er lokið er reiturinn **Vinnslustaða** stilltur á **Lokið** og reiturinn **Fjöldi aldursgreiningarlína** er stilltur. Ef runuvinnslan er endurtekin er reiturinn **Vinnslustaða** stilltur á **Í bið**.
7. Veldu hnappinn **Sía** við hliðina á reitnum **Fjöldi aldursgreiningarlína** til að fara yfir síurnar sem hefur verið bætt við fyrir runuvinnsluna.

Síðan **Geymsla aldursgreiningargagna viðskiptavinar** inniheldur ekki niðurstöðurnar. Gagnaeiningin **Geymsla aldursgreiningargagna viðskiptavinar** gerir þér hins vegar kleift að flytja út úttakið á hvaða sniðið sem er sem gagnastjórnun styður.

> [!NOTE]
> Áður en þú flytur út skaltu bæta við síu til að takmarka útfluttar niðurstöður við nýjustu aldursgreininguna. Bættu við til dæmis eftirfarandi skilyrði til að skila nýlegustu runukeyrslunni:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchName())
>
> Annars er hægt að bæta við eftirfarandi skilyrði til að skila nýlegustu runukeyrslunni fyrir núverandi notanda:
>
> (CustAgingDataStorageSysQueryRangeUtil::getLatestBatchNameForCurrentUser())
