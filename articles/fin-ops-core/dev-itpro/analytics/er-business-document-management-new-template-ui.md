---
title: Microsoft Office-notendaviðmót í viðskiptaskjalastjórnun (inniheldur myndband)
description: Í þessu efnisatriði er útskýrt hvernig á að nota nýja notandaviðmótið í eiginleika viðskiptaskjalastjórnunar í ramma rafrænnar skýrslugerðar.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b0c481e73daf74803d3582e4089e76dcd383e8a4
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937557"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala

[!include [banner](../includes/banner.md)]

Business Document Management leyfir notendum að breyta sniðmátum viðskiptaskjala með Microsoft 365-þjónustu eða viðeigandi Microsoft Office skjáborðsforriti. Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum. Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

Nýja notendaviðmótið (UI) er skýrara og þægilegra í notkun. Svæðið **Viðskiptaskjal** sýnir aðeins sniðmát sem eru í boði fyrir núverandi þjónustuaðila. Í eldra notandaviðmóti sýndi flipinn **Sniðmát** öll sniðmátin sem voru í boði fyrir alla þjónustuaðila. Hann sýndi einnig öll sniðmát sem voru búin til og breytt af öllum notendum í sama hlutverkinu.

Með hnappinum **Nýtt skjal** er hægt að búa til og breyta sniðmáti í rafrænni skýrslugerð (ER) sniði sem annar veitandi veitir. Í dæminu í þessu efni er veitan Microsoft. Einnig er hægt að stofna sniðmát með því að hlaða upp eigin sniðmáti á Excel sniði.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

Myndbandið [Búa til nýtt viðskiptaskjal með stjórnun viðskiptaskjala](https://youtu.be/gAIYl-mM_pw) (sýnt hér að ofan) er að finna í [Finance and Operations spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er aðgengilegur í YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt

Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.

Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.

1. Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Allt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.
2. Veldu **Virkja núna** til að kveikja á völdum eiginleika.
3. Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.

## <a name="edit-templates-that-are-owned-by-other-providers"></a>Breyta sniðmátum sem eru í eigu annarra veitenda

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala.](./media/BDM_overview_new_template1.png)

2. Í flipanum **Velja** skal velja skjalið til að nota sem sniðmát og síðan velja **Stofna skjal**.

    ![Gluggi viðskiptaskjala.](./media/BDM_overview_new_template2.png)

3. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
4. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
5. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
6. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

    ![Stofngluggi skjalagerðar.](./media/BDM_overview_new_template3.png)

Hnappurinn **Nýtt skjal** er notaður til að búa til og breyta sniðmáti á ER-sniði sem annar veitandi veitir. Í þessu dæmi er veitan Microsoft. Þegar þú velur **Nýtt skjal** geturðu skoðað öll sniðmát sem eru í eigu núverandi og annarra veitenda. Eftir að þú velur sniðmátið verður það opnað fyrir breytingar. Síðan verður breytt sniðmátið geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a>Hlaða upp sniðmáti sem notar fyrirliggjandi Excel-snið
Fylgið þessum skrefum til að veita nauðsynlegar upplýsingar áður en sniðmáti er hlaðið upp.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala.](./media/BDM_overview_new_template1.png)
    
2. Á síðunni **Búa til nýtt sniðmát**, í flipanum **Hlaða upp**, í flipanum **Sniðmát**, skal velja **Fletta** til að finna og velja Excel-skrána sem á að nota sem sniðmát. Í hlutanum **Sniðmát** er sjálfkrafa fyllt inn í reitina **Titill** og **Lýsing**. Þeir tilgreina heiti og lýsingu á nýrri skilgreiningu rafræns skýrslugerðarsniðs sem er sjálfkrafa búið til. Hægt er að breyta þessum reitum eftir þörfum.
3. Í hlutanum **Skjalagerð**, í reitnum **Heiti**, skal tilgreina gerð viðskiptaskjalsins. Þetta gildi verður notað til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans).

    ![Sniðmátsflipi.](./media/BDM_overview_new_UI_import_21.jpg)

4. Í flipanum **Gagnaveita**, í flýtiflipanum **Sía**, skal velja **Nota síu**. Í hlutanum **Gagnaveita**, er fyllt inn sjálfkrafa í reitinn **Heiti** eða hægt er að velja gildi handvirkt. Hægt er að nota síuna til að leita að viðeigandi heiti gagnaveitu eftir heiti, lýsingu, lands-/svæðiskóða og gerð viðskiptaskjals.

    ![Gagnagjafaflipi.](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > Flýtiflipinn **Sía** er notuð til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans). Hægt er að breyta öllum síureitum til að finna hentugustu gagnaveituna fyrir skjalið sem hlaðið er upp.
    > 
    > Skilyrðin í flýtiflipanum **Sía** eru notuð sem **EÐA** skilyrði.
    
5. Í flipanum **Vörpun** skal velja **Greina sjálfvirkt**. Reiturinn **Skilgreining rótar** er sjálfkrafa fylltur út eða hægt er að velja gildi handvirkt. Þessi flipi sýnir endavörpun eininganna úr sniðmátinu og líkaninu.

    ![Vörpunarflipi.](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > Vörpunin í hlutanum **Skipulag sniðmáts** notar fulla samsvörun á merkjum eða lýsingum í gagnaveitunni á tungumáli notanda og í heiti hólfs í sniðmátinu.

6. Veljið **Stofna skjal** til að staðfesta að ætlunin sé að stofna sniðmát og hefja breytingarferlið.

Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

Ef ekki er til nein veita í rafrænni skýrslugerð er hægt að búa hana til. Ef engin virk veita er til staðar er hægt að velja að virkja eina slíka.

- Til að búa til veitu skal breyta heiti veitunnar í reitnum **Heiti**, uppfæra veffang nýju veitunnar í reitnum **Veffang** og velja **Í lagi** til að staðfesta.

    ![Stofna nýja veitu í BDM.](./media/bdm_create_provider.png)
    
- Til að virkja núverandi veitu skal velja heiti veitunnar í reitnum **Skilgreiningarveita** og velja **Í lagi** til að stilla veituna sem virka.

    ![Virkja veitu í BDM.](./media/bdm_choose_provider.png)

> [!NOTE]
> Hvert BDM-sniðmát vísar í veituna sem höfund skilgreiningarinnar. Þess vegna þarf að hafa virka veitu fyrir sniðmátið.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
