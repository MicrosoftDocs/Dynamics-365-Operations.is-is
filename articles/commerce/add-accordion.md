---
title: Fellingareining
description: Þessi grein fjallar um harmonikkueiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: ec895476770f297825d6c88d0b0a5fef43a5c6ef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279157"
---
# <a name="accordion-module"></a>Fellingareining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um harmonikkueiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Fellingareiningar líta út eins og hólfaeiningar sem eru notaðar við skipulagningu upplýsinga eða eininga á síðu með því að bjóða upp á möguleika sem lítur út eins og skúffa sem hægt er að draga út. Fellingareiningar er hægt að nota á öllu síðum.

Innan hverrar fellingareiningar er hægt að bæta við einu eða fleiri fellingareiningaratriðum. Sérhvert atriði fellingareiningar felur í sér opnanlega skúffu. Innan hvers fellingareiningaratriðis er hægt að bæta við einni eða fleiri einingum. Engar takmarkanir eru á þeim gerðum eininga sem hægt er að bæta við fellingareiningaratriði.

Eftirfarandi mynd sýnir dæmi um fellingareiningu sem er notuð til að halda skipulagi á upplýsingum á síðu verslunar með algengum spurningum.

![Dæmi um fellingareiningu.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Eiginleikar fellingareiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Yfirskrift | Texti | Þessi eiginleiki sýnir valfrjálsa textafyrirsögn fyrir fellingareininguna. |
| Stækka allt | **Satt** eða **Ósatt** | Ef gildið er stillt á **Satt** er kveikt á víkka/draga saman virkninni þannig að hægt sé að víkka og draga saman öll atriði í fellingareiningunni. |
| Samskiptastíll | **Óháð** eða **Víkka aðeins eitt atriði** | Þessi eiginleiki skilgreinir samskiptastíl fellingaratriða. Ef gildið er stillt á **Óháð** er hægt að víkka og draga saman hvert fellingaratriði fyrir sig. Ef gildið er stillt á **Víkka aðeins eitt atriði** er aðeins hægt að víkka eitt atriði í einu. Þegar atriði eru víkkuð dragast saman þau atriði sem voru víkkuð á undan. |

## <a name="accordion-item-module-properties"></a>Eiginleikar fellingareiningaratriða

| Nafn eiginleika | Gildi | lýsing |
|----------------|--------|-------------|
| Titill | Texti | Þessi eiginleiki sýnir titiltexta fyrir atriði fellingareiningar. Með því að velja titilsvæðið geta notendur víkkað eða dregið saman hlutann. |
| Víkka sjálfgefið | **Satt** eða **Ósatt** | Ef gildið er stillt á **Satt** víkkar atriði fellingareiningar að sjálfgefnu þegar síðan er hlaðin inn. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Bæta fellingareiningu við síðu algengra spurninga

Til að bæta fellingareiningu við síðu algengra spurninga og stilla eiginleika hennar í svæðissmið skal fylgja þessum skrefum.

1. Opnið **Síður** og notið markaðssniðmát Fabrikam (eða annað sniðmát sem er með engum takmörkunum) til að búa til nýja síðu sem heitir **Algengar spurningar verslunar**.
1. Í **Aðal** rifa á **Sjálfgefin síða**, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Harmonikku** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði fellingareiningar skal velja **Fyrirsögn** við hliðina á blýantstákninu.
1. Í glugganum **Fyrirsögn**, undir **Texti fyrirsagnar**, skal færa inn **Algengar spurningar**. Veljið síðan **Í lagi**.
1. Á eiginleikasvæði fellingareiningar skal velja gátreitinn **Sýna allt víkkað** og síðan, í reitnum **Samskiptastíll**, skal velja **Óháð**.
1. Í **Harmonikku** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Harmonikku atriði** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði fellingareiningaratriðis, undir **Titill**, skal færa inn titiltexta (til dæmis **Hvernig virka skil?**).
1. Í **Harmonikku atriði** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Textablokk** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði textabálkseiningar skal slá inn stuttan texta (til dæmis **Skil þurfa að fara fram í gegnum símaver. Hringja skal í 1-800-FABRIKAM fyrir skil. Vörur eru með 30 daga skilareglu. Hefja verður skil innan þess tímaramma.**).
1. Í hólfinu **Felling** skal bæta við nokkrum fellingareiningaratriðum í viðbót. Í hverju fellingareiningaratriði skal bæta við textabálkseiningu með innihaldi.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Síðan mun sýna fellingareiningu með innihaldinu sem var bætt við.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Hólfeining](add-container-module.md)

[Flipaeining](add-tab.md)

[Textabálkseining](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
