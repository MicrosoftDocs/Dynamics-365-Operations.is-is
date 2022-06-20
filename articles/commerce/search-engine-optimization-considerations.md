---
title: Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt
description: Þessi grein fjallar um hagræðingu leitarvéla (SEO) fyrir síðuna þína frá þróun til framleiðslu.
author: psimolin
ms.date: 05/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: 6747df3c56fb05248210f78ebf2176a56ce78329
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896902"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a>Hugsanleg leitarvélabestun (SEO) fyrir vefsvæðið þitt


[!include [banner](includes/banner.md)]

Þessi grein fjallar um hagræðingu leitarvéla (SEO) fyrir síðuna þína frá þróun til framleiðslu.

## <a name="a-site-that-is-under-development"></a>Síða sem er í þróun

Til að tryggja að leitarvélar skrái ekki síðu sem er í þróun ættu allar síður að hafa **engin vísitala** og **nofollow** meta tags. Góð æfing er að búa til brot byggt á [MetaTags mát](metatags-module.md) sem inniheldur eftirfarandi meta tag færslu og tryggðu að brotinu sé bætt við HTML\<head\> hluta allra sniðmáta sem notuð eru á síðunni þinni.

```html
<meta name="robots" content="noindex,nofollow" /> 
```

## <a name="soft-launch-of-a-site"></a>Óbundin ræsing svæðis

Við „óbundna ræsingu“ er vefsíða gerð aðgengileg fyrir takmarkaðan markhóp eða markað áður en full kynning fer fram. Ef þú setur vefsíðuna þína á mjúkan hátt ættir þú að íhuga að yfirgefa **engin vísitala** meta tags á sínum stað. Á þennan hátt hjálpar þú til við að tryggja að óbundin ræsing sé áfram takmörkuð við þann takmarkaða markhóp sem þú vilt ná til.

## <a name="a-site-that-is-in-production"></a>Vefsvæði sem er í framleiðslu

Þegar vefur er í framleiðslu ættirðu að ganga úr skugga um að allar vefsíðurnar séu réttar merktar. Microsoft Dynamics 365 Commerce notar upplýsingarnar sem eru færðar inn fyrir síðu til að mynda allar upplýsingar um leitarvélabestun á þeirri síðu. Eftirfarandi einingar veita þessa virkni: yfirlit yfir flokksíðu, yfirlit yfir listasíðu og yfirlit yfir vörusíðu.

Til að hámarka flokkun leitarvéla notar flutningsramma báðar upplýsingar frá SEO eiginleikunum sem eru settir upp í Dynamics 365 Commerce og einingasértækar upplýsingar. Fyrir vefsvæði sem er í framleiðslu, ættir þú að ganga úr skugga um að robots.txt skráin geri kleift að gera skrá yfir allt vefsvæðið og að hún innihaldi tengla á birt skjal svæðiskorts. Þú ættir að kveikja á myndunarvirkni svæðiskorts á **Svæðisstillingar \> Vefkort virkjuð**.

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a>Stillingar á síðu SEO fyrir innri forsýningu, takmarkaða markhóp og alla markhópa

Vegna þess að Dynamics 365 Commerce styður „það sem þú sérð er það sem þú færð“ sannvottaðar forskoðanir í sjónrænum vefsmið, höfundar geta undirbúið efni síðunnar þeirra án þess að þurfa að hafa áhyggjur af því að upplýsingarnar verða sýnilegar gestum svæðisins. Ef síðu verður að birta, en útsetning hennar verður að vera takmörkuð, ætti hún að hafa **engin vísitala** meta tag, svo að það verði ekki skráð af leitarvélum. Þegar síðan er tilbúin fyrir alla markhópa ættu öll grunnlýsigögn SEO að vera til staðar til að hámarka skilvirkni flokkunar leitarvéla. Að auki er **engin takmörk** meta tag ætti að fjarlægja.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stjórna notendum og hlutverkum rafrænna viðskipta](manage-ecommerce-users-roles.md)

[Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar](add-telemetry.md)

[Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
