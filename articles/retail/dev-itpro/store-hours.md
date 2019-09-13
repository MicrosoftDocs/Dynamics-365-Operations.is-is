---
title: Búa til og uppfæra afgreiðslutíma verslunar
description: Þetta efni lýsir því hvernig á að búa til og uppfæra verslunartíma í höfuðstöðvum verslunarinnar.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 1b55b91246b22951f4e1d148f59444423e1d8a3d
ms.sourcegitcommit: e54607a2c80bec4db05045825914f50947f6e31e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917513"
---
# <a name="create-and-update-store-hours"></a>Búa til og uppfæra afgreiðslutíma verslunar

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Yfirlit

Frá einum stað geta smásalar stofnað, viðhaldið og stjórnað verslunarstundum fyrir mismunandi verslanir á landsvæðum. Þá er hægt að sýna verslunartímann á afgreiðslukössum. Á þennan hátt geta gjaldkerar deilt verslunartímum með viðskiptavinum og veitt betri þjónustu þeim kaupendum sem hafa áhuga á birgðum í öðrum verslunum. Einnig er hægt að prenta út verslunartímann á kvittunum, ef viðskiptavinir vilja fara aftur í búðina seinna.

Hægt er að stilla marga verslunartíma á mismunandi rásum. Þessar rásir innihalda verslanir á staðnum, símaver, farsíma og netverslunarsíður.

Ef viðskiptavinur er með tínslupöntun fyrir aðra verslun getur gjaldkerinn valið dagsetningar þegar tínslan verður tiltæk í þeirri verslun. Uppfletting verslunarinnar mun veita tilvísun í dagsetningar og tíma verslana. Gjaldkeri getur valið dagsetningu og staðsetningu og getur einnig prentað afhendingarkvittun sem felur í sér opnunartíma verslunarinnar.

Þessi aðgerð er fáanleg í Microsoft Dynamics 365 for Retail útgáfum 8.1.2 og nýrri.

## <a name="configure-store-hours"></a>Skilgreina afgreiðslutíma

Fylgja skal þessum skrefum til að skilgreina afgreiðslutíma.

1. Opnið **Retail** \> **Uppsetning rásar** \> **Afgreiðslutímar**.
2. Veldu **Nýtt** til að búa til nýtt sniðmát afgreiðslutíma. Veldu sniðmátið í vinstri glugganum til að nota sniðmát sem fyrir er.
3. Í glugganum **Bæta við sviði** skaltu tilgreina tímabilið, afgreiðslutímann og alla frídaga sem þarf.

    - Ef afgreiðslutími breytist ekki skaltu velja **Lýkur aldrei** í reitnum **Lokadagsetning**.
    - Ef afgreiðslutíminn er fyrir tiltekinn mánuð, viku eða dag, stillirðu viðeigandi dagsetningar í reitunum **Upphafsdagur** og **Lokadagsetning**.

    > [!NOTE]
    > Þú getur búið til mörg sniðmát sem hafa skarandi upphafs- og lokadagsetningar. Þess vegna getur þú til dæmis skilgreint afgreiðslutíma fyrir verslanir á mismunandi tímabeltum.

    ![Bæta við sviðsglugga](../dev-itpro/media/Storehours1.png "Bæta við sviðsglugga")

4. Tengdu sniðmát afgreiðslutíma við verslanirnar þar sem það verður notað. Í glugganum **Velja fyrirtækjahnúta** velurðu verslanir, svæði og fyrirtæki sem sniðmátið ætti að vera tengt við.

    - Aðeins er hægt að tengja eitt sniðmát afgreiðslutíma við hverja verslun.
    - Notaðu örvahnappana til að velja verslanir, svæði eða fyrirtæki. Dagatalið verður aðgengilegt í verslunum eða verslunarhópum og það verður sýnilegt á sölustað til viðmiðunar.

    ![Glugginn Veljið fyrirtækjahnúta](../dev-itpro/media/Storehours2.png "Glugginn Veljið fyrirtækjahnúta")

5. Á síðunni **Dreifingaráætlun** keyrirðu vinnslurnar **1070** og **1090** til að gera verslunartímann aðgengilegan sölustað.

## <a name="add-store-hours-to-printed-receipts"></a>Bættu afgreiðslutímum við prentaðar kvittanir

Fylgdu þessum skrefum til að bæta afgreiðslutíma við prentuðu POS kvittanir.

1. Opnaðu hönnuð kvittunar.
2. Veldu **Fótur** í neðra vinstra horninu.
3. Dragðu einguna **Afgreiðslutími** úr vinstri glugganum að fætinum neðst á kvittunarsniðmátinu.
4. Þú getur breytt sjálfgefna merkimiðanum á eingunni **Afgreiðslutími** eftir þörfum.
5. Vistaðu kvittunina og lokaðu kvittunarhönnuðinum.
6. Á síðunni **Dreifingaráætlun** skaltu keyra vinnslurnar **1070** og **1090**.
7. Skráðu þig inn POS
8. Ljúktu við sölu og veldu að prenta kvittun.

Kvittanir á sölustað innihalda nú afgreiðslutímann. Ef einhverjir frídagar voru með í sniðmátinu eru þeir sýndir á kvittuninni.

![Kvittunardæmi](../dev-itpro/media/Storehours3.png "Kvittunardæmi")
