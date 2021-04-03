---
title: Virkja sérsniðnar afurðaráðleggingar
description: Þetta efnisatriði lýsir því hvernig á að gera sérsniðnar afurðatillögur tiltækar fyrir viðskiptavini í Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: be460ec5ce8a9a625dc1a80f761bea9e2ab2f632
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477661"
---
# <a name="enable-personalized-recommendations"></a>Kveikja á sérsniðnum tillögum

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að gera sérsniðnar afurðatillögur tiltækar fyrir viðskiptavini í Microsoft Dynamics 365 Commerce.

Í Dynamics 365 Commerce geta smásalar gert persónulegar ráðleggingar um vörur (einnig þekktar sem persónugervingar) tiltækar. Þannig er hægt að fella persónulegar ráðleggingar inn í upplifun viðskiptavina á netinu og á sölustað (POS). Þegar kveikt er á sérstillingaraðgerðinni getur kerfið tengt kaup notanda og vöruupplýsingar til að búa til sérsniðnar ráðleggingar um vöru.

## <a name="personalization-prerequisites"></a>Forsendur sérstillingar

Áður en þú gerir persónulegar ráðleggingar um vörur tiltækar fyrir viðskiptavini skaltu hafa í huga að tillögur um vöru eru aðeins studdar notendum viðskiptamanna sem hafa flutt geymslu sína til Azure Data Lake Store. Áður en viðskiptavinir geta fengið persónulegar ráðleggingar um vöru verða smásalar að gera það [kveikja á ráðleggingum um vörur](enable-product-recommendations.md).

> [!NOTE]
> Með því að kveikja á tilmælum til vara kveikirðu líka á sérsniðinni. Hins vegar, ef þú slekkur á sérstillingu, slekkurðu ekki á öðrum tegundum ráðlegginga um vöru.

Nánari upplýsingar um afurðatillögur er að finna í [yfirliti yfir afurðatillögur í POS-skjölum](product-recommendations.md).

## <a name="turn-on-personalization"></a>Kveikja á aðlögun

Fylgdu þessum skrefum til að kveikja á persónuaðlögun.

1. Í Commerce Headquarters skal leita að **Eiginleikastjórnun**.
1. Veljið **Allir** til að sjá lista yfir tiltæka eiginleika. 
1. Í leitarreitnum skal slá inn **Ráðleggingar**.
1. Velja eiginleikann **Sérsniðnar afurðarráðleggingar**.
1. Á svæðinu **Sérsniðnar afurðaráðleggingar** skal velja **Virkja núna**.

![Kveikt á aðlögun](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> Þegar þú kveikir á sérsniðinni er ferlið við að búa til sérsniðna vöru meðmæla lista byrjað. Allt að einn dagur gæti verið nauðsynlegur áður en þessir listar eru tiltækir og sýnilegir á netinu og í POS.

## <a name="personalized-lists"></a>Sérsniðnir listar

Auk þess að gera ráð fyrir að sérsníða fyrirliggjandi vélalista, gera ráðleggingarþjónustan kleift að sérsníða reynslu af uppgötvun vöru bæði á netinu og í POS.

Eftir að kveikt er á sérstillingu geta smásalar sýnt kaupendum persónulega „Tillögur fyrir þig“ lista á netinu eða „Mælt með fyrir viðskiptavini“ lista á POS skautanna. Að auki geta smásalar beitt sérsniðningu á fyrirliggjandi vörumælalista og útvegað Almennu persónuverndarreglugerðina (GDPR) uppljóstrunarupplifun fyrir staðfesta notendur. Ef þú slekkur á sérsniðinni, slekkurðu einnig á þessum eiginleikum.

### <a name="online-picks-for-you-lists"></a>Listar yfir „Tillögur fyrir þig“ á netinu

„Tillögur fyrir þig“ listi er listi yfir gervigreindarvélar (AI-ML) sem sýnir staðfestum notanda persónulega lista yfir fyrirhugaðar vörur. Þessi listi er byggður á fjölrása kaupsögu notandans. Sérsniðnar ráðleggingar eru uppfærðar með virkum hætti þegar notandinn gerir fleiri kaup. Þessi tegund af lista styður einnig flokkun sía, svo að smásalar geti sýnt helstu val, byggðar á stigveldum siglinga.

Áður en „Tillögur fyrir þig“ listinn getur birst á hvaða e-Commerce síðu sem er þarf að uppfylla eftirfarandi notendakröfur:

- Notendur verða að vera skráðir inn. Nafnlausir notendur munu ekki sjá persónulegar tillögur.
- Notendur verða að hafa að minnsta kosti eina kaup á reikningi sínum.
- Notendur verða að taka þátt í að fá persónulegar ráðleggingar.

Eftirfarandi mynd sýnir dæmi um „Tillögur fyrir þig“ á netverslunarsíðu.

![Listar yfir „Tillögur fyrir þig“ á netinu](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a>Listar með „Mælt með fyrir viðskiptavini“ í POS

Til að auka upplifun viðskiptavinarins geta smásalar sérsniðið núverandi upplýsingasíður viðskiptavina með því að bæta við samhengislistann „Mælt með fyrir viðskiptavini“.

Eftirfarandi mynd sýnir dæmi um „Mælt með fyrir viðskiptavini“ á afgreiðslukassa.

![Listinn Mællt með fyrir viðskiptavini í POS](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a>Notaðu persónugervingu á fyrirliggjandi meðmæla lista

Söluaðilar geta beitt sérsniðum á fyrirliggjandi ráðleggingalista, svo sem „Nýtt“, „Væntanlegt“, „Mest selt“, „Fólk kann líka vel við“ og „Oft keypt saman.“ Þegar sérstillingu er beitt á núverandi lista eru hlutir sem skráður notandi keypti áður keyptir af þessum listum. Fyrir bæði nafnlausa notendur og notendur sem hafa afþakkað að fá persónulegar ráðleggingar, eru sjálfgefnar útgáfur af núverandi listum sýndar. Þess vegna þurfa smásalar ekki að hafa sérstaka síðureynslu handvirkt.

Til dæmis hefur skráður notandi þegar keypt svarta úrið og brúnu vinnuskóna sem birtast á listanum „Vinsælt - sjálfgildi“ á eftirfarandi mynd. Þess vegna mun notandinn sjá nýjar vörur í stað þessara vara, eins og sýnt er í listanum „Vinsælt - sérsniðið“.

![Að beita sérsniðum](./media/applypersonalization.png)

Fylgdu þessum skrefum til að beita sérsniðun á fyrirliggjandi meðmælalista í vefsvæðishönnuði Commerce.

1. Opnaðu núverandi síðu byggingarsíðu sem inniheldur vörusöfnunareiningu.
1. Í vinstri stýriglugganum velurðu vörusafnseininguna.
1. Í hægri stýriglugganum undir **Afurðir** velurðu listann.
1. Í **Veldu stillingu vörulistans** valmynd, undir **Gerð**, veldu gerð listans.
1. Veldu **Notaðu sérsnið** merktu við reitinn og veldu síðan **Í lagi**.

    ![Notkun sérsniðs á vinsældalista](./media/ApplyPersonalizationToTrending.PNG)

1. Vistaðu síðuna, ljúktu við að breyta því og birtu hana síðan. Eftir að síðunni er birt munu innskráðir notendur sjá sérsniðna vinsældalista.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Virkja Azure Data Lake Storage í Dynamics 365 Commerce-umhverfi](enable-adls-environment.md)

[Virkja ráðleggingar um afurðir](enable-product-recommendations.md)

[Virkja tillögur um að kaupa svipaða vöru](shop-similar-looks.md)

[Afþakka sérsniðnar tillögur](personalization-gdpr.md)

[Bæta afurðaráðleggingum við sölustað](product.md)

[Bæta við tillögum á færsluskjáinn](add-recommendations-control-pos-screen.md)

[Aðlagaðu niðurstöður AI-ML](modify-product-recommendation-results.md)

[Búðu til handvirkt myndaðar ráðleggingar](create-editorial-recommendation-lists.md)

[Búðu til tillögur með kynningargögnum](product-recommendations-demo-data.md)

[Algengar spurningar um afurðaráðleggingar](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
