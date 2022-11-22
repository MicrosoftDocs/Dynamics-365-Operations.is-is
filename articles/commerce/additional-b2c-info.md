---
title: Frekari B2C upplýsingar
description: Þessi grein veitir frekari upplýsingar um hvernig á að stilla leigjanda fyrirtækis til neytenda (B2C) í Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/14/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: b60ef15544cd30c44968ee7a588a8a9fb08e8223
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785808"
---
# <a name="additional-b2c-information"></a>Frekari B2C upplýsingar

[!include [banner](includes/banner.md)]

Þessi grein veitir frekari upplýsingar um hvernig á að stilla leigjanda fyrirtækis til neytenda (B2C) í Microsoft Dynamics 365 Commerce.

### <a name="customer-migration"></a>Flutningur viðskiptavina

Ef þú ert að íhuga að flytja skrár viðskiptavina frá fyrri vettvangi fyrir persónuskilaboð, vinsamlegast vinndu með Dynamics 365 Commerce teymi til að fara yfir fólksflutningaþörf þína.

Fyrir aukaleg Azure AD B2C skjöl um flutning viðskiptavina, sjá [Flytja notendur til Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-user-migration).

### <a name="custom-policies"></a>Sérsniðnar stefnur

Fyrir frekari upplýsingar um sérsníða Azure AD B2C samskipti og stefnuflæði umfram það sem boðið er upp á við B2C stöðluðu stefnur, sjá [Sérsniðnar stefnur í Azure Active Directory B2C](/azure/active-directory-b2c/active-directory-b2c-overview-custom). 

### <a name="secondary-admin"></a>Annar stjórnandi

Hægt er að bæta við valfrjálsum aukaforritareikningi í hlutanum **Notendur** af B2C leigjanda þínum. Þetta getur verið beinn reikningur eða almennur reikningur. Ef þú þarft að deila reikningi þvert á teymi, þá er einnig hægt að stofna sameiginlegan reikning. Vegna næmni gagnanna sem geymd eru í Azure AD B2C, ætti að fylgjast náið með sameiginlegum reikningi samkvæmt öryggisvenjum fyrirtækisins.

### <a name="set-up-a-custom-sign-in-domain"></a>Settu upp sérsniðið innskráningarlén

Azure AD B2C gerir þér kleift að setja upp sérsniðið innskráningarlén fyrir Azure AD B2C leigjandi. Fyrir leiðbeiningar, sjá [Virkja sérsniðin lén fyrir Azure Active Directory B2C](/azure/active-directory-b2c/custom-domain). 

Ef þú notar sérsniðið innskráningarlén verður að slá lénið inn í Commerce site builder.

Fylgdu þessum skrefum til að slá inn sérsniðið innskráningarlén í vefsíðugerð.

1. Í efra hægra horninu á vefsíðugerð, veldu vefskiptarofann og veldu síðan **Stjórna síðum**.
1. Í vinstri yfirlitsrúðunni, veldu **Stillingar leigjanda \> Auðkenningaruppsetning vefsvæðis**.
1. Í **Staðfestingarprófílar** kafla, veldu **Stjórna**.
1. Í valmyndinni til hægri velurðu **Breyta** hnappur (blýantartákn) við hliðina á auðkenningarsniði vefsvæðisins sem þú vilt slá inn sérsniðið lén fyrir.
1. Í **Breyta auðkenningarsniði vefsvæðis** svargluggi, undir **Skráðu inn sérsniðið lén**, sláðu inn sérsniðna innskráningarlénið þitt (til dæmis 'login.fabrikam.com').

> [!WARNING]
> Þegar þú uppfærir í sérsniðið lén fyrir Azure AD B2C leigjandi, breytingin hefur áhrif á upplýsingar um útgefanda leigjanda fyrir táknið sem myndast. Upplýsingar um útgefanda munu þá innihalda sérsniðna lénið í stað sjálfgefna lénsins sem veitt er af Azure AD B2C. Annað **Útgefandi** uppsetningu í höfuðstöðvum Commerce (**Verslun og verslun \> Uppsetning höfuðstöðva \> Færibreytur \> Viðskipti samnýtt færibreytur \> Auðkennisveitendur**) breytir samskiptum kerfisins við notendur síðunnar, sem getur hugsanlega búið til nýja viðskiptavinaskrá ef notandi er að auðkenna gegn nýja útgefanda. Allar sérsniðnar breytingar á léni ættu að vera vandlega prófaðar áður en skipt er yfir í sérsniðna lénið í beinni Azure AD B2C umhverfi.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Bæta við kennitöluveitendum (valfrjálst)](add-social-identity-providers.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
