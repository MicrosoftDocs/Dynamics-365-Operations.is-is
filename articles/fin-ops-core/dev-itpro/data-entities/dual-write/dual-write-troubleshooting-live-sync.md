---
title: Úrræðaleit í beinni samstillingarvandamál
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með beinni samstillingu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275418"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Úrræðaleit í beinni samstillingarvandamál

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með beinni samstillingu.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Lifandi samstilling kastar 403 Forbidden villa þegar þú býrð til skrá í forriti Finance and Operations

Þú gætir fengið eftirfarandi villuboð þegar þú stofnar skrá í forriti Finance and Operations:

*\[{\\"villa\\":{\\"kóði\\":\\"0x80072560\\",\\"skilaboð\\":\\"Notandinn er ekki meðlimur í fyrirtækinu.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*

Til að laga vandann fylgirðu skrefunum í [Kerfiskröfur og forsendur](requirements-and-prerequisites.md). Til að ljúka þessum skrefum verða notendur tvískiptra forrita sem eru búnir til í Common Data Service að hafa kerfisstjórarhlutverkið. Sjálfgefið eigendateymi verður einnig að hafa kerfisstjórarhlutverkið.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Lifandi samstilling fyrir einingu sýnir stöðugt svipaða villu þegar þú býrð til skrá í forriti Finance and Operations

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið villuboð eins og eftirfarandi í hvert skipti sem þú reynir að vista gögn um einingar í forriti Finance and Operations:

*Ekki hægt að vista breytingarnar í gagnagrunninum. Vinnueining getur ekki gert færslu. Ekki er hægt að skrifa gögn í mælieiningar einingar. Skrifun í UnitOfMeasureEntity mistókst með villuboðin Ekki var hægt að samstilla við mælieiningar einingar.*

Til að laga málið verður þú að ganga úr skugga um að forsendur tilvísunargagna séu til í bæði forriti Finance and Operations og Common Data Service. Til dæmis ef viðskiptavinurinn sem þú ert í forriti Finance and Operations tilheyrir ákveðnum viðskiptavinahópi skaltu ganga úr skugga um að viðskiptavinahópurinn sé til í Common Data Service.

Fylgdu þessum skrefum ef gögn eru til af báðum hliðum og þú hefur staðfest að málið er ekki gagnatengt.

1. Stöðvaðu tengda einingu.
2. Skráðu þig inn í forrit Finance and Operations og passaðu að skrár fyrir eininguna sem mistekst séu til í töflunum DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration. Hér er til dæmis hvernig fyrirspurnin lítur út ef einingin **Viðskiptavinir** er að mistakast.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Ef það eru skrár fyrir eininguna sem fellur ekki út jafnvel eftir að þú hættir vörpunar einingarinnar skaltu eyða þeim gögnum sem tengjast einingunni sem mistakast. Gerðu athugasemd við dálkinn **projectname** í DualWriteProjectConfiguration töflunni og sæktu færsluna í DualWriteProjectFieldConfiguration töfluna með því að nota verkefnisheitið til að eyða skránni.
4. Hefja vörpun einingarinnar. Staðfestu hvort gögnin séu samstillt án nokkurra vandamála.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Meðhöndla villur til að lesa eða skrifa réttindi þegar þú býrð til gögn í forriti Finance and Operations

Þú gætir fengið villuboð „Slæm beiðni“ sem líkjast eftirfarandi dæmi þegar þú býrð til gögn í forriti Finance and Operations.

![Dæmi um villuboðin Bad Request](media/error_record_id_source.png)

Til að laga málið verður þú að úthluta réttu öryggishlutverki til teymis kortlagða Dynamics 365 Sales eða Dynamics 365 Customer Service til að gera það sem vantar réttindi.

1. Í forriti Finance and Operations finnurðu viðskiptaeininguna sem er varpað í gagnasamsetningar tengingarsettinu.

    ![Fyrirtækjavörpun](media/mapped_business_unit.png)

2. Skráðu þig inn í umhverfið í líkanadrifna forritinu í Dynamics 365, farðu í **Stilling \> Öryggi** og finndu hóp varpaðrar viðskiptaeiningar.

    ![Hópur varpaðrar viðskiptaeiningar](media/setting_security_page.png)

3. Opnaðu síðuna fyrir hópinn sem á að breyta og veldu síðan **Stjórna hlutverkum** til að opna valmyndina **Stjórna hóphlutverkum**.

    ![Hnappurinn Stjórna hlutverkum](media/manage_team_roles.png)

4. Úthlutaðu hlutverkinu sem hefur lestrar-/skriftarréttindi fyrir viðkomandi einingar og veldu síðan **Í lagi**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>Laga samstillingarvandamál í umhverfi sem er með nýlega breytt Common Data Service umhverfi

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú stofnar gögn í forriti Finance and Operations:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Ekki tókst að mynda farm fyrir eininguna CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Stofnun farms tókst ekki með villunni Ógilt URI: URI er tómt."}\],"isErrorCountUpdated":true}*

Svona lítur villan út í líkanadrifnu forritinu í Dynamics 365:

*Óvænt villa kom upp úr ISV kóða. (ErrorType = ClientError) Óvænt undantekning frá viðbót (Keyra): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: tókst ekki að vinna úr einingareikningi - (Tengingartilraun mistókst vegna þess að tengdur aðili svaraði ekki á fullnægjandi hátt eftir nokkurn tíma, eða ekki tókst að koma á tengingu vegna þess að tengdur hýsill svaraði ekki*

Þessi villa kemur upp þegar Common Data Service umhverfi er rangt endurstillt á sama tíma og þú reynir að búa til gögn í forriti Finance and Operations.

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Skráðu þig inn á Finance and Operations sýndarvél (VM), opnaðu SQL Server Management Studio (SSMS) og leitaðu að gögnum í DUALWRITEPROJECTCONFIGURATIONENTITY töflunni þar sem **internalentityname** jafngildir **Viðskiptavinir V3** og **externalentityname** jafngildir **reikningar**. Hér er hvernig fyrirspurnin lítur út.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Notaðu heiti verkefnisins úr niðurstöðum fyrri fyrirspurnar til að keyra eftirfarandi fyrirspurn.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Gakktu úr skugga um að dálkurinn **externalenvironmentURL** sé með rétt Common Data Service eða forritsslóð. Eyða afritaskrám sem benda á ranga Common Data Service vefslóð. Eyða samsvarandi gögnum í DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION töflunum.
4. Hættu að varpa einingunni og endurræstu hana síðan
