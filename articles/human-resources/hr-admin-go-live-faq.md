---
title: Algengar spurningar um keyrslu
description: Í þessu efnisatriði eru algengar spurningar um hvernig á að keyra Dynamics 365 Human Resources innleiðingarverk.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 550e094fd34bfbdc66665be2ceed306de722c0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055341"
---
# <a name="go-live-faq"></a>Algengar spurningar um keyrslu 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Í þessu efnisatriði eru algengar spurningar um hvernig á að keyra Dynamics 365 Human Resources innleiðingarverk. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Hvenær get ég skilgreint og beðið um vinnsluumhverfið mitt? 

Yfirleitt er vinnsluumhverfi virkjað eftir að eftirfarandi skilyrði eru uppfyllt:

- Allar sérstillingar hafa verið kóðaðar.
- Samþykkisprófun notanda er lokið.
- Viðskiptavinurinn hefur samþykkt lausnina.
- Ekkert stendur í vegi fyrir keyrslu. 

Þegar hæfir viðskiptavinir eru á þessu stigi mun Microsoft FastTrack-teymið vinna með verkefnateyminu að gerð keyrslumats. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Hver eru skilyrðin fyrir virkjun vinnsluumhverfis? 

Fyrir lista yfir forkröfur skal skoða  [Undirbúa keyrslu](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Hvað er keyrslumat?  

Keyrslumatið er hluti af  [Microsoft FastTrack-áætluninni](/dynamics365/fasttrack/). Við þessa yfirferð leggur úrlausnarhönnuður mat á hvort innleiðingarverk sé tilbúið fyrir flutning og keyrslu. Þessi yfirferð er áskilin fyrir hvert innleiðingarverk áður en hægt er að óska eftir því að keyra vinnsluumhverfi. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Sandkassaumhverfin okkar eru virkjuð í gagnamiðstöð í miðríkjum Bandaríkjanna. Við viljum að vinnsluumhverfi okkar séu virkjuð í gagnamiðstöð í vesturríkjum Bandaríkjanna. Get ég valið vesturríki Bandaríkjanna sem gagnamiðstöð í vinnsluskilgreiningunni minni? 

LCS hindrar þig ekki í að velja aðra gagnamiðstöð þegar Human Resources-umhverfi er sett upp, en við mælum eindregið með því að velja ekki aðra gagnamiðstöð.  

Ef þú vilt að vinnsluumhverfið þitt sé í gagnamiðstöð í vesturríkjum Bandaríkjanna ættirðu fyrst að endurvirkja sandkassaumhverfi þín í gagnamiðstöð í vesturríkjum Bandaríkjanna, prófa þau og samþykkja. 

Frekari upplýsingar um val á réttri gagnamiðstöð er að finna í [Netkröfur](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Hvaða aðgangsstig er ég með í Azure-tilföngum fyrir Human Resources-umhverfið mitt?  

Aðgangur að umhverfi Human Resources er háður takmörkunum. Ekki er hægt að fá aðgang að sýndarvél eða Microsoft Internet Information Services (IIS). Einnig er ekki hægt að opna gagnagrunninn í gegnum Microsoft SQL Server Management Studio. 

Þótt þú getir ekki fengið beinan aðgang að Azure-tilföngum eða Dynamics 365 Human Resources-umhverfinu, eru til fleiri eiginleikar sem þú getur notað til að fá aðgang að gögnunum þínum:

- Hægt er að setja upp Azure SQL-gagnagrunn í eigin Azure-leigjanda og eiginleikann BYOD-gagnagrunnur til að samstilla gögn. Frekari upplýsingar er að finna í [Koma með eigin gagnagrunn (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).

- Hægt er að nota Dataverse-samþættingu til að samstilla valdar einingar við Dataverse-gagnagrunninn. Frekari upplýsingar eru í [Dataverse töflur](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Hversu oft er verið að afrita vinnslugrunninn minn? 

Gagnagrunnar eru varðir með sjálfvirkum öryggisafritunum með eftirfarandi millibili:

| Gerð öryggisafritunar | Tíðni |
| --- | --- |
| Heildarafritun gagnagrunns | Vikulega |
| Milliafritun gagnagrunns | Á 12-24 klukkustunda fresti |
| Öryggisafritun færslukladda | Á 5 til 10 mínútna fresti |

Microsoft heldur eftir nægum öryggisafritunum til að geta endurheimt tímapunkt innan síðustu 14 daga. 

Frekari upplýsingar er að finna í  [Fræðast um sjálfvirka öryggisafritun SQL-gagnagrunns](/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Get ég óskað eftir afriti af öryggisafritun vinnslugrunnsins míns? 

Nei. Hinsvegar er hægt að senda inn þjónustubeiðni um gagnagrunnsuppfærslu til að afrita vinnsluumhverfið þitt í sandkassaumhverfið. Hægt er að setja upp Azure SQL-gagnagrunn í eigin Azure-leigjanda og nota BYOD-gagnagrunnseiginleikann til að samstilla gögn úr vinnsluumhverfinu þínu. Frekari upplýsingar er að finna í [Koma með eigin gagnagrunn (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Hvernig flyt ég sandkasssumhverfið mitt í vinnslu fyrir keyrslu? 

Vegna þess að afritunareiginleiki er ekki í boði til að flytja umhverfið þitt úr sandkassa í vinnsluumhverfi, verður þú að nota gagnapakka til að flytja gögn í vinnsluumhverfið þitt.  

Við mælum með því að halda utan um skýran lista yfir einingar sem eru skilgreindar í sandkassanum þínu í gegnum verkið. Prófaðu síðan flutningsferlið á einhverjum gagnapakka sem þarf fyrir keyrsluna. Þú verður að færa gagnapakka handvirkt inn í vinnsluumhverfið þegar þú ert tilbúin(n) fyrir keyrsluna. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Hvað á ég að taka til bragðs ef vinnsluumhverfið mitt er niðri? 

Til að tilkynna stöðvun á vinnslu skal fylgja ferlinu sem lýst er í  [Tilkynna framleiðslustöðvun](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md). 

 ## <a name="see-also"></a>Sjá einnig

 [Undirbúa keyrslu](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]