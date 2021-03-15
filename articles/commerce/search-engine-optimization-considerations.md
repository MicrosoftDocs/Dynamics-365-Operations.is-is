---
title: Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt
description: Þetta efni nær yfir sjónarmið leitarvélabestun (SEO) fyrir síðuna þína frá þróun til framleiðslu.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 639d6fa74954b5f74560c7e51523ab2b4d2b7f62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989353"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt


[!include [banner](includes/banner.md)]

Þetta efni nær yfir sjónarmið leitarvélabestun (SEO) fyrir síðuna þína frá þróun til framleiðslu.

## <a name="a-site-that-is-under-development"></a>Síða sem er í þróun

Þó að vefsvæði sé í þróun ættu allar vefsíður að vera með **NOINDEX** og **NOFOLLOW** lýsimerki, svo að leitarvélar skrái ekki síðurnar og geymi þróunarútgáfur af síðunni þinni í skyndiminni. Til að gera þessa stillingu verður þú að bæta við sjálfgefinni lýsimerkjaeiningu við sniðmát vefsíðunnar. Sjálfgefnir lýsimerkjaeiginleikar verða síðan aðgengilegir í SEO eiginleikahlutanum í ritlinum. Þú getur notað þessa eiginleika til að stjórna lýsimerkjunum.

## <a name="soft-launch-of-a-site"></a>Óbundin ræsing svæðis

Við „óbundna ræsingu“ er vefsíða gerð aðgengileg fyrir takmarkaðan markhóp eða markað áður en full kynning fer fram. Ef þú setur óbundna ræsingu á vefsíðuna þína ættir þú að íhuga að hreyfa ekki við lýsimerkjunum **NOINDEX**. Á þennan hátt hjálpar þú til við að tryggja að óbundin ræsing sé áfram takmörkuð við þann takmarkaða markhóp sem þú vilt ná til.

## <a name="a-site-that-is-in-production"></a>Vefsvæði sem er í framleiðslu

Þegar vefur er í framleiðslu ættirðu að ganga úr skugga um að allar vefsíðurnar séu réttar merktar. Microsoft Dynamics 365 Commerce notar upplýsingarnar sem eru færðar inn á síðu til að birta allar SEO upplýsingar á þeirri síðu. Eftirfarandi einingar veita þessa virkni: yfirlit yfir flokksíðu, yfirlit yfir listasíðu og yfirlit yfir vörusíðu.

Til að hámarka flokkun leitarvéla notar flutningsramma báðar upplýsingar frá SEO eiginleikunum sem eru settir upp í Dynamics 365 Commerce og einingasértækar upplýsingar. Fyrir vefsvæði sem er í framleiðslu, ættir þú að ganga úr skugga um að robots.txt skráin geri kleift að gera skrá yfir allt vefsvæðið og að hún innihaldi tengla á birt skjal svæðiskorts. Þú ættir að kveikja á myndunarvirkni svæðiskorts á **Svæðisstillingar \> Vefkort virkjuð**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Stillingar á síðu SEO fyrir innri forsýningu, takmarkaða markhóp og alla markhópa

Vegna þess að Dynamics 365 Commerce styður „það sem þú sérð er það sem þú færð“ sannvottaðar forskoðanir í sjónrænum vefsmið, höfundar geta undirbúið efni síðunnar þeirra án þess að þurfa að hafa áhyggjur af því að upplýsingarnar verða sýnilegar gestum svæðisins. Ef birta verður síðu en útsetning hennar verður að vera takmörkuð ætti hún að hafa lýsimerkið **NOINDEX**, svo að það verði ekki skráð af leitarvélum. Þegar síðan er tilbúin fyrir alla markhópa ættu öll grunnlýsigögn SEO að vera til staðar til að hámarka skilvirkni flokkunar leitarvéla. Að auki ætti að fjarlægja lýsimerkið **NOLIMIT**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna notendum og hlutverkum rafrænna viðskipta](manage-ecommerce-users-roles.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)

[Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]