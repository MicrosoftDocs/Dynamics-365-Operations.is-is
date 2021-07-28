---
title: Skilgreina Dataverse-samþættingu
description: Þú getur kveikt eða slökkt á samþættingu á milli Microsoft Dataverse og Dynamics 365 Human Resources. Einnig er hægt að skoða samstillingarupplýsingar, hreinsa rakningargögn og endursamstilla töflu til að úrræðaleita vandamál með gögn milli umhverfanna tveggja.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1a1ee5345e2d6b3736d45e233a59ac4009a9f1c8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6344689"
---
# <a name="configure-dataverse-integration"></a>Skilgreina Dataverse-samþættingu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þú getur kveikt eða slökkt á samþættingu á milli Microsoft Dataverse og Dynamics 365 Human Resources. Einnig er hægt að skoða samstillingarupplýsingar, hreinsa rakningargögn og endursamstilla töflu til að úrræðaleita vandamál með gögn milli umhverfanna tveggja.

> [!NOTE]
> Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Þegar þú slekkur á samþættingu geta notendur gert breytingar á starfsmannahaldi eða Dataverse, en þessar breytingar eru ekki samstilltar milli umhverfisins tveggja.

Sjálfgefið er að slökktu sé á samþættingu gagna milli Human Resources og Dataverse.

Þú gætir viljað slökkva á samþættingu við þessar aðstæður:

- Þú ert að fylla út gögn í gegnum Data Management Framework og verður að flytja gögnin inn nokkrum sinnum til að koma þeim í rétt ástand.

- Það eru vandamál með gögn í annaðhvort Human Resources eða Dataverse. Ef slökkt er á samþættingu geturðu eytt skrá í einu umhverfi án þess að eyða því í hinu. Þegar þú kveikir aftur á samþættingu samstillist skráin í umhverfinu þar sem henni var ekki eytt við umhverfið þar sem henni var eytt. Samstilling hefst næst þegar runuvinnslan **Dataverse samstilling missti af beiðni samstillingar** keyrir.

> [!WARNING]
> Þegar þú slekkur á samþættingu gagna, vertu viss um að þú breytir ekki sömu skránni í báðum umhverfunum. Þegar þú kveikir aftur á samþættingu verður skráin sem þú breyttir síðast samstillt. Þess vegna, ef þú gerðir ekki sömu breytingar á skránni í báðum umhverfunum, getur gagnatap orðið.

## <a name="access-the-dataverse-integration-page"></a>Aðgangur að Dataverse sameiningarsíðu

1. Í mannauðssíðunni þar sem þú vilt skoða eða stilla stillingar fyrir samþættingu við Dataverse, veldu reitinn **Kerfisstjórnun**.

    [![Reitur kerfisstjórnunar.](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Veldu flipann **Tenglar**.

    [![Tenglaflipi.](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Undir **Sameiningar**, veldu **Dataverse stillingar**.

    [![Dataverse skilgreiningartengill.](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Kveiktu eða slökktu á samþættingu gagna milli mannauðs og Dataverse

- Til að kveikja á samþættingu skal stilla valkostinn **Virkja Dataverse-samþættingu** á **Já** á síðunni **Microsoft Dataverse-samþætting**.

    > [!NOTE]
    > Þegar þú kveikir á samþættingu verða gögn samstillt næst þegar runuvinnslan **Dataverse samstilling missti af beiðni samstillingar** keyrir. Öll gögn ættu að vera tiltæk eftir að runuvinnsla er lokið.

- Til að slökkva á samþættingu skaltu stilla valkostinn á **Nei**.

[![Kveikt eða slökkt á Dataverse samþættingunni.](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Við mælum eindregið með því að slökkva á Dataverse-samþættingu þegar gagnasamþættingarverk er framkvæmt. Stórar upphleðslur gagna geta haft umtalsverð áhrif á afköst. Til dæmis getur upphleðsla á 2000 starfsmönnum tekið nokkrar klukkustundir þegar kveikt er á samþættingu, og innan við klukkustund þegar slökkt er á henni. Tölurnar sem gefnar eru upp í þessu dæmi eru til sýnis eingöngu. Tíminn sem það nákvæmlega tekur að flytja inn færslur getur verið mjög breytilegur vegna ýmissa þátta.

## <a name="view-data-integration-details"></a>Skoða upplýsingar um gagnasamþættingu

Í flýtiflipanum **Stjórnun** á síðunni **Microsoft Dataverse-samþætting** er hægt að sjá hvernig línur eru tengdar saman milli Human Resources og Dataverse.

- Til að skoða línur fyrir töflu skal velja töfluna í reitnum **Dataverse-tafla**. Hnitanetið sýnir allar línur sem eru tengdar við valda töflu.

> [!NOTE]
> Ekki eru allar Dataverse-töflur á listanum sem stendur. Aðeins töflur sem styðja notkun sérstilltra reita birtast í hnitanetinu. Nýjar töflur verða fáanlegar með áframhaldandi útgáfum Human Resources.

Taflan inniheldur eftirfarandi reiti:

- **Dataverse-tafla** – Heiti töflunnar í Dataverse.
- **Dataverse-töflutilvísun** – Kennið sem Dataverse notar til að auðkenna færslu. Þetta gildi jafngildir Human Resources gildinu **RecId**. Kennið er hægt að finna þegar Dataverse-taflan í Microsoft Excel er opnuð.
- **Einingarheiti Human Resources** – Eining Human Resources sem síðast samstillti gögn við Dataverse. Einingin getur haft annaðhvort Dataverse forskeyti eða annað forskeyti.
- **Tilvísun Human Resources** - Gildið **RecId** sem er tengt skránni í Human Resources.
- **Eytt úr Dataverse** – Gildi sem segir til um hvort línu var eytt úr Dataverse.

> [!NOTE]
> Færslur í Human Resources samsvara línum í Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Fjarlægja tengingu á færslu Human Resources úr Dataverse-línu

Ef þú lendir í vandræðum við samstillingu gagna milli mannauðs og Dataverse, gætirðu verið fær um að leysa þau með því að hreinsa mælingarnar og láta endurstilla rakningartöfluna. Ef tenging er fjarlægð og línu síðan breytt eða henni eytt í Dataverse verða breytingarnar ekki samstilltar við Human Resources. Ef gerðar eru breytingar á Human Resources verður ný rakningarfærsla stofnuð og línan verður uppfærð í Dataverse.

- Til að fjarlægja tengingu á færslu Human Resources og Dataverse-línu skal velja töfluna í reitnum **Dataverse-tafla** og síðan velja **Hreinsa rakningarupplýsingar**.

[![Hreinsa rakningarupplýsingar.](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Til að keyra fulla samstillingu á töflunni eftir að rakning er hreinsuð skal sjá næsta skref.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Samstilla töflu á milli Human Resources og Dataverse

Notaðu þetta ferli þegar:

- Breytingar úr Dataverse taka of langan tíma að birtast í Human Resources.

- Þú verður að endurræsa rakningartöfluna þegar þú hefur eytt rakningunni.

Til að keyra fulla samstillingu á töflu milli Human Resources og Dataverse:

1. Veljið töfluna í reitnum **Dataverse-tafla**.

2. Veldu **Samstilla núna**.

[![Keyra fulla samstillingu.](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Sjá einnig

[Dataverse töflur](hr-developer-entities.md)<br>
[Skilgreina Dataverse-sýndartöflur](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Algengar spurningar um sýndartöflur Human Resources](hr-admin-virtual-entity-faq.md)<br>
[Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Hugtakauppfærslur](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]