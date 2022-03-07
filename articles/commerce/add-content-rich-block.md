---
title: Textabálkseining
description: Þetta efni fjallar um textabálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 9068c35eaeee68f97d81d168983d7281da09491cb0afd70cb8196010ce771b0d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723312"
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
1. Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Efnissniðmát**.
1. Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í svarglugganum **Velja sniðmát** skal velja **Efnissniðmát**. Undir **Síðuheiti** skal færa inn **Efnissíða** og síðan velja **Í lagi**.
1. Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.
1. Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.
1. Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**. 
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