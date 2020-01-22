---
title: Vinna með einingar
description: Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914795"
---
# <a name="work-with-modules"></a>Vinna með einingar

Þetta efni lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Yfirlit

Einingar eru rökréttir byggingarreitir sem mynda síðuuppbyggingu þína og þau hafa ýmsan tilgang og gildissvið. Sumir einingar eru hástigs gámar og eini tilgangur þeirra er að halda og skipuleggja aðrar einingar (undireiningar). Aðrar einingar, svo sem einföld myndstaðsetningareining, hafa mjög sérstakan tilgang. Aðrar einingar, svo sem hringekjueining, falla einhvers staðar á milli þessara tveggja flokka.

Sjálfgefið er svæði þitt í Dynamics 365 Commerce inniheldur byrjunarbúnaðareiningasafn sem gerir þér kleift að ná flestum grundvallaratriðum fyrir rafræn viðskipti. Þú ættir að geta smíðað vefsvæði frá einni verslun til annarrar með því að nota þessar einingar. Hins vegar gætirðu líka viljað aðlaga þessa einingar eða smíða nýjar sérsniðnar einingar fyrir sérstakar þarfir. Ef þú vilt smíða sérsniðnar einingar er hugbúnaðarþróunarbúnaður (SDK) í boði til að hjálpa þér að búa til sérsniðið einingasafn.

## <a name="container-modules-and-slots"></a>Gámaeiningar og -hólf

Eins og áður var getið eru sumar einingar hannaðar til að innihalda undireiningar. Þessar einingar eru þekktar sem *gámar* og þær gera ráð fyrir stigveldum ívafinna eininga. Gámaeiningar innihalda *hólf*. Hólf eru notuð til að takast á við skipulag og tilgang undireininga í gámnum. Dæmi um það er grunnsíðugámaeining (efsta stigs eining fyrir hverja síðu) sem skilgreinir nokkur mikilvæg hólf:

- Fyrirsagnarhólf
- Meginmálshólf
- Síðufótarhólf

Þróunaraðili einingarinnar skilgreinir þessi hólf og ákvarðar hvaða undireiningar og hversu margar undireiningar má setja beint í þau. Til dæmis gæti fyrirsagnarhólfið aðeins stutt eina einingu af gerðinni **Fyrirsagnareining** en meginmálshólfið gæti stutt ótakmarkaðan fjölda eininga af hvaða gerð sem er (nema aðrar gámaeiningar á síðunni).

Í höfundatækjunum þurfa síðuhöfundar ekki að vita fyrirfram hvaða einingar er hægt og ekki hægt að setja í hvert hólf. Þegar síðuhöfundar velja hólf og reyna síðan að velja einingu til að bæta við það sjá þeir síaða mynd af gerðum eininga sem eru studdar fyrir það hólf.

## <a name="content-modules"></a>Innihaldseiningar

Innihaldseiningar innihalda efni og fjölmiðlaþætti, svo sem texta (til dæmis fyrirsagnir, málsgreinar og krækjur) eða tilvísanir í eignir (til dæmis myndir, myndskeið og PDF skjöl). Dæmi um dæmigerðar gerðir innihaldseininga eru **Hetja**, **Eiginleiki** og **Borði**. Einingar af þessum þremur gerðum geta innihaldið texta eða miðla og þeir þurfa ekki neinar undireiningar til að gera eitthvað sýnilegt á síðu.

Meirihluti dæmigerðra, daglegra síðu- og efnisskriftaaðgerða fela í sér efniseiningar, fyrst og fremst vegna þess að þessar einingar skilgreina raunverulegt innihald sem birt er í yfirgámaeiningum þeirra. Margar efniseiningar eru í boði og þessar einingar eru venjulega síðustu verkin sem þú bætir við stigveldi síðunnar með ívöfðum einingum.

Eftirfarandi mynd sýnir hvernig einingar eru ívafðar innan í einingahólfum yfirgáms.

![Ívafðar einingar](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Bæta við eða fjarlægja einingar

Eftirfarandi aðferðir lýsa því hvernig á að bæta við og fjarlægja einingar.

### <a name="add-a-module"></a>Bæta við einingu

Til að bæta einingu við hólf eða gám á síðu skaltu fylgja þessum skrefum.

1. Veldu útlínugluggann til vinstri til að velja gám eða hólf sem hægt er að bæta undireiningunni við.

    > [!NOTE]
    > Einingahönnuðurinn skilgreinir listann yfir gerðir eininga sem hægt er að bæta við tiltekið hólf fyrir eininguna. Höfundar sniðmáts geta síðan fínstillt leyfða einingavalkosti til að tryggja stöðuga leitarvélabestun (SEO) og höfundarvirkni fyrir allar síðurnar sem eru smíðaðar úr ákveðnu sniðmáti.

1. Veldu úrfellingarhnappinn (**...**) fyrir eininguna og veldu síðan **Bæta við einingu**. Valmyndin **Bæta við einingu** birtist. Þessi gluggi er sjálfvirkt síaður þannig að hann sýnir aðeins einingar sem eru studdar í völdum gámi eða hólfi. Listinn yfir einingar ræðst af sniðmáti síðunnar eða skilgreiningu gámaeiningar.

    > [!NOTE]
    > Ef gámur eða hólf styður ekki nýjar undireiningar er valkosturinn **Bæta við einingu** er ekki í boði.

1. Leitaðu að og veldu einingu til að bæta við síðuna í valmyndinni.

    > [!TIP]
    > **Eiginleiki** og **Hetja** eru góðar einingagerðir fyrir byrjendur að vinna með.

1. Veldu **Í lagi** til að bæta valinni einingu við valinn gám eða hólf á síðunni þinni.

### <a name="remove-a-module"></a>Fjarlægja einingu

Til að fjarlægja einingu úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.

1. Veldu útlínuhnappinn við hliðina á nafni einingarinnar sem á að fjarlægja í yfirlitsrúðunni til vinstri og veldu síðan ruslatunnuhnappinn.
1. Þegar þú færð kvaðningu um að staðfesta að þú viljir fjarlægja eininguna skaltu velja **Í lagi**.

## <a name="configure-modules"></a>Skilgreina einingar

Eftirfarandi aðferðir lýsa því hvernig á að skilgreina efnis- og gámaeiningar.

### <a name="configure-a-content-module"></a>Stilla innihaldseiningu

Fylgdu þessum skrefum til að stilla efniseiningu á síðu.

1. Veldu útlínugluggann til vinstri, veldu gerð eininga fyrir efni (til dæmis, **Eiginleiki**, **Hetja** eða **Borði**).
1. Í eiginleikaglugganum til hægri skaltu stækka ívafðar stýringarnar með því að velja hausana og stilla öll nauðsynleg stjórnunargildi.
1. Ef eiginleikaglugginn er með hlutann **Grunnstilling gagna** skaltu velja hann til að stækka hann. Að öðrum kosti ferðu í skref 5.
1. Ef hnappurinn **Bæta við gagnagjafa** er til staðar skaltu velja hann og veldu síðan innihaldsatriðin sem á að bæta við.
1. Sláðu inn stillingar fyrir nauðsynlegar eða viðeigandi einingarstýringar.
1. Veljið **Vista**.

### <a name="configure-a-container-module"></a>Stillla gámaeiningu

Fylgdu þessum skrefum til að stilla gámaeiningu á síðu.

1. Veldu gámaeiningu á síðunni (til dæmis hringekju- eða vökvagámaeiningu).
1. Í eiginleikaglugganum til hægri skaltu stækka ívafðar stýringarnar með því að velja hausana og stilla öll nauðsynleg stjórnunargildi.
1. Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti annaðhvort gámsins eða hólfa innan í gámnum og síðan velurðu **Bæta við einingu**. Bættu síðan undireiningum við valinn gám. Fyrir frekari upplýsingar, sjá ferlið [Bæta við einingu](#add-a-module) fyrr í þessu efni.
1. Ef margar undireiningar eru til sem systkini í yfirgámi geturðu breytt skjápöntun þeirra í yfirgámnum. Veldu úrfellingarhnappinn fyrir eininguna og notaðu síðan upp örina og örvatakkana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Vinna með brot](work-with-fragments.md)

[Bæta gámaeiningu við síðu](add-container-module.md)

[Bæta við staðsetningareiningum á síðu](add-content-placement-modules.md)

[Unnið með birta hópa](publish-groups.md)

