---
title: Stofna svæði fyrir rafræn viðskipti
description: Þessi grein lýsir skrefunum og upplýsingum sem þarf til að búa til nýja netverslunarsíðu í Dynamics 365 Commerce vefsmiður.
author: bicyclingfool
ms.date: 03/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: ea9afd89ce9ff79edbe5bff609b9843026005493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270238"
---
# <a name="create-an-e-commerce-site"></a>Stofna svæði fyrir rafræn viðskipti

[!include [banner](includes/banner.md)]

Þessi grein lýsir skrefunum og upplýsingum sem þarf til að búa til nýja netverslunarsíðu í Dynamics 365 Commerce vefsmiður.

Þegar Dynamics 365 Commerce er veitt heimild fyrir rafrænum viðskiptamöguleikum, fær vefhönnuður úthlutað upphafssíðu sem hægt er að nota sem grunn fyrir eigin síðu. Ef þú vilt hins vegar byrja frá grunni eða ef þú vilt koma á öðru vefsvæði þarftu að koma á fót nýju svæði í hönnunarumhverfi vefsvæðis. 

## <a name="site-creation-prerequisites"></a>Forsendur stofnunar vefsvæðis

Notandi sem byggir vefsvæði verður að hafa Microsoft Azure Active Directory (Azure AD) notendareikningur innifalinn í Azure AD öryggishópur úthlutaður fyrir kerfisstjóra rafrænna viðskipta. Fyrir frekari upplýsingar, sjá [Settu upp nýjan leigjanda fyrir rafræn viðskipti](deploy-ecommerce-site.md).

> [!NOTE]
> Azure AD gestanotendur gætu haft mismunandi aðgangsheimildir í þínu Azure AD leigjanda. Jafnvel þótt það sé innifalið í Azure AD öryggishópur úthlutað fyrir kerfisstjóra rafrænna viðskipta, gæti gestanotandi þurft Azure AD **Ytri notendur** leyfisstillingar sem á að breyta til að búa til netverslunarsíðu í Commerce. 

Að aðlaga Azure AD **Ytri notendur** stillingar skaltu fylgja þessum skrefum.

1. Í Azure gáttinni skaltu fletta að þínu Azure AD leigjanda.
1. Fara til **Notendastillingar \> Ytri notendur** og veldu **Hafa umsjón með ytri samstarfsstillingum** hlekkur. Þetta opnar **Ytri samstarfsstillingar** síðu þar sem hægt er að stilla aðgang gesta, gestaboðsstillingar og samstarfstakmarkanir. 
1. Stilltu ytri samstarfsstillingar í samræmi við öryggisstefnur fyrirtækisins þíns. 

## <a name="set-up-your-site"></a>Setja upp síðuna

Til að setja upp síðuna þína skaltu gera eftirfarandi.

1. Opnaðu umhverfi vefsvæðishönnuðar. Þú getur fundið tengil á vefsvæði byggingaraðila í Microsoft Lifecycle Services (LCS) á umhverfisaðgerðarsíðunni fyrir Commerce.
1. Á heimasíðunni fyrir höfundarumhverfi svæðisins velurðu **Ný síða**.
1. Í svarglugganum **Nýtt svæði** gefurðu upp eftirfarandi upplýsingar.

| Svæði                               | Lýsing |
|-------------------------------------|-------------|
| Svæðaheiti                           | Sláðu inn skjáheitið sem ætti að nota fyrir síðuna þína í umhverfi höfundaréttarins. Þetta nafn er aðeins sýnilegt í höfundarumhverfinu og verður ekki sýnt viðskiptavinum. |
| Öryggishópur vefstjórans | Tilgreindu Microsoft Azure Active Directory (Azure AD) öryggishóp sem heldur utan um notendur sem hafa hlutverk stjórnanda vefsins á þessari síðu. |
| Sjálfgefin rás (númer rekstrareiningar) | Veldu netverslunina sem þessi síða mun þjóna sem vefverslun fyrir. Ef vefsvæðið á að styðja margar netverslanir verður að tengja verslanir við síðuna þína á **Síðustillingar** eftir að svæðið er sett upp. |
| Sjálfgefið tungumál                            | Tilgreindu sjálfgefið tungumál fyrir þessa netverslun og markað. Netverslun getur stutt mörg tungumál. Ef þú vilt styðja mörg tungumál fyrir þessa netverslun eða aðra netverslun geturðu stillt þann stuðning í **Stillingar svæðis** eftir að svæðið er settur upp.  |
| Lén                              | Veldu heiti léns sem mun þjóna sem lén fyrir þessa vefverslun. Ef þú hefur ekki stillt nein lén í LCS geturðu haft þennan reit auðan. Eftir að lénið þitt er stillt í LCS verðurðu að bæta því við netverslunina þína í **Stillingar svæðis**.  |
| Slóð                              | Þegar vefsvæðið þitt styður fleiri en eitt tungumál fyrir tiltekið lén, notaðu slóðareitinn til að búa til einstaka vefslóð fyrir það lén og tungumálasamsetningu. Ef tungumálið sem þú tilgreindir í reitnum **Sjálfgefið tungumál** er eina tungumálið sem þú munt styðja fyrir þetta lén eða heldur áfram að vera sjálfgefið tungumál eftir að þú hefur staðfært síðuna á fleiri tungumál mælum við með að þú hafir þennan reit auðan. |

Eftir að vefsvæðið þitt er búið til geturðu staðfest að það er tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina. Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að úthlutuðum afurðum eftir flokkum.

## <a name="rename-your-site"></a>Endurnefna síðuna þína

Til að endurnefna síðuna þína í Site builder skaltu fylgja þessum skrefum.

1. Til að opna lista yfir vefsvæði velurðu **Vefskiptaskipti** í efra hægra horninu og veldu síðan **Stjórna síðum**. 
1. Veldu gátreitinn við hliðina á síðunni sem þú vilt endurnefna og veldu síðan **Endurnefna** á skipanastikunni.
1. Í **Nýtt nafn síðunnar** valmynd, sláðu inn nýja nafnið á vefsvæðinu og veldu síðan **Allt í lagi**. Veflistinn mun uppfærast til að sýna nýtt nafn síðunnar.

## <a name="delete-a-site"></a>Eyða síðu

Fylgdu þessum skrefum til að eyða síðu í Site builder.

1. Til að opna lista yfir vefsvæði velurðu **Vefskiptaskipti** í efra hægra horninu og veldu síðan **Stjórna síðum**.
1. Veldu síðuna sem þú vilt eyða og veldu síðan **Eyða** á skipanastikunni.
1. Í **Eyða\<site name\>** valmynd, sláðu inn nafn vefsvæðisins og veldu síðan **Eyða**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md)

[Tengja svæði Dynamics 365 Commerce við netrás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Hlaða upp mörgum URL-framsendingum í einu](upload-bulk-redirects.md)

[Setja upp B2C-leigjanda í Commerce](set-up-B2C-tenant.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Stilla marga B2C leigjendur í viðskiptaumhverfi](configure-multi-B2C-tenants.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
