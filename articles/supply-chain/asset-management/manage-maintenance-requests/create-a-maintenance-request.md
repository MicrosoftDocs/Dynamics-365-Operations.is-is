---
title: Stofna viðhaldsbeiðnir
description: Þetta efni útskýrir hvernig á að stofna viðhaldsbeiðni í eignastjórnun.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7fc9ec2f6a9a8a11d824e4b5c13d5aa173541454
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571922"
---
# <a name="create-maintenance-requests"></a>Stofna viðhaldsbeiðnir

[!include [banner](../../includes/banner.md)]

 

Hægt er að nota viðhaldsbeiðnir ef viðhaldsstarfsmenn eða framleiðsluaðilar uppgötva að búnaður þarfnast viðgerðar, en ekki er hægt að gera viðgerðirnar strax.

**Dæmi:** Á meðan viðhaldsstarfsmaður er að gera við, uppgötvar hún að þjónusta verður aðra eign á sama stað. Viðhaldsstarfsmaðurinn hefur þó ekki tíma eða nauðsynlega varahluti til að framkvæma viðgerðarstarfið. Þess vegna býr hún til viðhaldsbeiðni um eignina og slærð inn stutta lýsingu á vandamálinu.

Hlutinn **Virkar viðhaldsbeiðnir** á rúðunni **Tengdar upplýsingar** hægra megin við síðuna **Allar eignir** eða **Virkar eignir** (**Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**) sýnir virkar viðhaldsbeiðnir sem eru tengdar við valda eign.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Viðhaldsbeiðnir** \> **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.
2. Veljið **Nýtt**.
3. Í svarglugganum **Stofna beiðni** í reitnum **Gerð viðhaldsbeiðni** velurðu gerð viðhaldsbeiðni. Mælt er með sjálfgefinni gerð.
4. Í reitnum **Lýsing** slærðu inn heiti eða titil sem lýsir viðhaldsbeiðninni stuttlega.
5. Í reitunum **Virk staðsetning** og **Eignir** velurðu virka staðsetningu eða eign eða sambland af virkri staðsetningu og eign, eftir þörfum. Þú getur stofnað viðhaldsbeiðni án þess að velja eign og hægt er að bæta eigninni við viðhaldsbeiðnina seinna. Ef viðhaldsstarfsmaðurinn sem er skráður inn í tengist auðlind sem er tengd eign er reiturinn **Eignir** er sjálfkrafa stilltur.

    Ef viðhaldsbeiðni er þegar fest við valda eign birtist skilaboðastika efst í valmyndinni **Stofna beiðni** til að láta þig vita um auðkenni núverandi viðhaldsbeiðni. Skilaboðastika tilkynnir þér einnig ef eignin fellur undir ábyrgðarsamning.

6. Í reitnum **Þjónustustig** velurðu þjónustustig sem gefur til kynna hversu brýn beiðnin er.
7. Ef þú valdir eign í þrepi 5 geturðu notað reitina **Bilunareinkenni**, **Bilunarsvæði** og **Bilunartegund** til að búa til villuskráningu.
8. Ef viðhaldsbeiðnin hefur valdið niðurtíma vegna viðhalds skaltu slá inn upphafsdagsetningu og -tíma niðurtímans.

    Reiturnn **Sett af stað af** er sjálfkrafa stilltur á nafnið þitt.

10. Reiturinn **Raunverulegt upphaf** er sjálfkrafa stilltur á núverandi dagsetningu og tíma. Þó er hægt að breyta gildinu eftir þörfum.
11. Í reitnum **Athugasemdir** slærðu inn allar viðbótar athugasemdir sem þarf.
12. Veljið **Í lagi**.

![Stofna viðhaldsbeiðni](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Síðari afgreiðsla beiðna um viðhald

Eftir að viðhaldsbeiðni er stofnuð, en áður en henni er breytt í vinnupöntun, ætti að uppfæra ýmsar upplýsingar um hana. Venjulega klárar skipuleggjandi eða annar stjórnandi starfsmaður þetta verkefni.

- Á síðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** velurðu beiðnina sem þú vilt vinna með og velur síðan **Breyta**.

Í upplýsingayfirlitinu geturðu uppfært ýmsar upplýsingar. Hér eru nokkur dæmi:

- Veldu og staðfestu eignina. Ef þú verður að velja aðra eign seinna geturðu stillt valkostinn **Eignir staðfestar** á **Nei**.
- Veldu ábyrgan starfsmannahóp og/eða ábyrgan viðhaldsstarfsmann. Nánari upplýsingar um nauðsynlega uppsetningu, sjá [Ábyrgir viðhaldsstarfskraftar](../setup-for-maintenance-requests/responsible-workers.md).
- Veldu gerð viðhaldsverks og, ef þessar upplýsingar eru viðeigandi, tengt afbrigði viðhaldsverks og ði og atvinnuverslun.
- Í reitunum **Breidd** og **Lengdargráða** slærðu inn landfræðileg hnit. Öll hnit sem er bætt við viðhaldsbeiðni eru sjálfkrafa færð yfir í tengda verkbeiðni. 

![Uppfæra viðhaldsbeiðni](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Ef þú velur eign þegar þú býrð til viðhaldsbeiðni geturðu bætt einni villu við eignina. Eftir að viðhaldsbeiðnin hefur verið stofnuð geturðu bætt við fleiri göllum eftir þörfum. Til að bæta við göllum velurðu **Eignavilla** á síðunni **Allar viðhaldsbeiðnir**.
