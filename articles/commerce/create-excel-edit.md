---
title: Stofna Excel-vinnubók til að breyta smásölufærslum
description: Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: bfc3f6898087445e0276994ceeb52c178785bf3604fa163939327e99a0564f64
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753109"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>Stofna Excel-vinnubók til að breyta smásölufærslum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að bæta svæðum við Excel-vinnubók til að hægt sé að breyta smásölufærslum í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Í boði er fyrirframskilgreint Excel-sniðmát sem viðskiptavinir geta opnað í ólíkum hlutum kerfisins og bæði notað til að breyta og endurskoða smásölufærslur. Viðskiptavinir hafa einnig kost á að stofna sérstillta Excel-vinnubók í þessum tilgangi.

## <a name="create-and-configure-an-excel-workbook"></a>Stofna og grunnstilla Excel-vinnubók

Fylgið eftirfarandi skrefum til að stofna Excel-vinnubók til að hægt sé að breyta smásölufærslum.

1. Opnið Excel og stofnið auða vinnubók.
1. Á flipanum **Setja inn** skal smella á **Innbæturnar mínar**.
1. Á svæðinu til vinstri skal velja tengilinn **Bæta við upplýsingum um þjón**.
1. Sláið inn vefslóðina og smellið síðan á **Í lagi**.
1. Fylgja skal eftirfarandi skrefum til að lagfæra vandamálið ef villuboðin „Engar skráningar smáforrita“ birtast:

    1. Opnið Commerce, **Kerfisstjórnun \> Uppsetning \> Færibreytur Office-forrits**.
    1. Á flýtiflipanum **Færibreytur forrits** er smellt á **Frumstilla færibreytur forrits**.
    1. Smellið á **Í lagi** í svarglugga staðfestingarboðanna.
    1. Á flýtiflipanum **Skráð smáforrit** skal smella á **Frumstilla skráningu smáforrits**.
    1. Endurtakið fyrri þrjú skrefin eftir þörfum.

1. Smellið á **Hönnun** og síðan á **Bæta við töflu**.
1. Veljið einingarnar sem verður bæta við Excel-vinnubókina til breytinga miðað við gögnin sem skal breyta. Notið töfluna hér á eftir til viðmiðunar.

    | Færslugerð | Gagnaeiningar sem skal nota |
    |------------------|----------------------|
    | Staðgreiddar færslur, pantanir á netinu, ósamstilltar pantanir viðskiptavinar, ósamstillt tilboð viðskiptavinar | Færsla (sannprófanleg), sölufærsla (sannprófanleg), greiðslufærslur (sannprófanlegar), skattfærslur (sannprófanlegar), afsláttarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar) |
    | Peningaflutningur í banka | Færsla (sannprófanleg), greiðslufærslur á vörslureikningi (sannprófanlegar) |
    | Peningaflutningur í öryggisskáp | Færsla (sannprófanleg), greiðslufærslur í öryggisskáp (sannprófanlegar) |
    | Talning skiptimyntar | Færsla (sannprófanleg), talningarfærslur skiptimyntar (sannprófanlegar) |
    | Tekjur, útgjöld | Færsla (sannprófanleg), tekju-/kostnaðarfærslur (sannprófanlegar), greiðslufærslur (sannprófanlegar) |
    | Skilgreina upphafsupphæð, skiptimynt fjarlægð, skiptimyntarfærsla, greiðslumáti skiptimyntar, greiðsla reiknings, innistæða viðskiptavinar | Færsla (sannprófanleg), greiðslufærslur (sannprófanlegar) |

    > [!NOTE]
    > Gætið þess að bæta einungis einni gagnaeiningu við hverja Excel-vinnubók. Þar að auki verður að bæta öllum svæðum merktum með lykiltákni við viðeigandi Excel-vinnubók.

1. Notið áskildar síur þegar lokið er við að grunnstilla vinnubókina. Gætið þess að nota sömu síur í öllum vinnublöðum skráarinnar. Ekki hlaða miklu magni af gögnum inn í Excel-skrána. Að öðrum kosti kann að draga úr afköstum og Excel og kerfið kann að verða hægara. Mælt er með því að „fyrirtæki“ og annað hvort „númer uppgjörs“ eða „færslunúmer“ sé alltaf notað sem síur fyrir viðkomandi skrá.
1. Smellið á **Uppfæra** til að hlaða gögnunum inn eftir að grunnstillingu síanna er lokið.
1. Sláið inn áskilin gögn og birtið. Ef hnappurinn **Birta** er ekki tiltækur var lykilsvæðum líklega ekki bætt í Excel-vinnubókina.

## <a name="additional-resources"></a>Frekari upplýsingar

[Breyta og endurskoða færslur staðgreiðslu við afhendingu og stjórnun reiðufjár](edit-cash-trans.md)

[Breyta og endurskoða netpöntun og ósamstilltar færslur pöntunar viðskiptavinar](edit-order-trans.md)

[Breyta fjárhagsvíddum fyrir smásölufærslur](edit-financial-dim.md)

[Bæta svæðum við Excel-vinnubók til að breyta smásölufærslum](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]