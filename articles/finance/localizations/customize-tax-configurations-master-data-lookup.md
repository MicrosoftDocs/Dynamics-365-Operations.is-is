---
title: Sérstilla skattaskilgreiningar fyrir uppflettingu aðalgagna
description: Í þessu efnisatriði er útskýrt hvernig á að sérstilla skattaskilgreiningar til að auka virkni uppflettingar aðalgagna.
author: kai-cloud
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 69541316ad4c6c4bb404ea142844ce596b5502b9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689129"
---
# <a name="customize-tax-configurations-for-master-data-lookup"></a>Sérstilla skattaskilgreiningar fyrir uppflettingu aðalgagna

[!include [banner](../includes/banner.md)]

Fylgdu skrefunum í þessu efnisatriði til að sérstilla skattaskilgreiningar til að auka virkni uppflettingar aðalgagna.

## <a name="import-a-tax-configuration-provided-by-microsoft"></a>Flytja inn skattaskilgreiningu í boði Microsoft

1. Í Regulatory configuration service (RCS), á vinnusvæðinu **Rafræn skýrslugerð**, skal velja skilgreiningarveitu **Microsoft**.
2. Veldu **Geymslur**.
3. Veldu **Altækt** og síðan **Opna**.
4. Veldu skattaskilgreiningu á borð við **Skilgreining skattaútreiknings** og því næst á flipanum **Útgáfur** skal velja útgáfu.
5. Velja **Innflutningur**.

> [!NOTE]
> Líkanavörpunin Dataverse er sjálfgefið flutt inn. Ef upp koma viðvörunarboð meðan á innflutningsferli skilgreiningar stendur skal virkja sýndareiningarnar í Dataverse. Frekari upplýsingar er að finna í [Virkja Dataverse sýndareiningar](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).

## <a name="create-a-customized-data-model-configuration"></a>Stofna sérstillta skilgreiningu gagnalíkans

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skattaskilgreiningar** og því næst velja skilgreiningu gagnalíkansins sem á að stækka. Veldu til dæmis **Gagnalíkan skattaútreiknings**.
2. Veljið **Stofna skilgreiningu**.
3. Veldu **Líkan skattskylds skjals afleitt frá heitinu: Gagnalíkan skattaútreiknings, Microsoft**.
4. Í reitinn **Heiti** skal færa inn **Sérstilling gagnalíkans**.
5. Veljið **Stofna skilgreiningu**.

## <a name="create-customized-reference-models"></a>Búa til sérstillt tilvísunarlíkön

1. Á síðunni **Skattaskilgreiningar** skal velja **Sérstilling gagnalíkans** og velja síðan **Hönnuður**.
2. Veldu úrfellingarhnappinn (**...**) og veldu síðan yfirlitið **Tilvísunarlíkan**.

    [![Tilvísunarlíkan.](./media/pic2.png)](./media/pic2.png)

3. Búðu til sérstillta tilvísunarlíkanið. Sérstillta líkanið er rótarlíkan. Sérstillta einingin er færslulisti. Sérstillti reiturinn er strengjareitur sem þú vilt nota í uppflettingunni. Þú getur bætt við fleiri reitum eftir þörfum.
4. Veldu úrfellingarhnappinn (**...**) og veldu síðan yfirlitið **Skattskylt skjal**.
5. Veldu eigindina sem á að binda við sérstillta tilvísunarlíkanið. Veldu til dæmis **Sérstillt eigind** og fylgdu síðan þessum skrefum:

    1. Veldu **Velja tilvísunarlíkan**.
    2. Veldu **Sérstillt líkan** og veldu síðan **Í lagi**. Heiti tilvísunarlíkansins er uppfært í gildið í reitnum **Raunlykill**.

        [![Svarglugginn Velja tilvísunarlíkan.](./media/pic5.png)](./media/pic5.png)

    3. Veldu **Vista** og síðan **Ljúka**.

## <a name="create-a-customized-model-mapping-configuration"></a>Stofna sérstillta skilgreiningu líkanavörpunar

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skattaskilgreiningar** og því næst velja skilgreininguna **Dataverse líkanavörpun**.
2. Í reitnum **Sjálfgefið fyrir líkanavörpun** skal velja **Nei**.
3. Veljið **Stofna skilgreiningu**.
4. Veldu **Líkanavörpun skattskylds skjals afleitt frá heitinu: Dataverse Líkanavörpun, Microsoft**.
5. Í reitinn **Heiti** skal færa inn **Líkanavörpun sérstillingar**.
6. Í reitnum **Marklíkan** skal velja gagnalíkanið **Gagnalíkan sérstillingar**.
7. Veljið **Stofna skilgreiningu**.

    [![Fellilisti í svarglugga fyrir stofnun skilgreiningar.](./media/pic6.png)](./media/pic6.png)

8. Veldu **Líkanavörpun sérstillingar** og stilltu reitinn **Tengt forrit** á tenginguna sem var búin til í skrefi 8 í [Setja upp umhverfi fyrir uppflettingar aðalgagna](tax-service-set-up-environment-master-data-lookup.md).
9. Stilltu reitinn **Sjálfgefið fyrir líkanavörpun** á **Já**.

## <a name="create-customized-model-mappings"></a>Búa til sérstilltar líkanavarpanir

1. Á síðunni **Skattaskilgreiningar** skal velja **Líkanavörpun sérstillingar**.
2. Veldu **Hönnuður** og veldu svo **Líkan sérstillingar**.

    [![Líkan sérstillingar.](./media/pic8.png)](./media/pic8.png)

## <a name="map-a-model-mapping-to-a-dataverse-entity"></a>Varpa líkanavörpun í Dataverse einingu

1. Á síðunni **Hönnuður líkanavörpunar** skal velja **Líkan sérstillingar** og síðan velja **Hönnuður**.
2. Í trénu **Gerðir gagnagjafa** skal velja **Dataverse Tafla**.
3. Á flipanum **Gagnagjafar** skal velja **Bæta við rót**.
4. Í reitinn **Heiti** skal færa inn **Sérstillt Dataverse**.
5. Í seinni reitnum **Heiti** skal velja einingu.
6. Veldu **Í lagi**.

    [![Svargluggi fyrir eiginleika gagnagjafa.](./media/pic9.png)](./media/pic9.png)

7. Veldu **Sérstillt Dataverse** og **Sérstillt eining** og veldu síðan **Binda**.

    [![Sérsniðið Dataverse og sérsniðin einingabinding.](./media/pic10.png)](./media/pic10.png)

8. Undir **Sérstillt Dataverse** og **Sérstilltur reitur** skal velja reit og síðan velja **Binda**.

    [![Sérstillt Dataverse og sérstillt reitarbinding.](./media/pic11.png)](./media/pic11.png)

9. Veldu **Vista** og síðan **Ljúka**.

## <a name="create-a-customized-tax-configuration"></a>Búa til sérstillta skattaskilgreiningu

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skattaskilgreiningar** og því næst velja **Skilgreining skattaútreiknings**.
2. Veljið **Stofna skilgreiningu**.
3. Veldu **Skilgreining skattþjónustu afleidd af heitinu: Skilgreining skattaútreiknings, Microsoft**.
4. Í reitinn **Heiti** skal færa inn **Skilgreining sérstillingar**.
5. Veljið **Stofna skilgreiningu**.
6. Veldu **Skilgreining sérstillingar** og veldu síðan **Hönnuður**.
7. Í reitnum **Gagnalíkan** skal velja **Gagnalíkan sérstillingar**.
8. Í reitnum **Útgáfa gagnalíkans** skal velja samsvarandi útgáfu gagnalíkans.

    [![Hluti eiginleika.](./media/pic13.png)](./media/pic13.png)

9. Velja **Lokið**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
