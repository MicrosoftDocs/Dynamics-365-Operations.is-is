---
title: Niðurtímaaðgerðir vegna viðhalds
description: Þetta efnisatriði útskýrir hvernig niðurtími viðhalds er notaður til að fá yfirlit yfir afkastagetu sem er nauðsynleg til að framkvæma viðhaldsverk á tilteknum eignum á tilteknu tímabili.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 986b2ae4cf7f7819caaf35e009fd4735f35e6928
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017955"
---
# <a name="maintenance-downtime-activities"></a>Niðurtímaaðgerðir vegna viðhalds

[!include [banner](../../includes/banner.md)]

Niðurtími vegna viðhalds er notaður til að fá yfirsýn yfir álag sem þarf til að sinna viðhaldsverkum á tilteknum eignum á tilteknu tímabili. Til dæmis er hægt að búa til skráningu á niðurtíma vegna viðhalds fyrir framleiðslulínu 10 í framleiðslusal 29-A á framleiðslusvæði 02. Viðhaldstími skráningar hefur upphafs- og lokatíma sem gefur til kynna tímabilið þegar eignir sem tengjast viðhaldsstöðvun eru ekki tiltækar til framleiðslu.

**Aðgerðir niðurtíma vegna viðhalds** er yfirlit yfir viðhaldsskemalínur og viðhaldsverk verkbeiðnar á tengdum eignum á tilteknu tímabili. Línurnar sem tengjast viðhaldsverkum verkbeiðni hafa allar áætlaðan upphafsdag innan viðhaldsstöðvunartímabilsins. Þú getur dregið út gagnlegar upplýsingar og gert breytingar á fyrirhuguðum viðhaldsverkum:

- Fáðu yfirlit yfir nauðsynleg lokunartímabil framleiðslutækja (eignir).  
- Fáðu yfirlit yfir fyrirhugað viðhald (klukkustundir), flokkað eftir hæfni (ábyrgir hópar viðhaldsstarfsmanna eða viðhaldsstarfsmenn), til dæmis álag rafvirkja, smiða eða annarra viðhaldshópa sem þarf til að sinna áætluðum viðhaldssverkum.  
- Gerðu leiðréttingar á viðhaldsskemalínum eða viðhaldsverkum í verkbeiðnum sem tengjast eignunum, til dæmis, breyttu upphafs- og lokatíma á línu eða veldu aðra viðhaldsstarfsmenn til að hámarka verkflæðið fyrir viðhaldsstarfsmenn og hópa viðhaldsstarfsmanna.

Þegar eignir hafa verið valdar í skráningu á niðurtíma vegna viðhalds eru allar opnar viðhaldsskemalínur og viðhaldsverk verkbeiðna sem tengjast virkum verkbeiðnum innifalin í skráningu niðurtíma vegna viðhalds.

## <a name="maintenance-downtime-activities"></a>Niðurtímaaðgerðir vegna viðhalds

Smelltu á **Eignastýring** > **Sameiginlegt** > **Aðgerðir niðurtíma vegna viðhalds** > **Allar aðgerðir niðurtíma vegna viðhalds** til að opna lista yfir allar aðgerðir niðurtíma vegna viðhalds og sjá nokkrar þeirra upplýsinga sem tengjast aðgerðunum. Smelltu á tengil í dálkinum **Aðgerðir niðurtíma vegna viðhalds** til að opna smáatriðið. Myndin hér að neðan sýnir dæmi um listann **Niðurtímaaðgerðir vegna viðhalds**.

![Mynd 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Stofna aðgerð niðurtíma vegna viðhalds

1. Smelltu á **Eignastýring** > **Sameiginlegt** > **Aðgerðir niðurtíma vegna viðhalds** > **Allar aðgerðir vegna viðhaldstíma** eða **Virkar aðgerðir niðurtíma vegna viðhalds**.

2. Smellt er á **Nýtt**.

3. Settu inn auðkenni í reitinn **Aðgerðir niðurtíma vegna viðhalds** og heiti í reitinn **Heiti**.

4. Settu tímabil viðhaldsstoppsins í reitina **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími**.

5. Á flýtiflipann **Eignir aðgerða niðurtíma vegna viðhalds** > smellirðu á **Bæta við línu** til að bæta eignum, einni í einu, við aðgerðir niðurtíma vegna viðhalds.

6. Smelltu á **Vista** þegar öllum eignum hefur verið bætt við. Myndin hér að neðan sýnir dæmi um viðbragðstíma viðhalds með tengdum eignum og viðhaldsstörfum.

7. Viðhaldsverk verkbeiðni og opnar viðhaldsskemalínur sem tengjast völdum eignum eru sýndar á flýtiflipunum **Afleidd viðhaldsverk verkbeiðna** og **Viðhaldsskemalínur**. Á flýtiflipanum **Almennt** > hópnum **Verkbeiðni** > reitnum **Spáðir viðhaldstímar** og flýtiflipanum **Almennt** > hópnum **Viðhaldsskema** > reitnum **Spáðir viðhaldstímar** sérðu heildarfjölda klukkustunda sem spáð er um viðhaldsverk verkbeiðna og viðhaldsskemalínur.

Myndin hér að neðan sýnir dæmi um ítarupplýsingarnar **Niðurtímaaðgerðir vegna viðhalds**.

![Mynd 2](media/20-preventive-maintenance.png)

>[!NOTE]
>Viðhaldsverk verkbeiðna og viðhaldsskemalínur sem tengjast völdum eignum eru sjálfkrafa uppfærðar ef nýjar verkbeiðnar eða viðhaldsskemalínur eru búnar til eftir að þú stofnaðir niðurtíma vegna viðhalds. Til dæmis, ef þú skipuleggur viðhaldsáætlanir eða viðhaldslotur á tengdum eignum tveimur dögum eftir að aðgerð niðurtíma vegna viðhalds var stofnuð, er nýjum viðhaldsskemalínum bætt sjálfkrafa við aðgerðir niðurtíma vegna viðhalds.

8. Í **Öllum aðgerðum niðurtíma vegna viðhalds** > **Aðgerðir niðurtíma vegna viðhalds** > velurðu aðgerðir niðurtíma vegna viðhalds á listanum og smellir á **Álag** til að opna gluggann **Reikna álag**. Notaðu þennan glugga til að fá yfirsýn yfir álag á t.d. dagsetningar, eignir, eignategundir og gerðir viðhaldsverka. Athugaðu að dagsetningarnar sem sýndar eru í glugganum eru upphafs- og lokadagsetningar sem valdar voru í **Aðgerðir niðurtíma vegna viðhalds**. Þessi útreikningur felur í sér eignir sem tengjast aðgerðum niðurtíma vegna viðhalds.

9. Í glugganum **Reikna álag** skal breyta upphafs- og lokatíma ef þess er krafist og velja hvort þú viljir taka verkbeiðnir og viðhaldsskemu með í útreikninginn. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegur þú vilt að útreikningur á álagi sé varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar eignir fyrir virka staðsetningu, sem eru valdar í aðgerðum niðurtíma vegna viðhalds, sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar álagslínur á öllum virkum staðsetningarstigum sem þær tengjast.

10. Smellið á **Í lagi** til að byrja að reikna. Heildarfjöldi klukkustunda er sýndur í yfirlitinu **Álag**. Á flipanum **Álag** > **Flokka eftir...** aðgerðasvæðisflokkar, smellið á viðeigandi hnappa til að fá ítarlegra yfirlit yfir úthlutun áætlaðra vinnustunda. Myndin hér að neðan sýnir niðurstöður útreiknings á **Getuálagi**.

![Mynd 3](media/21-preventive-maintenance.png)

11. Þegar þú hefur fengið yfirlit yfir álag, ef þú vilt gera leiðréttingar á viðhaldsvinnslum verkbeiðni eða viðhaldsáætlunarlínum skaltu fara aftur í **Niðurtímaaðgerðir vegna viðhalds** og velja línurnar sem á að leiðrétta á **Verkbeiðnir viðhaldsvinnsla sem verða til** og **Áætlunarlínur viðhalds** flýtiflipanna.

12. Smelltu á hnappinn **Stilla** og uppfærðu áætlaðar upphafs-/lokadagsetningar, þjónustustig eða ábyrga viðhaldsstarfsmenn fyrir valin viðhaldsverk verkbeiðni eða viðhaldsskemalínur.

13. Smelltu á **Í lagi** þegar þú hefur gert nauðsynlegar leiðréttingar. 

>[!NOTE]
>Viðhaldsverk verkbeiðna og viðhaldsskemalínur sem ekki eru innifaldar í tímabili niðurtíma vegna viðhalds eftir að þú hefur gert leiðréttingar eru sjálfkrafa fjarlægðar úr **Aðgerðum niðurtíma vegna viðhalds**.

14. Í **Öllum aðgerðum niðurtíma vegna viðhalds** > **Aðgerðir niðurtíma vegna viðhalds** > velurðu aðgerðir niðurtíma vegna viðhalds á listanum og smellir á **Vöruspá** til að opna gluggann **Reikna vöruspá**. Notaðu þennan glugga til að reikna út spár fyrir vörur (varahluti og aðra nauðsynlega hluti) og flokka þær til að fá yfirsýn, til dæmis eftir dagsetningu, eign, gerð eigna og gerð viðhaldsverks. Athugaðu að dagsetningarnar sem sýndar eru í glugganum eru upphafs- og lokadagsetningar sem valdar voru í **Aðgerðir niðurtíma vegna viðhalds**. Þessi útreikningur felur í sér varahluti og vörur sem tengjast eignunum sem valdar eru í aðgerðum niðurtíma vegna viðhalds.

15. Í glugganum **Reikna vöruspá** skal breyta upphafs- og lokatíma ef þess er krafist og velja hvort þú viljir taka verkbeiðnir og viðhaldsskemu með í útreikninginn. Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegur þú vilt að útreikningur á álagi sé varðandi virkar staðsetningar. Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar eignir fyrir virka staðsetningu, sem eru valdar í aðgerðum niðurtíma vegna viðhalds, sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi. Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar álagslínur á öllum virkum staðsetningarstigum sem þær tengjast.

16. Smellið á **Í lagi** til að byrja að reikna. Heildarfjöldi vöruspáa er sýndur í yfirlitinu **Vöruspá**. Á flipanum **Vöruspá** > **Flokka eftir...** aðgerðasvæðisflokkar, smellið á viðeigandi hnappa til að fá ítarlegra yfirlit yfir úthlutun áætlaðra vara. Skýringarmyndin hér fyrir neðan sýnir niðurstöður útreikninga úr **Vöruspá**.

![Mynd 4](media/22-preventive-maintenance.png)

- Þú getur afritað eignir frá einni aðgerð niðurtíma vegna viðhalds til annarrar. Í **Öllum aðgerðum niðurtíma vegna viðhalds** velurðu hnappinn **Afrita aðgerðir niðurtíma vegna viðhalds** og gerir val þitt í reitunum **Frá aðgerðum niðurtíma vegna viðhalds** og **Til aðgerða niðurtíma vegna viðhalds** og smelltu á **Í lagi**.
- Í **Öllum aðgerðum niðurtíma vegna viðhalds** skaltu smella á hnappinn **Viðhaldsskemalínur** eða hnappinn **Virkar verkbeiðnir** til að opna tengda lista og skoða línurnar sem tengjast völdum aðgerðum niðurtíma vegna viðhalds.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]