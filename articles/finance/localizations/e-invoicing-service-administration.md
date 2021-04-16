---
title: Stjórnunarhlutar rafrænna reikninga
description: Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á rafrænni reikningsfærslu.
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840029"
---
# <a name="electronic-invoicing-administration-components"></a>Stjórnunarhlutar rafrænna reikninga

[!include [banner](../includes/banner.md)]


Í þessu efnisatriði er að finna upplýsingar um hlutana sem tengjast stjórnun á rafrænni reikningsfærslu. Þar er einnig að finna upplýsingar um hvernig eigi að skilgreina rafræna reikningsfærsluþjónustu.

## <a name="azure"></a>Azure

Notið Microsoft Azure til að stofna leynilykil fyrir lyklageymslu og geymslureikning. Notið síðan leynilyklana í skilgreiningu á rafrænni reikningsfærslu.

## <a name="lifecycle-services"></a>Lifecycle Services

Notið Microsoft Dynamics Lifecycle Services (LCS) til að virkja microservices fyrir LCS-uppsetningarverkið.

> [!NOTE]
> Uppsetning örþjónustu í LCS krefst að minnsta kosti Tier 2 sýndarvélar. Nánari upplýsingar um umhverfisskipulag er að finna í [Umhverfisskipulag](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) er viðmótið sem er notað til að skilgreina rafræna reikningsfærslu. Tilföng eins og umhverfi og eiginleikar rafrænnar reikningsfærslu eru búin til, unnið með og hýst í RCS. Þegar tilföngin eru tilbúin eru þau birt í rafrænni reikningsfærsluþjónustu.

Fyrir RCS-innskráningu, sjá [Regulatory Services](https://marketing.configure.global.dynamics.com/).

Frekari upplýsingar um RCS er að finna í [Regulatory Configuration Services (RCS) – Altækir eiginleikar](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>Samþætting við rafræna reikningsfærslu 

Áður en hægt er að nota RCS til að skilgreina rafræna reikninga verður að skilgreina RCS til að leyfa samskipti við rafræna reikningsfærslu. Þessi skilgreining er kláruð í flipanum **Rafrænni reikningsfærslu** á síðunni **Færibreytur rafrænnar skýrslugerðar**.

#### <a name="service-endpoint"></a>Endastöð þjónustu

Rafræn reikningsfærsla er tiltæk í nokkrum Azure Datacenter löndum. Eftirfarandi tafla sýnir framboði eftir svæði.

| Staðsetning Azure-gagnamiðstöðvar |
|----------------------------|
| Austurhluti Bandaríkjanna                    |
| Vesturhluti Bandaríkjanna                    |
| Norðurhluti Evrópusambandsins                   |
| Vesturhluti Evrópusambandsins                    |

### <a name="service-environments"></a>Þjónustuumhverfi

Þjónustuumhverfi eru rökréttar skiptingar sem eru gerðar til að styðja framkvæmd á eiginleikum rafrænnar reikningsfærslu í rafrænni reikningsfærslu. Öryggislyklar og stafræn vottorð og umsjón (þ.e. aðgangsheimildir) verða að vera skilgreind á öryggisstigi þjónustunnar.

Viðskiptavinir geta búið til eins mörg þjónustuumhverfi og þeir vilja. Öll þjónustuumhverfi sem viðskiptavinur býr til eru óháð hvert öðru.

Þjónustuumhverfi verða að vera búin til og haldið við í RCS. Þegar þjónustuumhverfi eru tilbúin þarf að birta þau í rafrænni reikningsfærslu.

#### <a name="service-environment-status"></a>Staða þjónustuumhverfis

Hægt er að stjórna þjónustuumhverfum í gegnum stöðuna. Mögulegir valkostir eru:

- **Ekki birt** – Umhverfið hefur verið stofnað, en hefur ekki verið birt.
- **Birt** – Umhverfið hefur verið birt í rafrænni reikningsfærslu.
- **Breytt** – Eigindum útgefins umhverfis hefur verið breytt, en breytingarnar hafa ekki enn verið gefnar út.

#### <a name="customer-secrets"></a>Leynilyklar viðskiptavinar

Rafræn reikningsfærsluþjónusta ber ábyrgð á því að geyma öll viðskiptagögn í Azure-tilföngum sem fyrirtækið á. Til að tryggja að þjónustan virki rétt og að öll viðskiptagögnin sem þarf fyrir og eru búin til af rafrænni reikningsfærslu er aðeins opnuð af viðbótinni, þarf að stofna tvö aðaltilföng Azure:

- Azure-geymslureikningur (Blob-geymsla) sem geymir rafræna reikninga
- Azure-lyklageymsla sem geymir vottorð og URI geymslureikningsins

> [!NOTE]
> Úthluta verður tiltekinni lyklageymslu viðskiptavinar sem er sérstaklega notað með rafrænni reikningsfærslu.

Frekari upplýsingar er að finna í [Stofna Azure-geymslureikning og lyklageymslu](e-invoicing-create-azure-storage-account-key-vault.md).

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

Til að skilgreina endastöð þjónustunnar skal fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreyta rafræns skjals** og síðan í flipanum **Þjónusta innsendingar**, í reitinn **Vefslóð fyrir rafræna reikningsfærslu**, skal færa inn vefslóðina eins og lýst er í töflunni sem lýst er í hlutanum **Endastöð þjónustu**.

#### <a name="environments"></a>Umhverfi

Heiti umhverfis sem fært er inn í Finance and Supply Chain Management vísar í heitið á umhverfinu sem er búið til í RCS og birt í rafrænni reikningsfærslu.

Skilgreina þarf umhverfið í flipanum **Þjónustur innsendingar** á síðunni **Færibreyta rafræns skjals** þannig að allar beiðnir um að gefa út rafræna reikninga innihaldi umhverfið þar sem rafræn reikningsfærsla getur ákvarðað hvaða eiginleiki rafrænnar reikningsfærslu verður að vinna úr beiðninni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina rafræna reikninga í RCS](e-invoicing-configuration-rcs.md)
- [Gefa út rafræna reikninga í Finance and Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
