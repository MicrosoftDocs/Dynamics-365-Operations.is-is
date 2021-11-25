---
title: Geymsla aldursgreiningargagna viðskiptavinar
description: Þetta efnisatriði lýsir ferlinu við að nota ytri geymslu fyrir öldrunargögn viðskiptavina. Þú getur keyrt ferli öldrunargagnageymslu viðskiptavinar til að gera úttakið aðgengilegt til útflutnings á ytra kerfi.
author: JodiChristiansen
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ecd4f5359019e3c4778e21cc4946b9998cd519f
ms.sourcegitcommit: 9f8da0ae3dcf3861e8ece2c2df4f693490563d5e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/16/2021
ms.locfileid: "7817462"
---
# <a name="customer-aging-data-storage"></a>Geymsla aldursgreiningargagna viðskiptavinar

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þetta efnisatriði lýsir ferlinu við að nota ytri geymslu fyrir öldrunargögn viðskiptavina. Í Microsoft Dynamics 365 Finance, þú getur keyrt ferli öldrunargagnageymslu viðskiptavina til að gera úttakið aðgengilegt til útflutnings á ytra kerfi. Þegar þú keyrir ferlið eru sömu öldrunarskýrsluvalkostir sem eru tiltækir í kerfinu í boði fyrir ytri kerfi. Upplýsingarnar eru alltaf innifaldar í útfluttu gögnunum.

Það getur verið gagnlegt að gera öldrunargögn viðskiptavina aðgengileg ytra kerfi til geymslu í þeim tilvikum þar sem úttakið inniheldur marga viðskiptavini og/eða margar færslur. Ef núverandi **Öldrun viðskiptavina** Tímamörk skýrslunnar eru vegna þess að hún hefur of mikið af gögnum til að prenta, þessi eiginleiki býður upp á aðra leið til að fá sömu gögnin.

## <a name="enable-the-customer-aging-data-storage-feature"></a>Virkjaðu eiginleikann Geymslugagnageymslu öldrunar viðskiptavina

Áður en þú getur notað þennan eiginleika þarftu að virkja hann í kerfinu þínu. Stjórnendur geta notað eiginleikastjórnunarstillingarnar til að athuga stöðu eiginleikans og virkja hann ef þess er krafist. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** Inneign og innheimtur
- **Eiginleikaheiti:** Gagnageymsla viðskiptavina sem eldist

## <a name="run-the-customer-aging-data-storage-process"></a>Keyrðu ferli öldrunargagnageymslu viðskiptavinar

1. Fara til **Inneign og innheimtur \> Fyrirspurnir og skýrslur \> Viðskiptavinur \> Gagnageymsla viðskiptavina sem eldist**.
2. Veljið **Nýtt**.
3. Í **Nafn** reit, sláðu inn nafn fyrir ferlið.
4. Stilltu færibreyturnar sem eftir eru eins og þú þarfnast.

    > [!NOTE]
    > Færsluupplýsingar eru alltaf innifaldar og vinnslan fer alltaf fram í lotuvinnu.

5. Veldu **Í lagi**.
6. Endurnýjaðu **Gagnageymsla viðskiptavina sem eldist** síðu til að sjá **Nafn lotu** og **Lotu keyrslutími** gildi sem eru sýnd ásamt **Vinnslustaða** gildi. Þegar lotuvinnunni er lokið, er **Vinnslustaða** reiturinn er stilltur á **Lokað** og **Fjöldi öldrunarlína** reiturinn er stilltur. Ef lotuvinnan er endurtekin, er **Vinnslustaða** reiturinn er stilltur á **Að bíða**.
7. Veldu **Sía** hnappinn við hliðina á **Fjöldi öldrunarlína** reitinn til að skoða síurnar sem hefur verið bætt við fyrir runuvinnuna.

The **Gagnageymsla viðskiptavina sem eldist** síða inniheldur ekki niðurstöðurnar. Hins vegar er **Gagnageymsla viðskiptavina sem eldist** gagnaeining gerir þér kleift að flytja úttakið út á hvaða snið sem gagnastjórnun styður.

> [!NOTE]
> Áður en þú gerir útflutning skaltu bæta við síu til að takmarka útfluttar niðurstöður við nýjustu öldrun. Bættu til dæmis við eftirfarandi forsendum til að skila nýjustu runukeyrslunni:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchName())
>
> Að öðrum kosti skaltu bæta við eftirfarandi forsendum til að skila nýjustu runu keyrslu fyrir núverandi notanda:
>
> (CustAgingDataStorageSysQueryRangeUtil:: getLatestBatchNameForCurrentUser())
