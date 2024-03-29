---
title: Setja upp launanet
description: Launahnitanet eru notaðar til að skilgreina og viðhalda skipan launa fyrir launafyrirkomulög fastra launa.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691674"
---
# <a name="set-up-compensation-grids"></a>Setja upp launanet


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Launahnitanet eru notaðar til að skilgreina og viðhalda skipan launa fyrir launafyrirkomulög fastra launa. Hægt er að deila hnitanet launa milli margra áætlanir eða afrituð þegar ný launafyrirkomulag er stofnað.  Áður en launanet er stofnað, setja verður upp Stig og tilvísunarpunkta. Þessu dæmi mun búa til nýja Launaþrep gerð launanet með sýnigögn fyrir Stig- og Tilvísuninarpunkta. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Setja upp upplýsingar um hnitanet launa
1. Opnið **Mannauður** > **Laun** > **Föst laun** > **Launanet**.
2. Smellt er á **Nýtt**.
3. Í reitinn **hnitanet** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Tegund** skal velja valkost.
6. Færa inn eða velja gildi í svæðinu uppsetningu **Tilvísunar**.
7. Í reitinn **Gjaldmiðill** skal slá inn eða velja gildi.
8. Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.

## <a name="add-levels-to-the-compensation-structure"></a>Bæta við stigum í launaskipulag
1. Smellt er á **Launaskipulag**.
2. Í listanum skal merkja valda línu.
3. Sláðu inn eða veldu gildi í reitnum **stig**.
4. Smellt er á **Nýtt**.
5. Í listanum skal merkja valda línu.
6. Sláðu inn eða veldu gildi í reitnum **stig**.
7. Smellt er á **Nýtt**.
8. Í listanum skal merkja valda línu.
9. Sláðu inn eða veldu gildi í reitnum **stig**.
10. Smellt er á **Nýtt**.
11. Í listanum skal merkja valda línu.
12. Sláðu inn eða veldu gildi í reitnum **stig**.
13. Smellt er á **Nýtt**.
14. Í listanum skal merkja valda línu.
15. Sláðu inn eða veldu gildi í reitnum **stig**.

## <a name="fill-in-the-compensation-structure-with-values"></a>Fyllið inn í launaskipulag með gildum
1. Í listanum skal merkja valda línu.
    * Á þessum tímapunkti handvirkt er hægt að færa inn gildi launa í hverju svæði í töflu eða breyta Margar aðgerðir sem hægt er að nota auðveldlega mörg svæði eru fyllt út og framkvæma grunnútreikninga.  
2. Smellt er á **Fjöldabreyting**.
    * Fyrir þetta hnitanet notum við fyrst gildi miðpunkts á fyrsta stigi á öll svæði í töflunni. Þetta verður sem grunnur fyrir launafylki.  
3. Veljið valkost í svæðinu **gerð leiðréttingar**.
4. Í reitinn **Leiðréttingarupphæð** skal slá inn númer.
5. Merkið eða afmerkið allar línur í listanum.
6. Smellt er á **Nota á hnitanet**.
    * Nú munum við nota fjöldabreytingu til að stighækka upphæðir í hverri síðari stig með ákveðnum prósentu eða upphæð. Í þessu dæmi, hver launaþrep hafa er % 12,5 mun milli þeirra miðpunkta.  
7. Veljið valkost í svæðinu **gerð leiðréttingar**.
8. Í reitinn **Leiðréttingarupphæð** skal slá inn númer.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
10. Smellt er á **Nota á hnitanet**.
    * Nú munum við nota fjöldabreytingaraðgerð til að leiðrétta Lágmark og Hámark tilvísunarpunkta fyrir hvert stig. Þessu dæmi mun nota inn 50% mun svo tilvísunarpunktur Lágmark verður leiðrétt -20% og Hámark verður leiðrétta +20%.  
11. Í reitinn **Leiðréttingarupphæð** skal slá inn númer.
12. Færa inn eða veljið gildi í svæðinu **tilvísunarpunktur**.
13. Merkið eða afmerkið allar línur í listanum.
14. Smellt er á **Nota á hnitanet**.
15. Í reitinn **Leiðréttingarupphæð** skal slá inn númer.
16. Færa inn eða veljið gildi í svæðinu **tilvísunarpunktur**.
17. Merkið eða afmerkið allar línur í listanum.
18. Smellt er á **Nota á hnitanet**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
