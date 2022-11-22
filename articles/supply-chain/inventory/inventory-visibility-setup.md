---
title: Setja upp innbót birgðasýnileika
description: Þessi grein lýsir því hvernig á að setja upp Inventory Visibility Add-in fyrir Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762782"
---
# <a name="install-and-set-up-inventory-visibility"></a>Setja upp Inventory Visibility

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp Inventory Visibility Add-in fyrir Microsoft Dynamics 365 Supply Chain Management.

Þú verður að nota [Microsoft Dynamics Lífsferilsþjónusta](https://lcs.dynamics.com/v2) til að setja upp Inventory Visibility Add-in. Lifecycle Services er samstarfsgátt sem býður upp á umhverfi og safn af reglulega uppfærðum þjónustu sem hjálpa þér að stjórna líftíma forrita fjármála- og rekstrarforrita. Frekari upplýsingar er að finna í [Tilföng Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Við mælum með því að þú skráir þig í Inventory Visibility Add-in notendahópinn, þar sem þú getur fundið gagnlegar leiðbeiningar, fengið nýjustu uppfærslurnar okkar og sent inn allar spurningar sem þú gætir haft um notkun Birgðasýnileika. Til að taka þátt, vinsamlegast sendu tölvupóst til vöruteymisins Birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) og hafðu með þér auðkenni birgðakeðjustjórnunarumhverfis.

## <a name="inventory-visibility-prerequisites"></a>Skilyrði birgðasýnileika

Áður en þú setur upp birgðasýnileika verður þú að ljúka eftirfarandi verkum:

- Fáðu innleiðingarverkefni líftímaþjónustu þar sem að minnsta kosti eitt umhverfi er notað.
- Vertu viss um að lokið hafi verið við skilyrðin fyrir uppsetningu innbóta. Upplýsingar um þessar forsendur er að finna í [Yfirlit innbóta](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Sýnileiki birgða krefst ekki tengingu tvöföldrar skráningar.

> [!NOTE]
> Löndin og svæðin sem nú eru studd eru Kanada (CCA, ECA), Bandaríkin (WUS, ESB), Evrópusambandið (NEU, WEU), Bretland (SUK, Wuk), Ástralía (EAU, SEAU), Japan (EJP, WJP) og Brasilía (SBR, SCUS).

Ef einhverjar spurningar vakna um þessi skilyrði skaltu hafa samband við vöruteymi birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Setja upp innbót birgðasýnileika

Áður en þú setur upp innbótina skaltu skrá forrit og bæta leyniorði biðlara við Azure Active Directory (Azure AD) undir Azure-áskriftinni þinni. Leiðbeiningar er að finna í [Skrá forrit](/azure/active-directory/develop/quickstart-register-app) og [Bæta við leyniorði biðlara](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Vertu viss um að taka mið af **Auðkenni umsóknar (viðskiptavinar).**, **viðskiptavinar**, og **Auðkenni leigjanda** gildi, því þú þarft á þeim að halda síðar.

> [!IMPORTANT]
> Ef þú ert með fleiri en eitt Lifecycle Services umhverfi skaltu búa til annað Azure AD umsókn fyrir hvert þeirra. Ef þú notar sama forritsauðkenni og leigjandaauðkenni til að setja upp birgðasýnileikaviðbótina fyrir mismunandi umhverfi, mun táknvandamál eiga sér stað fyrir eldra umhverfi. Þar af leiðandi mun aðeins síðasta uppsetningin gilda.

Eftir að þú hefur skráð forrit og bætt leyniorði biðlara við Azure AD skaltu fylgja þessum skrefum til að setja upp innbót birgðasýnileika.

1. Skrá inn [Lífsferilsþjónusta](https://lcs.dynamics.com/Logon/Index).
1. Á heimasíðunni skal velja verkið þar sem umhverfið er í notkun.
1. Á verksíðunni skal velja umhverfið þar sem á að setja upp innbótina.
1. Á heimasíðu umhverfisins skal fletta niður þar til þú finnur hlutann **Innbætur umhverfis** í hlutanum **Power Platform samþætting**. Þar má finna heiti Dataverse umhverfisins. Staðfestu að heiti Dataverse umhverfis er það sem þú vilt nota fyrir birgðasýnileika.

    > [!NOTE]
    > Eins og er, aðeins Dataverse umhverfi sem var búið til með því að nota Lifecycle Services eru studd. Ef þín Dataverse umhverfi var búið til á annan hátt (til dæmis með því að nota PowerApps Admin Center), og ef það er tengt við Supply Chain Management umhverfið þitt, verður þú fyrst að laga kortlagningarvandann áður en þú setur upp Inventory Visibility Add-in.
    >
    > Það er mögulegt að dual-write umhverfið þitt sé tengt við a Dataverse dæmi á meðan Lifecycle Services er ekki sett upp fyrir Power Platform samþættingu. Þetta ósamræmi við tengingar getur valdið óvæntri hegðun. Við mælum með því að upplýsingar um líftímaþjónustu umhverfisins passi við það sem þú ert tengdur við í tvískrift svo hægt sé að nota sömu tenginguna fyrir viðskiptaviðburði, sýndartöflur og viðbætur. Sjáðu [Ósamræmi við tengingar](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) til að fá upplýsingar um hvernig eigi að laga kortlagningarvandann. Þegar kortlagningarvandamálið er leyst geturðu haldið áfram að setja upp Birgðasýnileika.

1. Í hlutanum **Innbætur umhverfis** skal velja **Setja upp nýja innbót**.

    ![Umhverfissíða í Lifecycle Services](media/inventory-visibility-environment.png "Umhverfissíða í Lifecycle Services")

1. Veldu tengilinn **Setja upp nýja innbót**. Listi yfir tiltækar innbætur birtist.
1. Í listanum skal velja **Birgðasýnileika**.
1. Stilltu eftirfarandi reiti fyrir umhverfið þitt:

    - **Auðkenni AAD-forritsins (biðlara)** – Sláðu inn Azure AD forritskennið sem þú bjóst til og skráðir hjá þér hér á undan.
    - **AAD-leigjandakenni** – Sláðu inn leigjandakennið sem þú skráðir hjá þér hér á undan.

    ![Uppsetningarsíða innbótar](media/inventory-visibility-setup.png "Uppsetningarsíða innbótar")

1. Samþykktu skilmálana með því að velja gátreitinn **Skilmálar**.
1. Velja **Setja upp**. Staða innbótar er sýnd sem **Í uppsetningu**. Þegar uppsetningunni er lokið skaltu endurhlaða síðuna. Staðan ætti að breytast í **Uppsett**.
1. Í Dataverse skal velja hlutann **Forrit** í vinstra yfirlitinu og staðfesta að **Birgðasýnileiki** Power Apps sé uppsettur. Ef hlutinn **Forrit** er ekki til skal hafa samband við afurðateymi birgðasýnileika í [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Ef kerfið varar þig við því að þú hafir ekki heimild til að setja upp Birgðasýnileika á Lifecycle Services, verður þú að hafa samband við kerfisstjórann til að breyta heimildinni þinni.
>
> Ef það tekur meira en klukkutíma að setja upp frá Lifecycle Services síðunni, þá skortir notendareikninginn þinn líklega leyfi til að setja upp lausnir í Dataverse umhverfi. Fylgdu þessum skrefum til að leysa málið:
>
> 1. Hætta við uppsetningarferlið Birgðasýnileikaviðbót af síðunni Lifecycle Services.
> 1. Skráðu þig inn á [Microsoft 365 stjórnendamiðstöð](https://admin.microsoft.com) og vertu viss um að notendareikningurinn sem þú vilt nota til að setja upp viðbótina hafi "Dynamics 365 Unified Operations Plan" leyfi sem henni er úthlutað. Úthlutaðu leyfinu ef þörf krefur.
> 1. Skráðu þig inn á [Power Platform stjórnendamiðstöð](https://admin.powerplatform.microsoft.com) með því að nota viðkomandi notandareikning. Settu síðan upp birgðasýnileikaviðbótina með því að gera eftirfarandi skref:
>     1. Veldu umhverfið þar sem þú vilt setja viðbótina upp.
>     1. Veldu **Dynamics 365 forrit**.
>     1. Veldu **Settu upp app**.
>     1. Veldu **Birgðasýnileiki**
>
> 1. Eftir að uppsetningunni er lokið, farðu aftur á síðu Lifecycle Services og reyndu aftur að setja upp aftur **Birgðasýnileiki** Bæta við.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Setja upp birgðasýnileika í Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Nota samþættingarpakka birgðasýnileika

Ef keyrð er útgáfa 10.0.17 eða eldri af Supply Chain Management skal hafa samband við stuðningshóp vegna innleiðingar birgðasýnileika á [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) til að fá skráarpakkann. Dreifðu síðan pakkanum í Lifecycle Services.

> [!NOTE]
> Ef villa vegna misræmis útgáfu kemur upp í uppsetningunni þarf að flytja inn handvirkt X++ verkið í þróunarumhverfið. Síðan skal stofna virkjanlega pakkann í þróunarumhverfinu og setja hann upp í þróunarumhverfinu.
>
> Kóðinn fylgir með Supply Chain Management útgáfu 10.0.18. Ef sú útgáfa eða nýrri er keyrð þarf ekki uppsetningu.

Gangið úr skugga um að kveikt sé á eftirfarandi eiginleikum í umhverfi Supply Chain Management. (Sjálfgefið er að kveikt er á þeim.)

| Lýsing eiginleika | Kóðaútgáfa | Skipta milli klasa |
|---|---|---|
| Gera notkun birgðavídda í InventSum-töflu virka eða óvirka      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Gera notkun birgðavídda í InventSumDelta-töflu virka eða óvirka | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Setja upp samþættingu fyrir Sýnileika birgða

Þegar þú hefur sett viðbótina upp skaltu undirbúa Supply Chain Management kerfið þitt til að vinna með það með því að gera eftirfarandi skref.

1. Í Supply Chain Management skal opna vinnusvæðið **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og kveikja á eftirfarandi eiginleikum:
    - *Samþætting sýnileika birgða* – Áskilið.
    - *Samþætting birgðasýnileika með mótbókun frátekningar* – Ráðlagt en valfrjálst. Krefst útgáfu 10.0.22 eða nýrri. Frekari upplýsingar er að finna í [Frátekningar birgðasýnileika](inventory-visibility-reservations.md).

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**.
1. Opnaðu flipann **Almennt** og gerðu eftirfarandi stillingar:
    - **Endastöð sýnileika birgða** – Færðu inn vefslóð umhverfisins þar sem þú keyrir birgðasýnileika. Frekari upplýsingar er að finna í [Finna endastöð þjónustu](inventory-visibility-configuration.md#get-service-endpoint).
    - **Hámarksfjöldi færslna í einni beiðni** – Stilltu á hámarksfjölda færslna sem á að hafa með í einni beiðni. Þú verður að færa inn jákvæða heiltölu sem er minna en eða jafnt og 1000. Sjálfgildið er 512. Við mælum eindregið með því að halda sjálfgefna gildinu nema þú hafir fengið ráðgjöf frá notendaþjónustu Microsoft eða sért á annan hátt viss um að þú þurfir að breyta því.

1. Ef þú virkjaðir valfrjálsa eiginleikann *Samþætting birgðasýnileika með mótbókun frátekningar* skaltu opna flipann **Mótbókun frátekningar** og gera eftirfarandi stillingar:
    - **Virkja mótbókun frátekningar** – Stilltu á *Já* til að virkja þessa virkni.
    - **Breytilykill fyrir mótbókun frátekningar** – Veldu stöðu birgðafærslu sem mun mótbóka frátekningar sem gerðar eru í birgðasýnileika. Þessi stilling ákvarðar stöðu pöntunarúrvinnslu sem setur af stað mótbókanir. Staða á birgðafærslu pöntunar sér um að rekja stigið. Veldu einn af eftirfarandi valkostum:
        - *Í pöntun* – Fyrir stöðuna *Í færslu* mun pöntun senda beiðni um mótbókun þegar hún er stofnuð. Magn mótbókunar verður magn stofnaðrar pöntunar.
        - *Taka frá* – Fyrir stöðuna *Taka frá pantaða færslu* mun pöntun senda beiðni um mótbókun þegar hún er tekin frá, tínd, fylgiseðill bókaður eða hún reikningsfærð. Beiðnin verður aðeins sett af stað í eitt skipti fyrir fyrsta skrefið þegar uppgefið ferli á sér stað. Magn mótbókunar verður magnið þar sem staða birgðafærslu breyttist úr *Í pöntun* í *Frátekið pantað* (eða síðari staða) í samsvarandi pöntunarlínu.

1. Farið í **Birgðastjórnun \> Reglubundið \> Samþætting sýnileika birgða** og virkjið verkið. Öll tilvik birgðabreytinga úr Supply Chain Management verða nú bókuð í birgðasýnileika.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Fjarlægja innbót birgðasýnileika

Til að fjarlægja birgðasýnileikaviðbótina skaltu fylgja þessum skrefum:

1. Skráðu þig inn í Supply Chain Management.
1. Fara til **Vörustjórnun \> Reglubundið \> Sameining birgðasýnileika** og slökkva á starfinu.
1. Farðu í Lifecycle Services og opnaðu síðuna fyrir umhverfið þar sem þú vilt fjarlægja viðbótina (sjá einnig [Settu upp birgðasýnileikaviðbótina](#install-add-in)).
1. Veldu **Fjarlægðu**.
1. Fjarlægingarferlið slítur nú birgðasýnileikaviðbótinni, afskrár viðbótina frá Lifecycle Services og eyðir öllum tímabundnum gögnum sem eru geymd í gagnaskyndiminni fyrir birgðasýnileikaviðbót. Hins vegar eru aðalbirgðagögn sem voru samstillt við þitt Dataverse áskrift er enn geymd þar. Til að eyða þessum gögnum skaltu ljúka restinni af þessari aðferð.
1. Opnið [Power Apps](https://make.powerapps.com).
1. Veldu **Umhverfi** á siglingastikunni.
1. Veldu Dataverse umhverfi sem er tengt líftímaþjónustuumhverfi þínu.
1. Fara til **Lausnir** og eyða eftirfarandi lausnum í eftirfarandi röð:
    1. Dynamics 365 Birgðasýnileiki – Akkeri
    1. Dynamics 365 Birgðasýnileiki – Viðbætur
    1. Dynamics 365 Birgðasýnileiki – Forrit
    1. Dynamics 365 Birgðasýnileiki – Stýringar
    1. Dynamics 365 Birgðasýnileiki – Grunnur 

    Þegar þú eyðir þessum lausnum er gögnum sem geymd eru í töflum einnig eytt.

> [!NOTE]
> Ef þú endurheimtir Supply Chain Management gagnagrunn eftir að þú hefur fjarlægt birgðasýnileikaviðbótina og vilt síðan setja viðbótina upp aftur, vertu viss um að þú hafir eytt gömlum birgðasýnileikagögnum sem eru geymd í Dataverse áskrift (eins og lýst er í fyrri aðferð) áður en þú setur viðbótina upp aftur. Þetta kemur í veg fyrir ósamræmi í gögnum sem annars gætu komið upp.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a> Hreinsaðu birgðasýnileikagögn frá Dataverse áður en þú endurheimtir Supply Chain Management gagnagrunninn

Ef þú hefur verið að nota Birgðasýnileika og endurheimtir síðan Supply Chain Management gagnagrunninn þinn, þá gæti endurheimti gagnagrunnurinn þinn innihaldið gögn sem eru ekki lengur í samræmi við gögn sem áður voru samstillt af Birgðasýnileika við Dataverse. Þetta ósamræmi í gögnum getur valdið kerfisvillum og öðrum vandamálum. Þess vegna er mikilvægt að þú hreinsar alltaf öll birgðasýnileikagögn úr Dataverse áður en þú endurheimtir Supply Chain Management gagnagrunn.

Ef þú þarft að endurheimta Supply Chain Management gagnagrunn skaltu nota eftirfarandi aðferð:

1. Fjarlægðu Inventory Visibility Add-in og fjarlægðu öll tengd gögn í Dataverse, eins og lýst er í [Fjarlægðu Inventory Visibility Add-in](#uninstall-add-in)
1. Endurheimtu Supply Chain Management gagnagrunninn þinn, til dæmis eins og lýst er í [Tímabundin endurheimt gagnagrunns (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) eða [Endurheimt framleiðslugagnagrunns á tímapunkti í sandkassaumhverfi](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Ef þú vilt samt nota það skaltu setja aftur upp og setja upp birgðasýnileikaviðbótina eins og lýst er í [Settu upp birgðasýnileikaviðbótina](#install-add-in) og [Settu upp samþættingu birgðasýnileika](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
