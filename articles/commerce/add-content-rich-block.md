---
title: Textabálkseining
description: Þetta efni fjallar um textabálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 18a4226d3b8dce1b46e6612521d70a3627b517d1
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780490"
---
# <a name="text-block-module"></a>Textabálkseining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um textabálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

Textabálkseining er eining sem er notuð til að bæta við textainnihaldi. Þetta efni getur verið upplýsandi eða kynningar.

Textabálkseiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er. Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.

## <a name="examples-of-text-block-modules-in-e-commerce"></a>Dæmi um textabálkseiningar í rafrænum viðskiptum

Hægt er að nota textabálkseiningar á eftirfarandi hátt:

* Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.
* Til upplýsinga á hvaða síðu sem er. Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.
* Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu. (til dæmis „Ókeypis sending fyrir pantanir yfir $50“).
* Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).

Eftirfarandi mynd sýnir dæmi um textabálkseiningu sem er notuð á heimasíðu.

![Dæmi um einingu textabálks.](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a>Eiginleikar textabálkseiningar

| Nafn eiginleika     | Virði                                            | lýsing |
|-------------------|--------------------------------------------------|-------------|
| RTF-snið         | RTF-snið                                        | Texti efnisgreinar. Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta. |
| Sérsniðið heiti klasa | Klasaheiti Cascading Style Sheets (CSS)        | Heiti sérsniðins CSS-klasa sem forritari veitir til að forsníða þessa einingu. Skilgreina ætti klasaheitið í þemapakkanum. |
| Leturtærð         | **Lítil**, **Miðlungs**, **Stór** eða **X-stór** | Leturstærð fyrir innihaldið. |

## <a name="add-a-text-block-module-to-a-page"></a>Bæta við textabálkseiningu á síðu

Fylgdu þessum skrefum til að bæta textabálkseiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í **Nýtt sniðmát** svargluggi, undir **Nafn sniðmáts**, koma inn **Efnissniðmát**.
1. Í **Líkami** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Sjálfgefin síða** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Efnissíða**, og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Efnissniðmát**, og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**. 
1. Í **Aðal** rauf á nýju síðunni, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Textablokk** mát og veldu síðan **Allt í lagi**. 
1. Í eiginleikaglugga textabálkseiningarinnar bætirðu texta við í reitinn **Mótaður texti**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Tilboðsborðaeining](add-alert.md)

[Myndaræmueining](add-carousel.md)

[Eining fyrir bálk með efni](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
