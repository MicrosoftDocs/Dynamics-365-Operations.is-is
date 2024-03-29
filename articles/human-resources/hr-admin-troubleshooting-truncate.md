---
title: Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio
description: Þessi grein útskýrir hvernig á að laga málið með stytt nöfn einstaklinga og stöður í stöðustigveldinu í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3663f5689fc0109caad01a285185f9f4ffa6fcca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865383"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Forðist stýfingu á texta í stöðustigveldi og útflutningi í Visio


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

Þegar viðskiptavinur skoðar stöðustigveldið í Microsoft Dynamics 365 Human Resources, eru nöfn á einstaklingum og stöðum stytt. Því getur reynst erfitt að taka skjámynd eða að prenta og dreifa stigveldinu.

![Stigveldi stöðu.](media/position-h.png)

**Orsök**

Þessi hegðun er samkvæmt hönnuninni.

**Lausn**

Því miður geta notendur ekki breytt stærð textans á auðveldan hátt. Hins vegar er hægt að flytja stöðustigveldið út úr Human Resources og flytja það síðan inn í Microsoft Visio. Þrátt fyrir að eftirfarandi grein hafi verið skrifuð fyrir Microsoft Dynamics AX 2012, gildir ferlið samt sem áður fyrir Human Resources: [Flytja út stöðustigveldi í Microsoft Visio](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Fylgið þessum skrefum til að flytja út í Visio.

1. Opnaðu í Human Resources **Stöður** listasíðu.

    Til að bæta frekar upplýsingum við skipurit fyrirtækis skal bæta reitum við listann **Stöður** svo þeir séu tiltækir þegar **Leiðsagnarforrit skipurits** er notað síðar í þessu ferli.

2. Í aðgerðasvæðinu skal velja hnappinn **Opna í Microsoft Office** og síðan, undir **Flytja út í Excel**, skal velja **Stöður**. Einnig er hægt að ýta á Ctrl+T.

    ![Flytjið út listasíðuna Stöður í Excel.](media/org-admin.png)

3. Vistið Excel-skrána sem er flutt út.

    ![Flytjið út í svarglugga Excel.](media/export-excel.png)

4. Í Visio skal velja **Visio - Búa til nýja** og síðan velja sniðmátsflokkinn **Viðskipti**.

    ![Ný skýringarmynd.](media/new.png)

5. Veljið **Leiðsagnarforrit fyrir myndrit fyrirtækis** og síðan **Búa til**.

    ![Svargluggi leiðsagnarforrits fyrir skipurit.](media/orgchart-wizard.png)

6. Veljið **Upplýsingar sem eru þegar vistaðar í skrá eða gagnagrunni** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 1.](media/orgchart-wizard7.png)

7. Veljið **Texta, „Org Plus“ (\*.txt) eða Excel-skrá** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 2.](media/orgchart-wizard3.png)

8. Flettið til að velja útfluttu Excel-skrána sem inniheldur stöðustigveldið og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 3.](media/orgchart-wizard2.png)

9. Stillið reitinn **Heiti** á **Staða**, stillið reitinn **Skýrslur til að** á **Skýrslur til að staðsetja** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 4.](media/orgchart-wizard1.png)

10. Veljið reitina sem á að sýna á hverjum hnút og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 5.](media/orgchart-wizard5.png)

11. Bætið dálknum **Staða** við listann **Móta gagnareiti** og veljið síðan **Næsta**.

    ![Leiðsagnarforrit skipurits 6.](media/orgchart-wizard6.png)

12. Myndir eru ekki í boði eins og er. Á næstu síðu skal því velja **Næsta**.
13. Veljið **Ég vil að leiðsagnarforritið raði myndriti fyrirtækisins sjálfkrafa niður á margar síður**.

    ![Leiðsagnarforrit skipurits 7.](media/orgchart-wizard4.png)

14. Veljið **Ljúka**.

    Ef einhverjar stöður eru ekki í skipulaginu verður notandi beðinn um að bæta þeim við skýringarmyndina.

Skýringarmyndin sem er búin til í Visio birtir hvern yfirmann á aðskildu vinnublaði.

Þegar Visio-skráin er búin til birtir hver hnútur viðeigandi upplýsingar sem byggjast á reitunum sem voru valdir til að hafa með á skýringarmyndinni.

![Skýringarmynd stigveldis.](media/hierarchy.png)

**Frekari valkostir**

Í Human Resources er hugsanlega líka hægt að nota vinnusvæðið **Fólk** til að skoða stigveldistengdar upplýsingar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
