---
title: Myndalistaeining
description: Þessi grein fjallar um myndlistaeiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.8
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: e89624a98d3cbdd861391e994386ae57d2c38aa0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269836"
---
# <a name="image-list-module"></a>Myndalistaeining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um myndlistaeiningar og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Myndlistareininguna er hægt að nota til að bæta safni mynda við vefsíður með einföldum hætti. Hægt er að skilgreina hverja mynd í röðinni með texta og tengja vefslóðir. Myndlistaeiningin er best til þess fallin að birta vörumerki eða lista sem inniheldur lógó.

> [!IMPORTANT]
> - Myndlistaeiningin er tiltæk í einingasafni Commerce frá og með Dynamics 365 Commerce útgáfu 10.0.20.
> - Myndalistaeiningin er sýnd í þema Adventure Works.

Eftirfarandi mynd sýnir dæmi þar sem myndlistaeining birtir lista með texta sem inniheldur lógó á B2C-vefsvæði Adventure Works.

![Dæmi um myndlistaeiningu sem birtir lista af texta sem inniheldur lógó](./media/Image_list.PNG)

Eftirfarandi mynd sýnir dæmi þar sem myndlistaeining birtir lista með lógóum á B2B-vefsvæði Adventure Works.

![Dæmi um myndlistaeiningu sem sýnir vörumerki](./media/Image_list_B2B.PNG)

## <a name="image-list-module-properties"></a>Eiginleikar myndlistaeiningar

| Nafn eiginleika | Gildi | lýsing |
|---------------|--------|-------------|
| Haus       | Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**) | Textafyrirsögn fyrir myndlistaeininguna. |
| Myndalisti    | Myndir, texti og vefslóðir | Hvert atriði í röðinni er mynd með texta og vefslóð. |

## <a name="add-an-image-list-module-to-a-new-page"></a>Bæta myndlistaeiningu við nýja síðu

Til að bæta myndlistaeiningu við nýja síðu og stilla nauðsynlega eiginleika í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og opnaðu markaðssetningarsniðmátið fyrir heimasíðu vefsvæðisins (eða búðu til nýtt sniðmát markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Myndlisti** mát og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og opnaðu heimasíðu vefsvæðisins (eða búðu til nýja heimasíðu með sniðmáti markaðssetningar).
1. Í **Aðal** rauf sjálfgefna síðunnar, veldu sporbaughnappinn (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Myndlisti**, og veldu síðan **Allt í lagi**.
1. Í eiginleikaglugganum fyrir myndlistaeininguna skal bæta við fyrirsögn (til dæmis **Vörumerkið okkar**).
1. Bættu við atriði myndalista og tilgreindu mynd, einhvern texta og framsenda vefslóð.
1. Bættu við og skilgreindu fleiri einingar fyrir atriði myndalista eftir þörfum.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Þema Adventure Works](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
