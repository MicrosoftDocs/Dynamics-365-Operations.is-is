---
title: Skilgreina verkstjórnun
description: Þessi grein lýsir því hvernig á að stilla verkefnastjórnunareiginleika í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.search.industry: ''
ms.openlocfilehash: cc2d75f52b183559de344982c8e4208000af786e
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746063"
---
# <a name="configure-task-management"></a>Skilgreina verkstjórnun

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að stilla verkefnastjórnunareiginleika í Microsoft Dynamics 365 Commerce.

Áður en Dynamics 365 Commerce stjórnendur og starfsmenn geta notað verkstjórnunaraðgerðir í verslun verður að stilla verkstjórnun. Stillingarþrepin fela í sér að veita stjórnendum og starfsmönnum leyfi, dreifa heimildum til viðskiptavina á sölustað (POS), setja upp POS tilkynningar og stilla reitina **Verk** á heimasíðu POS forrita.

## <a name="configure-permissions-for-store-managers"></a>Stilla heimildir fyrir verslunarstjóra

Sérhver starfskraftur í tiltekinni verslun getur skoðað öll verk sem þeim er úthlutað. Þeir geta einnig uppfært stöðu verka sem þeim er úthlutað. Aðilar eins og verslunarstjórar verða þó að hafa heimildir fyrir verkefnisstjórnun til að stjórna verkefnum sem eru úthlutað í verslunina og til að búa til eins tilgangs verkefni.

Fylgdu þessum skrefum til að stilla verkefnastjórnunarheimildir fyrir verslunarstjóra.

1. Farðu í **Retail og Commerce \> Starfsmenn \> Heimildaflokkar**.
1. Veldu sérstakan leyfishóp (til dæmis, **Stjórnandi**) og veldu síðan **Breyta**.
1. Á flýtiflipanum **Heimildir** stillirðu valkostinn **Leyfa verkefnastjórnun** á **Já**.
1. Á flýtiflipanum **Tilkynningar** bætirðu við aðgerðinni **Verkefnisstjórn** og slærð inn gildi í reitinn **Sýna röð**. Til dæmis, sláðu inn **2** ef aðgerðin **Uppfylling pöntunar** er þegar með gildi **Sýna röð** upp á **1**.
    
> [!NOTE]
> Ef aðili annar en stjórnandi verður að hafa heimildir fyrir verkefnisstjórnun í POS geturðu veitt einstaklingnum leyfi. Einnig er hægt að búa til nýjan leyfishóp fyrir utan stjórnendur og stilla valkostinn **Leyfa verkefnastjórnun** á **Já**.

Eftirfarandi skýringarmynd sýnir hvernig á að stilla verkefnastjórnunarheimildir fyrir verslunarstjóra.

![Stilling verkefnastjórnunarheimilda fyrir verslunarstjóra.](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Stilla heimildir fyrir starfsmenn

Starfsmenn verða að hafa heimildir til að búa til verkefnalista, stjórna úthlutunarviðmiðum og stilla endurtekningu hvaða verkefnalista sem er. Til að stilla þessar heimildir úthlutar þú starfsmönnum á hlutverkið **Stjórnandi smásöluverks**.

Til að skilgreina heimildir fyrir starfsmanns skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Starfsmenn \> Notendur**.
1. Velja starfsmann.
1. Á flýtiflipanum **Hlutverk notanda** velurðu **Úthluta hlutverkum**.
1. Í valmyndinni **Úthluta hlutverkum til notanda** velurðu hlutverkið **Stjórnandi smásöluverks** og velur síðan **Í lagi**.

## <a name="distribute-permissions-to-pos-clients"></a>Dreifðu heimildum til POS viðskiptavina

Áður en starfsmenn geta notað POS viðskiptavini verður að dreifa heimildum og samstilla við þá viðskiptavini.

Fylgdu þessum skrefum til að dreifa heimildum til POS viðskiptavina.

1. Farðu í **Retail og Commerce \> Upplýsingatækni í Retail og Commerce \> Dreifingaráætlun**.
1. Veldu dreifingaráætlunina **1060** (**Starfsfólk**) og veldu síðan **Keyra núna**.
1. Veldu dreifingaráætlunina **1070** (**Skilgreining rásar**) og veldu síðan **Keyra núna**.

## <a name="configure-pos-notifications-for-tasks"></a>Stilla POS tilkynningar fyrir verkefni

Verkefnisstjórnun verður að vera þannig stillt að tilkynningar séu tiltækar í POS forritinu.

Til að skilgreina POS-tilkynningar fyrir verk skal fylgja þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> POS-aðgerðir**.
1. Finndu aðgerðina **1400** (**Verkefnisstjórn**) og veldu gátreitinn **Virkja tilkynningar** fyrir hana.

Eftirfarandi mynd sýnir aðgerðina **Verkefnisstjórn** á síðunni **POS aðgerðir**.

![Aðgerð verkstjórnunar á aðgerðasíðu sölustaðar.](media/HQ-POS-Tasks-Notifications.png)

Frekari upplýsingar um hvernig á að stilla POS tilkynningar er að finna í [Sýna pöntunartilkynningar á sölustað (POS)](notifications-pos.md) grein.

> [!NOTE]
> Þegar þú vistar breytingarnar þínar munu eftirfarandi viðvörunarskilaboð birtast: **Aðgerðarfæribreyta verður ekki virkjuð í hnappahönnuður fyrir aðgerðakenni sem er jafnt eða minna en 4000. Ef þú ert að búa til sérsniðna aðgerð og vilt senda færibreytu frá hnappahönnuðunum skaltu nota aðgerðakenni sem er stærra en 4000.** Veldu **Loka** til að loka glugganum.


## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>Stilltu verkefnisreit á heimasíðu POS forrita

Áður en þú stillir reitinn **Verk** á heimasíðu POS forrits, sjá [Skjáútlit fyrir sölustað (POS)](pos-screen-layouts.md) til að fá upplýsingar um hvernig á að stilla og bæta við nýjum hnöppum við POS skjáútlit.

Til að stilla reitinn **Verk** á heimasíðu POS forrita fylgirðu þessum skrefum.

1. Farðu í **Retail og Commerce \> Uppsetningu rásar \> Uppsetning POS \> POS \> Skjáútlit**.
1. Veldu skjáskipulag, veldu skipulagstærð og veldu hnappanet.
1. Á flýtiflipanum **Hnappanet** velurðu **Hönnuður** til að breyta völdu hnappaneti.
1. Bættu við reitnum **Verk** á viðeigandi hluta heimasíðunnar.

Eftirfarandi mynd sýnir dæmi um reitinn **Verk** á heimasíðu POS.

![Verkreitur á heimasíðu sölustaðar.](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit verkstjórnunar](task-mgmt-overview.md)

[Búa til verkefnalista og bæta við verkum](task-mgmt-create-lists.md)

[Úthluta verkefnalistum til verslana eða starfsmanna](task-mgmt-assign-lists.md)

[Verkstjórnun á sölustað](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
