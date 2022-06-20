---
title: Stækkunarhæfniáhrif Commerce-vörulista fyrir B2B-sérstillingar
description: Þessi grein lýsir stækkanleikaáhrifum viðskiptaskránna fyrir B2B eiginleika í Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 04/28/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: f21d3375db69dd412325d00261bfc18e26d0c257
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849016"
---
# <a name="extensibility-impact-of-commerce-catalogs-for-b2b-customizations"></a>Stækkunarhæfniáhrif Commerce-vörulista fyrir B2B-sérstillingar

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir teygjanleikaáhrifum **Viðskiptabækur fyrir B2B** lögun í Microsoft Dynamics 365 Commerce.

Ef þú hefur áhuga á að útvíkka vörulistasamhengið í sérsniðnar aðstæður, gæti þurft að uppfæra sérstillingarnar þínar. Þessi uppfærsla fylgir stöðluðu ferli sem viðskiptavinir verða að fylgja, vegna þess að aðlögun þeirra styður kannski ekki sjálfkrafa nýjustu eiginleikana eftir að uppfærslur eru gerðar. Ef sérstillingarnar þínar innihalda nýja eiginleika eða villuleiðréttingar í upplifun þeirra, mælum við með að þú uppfærir sérstillingarkóðann í samræmi við það. Þessi uppfærsla líkist þeim breytingum sem Microsoft gæti hafa gert fyrir kjarnakóðann.

Skoðaðu sérsniðin tilvik sem fylgja til að ákvarða hvort uppfæra þarf sérsniðin þín.

> [!NOTE]
> - Öll forritunarviðmót söluforrita (API) ættu að vera meðvituð um vörulista. Þess vegna er mikilvægt að þú standist **CatalogID** breytu.
> - Sjálfgefin vörulisti (**CatalogID**=**0**) er ekki gildur vörulisti fyrir innskráða notendur fyrirtækja til fyrirtækja (B2B). Þess vegna mistakast öll API símtöl sem standast „0“ eða nota sjálfgefið gildi, vegna þess að notendur vefsvæðisins hafa ekki aðgang að vörulista 0. Til að fá rétta upplifun verður að uppfæra API símtöl viðskiptavina þannig að þau standist vörulistaauðkennið sem var valið í vörulistavalinu. Ef þú notar sjálfgefið gildi og notandinn skiptir um vörulista ætti vefsíðan að veita gögnin fyrir valinn vörulista. Þess vegna, til að passa við API sem eru keyrð úr kjarna viðskiptakóða, ættu sérsniðin API að standast valinn vörulista.

Eftirfarandi aðlögunartilvik krefjast þróunaruppfærslu:

- **Tilfelli 1:** Viðskiptavinur kynnir sitt eigið [gagnaaðgerð](e-commerce-extensibility/data-actions.md) sem kallar á vörutengda API eða gagnaaðgerð. Eftirfarandi uppfærsluskref eru nauðsynleg:

    1. Ef gagnaaðgerðin notar beint API símtal, uppfærðu gagnaaðgerðina þannig að hún standist vörulistaauðkenni, eins og sýnt er í eftirfarandi dæmi.

        ![Uppfærð gagnaaðgerð sem fer framhjá vörulistaauðkenni.](./media/customization1_a.png)

    1. Ef gagnaaðgerðin kallar á aðra vörutengda gagnaaðgerð inni í sérstillingunni verður að uppfæra kóðann þannig að hann standist nokkrar nýjar færibreytur, eins og **beiðniSamhengi**. The **beiðniSamhengi** færibreytan er notuð til að sækja núverandi auðkenni vörulista, eins og sýnt er á eftirfarandi sýnishorni.

        ![Uppfærð gagnaaðgerð sem sendir nýju færibreytuna.](./media/customization1_b.png)

- **Tilfelli 2:** Viðskiptavinur er með [hnekkt gagnaaðgerð](e-commerce-extensibility/data-action-overrides.md). Eftirfarandi uppfærsluskref er krafist:

    - Uppfærðu gagnaaðgerðina eins og fyrir tilvik 1.

- **Tilfelli 3:** Viðskiptavinur er með skoðunarviðbót, forskriftasprautueiningu eða [einræktuð eining](e-commerce-extensibility/modules-overview.md#clone-a-module-library-module) sem felur í sér kalla á API eða gagnaaðgerðir. Eftirfarandi uppfærsluskref er krafist:

    - Uppfærðu kóðann eins og fyrir tilvik 1, eins og sýnt er á eftirfarandi dæmi.

       ![Uppfærður kóði sem sendir nýju færibreytuna.](./media/customization3.png)

- **Tilfelli 4:** Viðskiptavinur notar a **getById** API símtal. Eftirfarandi uppfærsluskref er krafist:

    - Skiptu yfir í **getByIds** API kalla í staðinn, vegna þess að **getById** APT símtal hefur nokkrar takmarkanir og styður ekki vörulistavitund.

- **Tilfelli 5:** Viðskiptavinur hefur gagnaaðgerð sem sækir upplýsingar fyrir margar vörur sem gætu verið úr mismunandi vörulistum. Eftirfarandi uppfærsluskref er krafist:

    - Skiptu API símtölunum eftir vörulistaauðkenni. Til dæmis, fyrir API fyrir körfu, gæti körfan innihaldið vörur úr mismunandi vörulistum. Vörulínurnar ættu að vera flokkaðar eftir vörulistaauðkenni og þær ættu að kalla á API fyrir hvern vörulista fyrir sig, eins og sýnt er í eftirfarandi sýnishorni.

        ![Uppfærð gagnaaðgerð sem flokkar vörulínur eftir vörulistaauðkenni.](./media/customization5.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna Commerce-vörulista fyrir B2B-svæði](catalogs-b2b-sites.md)

[Algengar spurningar um Commerce-vörulista fyrir B2B](catalogs-b2b-sites-FAQ.md)
