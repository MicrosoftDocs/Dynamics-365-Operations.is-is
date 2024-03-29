---
title: Viðhaldslotur
description: Í þessari grein eru viðhaldslotur útskýrðar í Eignastýringu.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 519431d84652e45dcd45aefbbaaa2a0e2afe6349
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016508"
---
# <a name="maintenance-rounds"></a>Viðhaldslotur

[!include [banner](../../includes/banner.md)]

 

Í **Eignastjórnun** er hægt er að stofna viðhaldslotur fyrir ýmsar eignir, þar sem þú þarft að framkvæma svipað verk með reglulegu millibili. Til dæmis smurverk eða öryggisskoðunarstörf sem þarf að framkvæma á fjölda véla með sama millibili. Fyrsta skrefið er að búa til viðhaldslotu, einnig á eignum sem krefjast sams konar viðhaldsverka. Næst skipuleggur þú viðhaldsloturnar. Þegar þú hefur lokið áætlun um viðhaldsloturnar geturðu séð allar starfsskrárnar sem tengjast lotunni í **Allar viðhaldsáætlanir** og **Opnar viðhaldsáætlunarlínur**.

>[!NOTE]
>Einnig er hægt að setja upp viðhaldslotur á virkum staðsetningum til að ljúka við á eignunum sem voru settar upp á virkri staðsetningu þegar stofnað var til lotubyggðrar verkbeiðni. Sjá [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md) til að fá frekari upplýsingar um skipulag á viðhaldslotum á virkum stöðum.

## <a name="set-up-a-maintenance-round"></a>Setja upp viðhaldslotu

1. Smelltu á **Eignastjórnun** > **Uppsetning** > **Forvirkt viðhald** > **Viðhaldslotur**.

2. Smelltu á **Nýtt** til að stofna nýja viðhaldslotu.

3. Settu inn auðkenni í reitinn **Viðhaldslota** og heiti fyrir viðhaldsumferðina í reitinn **Heiti**.

4. Veldu upphafsdagsetningu fyrir lotu í reitnum **Upphafsdagur**.

5. Í reitunum **Ljúka innan daga** og **Ljúka innan klukkustunda** er hægt að setja inn áætlaða lokadagsetningu í dögum eða klukkustundum. Væntanlegur lokadagur er reiknaður miðað við upphafsdaginn, sem reiknaður er þegar línur viðhaldsskema eru búnar til. Til dæmis er hægt að setja „7“ í reitinn **Ljúka innan daga** til að gefa til kynna að skyldri vinnslu skuli vera lokið innan viku frá upphafsdegi.

6. Veldu „Já“ á skiptihnappinum **Stofna sjálfvirkt** ef verkbeiðnir skulu vera sjálfkrafa stofnaðar út frá viðhaldsskemalínum sem eru búnar til úr þessari viðhaldslotu.

7. Í reitnum **Gerð verkbeiðni** velurðu þá gerð verkbeiðni sem á að nota í verkbeiðnum sem búnar eru til úr þessari viðhaldslotu.

8. Í reitnum **Þjónustustig** velurðu það þjónustustig verkbeiðni sem á að nota í verkbeiðnum sem búnar eru til úr þessari viðhaldslotu.

9. Á flýtiflipanum **Eignalínur** smellirðu á **Bæta við** til að bæta við eign í viðhaldslotunni.

10. Línunúmer er sjálfkrafa fært inn í reitinn **Línunúmer** til að sýna röð eigna í viðhaldslotu.

11. Veljið eign í reitnum **Eign**.

12. Veldu gerð viðhaldsverka fyrir eignina í reitnum **Tegund viðhaldsverka**.

13. Veldu, ef þörf krefur **Afbrigði af gerð viðhaldsvinnslu** og **Viðskipti** sem tengjast tegund viðhaldsvinnslu.

14. Veldu endurtekningu (dag, viku osfrv.) í reitnum **Tímabilsgerð**.

15. Í reitinn **Tímabilstíðni** seturðu inn fjölda endurtekninga fyrir viðhaldslotuna. Dæmi: Ef þú hefur valið „Dag“ í reitnum **Tímabilsgerð** og þú setur inn töluna „7“ í þennan reit, eru nýjar viðhaldslotulínur stofnaðar við tímasetningu á forvirku viðhaldi einu sinni í viku.

16. Veldu upphafsdagsetningu eignarinnar sem á að vera með í viðhaldslotunni í reitnum **Upphafsdagsetning**. Þessi dagsetning getur verið frábrugðin upphafsdeginum sem sett er fram í viðhaldsumlotunni.

17. Endurtakið þrep 9-16 til 16 til að bæta fleiri eignum við viðhaldslotuna.

18. Á flýtiflipanum **Línur virkrar staðsetningar** smellirðu á **Bæta við** til að bæta við virkri staðsetningu í viðhaldslotunni. Vísaðu til lýsingar á tengdum reitum hér að ofan. Sömu reitir eru tiltækir og til að búa til eignalínu, en þú getur líka valið **Framleiðandi** og **Tegund** fyrir virka staðsetningu, ef þess er krafist. Ef þú velur aðeins virka staðsetningu á línu, en gerir ekkert val í **Gerð eignar**, **Framleiðandi**, **Tegund**, **Gerð viðhaldsverks**, **Afbrigði af viðhaldsverkum** og **Viðskipti** eru allar eignir sem tengjast þeirri virku staðsetningu á þeim tíma sem viðhaldsáætlun er tekin með í viðhaldslotunni.

19. Á flýtiflipanum **Söfn** smellirðu á **Bæta við** til að velja verkbeiðnisafn sem á að vera með í viðhaldslotunni. Hægt er að tengja nokkur verkbeiðnisöfn við eina viðhaldslotu.

20. Vistaðu uppsetninguna.

>[!NOTE]
>Reitirnir **Eignir** og **Línur** sem eru staðsettir í hópnum **Upplýsingar** á flýtiflipanum **Haus** sýnir heildarfjölda eigna og lína sem tengjast valinni viðhaldslotu.

Myndin hér að neðan sýnir og dæmi um viðhaldslotu sem inniheldur þrjár eignir.

![Mynd 1.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a>Tímasetja viðhaldslotur

Þegar þú hefur sett upp viðhaldslotu keyrirðu röðunarvinnslu til að tímasetja allar vinnslur sem tengjast viðhaldslotunni.

1. Smelltu á **Eignastýring** > **Reglubundið** > **Fyrirbyggjandi viðhald** > **Tímasetja viðhaldslotur** eða **Eignastýring** > **Viðhaldsáætlun** > **Allar viðhaldsáætlanir** eða **Opna áætlunarlínur viðhalds** eða **Opna viðhaldsáætlunarhópa** > velja viðhaldsáætlunarlínu úr listanum > **Viðhaldslotur** hnappurinn.

2. Í reitnum **Tímabil** skal velja tímabilsgerðina sem á að nota fyrir tímasetningarvinnsluna.

3. Í reitinn **Tímabilstíðni** skaltu setja inn fjölda tímabila sem eiga að vera með í tímasetningarvinnslunni. Upphaf tímasetningar er núverandi dagsetning.

4. Veldu „Já“ á skiptihnappnum **Stofna sjálfvirkt** ef verkbeiðni á að vera sjálfkrafa stofnuð á grundvelli viðhaldslotu.

>[!NOTE]
>Ef þessi rofahnappur er stilltur á „Já“ og rofahnappurinn **Stofna sjálfvirkt** er einnig stilltur á „Já“ í viðhaldslotunni í skjámyndinni **Viðhaldslotur** eru verkbeiðnir búnar til út frá viðhaldslotulínum og viðhaldsskemalínur með stöðuna „Verkbeiðni stofnuð“ eru einnig stofnaðar. Ef aðeins einn af rofahnöppunum **Stofna sjálfkrafa** eru stilltir á „Já“ í þessari fellivalmynd eða í **Viðhaldslotur** eru aðeins viðhaldsskemalínur stofnaðar með stöðuna „Stofnað“. Þá eru engar verkbeiðnir stofnaðar.

5. Ef þess er krafist geturðu valið sérstakar lotur eða annan upphafsdag fyrir röðunarvinnsluna. Smelltu á **Sía** og bættu við lotum sem á að vera með.

6. Smellt er á **OK**.

7. Nú geturðu séð verk viðhaldslotu í **Eignastýring** > **Viðhaldsáætlun** > **Allar viðhaldsáætlanir** eða **Opna áætlunarlínur viðhalds**. Ef tímasettar lotur eru tengdar við verkbeiðnisafn sérðu einnig viðhaldsskemalínur í **Opna viðhaldsskemasöfn**. Viðhaldsskemalínur sem eru stofnaðar úr lotum hafa tilvísunargerðina „Viðhaldslotur“.

Myndirnar tvær hér að neðan sýna tímaáætlun í glugganum **Tímasetja viðhaldslotur** og viðhaldsskemalínur búnar til í **Öll viðhaldsskemu** miðað við þá áætlunarvinnslu.

![Mynd 2.](media/14-preventive-maintenance.png)

![Mynd 3.](media/15-preventive-maintenance.png)

- Þegar verkbeiðnir eru búnar til handvirkt á eignum sem falla undir ábyrgð lánadrottins er sýndur gluggi til að gera notandanum grein fyrir ábyrgðinni. Þá er hægt að hætta við að búa til verkbeiðnina. Hætt er við athugun á ábyrgðartengslum vegna verkbeiðna sem eru búnar til sjálfkrafa.  
- Þú getur sett upp runuvinnslu á flýtiflipanum **Keyra í bakgrunni** til að skipuleggja lotur með reglulegu millibili.  
- Ef lota er innifalin í nokkrum verkbeiðnisöfnum (sjá [Verkbeiðnisöfn](../work-orders/work-order-pools.md)) er sýnd ein skrá fyrir hvert safn í **Opna viðhaldsskemasöfn**. Þetta er gert til að hámarka síunarvalkosti fyrir verkbeiðnisöfn.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]