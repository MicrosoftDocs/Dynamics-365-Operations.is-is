---
title: Veita starfsfólki í framleiðslu leiðarvísa með blönduðum veruleika
description: Þetta efnisatriði útskýrir hvernig á að samþætta framleiðslustýringareininguna í Microsoft Dynamics 365 Supply Chain Management við Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 727a3bc50ea55259c7260a9d060dac59473ee3c1
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645145"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a>Veita starfsfólki í framleiðslu leiðarvísa með blönduðum veruleika

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Starfsmenn í framleiðsluferli munu hagnast á viðeigandi leiðbeiningum sem eru veittar á réttum tíma í samhengi við verk þeirra. *Leiðbeiningar* eiga við í nokkrum þáttum vinnunnar, þar á meðal: samsetningu, þjónustu, aðgerðum, vottunum og öryggi. Í öllum þessum meginaðgerðum rekstursins geta virkar leiðbeiningar hjálpað starfsmönnum að ná meiri árangri og skila betri vinnu.

## <a name="introduction"></a>Inngangur

Hægt er að veita leiðbeiningar á mismunandi hátt. Eitt skilvirkt sendingarkerfi notar [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).

Dynamics 365 Guides getur hjálpað starfsfólki með verklegri kennslu. Hægt er að skilgreina stöðluð ferli með ítarlegum leiðbeiningum sem leiðbeina starfsmönnum um verkfæri og hluta sem þeir þurfa á að halda og sýna starfsmönnum hvernig á að nota þessi verkfæri í raunverulegum aðstæðum í vinnunni.

Hægt er að hengja leiðarvísa við ýmsa þætti framleiðslustýringar, þar á meðal:

- [Forði](#resources)
- [Tilfangaflokkar](#resource-groups)
- [Útgefnar afurðir](#released-products)
- [Formúlur](#formulas)
- [Formúluútgáfur](#formula-versions)
- [Uppskriftir](#bom)
- [Uppskriftaútgáfur](#bom-versions)
- [Leiðir](#routes)
- [Leiðarútgáfur](#route-versions)
- [Tengsl leiðaraðgerðar](#route-operation-relations)

> [!NOTE]
> Einnig er hægt að hengja leiðsagnir við Eignastýringu. Sjá frekari upplýsingar í [Samþætta Dynamics 365 Supply Chain Management (Eignastýring) við Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).

Þegar fyrsti starfsmaður í ferlinu velur verk í vinnusal í gegnum Supply Chain Management, getur starfsmaðurinn séð [viðkomandi leiðarvísa](#logic) á verkspjaldinu. Þegar starfsmaðurinn velur tiltekna leiðsögn, birtist QR-kóði fyrir þann leiðarvísi á skjánum. Starfsmaðurinn notar síðan HoloLens til að skanna QR-kóðann sem ræsir leiðsagnir og sýnir nauðsynlegar leiðbeiningar.

Eftirfarandi undirkaflar lýsa nokkrum völdum aðstæðum þar sem fyrirtæki í ýmsum atvinnugreinum sjá mestan hag í því að nota leiðarvísa til að kynna leiðbeiningar fyrir framleiðslu.

### <a name="assembly"></a>Smölun

![Nota leiðbeiningar í samsetningarverkum](media/instruction-guides-hero-assembly.png "Nota leiðarvísa í þjónustuverkum")

Leiðbeiningar í samsetningaraðgerðum sýna starfsmönnum þau verkfæri og hluta sem þeir þurfa á að halda og hvernig á að nota það í raunverulegum aðstæðum við vinnu.

Framleiðslustjórar geta búið til og úthlutað leiðsögn, til dæmis fyrir [framleiðsluleiðir](routes-operations.md), [aðgerðarvensl](routes-operations.md#operation-relations)eða [uppskrift](bill-of-material-bom.md). Starfsmenn munu finna viðeigandi leiðbeiningar um viðkomandi vinnsluupplifun í vinnusalnum.

### <a name="service"></a>Þjónusta

![Nota leiðarvísa í þjónustuverkum](media/instruction-guides-hero-service.png "Nota leiðarvísa í þjónustuverkum")

Bjóða tæknimönnum upp á leiðsagnir á vinnusvæðinu og koma þannig í veg fyrir þörfina á því að tímasetja frekari heimsóknir.

Þjónustustjórar geta úthlutað leiðbeiningum, t.d. á tilteknar [afurðir](../../commerce/product.md) sem fara í gegnum vanabundið gæðamat.

### <a name="quality"></a>Gæði

![Nota leiðarvísa í vinnu gæðaeftirlits](media/instruction-guides-hero-quality.png "Nota leiðarvísa í vinnu gæðaeftirlits")

Komið með nýja ferla og tryggið aukið samræmi með því að breyta þekkingu starfsmanna í endurtekið verkfæri.

Gæðastjórar geta úthlutað leiðbeiningum, t.d. á [afurðir](../../commerce/product.md) sem fara í gegnum vanabundið gæðamat.

### <a name="certifications"></a>Vottanir

![Nota leiðbeiningar fyrir verk sem tengjast vottun](media/instruction-guides-hero-certification.png "Nota leiðbeiningar fyrir verk sem tengjast vottun")

Gangið úr skugga um að sérhver starfsmaður uppfylli strangar kröfur með því að finna út hver þarf hjálp og hvar.

### <a name="safety"></a>Öryggi

![Nota leiðarvísa í öryggisleiðbeiningum](media/instruction-guides-hero-safety.png "Nota leiðarvísa í öryggisleiðbeiningum")

Gefið fyrirmæli sem fara í gegnum hættuleg ferli í sýnidæmi áður en það er reynt við raunverulegar aðstæður. Með blönduðum veruleika geta starfsmenn öðlast reynslu af hættulegum ferlum í sýnidæmi.

Framleiðslustjórar geta veitt nákvæmar leiðbeiningar um meðhöndlun á hættulegum efnum eða ferla viðkvæmrar meðhöndlunar með því að úthluta leiðbeiningum á [vörur](../../commerce/product.md), [leiðir](routes-operations.md) og [aðgerðir](routes-operations.md#operation-relations).

## <a name="get-started-with-instructions-and-guides"></a>Hafist handa með leiðbeiningar og leiðsögnum

Til að virkja leiðbeiningar í framleiðsluferlum býður Supply Chain Management upp á tilbúna samþættingu við Dynamics 365 Guides. Heimilað og uppsett forritstilvik Guides er nauðsynlegt til að búa til, vinna með og úthluta leiðbeiningum blandaðs veruleika á framleiðslueignir og framleiðsluvinnu.

### <a name="prerequisites"></a>Forkröfur

Til að nota þennan eiginleika verður kerfið að innihalda eftirfarandi:

- Dynamics 365 Supply Chain Management útgáfa 10.0.15 eða nýrri
- [Tvöföld skrif](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) fyrir forrit Supply Chain Management.
- [Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) útgáfa 400.0.1.48 eða nýrri

### <a name="turn-on-the-feature"></a>Kveikja á eiginleikanum

Til að bjóða upp á eiginleikann í kerfinu, þarf að virkja skilgreiningarlyklana. Þetta þarf aðeins að gera einu sinni. Til að gera þetta verður stjórnandi að gera eftirfarandi:

1. Setjið kerfið í viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
1. Stækkið hlutann **Blandaður veruleiki** og veljið svo gátreitinn **Leiðarvísir fyrir blandaðan veruleika**.
1. Stækkið hlutann **Framleiðslustýring** og veljið svo gátreitinn **Leiðbeiningar fyrir framleiðslu**.
1. Slökkvið á viðhaldsstillingu eins og lýst er í [Viðhaldsstilling](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a>Skilgreina hvernig leiðsagnir birtast í vinnusal

Til skilgreina hvernig leiðsagnir birtast í vinnusal skal fara í **Blandaður veruleiki \> Dynamics 365 Guides \> Skilgreina samþættingu leiðsagna**.

![Skilgreina samþættingu leiðsagna fyrir framleiðslu](media/instruction-guides-configure-integration.png "Skilgreina samþættingu leiðsagna fyrir framleiðslu")

Stilltu eftirfarandi reiti:

- **Microsoft Dataverse URL** - Tilgreindu URL fyrir Microsoft Dataverse umhverfi þar sem þú býrð til leiðarvísa. Sniðið er „contoso.crm4.dynamics.com“, þar sem fyrsti hluti URL er yfirleitt nefndur eftir fyrirtækinu (svo sem „contoso.“), annar hlutinn er sértækur fyrir gagnasvæði í umhverfinu (svo sem „crm4.“), og síðasti hlutinn er lénið (t.d. „dynamics.com“). Ein leið til að finna rétt URL er að fara á [Home.Dynamics.com](https://home.dynamics.com/) og opna síðan Guides forritið. Þegar Guides opnast birtist URL í veffangastiku vafrans (aðeins skal taka grunnslóðina, sem ætti að líkjast fyrra dæmi). Þetta gildi er notað til að setja saman slóð fyrir leiðsagnirnar og verður kóðað inn í QR-kóðana.
- **Stærð QR-kóða** - Stillið myndastærð QR-kóðans. Við mælum með því að velja stærð sem fyllir stærstan hluta skjásins, en ekki meira. Oftast er *15* gott gildi.
- **Stig villuleiðréttingar QR-kóða** - Stillið uppskiptingu QR-kóðans. Hærri uppskipting getur aukið áreiðanleika kóðans, en **Stærð QR-kóðans** verður að vera nógu stór til að styðja nákvæmnina sem valið leiðréttingarstig þarf.

> [!TIP]
> - QR-kóðastærðir sem eru of stórar fyrir skjáinn taka lengri tíma að myndast og síðan vera skalaðar niður til að passa inn á skjáinn. Þetta hefur engan ávinning í för með sér.
> - QR-kóðastærðir sem eru of litlar geta dregið úr getu HoloLens til að lesa kóðann rétt í sumum umhverfum.
> - Við mælum með því að prófa stillingarnar fyrir hvert tæki sem mun birta QR-kóða fyrir HoloLens notendur. Veljið stillingar sem bjóða upp á nógu góðan læsileika í umhverfi vinnusalar.  

## <a name="get-an-overview-of-all-guide-assignments"></a>Fá yfirlit yfir allar úthlutanir leiðsagna

Notið síðuna **Allar leiðsagnir** til að sjá lista yfir allar tiltækar leiðsagnir í fyrirtækinu og allar úthlutanir á framleiðsluferli og tilföng. Til að opna hana skal fara í **Blandaður veruleiki \> Leiðsagnir \> Allar leiðsagnir**. Efst í listanum eru allar tiltækar leiðsagnir sýndar og hægt er að nota reitinn hér til að sía listann. Neðst í listanum eru allar úthlutaðar leiðsagnir sýndar og tækjastika er í boði til að stjórna þeim.

![Stjórna leiðarvísum](media/instruction-guides-allguides.png "Stjórna leiðarvísum")

Eftirfarandi kaflar lýsa þeim tegundum hluta sem hægt er að úthluta leiðarvísa á. Í hverjum úthlutuðum leiðarvísi eru leiðbeiningar sem eru sjálfkrafa hengdar við viðeigandi framleiðsluverk sem verða í boði í vinnusalnum.

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a>Tengja leiðarvísi við tilfang

Bætið leiðarvísi við [tilfang](operations-resources.md) til að bjóða upp á leiðarvísinn í samhengi við viðeigandi framleiðsluverk.

### <a name="typical-scenario-using-resources"></a>Dæmigerðar aðstæður sem nota tilföng

Til dæmis væri hægt að hengja leiðarvísi með almennu vélaröryggi eða leiðbeiningum um meðhöndlun við tilfang af vélargerðinni. Síðan verður leiðarvísirinn tiltækur fyrir hvert verk sem er framkvæmt á vélinni.

### <a name="add-a-guide-to-a-resource"></a>Bæta leiðarvísi við tilfang

Leiðarvísi bætt við tilfang:

1. Opnið **Framleiðslustýring \> Uppsetning \> Tilföng \> Tilföng**.
1. Í listasvæðinu skal velja tilfang sem á að úthluta leiðarvísi á.
1. Stækkið flýtiflipann **Tengdir leiðarvísar**.
1. Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**. Nýrri línu er bætt við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta. Ef til er mikill fjöldi leiðarvísa, er hægt að sía listann til að finna þann sem verið er að leita að.
    ![Stjórna leiðarvísum](media/instruction-guides-allguides.png "Stjórna leiðarvísum")

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a>Tengja leiðarvísi við tilfangaflokk

Hægt er að bæta leiðarvísi við [tilfangaflokka](tasks/define-discrete-manufacturing-resource-group.md) ef þeir eru notaðir til að stjórna hópum af vélum, framleiðslulínum eða vinnuflokkum.

### <a name="typical-scenarios-using-resource-groups"></a>Dæmigerðar aðstæður með tilfangaflokkum

**Dæmi 1:** Tilfangaflokkur hefur verið skilgreindur fyrir nokkrar vélar af sömu gerðinni. Í stað þess að úthluta viðeigandi leiðarvísi um meðhöndlun fyrir vélargerðina á öll viðeigandi tilföng, mætti þess í stað úthluta leiðarvísinum á tilfangaflokkinn sem endurspeglar þessa vélargerð.

**Dæmi 2:** Tilfangaflokkur hefur verið skilgreindur fyrir vinnuflokk sem inniheldur mismunandi vélar og til er leiðarvísir sem veitir almennar leiðbeiningar um hvernig á að halda utan um vinnuflokkinn. Leiðarvísirinn á við um hvers kyns framleiðsluaðgerðir í þessum vinnuflokki.

### <a name="add-a-guide-to-a-resource-group"></a>Bæta leiðarvísi við tilfangaflokk

Til að bæta leiðarvísi við tilfangaflokk:

1. Farið í **Framleiðslustýringu \> Uppsetning \> Tilföng \> Tilfangaflokkar**.
1. Í listasvæðinu skal velja tilfangaflokkinn sem á að úthluta leiðarvísi á.
1. Stækkið flýtiflipann **Tengdir leiðarvísar**.
1. Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**. Nýrri línu er bætt við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta. Ef til er mikill fjöldi leiðarvísa, er hægt að sía listann til að finna þann sem verið er að leita að.
    ![Leiðarvísi bætt við tilfangaflokk](media/instruction-guides-resourcegroup.png "Leiðarvísi bætt við tilfangaflokk")

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a>Tengja leiðarvísi við útgefna afurð

Hægt er að bæta leiðarvísi við hvaða [útgefna afurð](../pim/tasks/create-released-product-single-company.md) sem er.

### <a name="typical-scenario-using-released-products"></a>Dæmigerðar aðstæður þar sem útgefnar afurðir eru notaðar

Leiðarvísar á framleiðslustigi hjálpa starfsmönnum í vinnusal með leiðbeiningar sem tengjast stýringu eða meðhöndlun á tiltekinni útgefinni afurð eða vöru.

### <a name="add-a-guide-to-a-released-product"></a>Bæta leiðarvísi við útgefna afurð

Leiðarvísi bætt við útgefna afurð:

1. Opna **Framleiðslustjórnun \> Afurðir \> Útgefnar afurðir**.
1. Opnið afurðina sem á að úthluta leiðarvísi á.
1. Á aðgerðasvæðinu skal opna flipann **Hönnuður** og í flokknum **Yfirlit** skal velja **Tengdir leiðarvísar**.
1. Síðan **Tengdir leiðarvísar** opnast fyrir valda afurð.
1. Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið. 
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við útgefna afurð](media/instruction-guides-ReleasedProduct-AddGuides.png "Leiðarvísi bætt við útgefna afurð")

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a>Tengja leiðarvísi við formúlu

Hægt er að bæta leiðarvísi við hvaða [formúlu](bill-of-material-bom.md#formulas-co-products-and-by-products) sem er.

### <a name="typical-scenario-using-formulas"></a>Dæmigerðar aðstæður með því að nota formúlur
  
Leiðarvísar á formúlustigi bjóða starfsmönnum í vinnusal upp á leiðarvísi fyrir meðhöndlun í samhengi við formúlu eða uppskrift. Einnig er hægt að úthluta leiðsögnum á útgáfur formúlu.

> [!NOTE]
> Hægt er að úthluta leiðsögn sem tengist framleiðsluferlum sem byggja á formúlu eða leið, leiðarútgáfu, eða tengsl leiðarútgáfa.  

> Ekki er hægt að tengja leiðarvísa við einstakar formúlulínur sem stendur.

### <a name="add-a-guide-to-a-formula"></a>Bæta leiðarvísi við formúlu

Leiðarvísi bætt við formúlu:

1. Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.
1. Opnið formúluna sem á að úthluta leiðarvísi á.
1. Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.
1. Stækkið flýtiflipann **Tengdir leiðarvísar**.
1. Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**. Nýrri línu er bætt við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við formúlu](media/instruction-guides-Formula.png "Leiðarvísi bætt við formúlu")

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a>Tengja leiðarvísi við formúluútgáfu

Hægt er að bæta leiðarvísi við [formúluútgáfu](bill-of-material-bom.md#bom-and-formula-versions).

### <a name="typical-scenario-using-formula-versions"></a>Dæmigerðar aðstæður þar sem formúluútgáfur eru notaðar

Leiðarvísar sem eru hengdir við ákveðna útgáfu af formúlu veita starfsmönnum vinnusalar leiðbeiningar sem fara í gegnum framleiðslu þessarar útgáfu af formúluuppskriftinni.

> [!TIP]
> Hægt er að úthluta leiðsögn sem tengist framleiðsluferlum sem byggja á þessari formúluútgáfu á leið, leiðarútgáfu, eða tengsl leiðarútgáfa.  

> [!NOTE]
> Ekki er hægt að tengja leiðarvísa við einstakar formúlulínur sem stendur.

### <a name="add-a-guide-to-a-formula-version"></a>Bæta leiðarvísi við formúluútgáfu

Leiðarvísi bætt við formúluútgáfu:

1. Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Formúlur**.
1. Opnið formúluna sem inniheldur útgáfu sem úthluta á leiðarvísi á.
1. Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.
1. Í flýtiflipanum **Formúluútgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.
1. Í tækjastikunni **Formúluútgáfur** skal velja **Tengdir leiðarvísar**.
    ![Opna leiðarvísana sem tengjast valdri formúluútgáfu](media/instruction-guides-FormulaVersion.png "Opna leiðarvísana sem tengjast valdri formúluútgáfu")
1. Síðan **Tengdir leiðarvísar** opnast fyrir formúluútgáfuna.
1. Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið. 
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við formúluútgáfu](media/instruction-guides-FormulaVersionAddGuide.png "Leiðarvísi bætt við formúluútgáfu")

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a>Bæta leiðarvísi við uppskriftir

Hægt er að bæta leiðarvísi við [uppskriftir](bill-of-material-bom.md).

### <a name="typical-scenario-using-bills-of-materials"></a>Dæmigerðar aðstæður með uppskriftum

Leiðarvísar sem tengjast uppskrift veita starfsmönnum vinnusalar leiðbeiningar sem útskýra hvernig á að undirbúa og meðhöndla efni úr uppskrift. Einnig er hægt að úthluta leiðarvísum á útgáfur uppskriftar.

> [!NOTE]
> Ekki er hægt að tengja leiðarvísa við einstakar uppskriftarlínur sem stendur.

### <a name="add-a-guide-to-a-bill-of-materials"></a>Bæta leiðarvísi við uppskriftir

Leiðarvísi bætt við uppskrift:

1. Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Uppskriftir**.
1. Opnið uppskriftirnar sem á að úthluta leiðarvísi á.
1. Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.
1. Stækkið flýtiflipann **Tengdir leiðarvísar**.
1. Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**. Nýrri línu er bætt við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við uppskrift](media/instruction-guides-BOM.png "Leiðarvísi bætt við uppskrift")

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a>Bæta leiðarvísi við uppskriftarútgáfu

Hægt er að bæta leiðarvísi við hvaða [uppskriftarútgáfu](bill-of-material-bom.md#bom-and-formula-versions) sem er.

### <a name="typical-scenario-using-bill-of-materials-versions"></a>Dæmigerðar aðstæður þar sem uppskriftarútgáfur eru notaðar

Leiðarvísar sem hengdir eru við staka uppskriftarútgáfu veita starfsmönnum vinnusalar leiðbeiningar sem útskýra hvernig á að undirbúa og meðhöndla efni fyrir útgáfu af uppskrift sem er frábrugðin almennu uppskriftinni eða öðrum útgáfum hennar.

> [!NOTE]
> Ekki er hægt að tengja leiðarvísa við einstakar uppskriftarlínur sem stendur.

### <a name="add-a-guide-to-a-bill-of-materials-version"></a>Bæta leiðarvísi við uppskriftarútgáfu

Til að bæta við leiðarvísinum fyrir uppskriftarútgáfu:

1. Farið í **Stjórnun framleiðsluupplýsinga \> Uppskriftir og formúlur \> Uppskriftir**.
1. Opnið uppskriftina sem inniheldur útgáfu sem úthluta á leiðarvísi á.
1. Opnið flipann **Haus** fyrir ofan efsta flýtiflipann.
1. Í flýtiflipanum **Uppskriftaútgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.
1. Í tækjastikunni **Uppskriftaútgáfur** skal velja **Tengdir leiðarvísar**.
    ![Opna leiðarvísana sem tengjast valdri uppskriftarútgáfu](media/instruction-guides-BOMVersion.png "Opna leiðarvísana sem tengjast valdri uppskriftarútgáfu")
1. Síðan **Tengdir leiðarvísar** opnast fyrir uppskriftarútgáfuna.
1. Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við uppskriftarútgáfu](media/instruction-guides-BOMVersionAddGuide.png "Leiðarvísi bætt við uppskriftarútgáfu")

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a>Tengja leiðarvísi við leið

Hægt er að bæta leiðarvísi við hvaða [leið](routes-operations.md) sem er.

### <a name="typical-scenario-using-routes"></a>Dæmigerðar aðstæður með leiðum

Leiðir eru gjarnan notaðar til að segja til um hvernig á framleiða ákveðna útgefna afurð samkvæmt uppskrift eða uppskriftarútgáfu og með safn af tilföngum eða tilfangaflokkum.

Úthlutið leiðarvísi á leið til að veita ítarlegar leiðbeiningar fyrir viðkomandi framleiðsluferli.

### <a name="add-a-guide-to-a-route"></a>Bæta leiðarvísi við leið

Leiðarvísi bætt við leið:

1. Farið í **Framleiðslustýring \> Allar leiðir**.
1. Opnið leiðina sem á að úthluta leiðarvísi á.
1. Stækkið flýtiflipann **Tengdir leiðarvísar**.
1. Veljið **Bæta við** úr tækjastikunni **Tengdir leiðarvísar**. Nýrri línu er bætt við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við leið](media/instruction-guides-Route.png "Leiðarvísi bætt við leið")

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a>Tengja leiðarvísi við leiðarútgáfu

Hægt er að bæta leiðarvísi við hvaða [leiðarútgáfu](routes-operations.md#route-versions) sem er.

### <a name="typical-scenario-using-route-versions"></a>Dæmigerðar aðstæður með leiðaútgáfum

Leiðarútgáfur eru yfirleitt notaðar til að tilgreina afbrigði af framleiðsluferlum sem byggja á fyrirliggjandi leið. Hægt er að úthluta mismunandi leiðarvísum á hverja leiðarútgáfu.

### <a name="add-a-guide-to-a-route-version"></a>Bæta leiðarvísi við leiðarútgáfu

Leiðarvísi bætt við leiðarútgáfu:

1. Farið í **Framleiðslustýring \> Allar leiðir**.
1. Opnið leiðina sem á að úthluta leiðarvísi á.
1. Í flýtiflipanum **Útgáfur** skal velja útgáfuna sem úthluta á leiðarvísi á.
1. Í tækjastikunni **Útgáfur** skal velja **Tengdir leiðarvísar**.
    ![Opna leiðarvísana sem tengjast valdri leiðarútgáfu](media/instruction-guides-RouteVersion.png "Opna leiðarvísana sem tengjast valdri leiðarútgáfu")
1. Síðan **Tengdir leiðarvísar** opnast fyrir uppskriftarútgáfuna.
1. Veljið **Bæta við** á aðgerðasvæðinu til að bæta nýrri línu við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta.
    ![Leiðarvísi bætt við leiðarútgáfu](media/instruction-guides-RouteVersionAddGuide.png "Leiðarvísi bætt við leiðarútgáfu")

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a>Tengja leiðarvísi við tengsl leiðaraðgerðar

Hægt er að bæta við leiðarvísi á hvaða [tengsl leiðaraðgerðar](routes-operations.md#operation-relations) sem er.

### <a name="typical-scenario-using-route-operation-relations"></a>Dæmigerðar aðstæður þar sem tengsl leiðaraðgerðar eru notuð

Aðgerðatengsl eru sértækasta leiðin til að bæta leiðsögn við framleiðsluferli og tengdar aðgerðir. Hægt er að tilgreina leiðsögn fyrir hverja aðgerð í leið og tilgreina mismunandi leiðsagnir fyrir hvers kyns samhengi af tengslum sem tilgreind eru fyrir leið, t.d. fyrir tilteknar vörur, skilgreiningar o.m.fl. Einnig er hægt að tilgreina á hvaða stigum í aðgerðinni leiðsögnin gildir (svo sem uppsetningu, biðröð, ferli eða flutning).

> [!NOTE]
> Ef leiðarvísar eru tilgreindir fyrir mörg aðgerðartengsl leiðar, þ.á.m. þessir leiðarvísar, verður aðeins leiðarvísirinn úr sértækustu tengslunum sýndur í vinnusal fyrir verkið sem er búið til.

### <a name="add-a-guide-to-a-route-operation-relation"></a>Bæta leiðarvísi við tengsl leiðaraðgerðar

Leiðarvísi bætt við tengsl leiðaraðgerðar:

1. Farið í **Framleiðslustýring \> Allar leiðir**.
1. Opnið leiðina sem á að úthluta leiðarvísi á.
1. Á aðgerðasvæðinu skal opna flipann **Leið** og í flokknum **Vinna með** skal velja **Upplýsingar um leið**.
1. Síðan **Upplýsingar um leið** opnast fyrir valda leið.
1. Í efsta hnitanetinu skal velja aðgerðina sem á að fá leiðsögn.
1. Í neðsta hnitanetinu skal velja sértæk tengsl (eða almennu tengslin **Allt**).
    ![Velja aðgerð og síðan tengsl](media/instruction-guides-RouteOperationRelation.png "Velja aðgerð og síðan tengsl")
1. Fyrir ofan neðsta hnitanetið skal opna flipann **Tengdir leiðarvísar**. ![Flipinn tengdir leiðarvísar](media/instruction-guides-RouteOperationRelation-AddGuide.png "Flipi tengdra leiðarvísa")
1. Veljið **Bæta við** í tækjastikunni efst í neðsta hnitanetinu til að bæta nýrri línu við hnitanetið.
1. Fyrir nýju línuna skal nota fellilistann í dálkinum **Heiti** til að velja leiðarvísinn sem á að úthluta. Það sem eftir er af línunni skal velja gátreitinn fyrir hvert samhengi þar sem valinn leiðarvísir á að vera tiltækur.

> [!NOTE]
> Hægt er að bæta við einum eða fleiri leiðarvísum fyrir hvert stig af hverri aðgerð.

## <a name="select-guides-from-the-shop-floor-execution-interface"></a>Velja leiðarvísa úr keyrsluviðmóti vinnusalar

Þegar starfsmaður opnar verklista í keyrsluviðmóti vinnusalar, finnur Supply Chain Management viðeigandi leiðarvísa fyrir verkin sem sýnd eru. Notið hnappinn **Leiðarvísar** til að skoða viðeigandi leiðarvísa.

![Leiðarvísishnappur í keyrsluviðmóti vinnusalar](media/instruction-guides-Shopfloor1.png "Leiðarvísishnappur í keyrsluviðmóti vinnusalar")

Síðan skal setja á HoloLens og fá aðgang að viðkomandi leiðarvísi með því að skanna QR-kóðann og virkja leiðarvísinn.

![QR-kóði til að fá aðgang að leiðsögnum með því að nota HoloLens](media/instruction-guides-Shopfloor2.png "QR-kóði til að fá aðgang að leiðsögnum með því að nota HoloLens")

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a>Að leysa úr reglunni fyrir val á leiðarvísum

Hægt er að bæta leiðarvísum við eftirfarandi framleiðslugögn:

- [Forði](#resources)
- [Tilfangaflokkar](#resource-groups)
- [Útgefnar afurðir](#released-products)
- [Formúlur](#formulas)
- [Formúluútgáfur](#formula-versions)
- [Uppskriftir](#bom)
- [Uppskriftaútgáfur](#bom-versions)
- [Leiðir](#routes)
- [Leiðarútgáfur](#route-versions)
- [Tengsl leiðaraðgerðar](#route-operation-relations)

Þegar Supply Chain Management býr til verkin fyrir framleiðslugólfið, safnar það saman viðeigandi leiðarvísum úr þessum upprunastöðum. Taka skal tillit til eftirfarandi mikilvægra reglna.

- Ef uppskriftarútgáfa eða formúluútgáfa er hengd við leið eða framleiðslupöntun, þá verða allir leiðarvísar sem hengdir eru við þessa útgáfu, og einnig leiðarvísar sem hengdir eru við yfiruppskrift eða -formúlu þessara útgáfu, sýndir í verkinu.
- Ef leiðarútgáfa eða framleiðsluútgáfa er hengd við framleiðslupöntun, þá verða allir leiðarvísar sem hengdir eru við þessa útgáfu, og einnig leiðarvísar sem hengdir eru við yfirleið þessara útgáfu, sýndir í verkinu.
- Ef mörg tengsl leiðaraðgerða eru skilgreind sem innihalda tengslin *Allt* og leiðarvísum er úthlutað á þau, verða aðeins leiðarvísarnir úr sértækustu tengslunum sýndir fyrir verkið.  

![Skýringarmynd um úrlausn viðeigandi leiðarvísa](media/instruction-guides-Resolve.png "Skýringarmynd um úrlausn viðeigandi leiðarvísa")
