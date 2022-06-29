---
title: Færa, skipta út og setja upp eignir
description: Þessi grein útskýrir hvernig á að færa, skipta út og setja upp eignir í eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectReplace, EntAssetObjectInstallLookup, EntAssetObjectMove, EntAssetObjectTableEditSubObjects
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a6b5a2904d21782ae422d06eaaf03c5d5e51ab9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015580"
---
# <a name="move-replace-and-install-assets"></a>Færa, skipta út og setja upp eignir

[!include [banner](../../includes/banner.md)]

 

Þessi grein útskýrir hvernig á að færa, skipta út og setja upp eignir í eignastýringu. Þú getur búið til einstakar eignir sem hafa engin tengsl við aðrar eignir, eða þú getur búið til eignaskipulag sem felur í sér yfireign (efsta eign) og tengdar undireignir (undireignir). Í eignastýringu eru þrjár leiðir til að færa og breyta staðsetningu eignar:

- **Færa** - Færa eign annaðhvort í aðra eignaskipan eða á annan stað í sömu eignaskipan.
- **Skipta út** - Fjarlægðu eign tímabundið úr eignaskipan svo hægt sé að gera við eða endurnýja hana og bæta síðan endurnýjuðu eigninni aftur við eignaskipan síðar. Að öðrum kosti, skipta varanlega notuðu eign út fyrir nýja eign.
- **Setja upp** - Settu upp yfireign og allar tengdar undireignir á virkum stað.

> [!NOTE]
> Eignin sem þú flytur, skiptir út eða setur upp gæti tengst annarri virkri staðsetningu. Í því tilfelli gæti eignin notað fjárhagsvíddir á virkri staðsetningu. Á síðunni **Gerðir virkra staðsetninga** setur þú upp meðhöndlun fjárhagsvíddar á virkum staðsetningum.

## <a name="move-asset"></a>Færa eign

Notaðu virknina **Færa eign** til að færa eign annaðhvort í aðra eignaskipan eða á annan stað í sömu eignaskipan. Þú getur líka fært eign út úr eignaskipan þannig að hún verði sjálfstæða eign sem hefur engin tengsl við uppbyggingu.

> [!NOTE]
> Ekki nota þessa aðgerð ef verið er að gera við eignir eða skipta tímabundið út. Í staðinn skaltu nota **Skiptu um eign** virkni sem lýst er síðar í þessari grein.

1. Veldu **Eignastýring** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.
2. Á listanum, veljið eign til að færa. Ef eignin er með undireignir þá færir þú líka þessar eignir.
3. Velja **Færa eign**.
4. Til að færa eignina þannig að hún verði hluti af eignaskipan skaltu velja nýju yfireignina í reitnum **Yfireign**. Ef þú ert að flytja undireign, og þú vilt gera hana að sjálfstæða eign sem hefur engin tengsl við uppbyggingu, skaltu hafa reitinn **Yfireign** auður.
5. Sjálfgefið er að reiturinn **Virkt** sé sjálfkrafa stilltur á núverandi dagsetningu og tíma. Hins vegar getur þú valið annan dag og tíma sem eignaflutningurinn gildir frá.
6. Veljið **Í lagi**.

## <a name="replace-asset"></a>Skipta út eign

Notaðu virknina **Skipta út eign** í tengslum við viðgerðir, endurbætur eða varanlega skipti á slitinni eign með nýrri eign. Þessi aðgerð er notuð til að skipta út undireignum í eignaskipan. Fyrir yfireignir (það er að segja eignir sem ekki eru með yfireign eins og er) er þessi skipti gerð á virkan stað. Nánari upplýsingar um hvernig á að skipta um yfireignir á virkum stað, sjá [Setja upp eignir á virkum staðsetningum](../functional-locations/install-objects-on-functional-locations.md).

> [!NOTE]
> Ef viðgerðarverkstæði er tengd framleiðsludeildinni þinni geturðu búið til virkar staðsetningar eins og **Viðger**, **Rusl**, og **Geymsla** til að sjá um viðgerðir og skipti á eignum.

1. Veldu **Eignastýring** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.
2. Á listanum, veljið undireign til að skipta út. Ef eignin er með undireignir þá skiptir þú um þessar eignir.
3. Veldu **Skipta út eign**.

    Reiturinn **Breytt skipulag** sýnir síðustu dagsetningu og tíma sem valin eign og tengdar undireignir voru færð í eignaskipan.

4. Í lutanum **Valin eign** í reitnum **Virk markstaðsetning** veldu hagnýta staðsetningu til að færa eignina til. Veldu til dæmis staðsetninguna **Viðgerð** eða **Rusl**.

    Í hlutanum **Yfireign** sýnir reiturinn **Virkt** síðustu dagsetningu og tíma sem yfireignin og tengdar undireignir voru settar upp eða fluttar á núverandi virka staðsetningu.

5. Í hlutanum **Ný eign** velurðu í reitnum **Eignir** eignina sem á að setja inn sem tímabundin eða varanleg skipti fyrir valda eign. Þessi eign gæti nú verið staðsett á öðrum virkum stað, svo sem **Geymsla**.
7. Í hlutanum **Virkt frá** er reiturinn **Virkt** sjálfkrafa stilltur á núverandi dagsetningu og tíma. Hins vegar getur þú valið annan dag og tíma sem eignaskiptin gildir frá.
8. Veljið **Í lagi**.

## <a name="install-asset"></a>Settu upp eign

Notaðu aðgerðina **Setja upp eign** til að setja upp eignaskipulag á virkan stað.

> [!NOTE]
> Veldu alltaf yfireign. Yfireignin og tengdar undireignir verða færðar á valda staðsetningu.

1. Veldu **Eignastýring** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.
2. Veldu listann á yfireignina sem á að setja upp á öðrum virkum stað.
3. Velja **Setja upp eign**.

    Hlutinn **Eigindi** sýnir þær eignaeigindir sem eru settar upp á yfireigninni.

4. Í reitnum **Virk staðsetning** skal velja nýja staðsetningu.
5. Sjálfgefið er að reiturinn **Virkt** sé sjálfkrafa stilltur á núverandi dagsetningu og tíma. Hins vegar getur þú valið annan dag og tíma sem uppsetning á eignaskipulaginu gildir frá.
6. Veljið **Í lagi**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]