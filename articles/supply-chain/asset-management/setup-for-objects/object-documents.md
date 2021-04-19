---
title: Eignaskjöl
description: Þetta efni skýrir eignaskjöl í eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8458c302b506f9f048b7886f55a392d9afceb446
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808377"
---
# <a name="asset-documents"></a>Eignaskjöl

[!include [banner](../../includes/banner.md)]

 

Þetta efni skýrir eignaskjöl í eignastýringu.

Í eignastýringu geturðu sett upp skjöl þannig að þau tengjast sjálfkrafa starfstegundum, eignaframleiðendum, eignategundum eða eignum til dæmis. Þessi virkni er gagnleg þegar uppfærðar útgáfur skjala eru gefnar út. Í því tilfelli þarftu bara að setja uppfærða skjalið á staðalstaðinn sem þú notar fyrir þig Supplu Chain Management skjöl og hengdu skjalið við eignaskjalaskrána sem þú hefur búið til. Síðan er hægt að nálgast uppfærða skjalið frá **Allar eignir**, **Virkar eignir**, **Virku eignir mínar**, **Allar vinnupantanir**, og **Virk störf til pöntunar** valmyndaratriðin. Ferlið til að hengja skjöl við eignaskjalaskrá notar staðlaða skjal meðhöndlunarkerfisins.

**Dæmi 1:** Skjal sem tengist starfstegund gæti lýst verklagi fyrir þá starfstegund.

**Dæmi 2:** Skjal sem er tengt samsetningu eignategundar, framleiðanda og líkans gæti verið staðlaða handbók fyrir valið líkan eignaframleiðanda.

## <a name="create-asset-document-relation"></a>Stofna tengsl eignaskjals

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignaskjöl**.
2. Veldu **Nýtt** til að búa til skrá eignaskjals.
3. Það fer eftir hversu sértækt þú vilt að skjalatengslin séu en gerðu viðeigandi val í einum eða fleiri eftirfarandi reita: **Eignagerð**, **Framleiðandi**, **Líkan**, **Eign**, **Starfsflokkur**, **Starfsgerð**, **Atvinnugerðafbrigði**, og **Vinnsluþörf**. Valkostirnir sem eru í boði í **Atvinnugerðafbrigði** og **Starfsskylda** reitirnir fara eftir vali þínu í reitnum **Atvinnugerð**.

    > [!NOTE]
    > Þegar kerfið leitar að skjölum sem ættu að tengjast eign eða verkpöntun fer Eignastjórn í gegnum allar eignaskjalaskrár til að athuga hvort mögulegt sé samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, Eignastjórnun kannar fyrst hvort samsvörun finnist fyrir reitinn **Vinnsluþörf**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Atvinnugerðafbrigði**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Vinnslugerð** og svo framvegis. Eins og þú sérð á skipulagi síðunnar **Eignaskjöl** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik. Nokkur skjöl gætu verið tengd eign eða verkpöntun. Þú getur breytt þjónustustiginu í viðhaldsbeiðni eða vinnupöntun eins og þú þarft.

4. Veldu **Viðhengi**. Staðalsíðan **Meðhöndlun skjala** birtist.
5. Settu upp skjölin eða athugasemdirnar sem eiga að fylgja skránni yfir eigna skjalið. Eftir að þú hefur fest skjöl við **Viðhengi** reiturinn sýnir fjölda skjala sem tengjast skránni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]