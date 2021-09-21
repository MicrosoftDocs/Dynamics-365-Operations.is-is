---
title: Stjórnunarhlutar rafrænna reikninga
description: Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á rafrænni reikningsfærslu.
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463882"
---
# <a name="electronic-invoicing-administration-components"></a>Stjórnunarhlutar rafrænna reikninga

[!include [banner](../includes/banner.md)]


Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á rafrænni reikningsfærslu. Þar er einnig að finna upplýsingar um hvernig eigi að skilgreina rafræna reikningsfærsluþjónustu.

## <a name="azure"></a>Azure

Notaðu Microsoft Azure til að stofna leynilykla fyrir lyklageymsluna og settu upp geymslureikning. Notaðu síðan leynilykla lyklageymslunnar og SAS-lykil geymslureikningsins í skilgreiningu rafrænnar reikningsfærslu.

## <a name="lifecycle-services"></a>Lifecycle Services

Notaðu Microsoft Dynamics Lifecycle Services (LCS) til að virkja innbót rafrænnar reikningsfærslu fyrir LCS-uppsetningarverkið.

> [!NOTE]
> Uppsetning innbóta í LCS krefst að minnsta kosti **Umhverfi í lagi 2**. Nánari upplýsingar um umhverfisskipulag er að finna í [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er viðmótið sem er notað til að skilgreina rafræna reikningsfærslu. Tilföng eins og umhverfi og eiginleikar rafrænnar reikningsfærslu eru búin til, unnið með og hýst í RCS. Þegar tilföngin eru tilbúin eru þau birt í rafrænni reikningsfærsluþjónustu.

Fyrir RCS-innskráningu, sjá [Regulatory Services](https://marketing.configure.global.dynamics.com/).

Frekari upplýsingar um RCS er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Samþætting við rafræna reikningsfærslu 

Áður en hægt er að nota RCS til að skilgreina rafræna reikninga verður að skilgreina RCS til að leyfa samskipti við rafræna reikningsfærslu. Þessi skilgreining er kláruð í flipanum **Rafrænni reikningsfærslu** á síðunni **Færibreytur rafrænnar skýrslugerðar**.

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>Endastöð þjónustu

Rafræn reikningsfærsla er tiltæk í nokkrum Azure Datacenter löndum. Eftirfarandi tafla sýnir framboði eftir svæði.


| Gagnamiðstöð Azure-staðsetningar | URI fyrir endastöð þjónustu                                                       |
|----------------------------|----------------------------------------------------------------------------|
| Bandaríkin              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| Evrópa                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Bretland             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| Asía                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>Þjónustuumhverfi

Þjónustuumhverfi eru rökréttar skiptingar sem eru gerðar til að styðja framkvæmd á altækum eiginleikum í rafrænni reikningsfærslu. Öryggislyklar og stafræn vottorð og umsjón (þ.e. aðgangsheimildir) verða að vera skilgreind á öryggisstigi þjónustunnar.

Viðskiptavinir geta búið til eins mörg þjónustuumhverfi og þeir vilja. Öll þjónustuumhverfi sem viðskiptavinur býr til eru óháð hvert öðru.

Þjónustuumhverfi verða að vera búin til og haldið við í RCS. Þegar þjónustuumhverfi eru tilbúin þarf að birta þau í rafrænni reikningsfærslu.

#### <a name="service-environment-status"></a>Staða þjónustuumhverfis

Hægt er að stjórna þjónustuumhverfum í gegnum stöðuna. Mögulegir valkostir eru:

- **Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.
- **Birt** – Umhverfið hefur verið birt í rafrænni reikningsfærslu.
- **Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.

#### <a name="customer-secrets"></a>Leynilyklar viðskiptavinar

Rafræn reikningsfærsluþjónusta ber ábyrgð á því að geyma öll viðskiptagögn í Azure-tilföngum sem fyrirtækið á. Til að tryggja að þjónustan virki rétt og að öll viðskiptagögnin sem þarf fyrir og eru búin til af rafrænni reikningsfærslu er aðeins opnuð af viðbótinni, þarf að stofna tvö aðaltilföng Azure:

- Azure-geymslureikningur (Blob-geymsla) sem geymir rafræn skjöl, þ.m.t. rafræna reikninga, niðurstöður skjalaumbreytinga og svör frá ytri vefþjónustum.
- Azure-lyklageymsla sem geymir vottorð og URI geymslureikningsins (SAS-merki).


Úthluta þarf sérstakri lyklageymslu og geymslureikningi viðskiptavinar sérstaklega til að nota með rafrænni reikningsfærslu. Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

Til að fylgjast með ástandi lyklageymslunnar og fá tilkynningar skal skilgreina Azure Monitor fyrir lyklageymslu. Með því að virkja innskráningu lyklageymslu er hægt að fylgjast með hvernig, hvenær og hver opnar lyklageymsluna. Frekari upplýsingar er að finna í [Fylgjast með Azure-lyklageymslu og senda út tilkynningar](/azure/key-vault/general/alert) og [Hvernig á að virkja innskráningu lyklageymslu](/azure/key-vault/general/howto-logging?tabs=azure-cli).

Best er að breyta leynilyklunum með reglulegu millibili. Frekari upplýsingar er að finna í [Fylgigögn leynilykla](/azure/key-vault/secrets/).

#### <a name="users"></a>Notendur

Hvert þjónustuumhverfi verður að sýna notendurna sem geta tengst frá Dynamics 365 Finance og Dynamics 365 Supply Chain Management í rafræna reikningsfærslu.

#### <a name="publication"></a>Birting

Gefa þarf út þjónustuumhverfi í rafrænni reikningsfærslu áður en hægt er að nota þau. Finance and Supply Chain Management getur aðeins opnað útgefin umhverfi. Þar að auki verður að birta þjónustuumhverfi áður en nokkrar uppfærslur á eigindum þess taka gildi í þjónustu rafrænnar reikningsfærslu.

### <a name="connected-applications"></a>Tengd forrit

Tengd forrit eru tilvik Finance and Supply Chain Management sem þú gætir viljað nálgast í gegnum RCS. Fyrir utan vefslóð forritsins og leigjanda þess, inniheldur tengt forrit innskráningarupplýsingar sem gerir RCS kleift að tengjast við umhverfið.

Í gegnum tengd forrit er hægt að skilgreina hluta af eiginleika rafrænnar reikningsfærslu í Finance and Supply Chain Management til að fá allan eiginleika rafrænnar reikningsfærslu til að virka.

## <a name="finance-and-supply-chain-management"></a>Finance and Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Samþætting við rafræna reikningsfærslu

Áður en hægt er að nota Finance and Supply Chain Management til að gefa út rafræna reikninga í gegnum rafræna reikningsfærslu þarf að skilgreina það til að leyfa samskipti við þjónustuna.

#### <a name="electronic-invoicing-integration-feature"></a>Samþættingareiginleiki rafrænnar reikningsfærslu

Til að virkja samskipti á milli Finance and Supply Chain Management og rafrænnar reikningsfærslu þarf að kveikja á eiginleikanum **Samþætting rafrænnar reikningsfærslu** á vinnusvæðinu **Eiginleikastjórnun**.

#### <a name="service-endpoint"></a>Endastöð þjónustu

Endastöð þjónustu er vefslóðin þar sem rafræn reikningsfærsla er staðsett. Áður en hægt er að gefa út rafræna reikninga verður að skilgreina endastöð þjónustunnar í Finance and Supply Chain Management til að leyfa samskipti við þjónustuna.

Til að skilgreina endastöð þjónustunnar skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreyta rafræns skjals** og síðan í flipanum **Rafræn reikningsfærsla**, í reitinn **Vefslóð endastöðvar**, skal færa inn viðeigandi vefslóð úr töflunni í hlutanum [Endastöð þjónustu](#svc-endpoint-uris) fyrr í þessu efnisatriði.

#### <a name="environments"></a>Umhverfi

Heiti umhverfis sem fært er inn í Finance and Supply Chain Management vísar í heitið á umhverfinu sem er búið til í RCS og birt í rafrænni reikningsfærslu.

Umhverfið verður að vera stillt í flipanum **Rafræn reikningsfærsla** á síðunni **Færibreytur rafrænna skjala**. Þannig innihalda allar beiðnir um að gefa út rafræna reikninga umhverfið þar sem rafræn reikningsfærsla getur ákvarðað hvaða eiginleiki rafrænnar reikningsfærslu verður að vinna úr beiðninni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina rafræna reikninga í RCS](e-invoicing-configuration-rcs.md)
- [Gefa út rafræna reikninga í Finance and Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
