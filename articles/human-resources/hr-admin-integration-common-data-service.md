---
title: Skilgreina Common Data Service-samþættingu
description: Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og tilviks af Microsoft Dynamics 365 Human Resources. Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009384"
---
# <a name="configure-common-data-service-integration"></a>Skilgreina Common Data Service-samþættingu

Þú getur kveikt eða slökkt á samþættingu á milli Common Data Service og tilviks af Microsoft Dynamics 365 Human Resources. Þú getur einnig skoðað upplýsingar um samstillingu, hreinsað mælingargögn og endurstillt eining til að hjálpa til við að leysa úr gögnum á milli umhverfanna tveggja.

Þegar þú slekkur á samþættingu geta notendur gert breytingar á starfsmannahaldi eða Common Data Service, en þessar breytingar eru ekki samstilltar milli umhverfisins tveggja.

Sjálfgefið er annaðhvort er slökkt eða kveikt á samþættingu Human Resources og Common Data Service slökkt eða slökkt, allt eftir tilvist sýnigagna í umhverfinu:

- **Slökkt** fyrir nýtt umhverfi sem inniheldur ekki kynningargögn
- **Kveikt** fyrir nýtt umhverfi sem inniheldur kynningargögn

Nýtt umhverfi sem inniheldur prufugögn mun byrja að samstilla gögn þegar þeim er úthlutað.

Þú gætir viljað slökkva á samþættingu við þessar aðstæður:

- Þú ert að fylla út gögn í gegnum Data Management Framework og verður að flytja gögnin inn nokkrum sinnum til að koma þeim í rétt ástand.

- Það eru vandamál með gögn í annaðhvort Human Resources eða Common Data Service. Ef slökkt er á samþættingu geturðu eytt skrá í einu umhverfi án þess að eyða því í hinu. Þegar þú kveikir aftur á samþættingu verður skráin í umhverfinu þar sem henni var ekki eytt samstillt aftur við umhverfið þar sem henni var eytt. Samstilling hefst næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir.

> [!WARNING]
> Þegar þú slekkur á samþættingu gagna, vertu viss um að þú breytir ekki sömu skránni í báðum umhverfunum. Þegar þú kveikir aftur á samþættingu verður skráin sem þú breyttir síðast samstillt. Þess vegna, ef þú gerðir ekki sömu breytingar á skránni í báðum umhverfunum, getur gagnatap orðið.

## <a name="access-the-common-data-service-integration-page"></a>Aðgangur að Common Data Service sameiningarsíðu

1. Í mannauðssíðunni þar sem þú vilt skoða eða stilla stillingar fyrir samþættingu við Common Data Service, veldu reitinn **Kerfisstjórnun**.

    [![Reiturinn Kerfisstjórnun](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Veldu flipann **Tenglar**.

    [![Tegnlaflipi](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Undir **Sameiningar**, veldu **Common Data Service stillingar**.

    [![Common Data Service skilgreiningartengill](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Kveiktu eða slökktu á samþættingu gagna milli mannauðs og Common Data Service

- Til að kveikja á samþættingu skaltu stilla valkostinn **Virkja samþættingu við Common Data Service** á **Já**.

    > [!NOTE]
    > Þegar þú kveikir á samþættingu verða gögn samstillt næst þegar runuvinnslan **Common Data Service samstilling missti af beiðni samstillingar** keyrir. Öll gögn ættu að vera tiltæk eftir að runuvinnsla er lokið.

- Til að slökkva á samþættingu skaltu stilla valkostinn á **Nei**.

[![Kveikt eða slökkt á Common Data Service samþættingu](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Skoða upplýsingar um gagnasamþættingu

Á flýtiflipanum **Stjórnun** á síðunni **Common Data Service samþætting** er hægt að sjá hvernig skrár eru tengdar saman milli Human Resources og Common Data Service.

- Til að skoða skrár fyrir einingu velurðu aðilann í reitnum **Heiti CDS einingar**. Taflan sýnir allar færslur sem eru tengdar völdum einingum.

[![Skoða færslur fyrir einingu](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Ekki eru allar einingar Common Data Service eru sem stendur skráðar. Aðeins einingar sem styðja notkun sérsniðinna reita birtast í töflunni. Nýjar einingar verða tiltækar með stöðugu losun Human Resources.

Taflan inniheldur eftirfarandi reiti:

- **CDS-einingaheiti** - Heiti öryggiseiningarinnar í Common Data Service.
- **Tilvísun CDS einingar** - Kennimerkið sem Common Data Service notar til að bera kennsl á skrá. Þetta gildi jafngildir Human Resources gildinu **RecId**. Þú getur fundið kennimerki þegar þú opnar Common Data Service einingu í Microsoft Excel.
- **Einingaheiti Human Resources** - Einingin sem síðast samstillti gögn við Common Data Service. Einingin getur haft annaðhvort Common Data Service forskeyti eða annað forskeyti.
- **Tilvísun Human Resources** - Gildið **RecId** sem er tengt skránni í Human Resources.
- **Var eytt úr CDS** - Gildi sem gefur til kynna hvort skránni hafi verið eytt úr Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Fjarlægðu tengsl skrárinnar í Human Resources úr Common Data Service

Ef þú lendir í vandræðum við samstillingu gagna milli mannauðs og Common Data Service, gætirðu verið fær um að leysa þau með því að hreinsa mælingarnar og láta endurstilla rakningartöfluna. Ef þú fjarlægir tenginguna og breytir síðan eða eyðir skrá í Common Data Service, breytingarnar verða ekki samstilltar við Human Resources. Ef þú gerir breytingar á Human Resources verður ný rekja rakningarskrá til og færslan uppfærð í Common Data Service.

- Til að fjarlægja tengsl skrár milli mannauðs og Common Data Service, veldu eininguna í reitnum **Heiti CDS einingar** og veldu síðan **Hreinsa rakningarupplýsingar**.

[![Hreinsun rakningarupplýsinga](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Sjá næstu aðferð til að keyra fulla samstillingu á einingunni eftir að þú hefur eytt mælingunni.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Samstilltu eining milli Human Resources og Common Data Service

Notaðu þessa aðferð ef breytingar eru frá Common Data Service tekur of langan tíma að birtast í Human Resources, eða ef þú verður að endurnýja mælingarborðið eftir að þú hefur hreinsað mælingarnar.

- Til að keyra fulla samstillingu á aðila milli mannauðs og Common Data Service, veldu eininguna í reitnum **Heiti CDS einingar** og veldu síðan **Samstilla núna**.

[![Keyri fulla samstillingu](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)


