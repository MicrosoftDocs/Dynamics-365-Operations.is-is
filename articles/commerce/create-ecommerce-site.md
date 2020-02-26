---
title: Stofna svæði fyrir rafræn viðskipti
description: Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d3d8a290f06d9734be21f2d59152acac6857506
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002014"
---
# <a name="create-an-e-commerce-site"></a>Stofna svæði fyrir rafræn viðskipti


[!include [banner](includes/banner.md)]

Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.

Áður en hægt er að hefja þróun á netverslunarsíðunni verðurðu fyrst að stofna nýja síðu í vefsvæðishönnuðinum. 


Til að byrja að þróa netverslunarsíðuna þína verðurðu fyrst að stofna nýja síðu í umhverfi höfundaréttarins. Áður en þú getur búið til nýja síðu verður að búa til að minnsta kosti eina netverslun í Commerce. 


## <a name="set-up-your-site"></a>Setja upp síðuna

Til að setja upp síðuna þína skaltu gera eftirfarandi.

1. Opnaðu umhverfi vefsvæðishönnuðar. Þú getur fundið tengil á vefsvæði byggingaraðila í Microsoft Lifecycle Services (LCS) á umhverfisaðgerðarsíðunni fyrir Commerce.
1. Á heimasíðunni fyrir höfundarumhverfi svæðisins velurðu **Ný síða**.
1. Í svarglugganum **Nýtt svæði** gefurðu upp eftirfarandi upplýsingar.

| Svæði                               | Lýsing |
|-------------------------------------|-------------|
| Svæðaheiti                           | Sláðu inn skjáheitið sem ætti að nota fyrir síðuna þína í umhverfi höfundaréttarins. Þetta nafn er aðeins sýnilegt í höfundarumhverfinu og verður ekki sýnt viðskiptavinum. |
| Öryggishópur vefstjórans | Tilgreindu Microsoft Azure Active Directory (Azure AD) öryggishóp sem heldur utan um notendur sem hafa hlutverk stjórnanda vefsins á þessari síðu. |
| Sjálfgefin rás (númer rekstrareiningar) | Veldu netverslunina sem þessi síða mun þjóna sem vefverslun fyrir. Ef þú vilt að netverslunarsíðan þín styðji margar netverslanir, verður þú að tengja verslanirnar við síðuna þína á **Stillingar svæðis** eftir að svæðið er sett upp. |
| Sjálfgefið tungumál                            | Tilgreindu sjálfgefið tungumál fyrir þessa netverslun og markað. Netverslun getur stutt mörg tungumál. Ef þú vilt styðja mörg tungumál fyrir þessa netverslun eða aðra netverslun geturðu stillt þann stuðning í **Stillingar svæðis** eftir að svæðið er settur upp.  |
| Lén                              | Veldu heiti léns sem mun þjóna sem lén fyrir þessa vefverslun. Ef þú hefur ekki stillt nein lén í LCS geturðu haft þennan reit auðan. Eftir að lénið þitt er stillt í LCS verðurðu að bæta því við netverslunina þína í **Stillingar svæðis**.  |
| Slóð                              | Þegar vefsvæðið þitt styður fleiri en eitt tungumál fyrir tiltekið lén, notaðu slóðareitinn til að búa til einstaka vefslóð fyrir það lén og tungumálasamsetningu. Ef tungumálið sem þú tilgreindir í reitnum **Sjálfgefið tungumál** er eina tungumálið sem þú munt styðja fyrir þetta lén eða heldur áfram að vera sjálfgefið tungumál eftir að þú hefur staðfært síðuna á fleiri tungumál mælum við með að þú hafir þennan reit auðan. |


Eftir að vefsvæðið þitt er búið til geturðu staðfest að það er tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina. Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að úthlutuðum afurðum eftir flokkum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skilgreina lénsheiti](configure-your-domain-name.md)

[Uppsetning á nýju vefsvæði fyrir rafræn viðskipti](deploy-ecommerce-site.md)

[Tengja netsvæði við rás](associate-site-online-store.md)

[Vinna með skrárnar robots.txt](manage-robots-txt-files.md)

[Setja upp sérsniðnar síður fyrir innskráningu notenda](custom-pages-user-logins.md)

[Bæta við stuðningi fyrir efnisbirtingarnet (CDN)](add-cdn-support.md)

[Virkja greiningu á verslun eftir staðsetningu](enable-store-detection.md)
