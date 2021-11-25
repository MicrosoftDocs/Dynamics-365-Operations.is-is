---
title: Vinnusvæði Starfsmannastjórnunar
description: Þetta efnisatriði lýsir hugmyndunum á bak við vinnusvæði starfsmannastjórnunar.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPosition, HcmPersonnelManagementWorkspace
audience: Application User
ms.author: twheeloc
ms.reviewer: twheeloc
ms.search.scope: Human Resources
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4332be972ab3dc81e7e4f3cc297a91cd247e721e
ms.sourcegitcommit: 7e0e2a266d9a9473df72e207554d9bd150e17ce3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2021
ms.locfileid: "7771339"
---
# <a name="personnel-management-workspace"></a>Vinnusvæði Starfsmannastjórnunar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vinnusvæði **Starfsmannastjórnunar** inniheldur mikið efni. Það inniheldur starfsmannahreyfingar, fylgist með breytingum starfsmanna, opnar stöður, heimilisfangsbreytingar, skráningar sem renna út og greiningar og veitir tengla á sérstakar upplýsingar. Í þessu efnisatriði er að finna ítarlegar upplýsingar um hvern hluta vinnusvæðisins.

## <a name="activity-tab"></a>Aðgerðarflipi

Flipinn **Aðgerð** inniheldur hluta sem flokka starfskrafta út frá stöðu þeirra í ráðningarferlinu:

- **Umsækjendur til að ráða**
- **Byrjar bráðlega**
- **Nýlegar ráðningar**
- **Hætti**
- **Hættir**

Þegar starfsmaður er í einu af þessum stigum eru tilteknar aðgerðir í boði sem hnappur eða spjald, eða í valmyndinni sem birtist þegar þú velur úrfellingarmerkið (**...**) efst uppi hægra megin. Eftirfarandi undirkaflar lýsa hlutunum í flipanum **Aðgerð** og birtir lista yfir aðgerðirnar sem eru í boði.

### <a name="candidates-to-hire"></a>Umsækjendur til að ráða

Hlutinn **Umsækjendur til að ráða** á vinnusvæði er fylltur út frá mörgum upprunum:

- OData-eining
- LinkedIn-samþætting
- Gögn sem eru slegin inn handvirkt í afurðina

Þegar umsækjendur birtast í hlutanum **Umsækjendur sem á að ráða** er hægt að framkvæma eftirfarandi aðgerðir með því að velja úrfellingarmerkið á umsækjendaspjaldinu:

- **Hunsa umsækjanda**
- **Ekki ráða**
- **Ráða**

> [!NOTE]
> Ef verið er að fylla út umsækjendalistann frá Microsoft Dataverse munu sömu umsækjendur birtast í öllum lögaðilum vegna þess að lögaðili hefur ekki verið tengdur við umsækjanda.

### <a name="starting-soon"></a>Byrjar bráðlega

Í hlutanum **Byrjar bráðlega** sýnir starfskrafta sem eru með upphafsdag fram í tímann. Listanum er raðað eftir upphafsdegi. Upphafsdagsetningin sem er næst gögnum dagsins í dag er sýnd fyrst.

Ef stjórnandinn kemur ekki fram á spjaldinu hefur ekki verið úthlutað stöðu fyrir starfsmanninn.

> [!NOTE] 
> Við mælum með því að þú úthlutar starfsmanni stöðu áður en þú notar gátlista. Stundum er inngönguverkefnum úthlutað til yfirmanns nýráðins starfsmanns. Ef engu starfi er úthlutað er hins vegar ekki hægt að ákvarða yfirmann nýja starfsmannsins. Í því tilfelli verða ráðningarverk sem yfirmenn eiga að sjá um úthlutað á eiganda gátlistans í staðinn.

Þegar starfskraftar birtast í hlutanum **Byrja bráðlega** eru eftirfarandi aðgerðir í boði fyrir þá:

- Úthluta stöðu
- Staðfesta ráðningu
- Úthluta föstum launum
- Úthluta breytilegri uppbót
- Skoða í stigveldi
- Nota gátlista\*\*

\*\* Þessi aðgerð er sjálfgefna aðgerðin. Hún birtist sem hnappur á spjaldinu.

### <a name="recent-hires"></a>Nýlegar ráðningar

Í hlutanum **Nýlegar ráðningar** sýnir starfskrafta sem eru með nýlegan upphafsdag. Listanum er raðað eftir upphafsdegi. Upphafsdagsetningin sem er næst deginum í dag er sýnd fyrst.

Listinn sýnir sjálfgefið starfsmenn sem voru ráðnir á síðustu sjö dögum. Til að breyta þessari stillingu, á síðunni **Færibreytur Human Resources**, í flipanum **Almennt**, skal skilgreina tímaramma fyrir **Nýlegar ráðningar**. Gögnin í hlutanum **Nýlegar ráðningar** er hægt að sýna fyrir tiltekinn fjölda daga, mánaða eða ára. Til að skoða til dæmis lista yfir starfskrafta sem voru ráðnir á síðustu 14 dögum skal stilla reitinn **Tímabil** á **14** og reitinn **Eining** á **Dagar**.

> [!NOTE]
> Stillingarnar á síðunni **Færibreytur Human Resources** eru sértækar fyrirtækinu. Þess vegna getur tímaramminn sem þú skoðar fyrir nýlegar ráðningar verið mismunandi eftir fyrirtækjum. Í USMF-fyrirtækinu er til dæmis hægt að skoða allar nýjar ráðningar frá síðustu sjö dögum. Hins vegar, í USSI fyrirtækinu, gætirðu viljað skoða allar nýráðningar síðustu 14 daga. Í þessu tilviki skaltu opna **Mannauðsbreytur** síðu í hverju fyrirtæki og stilltu færibreyturnar eftir þörfum.

Ef stjórnandinn kemur ekki fram á spjaldinu hefur ekki verið úthlutað stöðu fyrir starfsmanninn.

Þegar starfskraftar birtast í hlutanum **Nýlegar ráðningar** eru eftirfarandi aðgerðir í boði fyrir þá:

- Úthluta stöðu
- Staðfesta ráðningu
- Föst laun
- Úthluta breytilegri uppbót
- Skoða í stigveldi
- Nota gátlista\*\*

\*\* Þessi aðgerð er sjálfgefna aðgerðin. Hún birtist sem hnappur á spjaldinu.

### <a name="exiting"></a>Hætti

Í hlutanum **Hættir** eru sýndir starfskraftar sem eru með starfslokadag fram í tímann. Listanum er raðað eftir starfslokadegi. Starfslokadagurinn sem er næst deginum í dag er sýndur fyrst. 

Listinn sýnir sjálfgefið starfskrafta sem eru með starfslokadag á næstu sjö dögum. Til að breyta þessari stillingu, á síðunni **Færibreytur Human Resources**, í flipanum **Almennt**, skal skilgreina tímaramma fyrir **Skoða starfskrafta sem eru að hætta**. Gögnin í hlutanum **Hættir** er hægt að sýna fyrir tiltekinn fjölda daga, mánaða eða ára. Til að skoða til dæmis lista yfir starfskrafta sem munu hætta störfum á næstu 14 dögum skal stilla reitinn **Tímabil** á **14** og reitinn **Eining** á **Dagar**.

Þegar starfskraftar birtast í hlutanum **Hættir** eru eftirfarandi aðgerðir í boði fyrir þá:

- Nota gátlista\*\*
- Staðfesta ráðningu
- Skoða í stigveldi

\*\* Þessi aðgerð er sjálfgefna aðgerðin. Hún birtist sem hnappur á spjaldinu.

### <a name="exited"></a>Hættir

Í hlutanum **Hættur** eru sýndir starfskraftar sem eru með nýlegan starfslokadag. Listanum er raðað eftir starfslokadegi. Starfslokadagurinn sem er næst deginum í dag er sýndur fyrst.

Listinn sýnir sjálfgefið starfskrafta sem eru með starfslokadag á síðustu sjö dögum. Til að breyta þessari stillingu, á síðunni **Færibreytur Human Resources**, í flipanum **Almennt**, skal skilgreina tímaramma fyrir **Skoða starfskrafta sem eru hættir**. Gögnin í hlutanum **Hættur** er hægt að sýna fyrir tiltekinn fjölda daga, mánaða eða ára. Til að skoða til dæmis lista yfir starfskrafta sem hættu störfum á síðustu 14 dögum skal stilla reitinn **Tímabil** á **14** og reitinn **Eining** á **Dagar**.

Þegar starfskraftur birtist í hlutanum **Hættur** eru eftirfarandi aðgerðir í boði fyrir hann:

- Nota gátlista\*\*
- Staðfesta ráðningu
- Skoða í stigveldi

\*\* Þessi aðgerð er sjálfgefna aðgerðin. Hún birtist sem hnappur á spjaldinu.

## <a name="employee-changes-tab"></a>Flipi starfsmannabreytinga

Flipinn **Starfsmannabreytingar** sýnir lista yfir allar starfsmannaaðgerðir starfskrafts. Þessi listi er ekki sjálfgefið í boði. Til að virkja aðgerðina skal á síðunni **Samnýttar færibreytur Human Resources**, í flipanum **Starfsmannaaðgerðir**, stilla valkostinn **Virkja aðgerðir starfskrafts** á **Já**.

## <a name="position-changes-tab"></a>Flipi stöðubreytinga

Flipinn **Stöðubreytingar** sýnir lista yfir allar starfsmannaaðgerðir stöðu. Þessi listi er ekki sjálfgefið í boði. Til að virkja aðgerðina skal á síðunni **Samnýttar færibreytur Human Resources**, í flipanum **Starfsmannaaðgerðir**, stilla valkostinn **Virkja aðgerðir stöðu** á **Já**.

## <a name="open-positions-tab"></a>Flipi fyrir opnar stöður

Flipinn **Opnar stöður** sýnir allar opnar stöður. Til að birtast á listanum verða stöður að vera með virkjunardagsetningu fyrir daginn í dag eða fyrr og þær mega ekki vera með núverandi úthlutun starfskrafts.

> [!NOTE]
> Listinn tekur til úthlutunar starfsmanns frá og með deginum í dag. Allar stöður sem hafa úthlutun starfskrafts fram í tímann munu áfram sjást í listanum. Hins vegar verður staðan fjarlægð úr listanum eftir að gildisdagsetningu á úthlutun starfskrafts er náð.

## <a name="expiring-records-tab"></a>Flipi fyrir færslur sem eru að renna út

Flipinn **Færslur sem eru að renna út** sýnir öll atriði sem hafa runnið út á tíma eða munu renna út fyrir starfskrafta í fyrirtækinu þar sem notandinn er innskráður. Eftirfarandi atriði sjást í listanum:

- **Skírteini**
- **Auðkenning**
- **Reynslutímar**
- **Skoðanir**
- **Prófanir**

Til að tilgreina hvort listinn sýnir útrunnar færslur eða færslur sem eru að renna út skal á síðunni **Færibreytur Human Resources**, í flipanum **Almennt**, skilgreina tímaramma fyrir annaðhvort **Færslur sem eru að renna út** eða **Útrunnar færslur**. Gögnin í flipanum **Færslur sem eru að renna út** er hægt að sýna fyrir tiltekinn fjölda daga. Til að skoða til dæmis listann yfir færslur sem munu renna út á næstu 14 dögum skal stilla reitinn **Fjöldi daga** á **14**.

> [!NOTE] 
> Ef þú stillir tímarammann fyrir **Útrunnar færslur** eða **Færslur sem eru að renna út** á **0** á síðunni **Færibreytur Human Resources** sýnir listinn ekki engar af þessum færslum.

## <a name="employees-tile"></a>Starfsmannareitur

Reiturinn **Starfsmenn** sýnir fjölda starfsmanna sem starfa í fyrirtækinu þar sem notandinn er innskráður. Þegar reiturinn **Starfsmenn** er valinn sýnir ný síða upplýsingar um starfsmennina.

## <a name="contractors-tile"></a>Verktakareitur

Reiturinn **Verktakar** sýnir fjölda verktaka sem starfa í fyrirtækinu þar sem notandinn er innskráður. Þegar reiturinn **Verktakar** er valinn sýnir ný síða upplýsingar um verktakana.

## <a name="open-positions-tile"></a>Reitur fyrir opnar stöður

Reiturinn **Opnar stöður** gefur upp fjölda opinna staða. Þegar reiturinn **Opnar stöður** er valinn sýnir ný síða upplýsingar um opnu stöðurnar. Til að vera teknar með í fjöldanum verða stöður að vera með virkjunardagsetningu fyrir daginn í dag eða fyrr og þær mega ekki vera með núverandi úthlutun starfskrafts.

> [!NOTE]
> Reiturinn tekur til úthlutunar starfsmanns frá og með deginum í dag. Allar stöður sem hafa úthlutun starfskrafts fram í tímann munu áfram vera hluti af talningunni. Hins vegar verður staðan fjarlægð úr talningunni eftir að gildisdagsetningu á úthlutun starfskrafts er náð.

## <a name="approvals-tile"></a>Samþykktarreitur

Reiturinn **Samþykktir** sýnir talningu á öllum atriðum verkflæðis sem bíða eftir samþykki núverandi notanda. Þegar reiturinn **Samþykktir** er valinn sýnir ný síða upplýsingar um atriði verkflæðisins sem þurfta samþykki þitt.

## <a name="address-changes-tile"></a>Reitur fyrir breytingar á aðsetri

Reiturinn **Breytingar á aðsetri** sýnir talningu á öllum breytingum aðseturs sem voru gerðar á dagafjöldanum sem er gefinn upp á síðunni **Færibreytur Human Resources**. Þegar reiturinn **Breytingar á aðsetri** er valinn, sýnir ný síða upplýsingarnar um allar breytingar á aðsetri. Efst í hægra horni síðunnar er hægt að velja **Hafa seinni tíma breytingar á aðsetri með** til að skoða breytingar á aðsetri sem eru með dagsetningu fram í tímann.

Frekari upplýsingar um hvernig á að skoða og stjórna breytingum á aðsetri er að finna í [Skoða og hafa umsjón með breytingum á aðsetri](hr-personnel-view-address-changes.md).
