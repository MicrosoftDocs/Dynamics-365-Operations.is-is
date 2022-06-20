---
title: Tengja tilraun og breyta afbrigðum
description: Þessi grein lýsir því hvernig á að tengja tilraun í þjónustu þriðja aðila við Dynamics 365 Commerce, og hvernig á að breyta tilbrigðum fyrir tilraunina.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942823"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Tengja tilraun og breyta afbrigðum

Þessi grein lýsir því hvernig á að tengja tilraunina þína í Commerce og gera breytingar á afbrigðum þínum þannig að þau samræmist tilgátunni þinni. 

Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum.

[ ![Tilraunaferli notanda - Tengja og breyta.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Þegar [búið er að setja upp tilraunina](experimentation-setup.md) í þjónustu þriðja aðila skal tengja tilraunina við Dynamics 365 Commerce og breyta afbrigðum tilraunarinnar.

## <a name="connect-your-experiment"></a>Tengja tilraun
Til að tengja tilraunina þarf að ræsa leiðsagnarforritið **Tengja tilraun**. Leiðsagnarforritið fer með þér í gegnum skrefin sem þarf til að tengja tilraunina. Þegar leiðsagnarforritinu er lokið er tillraunin tengd og afbrigði eru búin til og þau tilbúin fyrir breytingar.

Til að hefjast handa við að tengjasting tilraun í Commerce svæðasmíð skal fylgja þessum skrefum.

1. Til að ræsa **Connect-tilraun** leiðsagnarforritið skal velja **Tilraunir** í vinstra yfirlitssvæði og síðan velja **Tengja**. Einnig er hægt að opna leiðsagnarforritið af síðu eða broti með því að breyta því og velja **Connect tilraun** á skipanastikunni.

    > [!NOTE]
    > - Síða getur aðeins verið tengd við eina tilraun í einu. Til að tengja síðu við aðra tilraun skal fyrst eyða tilrauninni sem síðan er tengd við.
    > - Þú getur aðeins gert tilraunir á síðum með sérsniðnu skipulagi. Ef síðan þín er með forstillt útlit, breyttu því fyrst í sérsniðið skipulag. Þú getur gert þetta með því að fara á síðuna og velja **Umbreyttu í sérsniðið skipulag** á skipanastikunni. Fyrir frekari upplýsingar um skipulag, sjá [Forstillt og sérsniðið skipulag](templates-layouts-overview.md#preset-and-custom-layouts). 

1. Ef þú ert að tengjast tilraun frá **Tilraunir** flipann í vinstri yfirlitsrúðunni, veldu nafn tilraunarinnar af listanum sem birtist.
1. Veldu síðuna eða brotið sem þú vilt keyra tilraunina þína á.
1. Í lokaskrefi leiðsagnarforritsins skal velja **Búa til afbrigði og hætta í leiðsagnarforritinu**. Afbrigði eru búin til fyrir tilraunina. 

> [!NOTE]
> Ef ætlunin er að tímasetja hvenær tilraunin er birt á lifandi svæðinu, skal ganga úr skugga um efnið sem tengja á við tilraunina sé tiltækt í birtingarhóp *áður en* þú tengir tilraunina. Frekari upplýsingar um birtingarhópa er að finna í [Vinna með birtingarhópa](publish-groups.md).

## <a name="edit-your-variations"></a>Breyta afbrigðum

Þegar þú ferð út úr **Tengja tilraun** töframaður, afbrigði eru búin til fyrir þig. Fylgdu skrefunum hér að neðan til að breyta tilbrigðum þannig að þau endurspegli valið sem þú þarft að sannreyna í tilraunatilgátunni.

1. Í yfirliti ritils skal nota fellivalmynd afbrigðanna fyrir neðan skipanastikuna til að breyta hverju afbrigði fyrir sig samkvæmt upprunalegu tilgátunni. Þú gætir einnig viljað setja upp samanburðar- eða grunnafbrigði með því að skilja eitt þessarar afbrigða eftir óbreytt.
1. Veldu eininguna sem á að gera tilraunir á, veldu úrfellingarmerkið (...) og veldu síðan **Bæta við tilraun**.

> [!NOTE]
> Íhugaðu að koma á stýringu eða grunnafbrigði með því að láta eitt af tilbrigðunum óbreytt.

## <a name="previous-step"></a>Fyrra skref
[Setja upp tilraun](experimentation-setup.md) 


## <a name="next-step"></a>Næsta skref
[Forskoða og birta tilraun](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
