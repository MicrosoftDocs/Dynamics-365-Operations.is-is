---
title: Bættu við samfélagsmiðlum
description: Þessi grein lýsir því hvernig á að bæta við félagslegum auðkennisveitendum í Microsoft Azure gátt.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.openlocfilehash: 5596097a5484acafda54adcfffa68fb59c8fbc65
ms.sourcegitcommit: 774f8f97a0b14cf1199bd1802178ccf536a25ade
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/17/2022
ms.locfileid: "9785811"
---
# <a name="add-social-identity-providers"></a>Bættu við samfélagsmiðlum

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að bæta við félagslegum auðkennisveitendum í Microsoft Azure gátt.

Kennitöluveitendur leyfa notendum að nota samfélagsreikninga sína til staðfestingar. Valfrjálst er að bæta við sannvottun fyrir kennisveitanda í Dynamics 365 Commerce. 

Ef auðkenningu fyrir samfélagsleg auðkenni er ekki bætt við er sjálfgefið Azure Active Directory (Azure AD) B2C prófílar verða aðalsniðin fyrir notendahópinn þinn. Notendur munu velja eigið notandanafn (valin netföng) og setja lykilorð. Azure AD B2C staðfestir notendur beint. 

Ef staðfesting á kennitöluveitanda bætist við og notandi velur einn af þeim kennitöluveitendum sem eru í boði er eining samt stofnuð í Azure AD B2C leigjandi. Azure AD B2C mun síðan staðfesta persónuskilríki notandans hjá kennitöluveitanda.

> [!NOTE]
> Innskráning kennisveitanda stofnar skrá í B2C leigjandanum, en á öðru sniði en staðbundnir reikningar þar sem það mun kalla tilvísun ytri kennitöluveitanda til staðfestingar. Notandinn getur notað sama netfang á milli kennitöluveitenda, sem þýðir að notandanafn tölvupóstsins sem notað er til sannvottunar er hugsanlega ekki einkvæmt fyrir leigjanda. Azure AD B2C mun einungis framfylgja því að notendur hafi einkvæmt netfang á B2C reikningum.

Áður en þú getur bætt við kennitöluveitanda til að staðfesta, verður þú að fara í gátt kennisveitanda og setja upp umsókn um kennisveitanda samkvæmt leiðbeiningunum í Azure AD B2C skjöl. Hér fyrir neðan er listi yfir tengla á fylgiskjölin.

- [Amazon](/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [Azure AD (Stakur leigjandi)](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [Microsoft-reikningur](/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [Facebook](/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [GitHub](/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [Google](/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [LinkedIn](/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [OpenID Connect](/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [Twitter](/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a>Bættu við og settu upp kennisveitanda

> [!NOTE]
> Að bæta við veitendum félagslegra auðkenninga er valfrjálst skref þegar þú setur upp leigjanda frá fyrirtæki til neytenda (B2C) í Microsoft Dynamics 365 Commerce.

Fylgdu þessum skrefum til að bæta við og setja upp kennisveitanda.  

1. Farðu á Azure gáttina **Persónuaðilum**.
1. Veljið **Bæta við**. Skjárinn **Bæta við kennisveitanda** birtist.
1. Undir **Nafn**, sláðu inn nafnið sem á að birtast notendum á innskráningarskjánum þínum.
1. Undir **Gerð auðkennisveitanda**, veldu auðkennisveitanda af listanum.
1. Veljið **Í lagi**.
1. Veldu **Setja þennan kennisveitanda upp** til að fá aðgang að skjánum **Setja upp kennisveitanda**.
1. Undir **Biðlarakenni**, sláðu inn biðlarakennið eins og það er fengið úr forritsuppsetningu kennisveitandans.
1. Undir **Leynilykill biðlara**, sláðu inn leynilykill biðlara eins og það er fengið úr forritsuppsetningu kennisveitandans.
1. Hengdu notendaflæði fyrir innskráningar-/skráningarreglur:
1. Fara til **Azure AD B2C - Notendastreymi (reglur) \> {innskráningarstefna þín fyrir innskráningu} \> Kennisveitendur**.
1. Til að hengja innskráningu/skráningu notendaflæðisstefnu skaltu velja hverja auðkennisveitu sem þú hefur sett upp fyrir reikninginn þinn. Til að prófa flæði, veldu **Keyra notendaflæði** fyrir hvern auðkennisaðila. Nýr flipi sýnir innskráningarsíðuna sem sýnir valreitinn fyrir nýja auðkennisveitu.

Eftirfarandi mynd sýnir dæmi um skjáina **Bæta við kennisveitanda** og **Setja upp kennitöluveitanda** í Azure AD B2C.

![Að bæta við kennitöluveitanda fyrir forritið.](./media/B2CImage_14.png)

Eftirfarandi mynd sýnir dæmi um hvernig eigi að velja kennisveitendur á síðunni Azure AD B2C **Kennisveitendur**.

![Veldu alla kennitöluveitendur til að gera kleift að nota fyrir stefnu þína.](./media/B2CImage_16.png)

Eftirfarandi mynd sýnir dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan.

> [!NOTE]
> Ef notaðar eru sérstilltar síður sem eru innbyggðar í Commerce fyrir notandaflæðin verður að bæta hnöppunum fyrir kennitöluveitur við með því að nota stækkunareiginleikana í einingasafni Commerce. Auk þess, þegar forritin eru sett upp með ákveðinni kennitöluveitu, gætu strengir vefslóða eða skilgreininga verið í sumum tilfellum gert greinarmun á há- og lágstöfum. Frekari upplýsingar er að finna í tengingarleiðbeiningum kennitöluveitanda.
 
![Dæmi um sjálfgefinn innskráningarskjá með innskráningarhnappi fyrir kennitöluveitanda sýndan.](./media/B2CImage_17.png)

## <a name="next-steps"></a>Næstu skref

Til að halda áfram ferlinu við að setja upp B2C leigjanda í Commerce skaltu halda áfram að [Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp B2C-leigjanda í Commerce](set-up-b2c-tenant.md)

[Búðu til eða tengdu við núverandi Azure AD B2C leigjandi í Azure gáttinni](create-link-aad-b2c-tenant.md)

[Stofna B2C forrit](create-b2c-app.md)

[Stofna notandaflæðisstefnu](create-user-flow-policies.md)

[Uppfærðu höfuðstöðvar viðskipta með nýju Azure AD B2C upplýsingar](update-hq-aad-b2c-info.md)

[Stilla B2C leigjanda þinn í Commerce vefsvæðishönnuði](config-b2c-tenant-site-builder.md)

[Frekari B2C upplýsingar](additional-b2c-info.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
