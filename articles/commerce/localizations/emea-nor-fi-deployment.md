---
title: Leiðbeiningar um uppsetningu fyrir sjóðsvélar fyrir Noreg
description: Þessi grein veitir leiðbeiningar um hvernig á að virkja virkni peningakassa fyrir Microsoft Dynamics 365 Commerce staðsetning fyrir Noreg.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 1f2226432237662e28b9e26017020ab81bb6026b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899068"
---
# <a name="deployment-guidelines-for-cash-registers-for-norway"></a>Leiðbeiningar um uppsetningu fyrir sjóðsvélar fyrir Noreg

[!include[banner](../includes/banner.md)]

Þessi grein veitir leiðbeiningar um hvernig á að virkja virkni peningakassa fyrir Microsoft Dynamics 365 Commerce staðsetning fyrir Noreg. Staðsetningin samanstendur af nokkrum framlengingum á íhlutum. Þessar viðbætur gera þér kleift að framkvæma aðgerðir eins og að prenta sérsniðna reiti á kvittanir, skrá viðbótarendurskoðunarviðburði, sölufærslur og greiðslufærslur á sölustað (POS), undirrita sölufærslur stafrænt og prenta skýrslur á staðbundnu sniði. Fyrir frekari upplýsingar um staðsetningar fyrir Noreg, sjá [Gjaldkassavirkni fyrir Noreg](./emea-nor-cash-registers.md). Fyrir frekari upplýsingar um hvernig á að stilla Commerce fyrir Noreg, sjá [Settu upp Commerce fyrir Noreg](./emea-nor-cash-registers.md#setting-up-commerce-for-norway).

> [!WARNING]
> Vegna takmarkana á [ný sjálfstæð umbúða- og framlengingarlíkan](../dev-itpro/build-pipeline.md), sem stendur er ekki hægt að nota það fyrir þessa staðsetningaraðgerð. Þú verður að nota útgáfu stafræna undirskriftarsýnishornsins fyrir Noreg í fyrri útgáfu smásöluhugbúnaðarþróunarsettsins (SDK) á sýndarvél þróunaraðila (VM) í Microsoft Dynamics Lífsferilsþjónusta (LCS). Fyrir frekari upplýsingar, sjá [Leiðbeiningar um dreifingu fyrir sjóðvélar fyrir Noreg (arfleifð)](./emea-nor-loc-deployment-guidelines.md).
>
> Stuðningur við nýja óháða umbúða- og framlengingarlíkanið fyrir skattasamþættingarsýni er fyrirhugað fyrir síðari útgáfur.

## <a name="set-up-fiscal-registration-for-norway"></a>Settu upp ríkisfjármálaskráningu fyrir Noreg

Úrtak ríkisfjármálaskráningar fyrir Noreg er byggt á [virkni í ríkisfjármálum](fiscal-integration-for-retail-channel.md) og er hluti af Retail SDK. Sýnið er staðsett í **src\\ Fiscal Integration\\ SequentialSignatureNorway** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla (td [sýnishornið í útgáfu/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34/src/FiscalIntegration/SequentialSignatureNorway)). Sýnið [felst í](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) af ríkisfjármálaskjalaveitu og fjárhagstengi, sem eru framlengingar á viðskiptatímanum (CRT). Fyrir frekari upplýsingar um hvernig á að nota Retail SDK, sjá [Smásölu SDK arkitektúr](../dev-itpro/retail-sdk/retail-sdk-overview.md) og [Settu upp smíðisleiðslu fyrir SDK fyrir sjálfstæða umbúðir](../dev-itpro/build-pipeline.md).

Ljúktu við uppsetningarskref fjárhagsskráningar sem lýst er í [Settu upp fjárhagslega samþættingu fyrir viðskiptarásir](./setting-up-fiscal-integration-for-retail-channel.md):

1. [Settu upp fjárhagslega skráningarferli](./setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Gakktu úr skugga um að þú takir eftir stillingum fjárhagsskráningarferlisins sem eru [sérstaklega við Noreg](#configure-the-fiscal-registration-process).
1. [Stilltu stillingar fyrir villumeðferð](./setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Virkja handvirka framkvæmd frestaðrar fjárhagsskráningar](./setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Stilltu rásaríhluti](#configure-channel-components).

### <a name="configure-the-fiscal-registration-process"></a>Stilltu fjárhagsskráningarferlið

Fylgdu þessum skrefum til að virkja skattaskráningarferlið fyrir Noreg í höfuðstöðvum viðskipta.

1. Hlaða niður stillingarskrám fyrir veitanda fjárhagsskjala og fjárhagstengi frá Commerce SDK:

    1. Opnaðu [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions/) geymsla.
    1. Opnaðu síðasta tiltæka útgáfuútibú (til dæmis, **[útgáfa/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.34)**).
    1. Opið **src \> Fiscal Integration \> SequentialSignatureNorway \> CommerceRuntime**.
    1. Sæktu stillingarskrá ríkisskjalaveitunnar á **DocumentProvider.SequentialSignNorway \> Stillingar \> DocumentProviderSequentialSignatureNorwaySample.xml** (til dæmis, [skrána til útgáfu/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/DocumentProvider.SequentialSignNorway/Configuration/DocumentProviderSequentialSignatureNorwaySample.xml)).
    1. Sæktu stillingarskrá fjárhagstengis á **Connector.SequentialSignNorway \> Stillingar \> ConnectorSequentialSignatureNorwaySample.xml** (til dæmis, [skrána til útgáfu/9.34](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.34/src/FiscalIntegration/SequentialSignatureNorway/CommerceRuntime/Connector.SequentialSignNorway/Configuration/ConnectorSequentialSignatureNorwaySample.xml)).

1. Fara til **Verslun og verslun \> Uppsetning höfuðstöðva \> Færibreytur \> Sameiginlegar færibreytur**. Á **Almennt** flipann, stilltu **Virkja samþættingu í ríkisfjármálum** valmöguleika til **Já**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingar**, og hlaðið inn stillingarskrá fjárhagstengis sem þú sóttir áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Veitendur ríkisfjármálaskjala**, og hlaðið inn stillingaskrá fjárhagsskjalaveitunnar sem þú hleður niður áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tengi virka snið**. Búðu til nýtt virknisnið fyrir tengi og veldu skjalaveituna og tengið sem þú hleður inn áðan.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**. Búðu til nýtt tæknisnið fyrir tengi og veldu tengið sem þú hleður inn áðan. Stilltu tengigerðina á **Innri**.
1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Fjárhagstengingarhópar**, og búðu til nýjan fjárhagstengihóp fyrir virknisniðið tengi sem þú bjóst til áður.
1. Fara í **uppsetningu á fjárhagssamþættingu \>\> fjárhagssamþættingar \> fjárhags**. Stofna nýtt fjárhagsskráningarferli og skref fjárhagsskráningarferlis og velja fjárhagstengiflokkinn sem var stofnaður áður.
1. Farðu í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Forstillingar sölustaðar \> Virknireglur**. Veljið virknireglu sem er tengd versluninni þar sem virkja á skráningarferlið. Á flýtiflipanum **Fjárhagsskráningarferli** skal velja fjárhagsskráningarferlið sem var stofnað áður. Á **Þjónusta í ríkisfjármálum** Flýtiflipi, veldu tæknisniðið sem þú bjóst til áðan. 
1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**. Opnaðu dreifingaráætlunina og veldu störf **1070** og **1090** að flytja gögn í rásargagnagrunninn.

### <a name="configure-the-digital-signature-parameters"></a>Stilltu breytur stafrænna undirskriftar

Þú verður að stilla vottorð sem verða notuð fyrir stafræna undirritun söluviðskipta í verslun. Stafrænt skilríki sem er geymt í Azure Key Vault er notað til að gera undirskriftina. Fyrir offline stillingu Modern POS er einnig hægt að undirrita með því að nota stafrænt skilríki sem er geymt í staðbundinni geymslu vélarinnar sem Modern POS er sett upp á.

Áður en hægt er að nota stafrænt skilríki sem er geymt í Key Vault geymslu verður að ljúka eftirfarandi skrefum.

1. Búa verður til Key Vault geymsluna. Við mælum með því að þú setjir geymsluna á sama landfræðilega svæði og Commerce Scale Unit.
1. Hlaða verður upp vottorðinu í Key Vault geymsluna sem base64 strengjaleyndarmál.
1. Forritið Application Object Server (AOS) verður að hafa heimild til að lesa leyndarmál úr Key Vault geymslunni.

Fyrir frekari upplýsingar um hvernig á að vinna með Key Vault, sjá [Byrjaðu með Azure Key Vault](/azure/key-vault/key-vault-get-started).

Næst, á **Helstu færibreytur Vault** síðu, þú verður að tilgreina færibreytur fyrir aðgang að Key Vault geymslunni:

- **Nafn** og **Lýsing** – Nafn og lýsing á Key Vault geymslunni.
- **Vefslóð lykilhólfs** – Vefslóð Key Vault geymslunnar.
- **Key Vault viðskiptavinur** – Gagnvirkt auðkenni viðskiptavinarins Azure Active Directory (Azure AD) forrit sem er tengt við Key Vault geymsluna í auðkenningarskyni. Þessi viðskiptavinur ætti að hafa aðgang að því að lesa leyndarmál úr geymslunni.
- **Key Vault leynilykill** – Leynilykill sem er tengdur við Azure AD forrit sem er notað til auðkenningar í Key Vault geymslunni.
- **Nafn**, **·**, og **Leynileg tilvísun** – Nafn, lýsing og leynileg tilvísun skírteinisins.

Næst verður þú að stilla tengi fyrir vottorðin þín sem eru geymd í Key Vault eða staðbundinni vottorðageymslu. Þetta tengi er notað til að undirrita á ráshliðinni.

1. Fara til **Verslun og verslun \> Rásaruppsetning \> Samþætting í ríkisfjármálum \> Tæknisnið fyrir tengi**.
1. Á **Stillingar** Flýtiflipi, tilgreindu eftirfarandi færibreytur fyrir stafrænar undirskriftir:

    - **Leynilegt nafn** – Veldu leyndarmálið sem þú stilltir áðan á **Helstu færibreytur Vault** síðu.
    - **Þumalfingur fyrir staðbundið vottorð** – Gefðu upp þumalfingur fyrir vottorð sem er geymt á staðnum.
    - **Hash reiknirit** - Tilgreindu eitt af dulkóðunarkássa reikniritunum sem eru studdar af Microsoft .NET, eins og **SHA1**.
    - **Nafn vottorðsverslunar** – Þessi reitur er valfrjáls. Notið hann til að tilgreina sjálfgefið heiti verslunar sem á að nota til að leita að staðbundnum vottorðum.
    - **Staðsetning vottorðaverslunar** – Þessi reitur er valfrjáls. Notið hann til að tilgreina sjálfgefna staðsetningu verslunar sem á að nota til að leita að staðbundnum vottorðum.
    - **Prófaðu staðbundið vottorð fyrst** – Veldu þennan valkost til að nota vottorðið frá staðbundinni verslun sjálfgefið til að undirrita gögn, í stað vottorðsins frá Key Vault.
    - **Virkjaðu heilsufarsskoðun** – Fyrir frekari upplýsingar um heilsufarsskoðunareiginleikann, sjá [Heilbrigðisskoðun ríkisfjármála](./fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).

> [!NOTE]
> - Aðeins **SHA1** dulmáls kjötkássa reiknirit er nú viðunandi fyrir Noreg.
> - Sjálfgefnu verslunarheiti og staðsetningu verslunar er bætt við til að einfalda ferlið við að leita að staðbundnum vottorðum inn CRT. X509StoreProvider er með lista yfir möppur þar sem vottorð eru geymd. Ef sjálfgefið verslunarheiti og sjálfgefin staðsetning verslunar eru ekki tilgreind, reynir X509StoreProvider að finna vottorð í öllum möppum á listanum.

### <a name="configure-channel-components"></a>Skilgreina rásaríhluti

### <a name="development-environment"></a>Þróunarumhverfi

Fylgdu þessum skrefum til að setja upp þróunarumhverfi svo þú getir prófað og stækkað sýnishornið.

1. Klóna eða hlaða niður lausnageymslunni [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions). Veldu rétta útgáfu útgáfu útibús í samræmi við SDK / umsóknarútgáfuna þína. Frekari upplýsingar er að finna í [Download Retail SDK sýni og tilvísunarpakkar frá GitHub og NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Opnaðu **SequentialSignatureNorway.sln** lausn undir **Dynamics365Commerce.Solutions\\ Fiscal Integration\\ SequentialSignatureNorway**, og byggja það.
1. Setja upp CRT viðbætur:

    1. Finndu uppsetningarforrit viðbótarinnar CRT:

        - **Eining viðskiptaskala:** Í **SequentialSignatureNorway\\ ScaleUnit\\ ScaleUnit.SequentialSignNorway.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ScaleUnit.SequentialSignNorway.Installer** uppsetningarforrit.
        - **Staðbundið CRT á Modern POS:** Í **SequentialSignatureNorway\\ ModernPOS\\ ModernPos.SequentialSignNorway.Installer\\ bin\\ Villuleit\\ net461** möppu, finndu **ModernPos.SequentialSignNorway.Installer** uppsetningarforrit.

    1. Ræsa uppsetningarforrit viðbótarinnar CRT úr skipanalínunni:

        - **Mælieining viðskiptakvarða:**

            ```Console
            ScaleUnit.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

        - **Staðbundið CRT á modern POS:**

            ```Console
            ModernPOS.SequentialSignNorway.Installer.exe install --verbosity 0
            ```

### <a name="production-environment"></a>Framleiðsluumhverfi

Fylgið skrefunum í [Setja upp byggingarpípu fyrir fjárhagssamþættingarsýni](fiscal-integration-sample-build-pipeline.md) til að búa til og losa skýjaskalaeininguna og virkjanlega sjálfsafgreiðslupakka fyrir fjárhagssamþættingarsýnið. The **SequentialSignatureNorway build-pipeline.yaml** sniðmát YAML skrá er að finna í **Leiðsla\\ YAML_skrár** mappa af [Dynamics 365 Commerce Lausnir](https://github.com/microsoft/Dynamics365Commerce.Solutions) geymsla.

### <a name="enable-the-digital-signature-in-offline-mode-for-modern-pos"></a>Virkjaðu stafrænu undirskriftina í ótengdum ham fyrir Modern POS

Til að virkja stafræna undirskrift í ótengdum ham fyrir Modern POS, verður þú að fylgja þessum skrefum eftir að þú hefur virkjað Modern POS á nýju tæki.

1. Skráðu þig inn í POS.
1. Á **Gagnagrunnstengingarstaða** síðu skaltu ganga úr skugga um að ónettengdi gagnagrunnurinn sé að fullu samstilltur. Þegar verðmæti **Niðurhal í bið** sviði er **0** (núll), gagnagrunnurinn er að fullu samstilltur.
1. Skráðu þig út af POS.
1. Bíddu eftir að ónettengdi gagnagrunnurinn sé samstilltur að fullu.
1. Skráðu þig inn í POS.
1. Á **Gagnagrunnstengingarstaða** síðu skaltu ganga úr skugga um að ónettengdi gagnagrunnurinn sé að fullu samstilltur. Þegar verðmæti **Viðskipti í bið í ótengdum gagnagrunni** sviði er **0** (núll), gagnagrunnurinn er að fullu samstilltur.
1. Opnaðu Modern POS aftur.
