---
title: Vinna með einingar
description: Þetta efnisatriði lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce16aa98a37cd5dec60bcdbf86f59f74810da9755a6d3514bdd3e38a21afb748
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728265"
---
# <a name="work-with-modules"></a>Vinna með einingar

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig og hvenær á að nota einingar í Microsoft Dynamics 365 Commerce.

Einingar eru rökréttir byggingarreitir sem mynda síðuuppbyggingu þína og þau hafa ýmsan tilgang og gildissvið. Sumir einingar eru hástigs gámar og eini tilgangur þeirra er að halda og skipuleggja aðrar einingar (undireiningar). Aðrar einingar, svo sem einföld myndstaðsetningareining, hafa mjög sérstakan tilgang. Aðrar einingar, svo sem hringekjueining, falla einhvers staðar á milli þessara tveggja flokka.

Sjálfgefið er að Dynamics 365 Commerce-svæðið innihaldi einingarsafn sem gerir þér kleift að meðhöndla flestar aðstæður rafrænna viðskipta. Þú ættir að geta smíðað vefsvæði frá einni verslun til annarrar með því að nota þessar einingar. Hins vegar gætirðu líka viljað aðlaga þessa einingar eða smíða nýjar sérsniðnar einingar fyrir sérstakar þarfir. Ef þú vilt smíða sérsniðnar einingar er hugbúnaðarþróunarbúnaður (SDK) í boði til að hjálpa þér að búa til sérsniðið einingasafn.

## <a name="container-modules-and-slots"></a>Gámaeiningar og -hólf

Eins og áður var getið eru sumar einingar hannaðar til að innihalda undireiningar. Þessar einingar eru þekktar sem *gámar* og þær gera ráð fyrir stigveldum ívafinna eininga. Gámaeiningar innihalda *hólf*. Hólf eru notuð til að takast á við skipulag og tilgang undireininga í gámnum. Dæmi um það er grunnsíðugámaeining (efsta stigs eining fyrir hverja síðu) sem skilgreinir nokkur mikilvæg hólf:

- Fyrirsagnarhólf
- Undirfyrirsagnarhólf
- Aðalhólf
- Síðufótarhólf
- Undirsíðufótarhólf

Þróunaraðili einingarinnar skilgreinir þessi hólf og ákvarðar hvaða undireiningar og hversu margar undireiningar má setja beint í þau. Til dæmis gæti fyrirsagnarhólfið aðeins stutt eina einingu af gerðinni **Fyrirsagnareining** en meginmálshólfið gæti stutt ótakmarkaðan fjölda eininga af hvaða gerð sem er (nema aðrar gámaeiningar á síðunni).

Í höfundatækjunum þurfa síðuhöfundar ekki að vita fyrirfram hvaða einingar er hægt og ekki hægt að setja í hvert hólf. Þegar síðuhöfundar velja hólf og reyna síðan að velja einingu til að bæta við það sjá þeir síaða mynd af gerðum eininga sem eru studdar fyrir það hólf.

## <a name="content-modules"></a>Innihaldseiningar

Innihaldseiningar innihalda efni og fjölmiðlaþætti, svo sem texta (til dæmis fyrirsagnir, málsgreinar og krækjur) eða tilvísanir í eignir (til dæmis myndir, myndskeið og PDF skjöl). Dæmigerðar gerðir efniseininga innihalda efnisbálk, textabálk og einingar tilboðsborða. Einingar af þessum þremur gerðum geta innihaldið texta eða miðla og þeir þurfa ekki neinar undireiningar til að gera eitthvað sýnilegt á síðu.

Meirihluti dæmigerðra, daglegra síðu- og efnisskriftaaðgerða fela í sér efniseiningar, fyrst og fremst vegna þess að þessar einingar skilgreina raunverulegt innihald sem birt er í yfirgámaeiningum þeirra. Margar efniseiningar eru í boði og þessar einingar eru venjulega síðustu verkin sem þú bætir við stigveldi síðunnar með ívöfðum einingum.

Eftirfarandi mynd sýnir hvernig einingar eru ívafðar innan í einingahólfum yfirgáms.

![Faldaðar einingar.](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Bæta við eða fjarlægja einingar

Eftirfarandi aðferðir lýsa því hvernig á að bæta við og fjarlægja einingar.

### <a name="add-a-module"></a>Bæta við einingu

Til að bæta einingu við hólf eða gám á síðu skaltu fylgja þessum skrefum.

1. Á yfirlitssvæðinu vinstra megin eða beint á aðalvinnusvæðinu skal velja svæði eða hólf þar sem bæta á undireiningu við.

    > [!NOTE]
    > Einingahönnuðurinn skilgreinir listann yfir gerðir eininga sem hægt er að bæta við tiltekið hólf fyrir eininguna. Sniðmátshöfundar geta þá fínstillt leyfilega valkosti eininga til að hjálpa til við að tryggja stöðuga leitarvélabestun og skilvirkni höfundarverks fyrir allar síðurnar sem búnar til samkvæmt tilteknu sniðmáti. Þegar einingu er bætt við hólf, er svarglugginn **Bæta við einingu** sjálfkrafa síaður þannig að hann sýni aðeins einingar sem eru studdar í völdu svæði eða hólfi. Þessi listi yfir leyfðar einingar ákvarðast af sniðmáti síðunnar eða skilgreiningu svæðiseiningar.

1. Ef yfirlitssvæðið er notað skal velja úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar og síðan velja **Bæta við einingu**. Ef stýringarnar eru notaðar beint innan vinnusvæðisins skal velja plúsmerkið (**+**) í auðu hólfi eða samliggjandi við valda einingu, og síðan velja **Bæta við einingu**.

    > [!NOTE]
    > Ef gámur eða hólf styður ekki nýjar undireiningar er valkosturinn **Bæta við einingu** er ekki í boði.

1. Í svarglugganum **Bæta við einingu** skal velja einingu til að bæta við síðuna þína.

    > [!TIP]
    > **Efnisbálkur** er góð einingagerð fyrir byrjendur til að vinna með.

1. Veldu **Í lagi** til að bæta valinni einingu við valinn gám eða hólf á síðunni þinni.

### <a name="remove-a-module"></a>Fjarlægja einingu

Til að fjarlægja einingu úr hólfi eða gámi á síðu skaltu fylgja þessum skrefum.

1. Á yfirlitssvæðinu vinstra megin skal velja úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar sem á að fjarlægja og síðan velja ruslakörfutáknið. Einnig er hægt í aðalvinnusvæðinu að velja ruslakörfutáknið í tækjastiku valdrar einingar.
1. Þegar beðið er um að staðfesta að ætlunin sé að fjarlægja eininguna, skal velja **Í lagi**.

## <a name="move-a-module-to-a-new-position"></a>Færa einingu á nýjan stað

Til að færa einingu yfir á nýjan stað innan síðunnar, skal nota eina af eftirfarandi aðferðum.

### <a name="move-a-module-using-the-outline-pane"></a>Færa einingu með yfirlitssvæðinu

Til að færa einingu með yfirlitssvæðinu skal fylgja þessum skrefum.

1. Veljið og haldið einingunni sem á að færa á yfirlitssvæðinu, dragið síðan eininguna yfir á nýja staðsetningu í yfirlitinu. Bláa línan í yfirlitinu og á vinnusvæðinu sýnir hvar hægt er að staðsetja eininguna.
1. Sleppið einingunni til að fella hana inn í nýja staðinn.

### <a name="move-a-module-directly-within-the-canvas"></a>Færa einingu beint innan vinnusvæðisins

Til að færa einingu beint innan vinnusvæðisins skal fylgja þessum skrefum.

1. Veljið eininguna sem á að færa innan vinnusvæðisins. 
1. Veljið annaðhvort örvatákn sem vísar upp eða niður í tækjastiku einingarinnar og dragið síðan örina yfir á nýjan stað á síðunni. Bláa línan á vinnusvæðinu og í yfirlitinu sýnir hvar hægt er að staðsetja eininguna. Ef ekki er hægt að færa einingu upp eða niður, verður örvartáknið skyggt. 
1. Sleppið einingunni til að fella hana inn í nýja staðinn.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Færa einingu með úrfellingarvalmyndinni

Til að færa einingu með úrfellingarvalmyndinni skal fylgja þessum skrefum.

1. Veljið einingu í annaðhvort yfirlitinu eða vinnusvæðinu.
1. Veljið úrfellingarmerkið (**...**) við hliðina á heiti einingarinnar á yfirlitssvæðinu eða í tækjastiku einingarinnar á vinnusvæðinu.
1. Ef hægt er að færa eininguna upp eða niður innan svæðis eða hólfs birtast valmöguleikar fyrir **Færa upp** eða **Færa niður**. Veljið æskilegan færsluvalkost til að færa eininguna upp eða niður miðað við aðrar einingar.

## <a name="configure-modules"></a>Skilgreina einingar

Eftirfarandi aðferðir lýsa því hvernig á að skilgreina efnis- og gámaeiningar.

### <a name="configure-a-content-module"></a>Stilla innihaldseiningu

Fylgdu þessum skrefum til að stilla efniseiningu á síðu.

1. Á yfirlitssvæðinu vinstra megin skal útvíkka tréð og velja einhverja efniseiningu (til dæmis **Efnisbálkur**). Einnig er hægt að velja eininguna á aðalvinnusvæðinu.
1. Á eiginleikasvæði einingarinnar hægra megin skal færa inn eiginleika fyrir eiginleikastýringar sem óskað er eftir.
1. Á skipanastikunni skal velja **Vista**. Þetta mun einnig endurnýja forskoðunardúkinn.

### <a name="edit-module-text-properties"></a>Breyta textaeiginleikum einingar

Textaeiginleikar einingar sem ekki eru skrifvarðar er hægt að breyta á vinnusvæðinu.

Til að breyta textaeiginleikum einingar skaltu fylgja þessum skrefum.

1. Veljið textastýringuna á vinnusvæðinu og farið með bendilinn þangað sem á að breyta texta.
1. Sláið inn textann.
1. Veljið hvar sem er fyrir utan textaefnið til að halda áfram að breyta öðru efni.

### <a name="inline-image-selection"></a>Innfellt val myndar

Myndaeiningar sem ekki eru skrifvarðar er hægt að breyta á vinnusvæðinu.

Til að velja nýja mynd fyrir efniseiningu skal fylgja þessum skrefum.

1. Á vinnusvæðinu skal tvísmella á myndina. Þá kemur upp gluggi fyrir val á miðli.
1. Finnið og veljið nýja mynd sem á að nota og veljið síðan **Í lagi**. Nýja myndin er nú sýnd á vinnusvæðinu.

### <a name="configure-a-container-module"></a>Stillla gámaeiningu

Fylgdu þessum skrefum til að stilla gámaeiningu á síðu.

1. Veldu gámaeiningu á síðunni (til dæmis hringekju- eða vökvagámaeiningu).
1. Í eiginleikaglugganum til hægri skaltu stækka ívafðar stýringarnar með því að velja hausana og stilla öll nauðsynleg stjórnunargildi.
1. Í útlínuglugganum til vinstri velurðu úrfellingarhnappinn við hliðina á heiti annaðhvort gámsins eða hólfa innan í gámnum og síðan velurðu **Bæta við einingu**. Bættu síðan undireiningum við valinn gám. Fyrir frekari upplýsingar, sjá hlutann [Vinna með einingar](#add-a-module) fyrr í þessu efni.
1. Ef margar undireiningar eru til sem systkini í yfirgámi geturðu breytt skjápöntun þeirra í yfirgámnum. Veldu úrfellingarhnappinn fyrir eininguna og notaðu síðan upp örina og örvatakkana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Vinna með brot](work-with-fragments.md)

[Bæta gámaeiningu við síðu](add-container-module.md)

[Vinna með birtingarhópa](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
