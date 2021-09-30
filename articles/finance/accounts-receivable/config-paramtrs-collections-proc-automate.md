---
title: Skilgreina færibreytur fyrir sjálfvirkt innheimtuferli
description: Þetta efnisatriði lýsir færibreytunum sem hafa áhrif á sjálfvirk innheimtuferli og veitir leiðsögn fyrir stillingu þeirra þannig að sjálfvirka ferlið endurspegli áform og væntingar þínar.
author: JodiChristiansen
ms.date: 08/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-26
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 3055e10375f1b0be936e3ed0344cdf33dc7bc7e9
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487075"
---
# <a name="configure-parameters-for-collection-process-automation"></a>Skilgreina færibreytur fyrir sjálfvirkt innheimtuferli

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir færibreytunum sem hafa áhrif á sjálfvirk innheimtuferli og veitir leiðsögn fyrir stillingu þeirra þannig að sjálfvirka ferlið endurspegli áform og væntingar þínar. Fyrir upplýsingar um hvernig á að gera innheimtuferla sjálfvirka skal skoða [Sjálfvirkni innheimtuferlis](collections-process-automate.md).

## <a name="general"></a>Almennt
Færðu inn tölu í **Prósentuhlutfall viðskiptavina í hverju runuverki** til að ákvarða fjölda runuverka eftir sjálfvirkniferli. Stilltu **Bóka innheimtubréf sjálfkrafa** á **Já** þannig að gerð aðgerðar fyrir innheimtubréf muni bóka bréfið í sjálfvirka ferlinu. Stillið **Stofna verkþætti fyrir sjálfvirkni** á **Já** til að stofna og loka verkþáttum fyrir gerðir aðgerðar sem ekki eru verkþáttargerðar til að skoða öll sjálfvirku skrefin sem eru tekin á reikningi. Skilgreindu fjölda daga sem innheimtuferill er geymdur í **Dagar sem geyma á feril sjálfvirks innheimtuferlis**. Þegar reikningur nær til síðasta skrefs innheimtuferlisins verður hann ekki notaður til að búa til gerðir sjálfvirkniaðgerða í framtíðinni ef **Útiloka reikning eftir virkjun síðasta skref ferlis** er stillt á **Já**. Næstelsti reikningurinn ákvarðar næsta sjálfvirkniskref til að tryggja að sjálfvirkniaðgerðir fyrir innheimtuferlið haldi áfram. 

## <a name="payment-predictions"></a>Greiðsluspár
Frá og með útgáfu 10.0.21 eru greiðsluspár viðskiptavina, sem finna má í fjármálainnsýn, spáir fyrir um hvort reikningur verði greiddur í tíma, of seint eða mjög seint. Hægt er að stilla hvern þessara flokka í fjármálainnsýn. Ef spáð er fyrir að reikningar verði greiddir seint er mikilvægt að hefja innheimtuferlið áður en reikningurinn fellur á gjalddaga. Hægt er að nota þessar spár til að búa til innheimtuaðgerðir þegar sjálfvirkni innheimtuferlis er keyrð. Stilltu **Virkja greiðsluspár** á **Já** til að nota greiðsluspár viðskiptavina til að búa til innheimtuaðgerðir sem byggja á líkum á því að reikningurinn verði greiddur of seint. 

Frekari upplýsingar um greiðsluspár viðskiptavina og fjármálainnsýn er að finna í [Greiðsluspár viðskiptavina](payment-insights-overview.md).

Þegar greiðsluspárlíkan viðskiptavina er keyrt úthlutar það prósentu á spána um að reikningur verði greiddur á réttum tíma, of seint eða mjög seint. Hægt er að nota þessar upplýsingar til að hefja innheimtuaðgerðir sjálfkrafa með sjálfvirku innheimtuferli í tilvikum þegar búist er við greiðsludrætti. Þú getur skoðað þessar prósentur á síðunum **Greiðsluspár fyrir hvern viðskiptavin** eða **Greiðsluspár fyrir hverja færslu** undir **Skuldir og innheimta > Innheimtur**. 

Ef greiðsluspá að meðaltali fyrir reikning viðskiptavinar er minni en viðmiðunarprósentan er ekki þörf á neinum aðgerðum. Ef spá reiknings er meiri en eða jafnt og viðmiðunarprósentan er ein aðgerð búin til á hvern viðskiptavin. Fyrir **Spá: seint** skal færa inn **Viðmiðunarprósentu** sem segir til um hvenær sjálfvirkni innheimtuferlis eigi að búa til innheimtuaðgerðir. Þetta er samanlagt gildi fyrir bæði of seint og mjög seint. Veldu **Sniðmát viðskiptaskjals** til að nota fyrir stofnaða aðgerð eða búðu til nýja. Þetta auðkennir **Gerðina**, **Tilganginn** og **Dagar þar til verkþætti er lokað**. Færðu inn **Athugasemdir** sem verða sjálfgefið lýsingin þegar aðgerðin er stofnuð. Fyrir **Spá: mjög seint** skal færa inn **Viðmiðunarprósentu** sem segir til um hvenær sjálfvirkni innheimtuferlis eigi að búa til innheimtuaðgerðir fyrir viðskiptavin sem spáð er að greiði reikninga mjög seint. Veldu **Sniðmát viðskiptaskjals** til að nota fyrir stofnaða aðgerð. Þetta auðkennir **Gerðina**, **Tilganginn** og **Dagar þar til verkþætti er lokað**. Færðu inn **Athugasemdir** sem verða sjálfgefið lýsingin þegar aðgerðin er stofnuð. 

### <a name="example"></a>Dæmi
Ef síðbúin viðmiðunarprósenta er stillt á 60%. Þegar greiðsluspár viðskiptavina eru keyrðar fyrir hvern reikning fær kerfið úthlutað prósentuhlutfalli spár fyrir að fá greitt á réttum tíma, seint eða mjög seint. Ef greiðsluspáin um að reikningurinn verði greiddur seint er 59% eða lægri verður engin innheimtuaðgerð búin til fyrir reikninginn í sjálfvirka innheimtuferlinu. Ef greiðsluspá viðskiptavinar fyrir reikning er hærri en eða jöfn 60% er innheimtuaðgerð búin til meðan á sjálfvirka innheimtuferlinu stendur. 

> [!NOTE]
> Lagt er mat á spá fyrir mjög seint á undan spá fyrir of seint vegna þess að mjög seint felur í sér reikninga sem spáð er að verði greiddir of seint. Innheimtuferlið býr aðeins til eina aðgerð ef reikningurinn fellur bæði undir viðmiðin seint og mjög seint. Í því tilfelli notar kerfið aðgerð fyrir mjög seint og viðskiptaskjal vegna þess að mjög seint er sett í hærri forgang. Aðrar aðgerðir sem hafa verið búnar til verða ekki búnar til aftur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
